# 澔學帳號登入現況

## 簡介

澔學使用者（[澔學是什麼？](https://app.gitbook.com/s/wMUWuSn1WpoX6sUW8OlS/introductions/ming-ci-jie-shi/pagamo-zhu-ye/hao-xue#hao-xue-shi-shen-me)）通常都是透過親師生平台登入 PaGamO，在使用者第一次登入時會先確認使用者是否有授權 PaGamO 存取澔學資料，有才會轉跳 PaGamO 平台，我們同時能處理的登入人數為 100 人，超過就會進入等排隊登入中。

使用者進入 PaGamO，我們會透過以下三個流程來讓使用者獲得相對應的服務。

### 1. 基本資料更新：

* 我們根據澔學的 API 資料更新使用者 user 的資料，如果過程更新失敗的話，使用者也可至個人設定頁面點擊手動驗證，來手動觸發完成資料更新。
* API 資料可考圖片的左下部分，其中新北有一隻 my\_principal 是澔學給新北的專屬 API
* 完成使用者 user 資料的更新後，我們就會處理使用者 GC 在世界中的資料：
  1. 學生身份：
     1. 加入對應的世界（根據 one\_campus\_app)
     2. 建立、加入、退出或封存班級
  2. 老師身份：
     1. 加入對應世界（根據 one\_campus\_app)，並給予教師權限
     2. 建立、加入、退出或封存班級
     3. 處理花蓮專屬世界的學校管理者權限（本次開發會移除的項目）

{% embed url="https://www.figma.com/board/q93nPzlkCkL1u37WI8xCsd/%E6%BE%94%E5%AD%B8%E4%B8%B2%E6%8E%A5%E6%A9%9F%E5%88%B6%E8%A6%8F%E5%8A%83?node-id=893-2865&t=3pcirVamNl1M0Kra-0" %}
主要為 Figma 中的左側與中間上部分
{% endembed %}

### 2. 花蓮專屬世界邏輯：

1. 在 one\_campus\_app 有將花蓮使用者對應到花蓮專屬世界中（上圖），所以上述「基本資料更新」期使就會影響花蓮專屬世界(給予教師權限)
2. 但在執行上述設定後，花蓮後續還會一塊專屬的花蓮邏輯，專門處理教材授權與 GC 到期日

{% embed url="https://www.figma.com/board/q93nPzlkCkL1u37WI8xCsd/%E6%BE%94%E5%AD%B8%E4%B8%B2%E6%8E%A5%E6%A9%9F%E5%88%B6%E8%A6%8F%E5%8A%83?node-id=893-2866&t=3pcirVamNl1M0Kra-0" %}

### 3. 新北專屬世界邏輯：

在了解新北專屬世界邏輯前，必須先知道我們因為 [2017\~ 新北電競與暑假作業](https://redmine.bonio.com.tw/issues/5791) 的合作關係，所以當新北使用者透過澔學登入後，我們會依據師生所屬的年段（僅限國中小）與 one\_campus\_app 資料， 在公開世界中執行「基本資料更新」，所以新北在公開世界會有班級資訊，<mark style="color:red;">而這個班級跟縣市合作案完全無關</mark>

新北專屬世界邏輯主要分為以下兩種：

#### A. 加入專屬世界與班級

根據使用者身份不同，我們會執行不同的行為：

1. 學生：加入班級、授權教材（僅有班級授權）
2. 老師：給予教師後台權限、加入班級（如屬於校管權限則會加入更多符合條件班級）

{% embed url="https://www.figma.com/board/q93nPzlkCkL1u37WI8xCsd/%E6%BE%94%E5%AD%B8%E4%B8%B2%E6%8E%A5%E6%A9%9F%E5%88%B6%E8%A6%8F%E5%8A%83?node-id=893-2717&t=3pcirVamNl1M0Kra-0" %}

**B. 授權與移除使用者教材**

會根據授權教材清單、同學身上帶有的學年學期資訊進行教材授權與移除：

1. 授權教材：同學學年學期符合授權條件，且班級被寫在教材授權清單中。（授權教材是寫死的）
2. 移除教材：
   1. 執行條件：
      1. 使用者未授權教材：同學身上有「數位學習精進案自動授權」標籤的教材 - 使用者目前有授權的教材&#x20;
      2. 使用者未授權教材的教材起派日與「當前學年學期」一致
   2. &#x20;執行結果：
      1. 取消訂閱，使用者之後不會再收到新教材
      2. 使用者無法看到過去已派發的任務紀錄與答題數據 (user\_mission 變更為 canceled)，如該 user\_mission 仍在其他教材(resouse\_id)之下時，使用者一樣可以看到該任務與答題數據

{% embed url="https://www.figma.com/board/q93nPzlkCkL1u37WI8xCsd/%E6%BE%94%E5%AD%B8%E4%B8%B2%E6%8E%A5%E6%A9%9F%E5%88%B6%E8%A6%8F%E5%8A%83?node-id=893-2810&t=3pcirVamNl1M0Kra-0" %}
