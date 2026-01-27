# 三：開發工項

## 如之前未接觸澔學相關流程，在開發前，可先閱讀：

{% content-ref url="../si-qi-ta-xiang-guan-nei-rong/hao-xue-zhang-hao-deng-ru-xian-kuang.md" %}
[hao-xue-zhang-hao-deng-ru-xian-kuang.md](../si-qi-ta-xiang-guan-nei-rong/hao-xue-zhang-hao-deng-ru-xian-kuang.md)
{% endcontent-ref %}

## 澔學登入改版流程總覽： <a href="#id-1" id="id-1"></a>

1. 流程檔案位置：[FigJam](https://www.figma.com/file/q93nPzlkCkL1u37WI8xCsd/%E6%BE%94%E5%AD%B8%E4%B8%B2%E6%8E%A5%E6%A9%9F%E5%88%B6%E8%A6%8F%E5%8A%83?type=whiteboard\&node-id=0-1)
2. 此流程由左至右，總計分為 4 個部分，簡單說明如下：
   1. 使用者與公開世界資料更新：根據澔學資料更新 user 與 GC 在三大公開世界的班級與權限設定
   2. 加入專屬世界流程：如果來自新北/花蓮澔學，就根據條件加入指定世界與班級、並給予對應的權限
   3. 專屬世界教材授權與移除流程：根據年段授權或班級授權清單，授權或移除學生教材對應的任務相關資料
   4. 專屬世界班級封存與退出流程：根據師生 API 班級資料，判斷是否退出或封存特定的 PaGamO 班級

{% embed url="https://www.figma.com/board/q93nPzlkCkL1u37WI8xCsd/%E6%BE%94%E5%AD%B8%E4%B8%B2%E6%8E%A5%E6%A9%9F%E5%88%B6%E8%A6%8F%E5%8A%83?node-id=893-2601&t=3pcirVamNl1M0Kra-0" %}

## 工項總覽

Redmine 母票：[https://redmine.bonio.com.tw/issues/38286](https://redmine.bonio.com.tw/issues/38286)

<table><thead><tr><th width="342">工項名稱</th><th width="74">team</th><th>redmine 追蹤票</th></tr></thead><tbody><tr><td><a data-mention href="./#id-1-1">#id-1-1</a></td><td>後端</td><td><a href="https://redmine.bonio.com.tw/issues/38448">https://redmine.bonio.com.tw/issues/38448</a></td></tr><tr><td><a data-mention href="./#id-1-2">#id-1-2</a></td><td>後端</td><td><a href="https://redmine.bonio.com.tw/issues/38286">https://redmine.bonio.com.tw/issues/38286</a></td></tr><tr><td><a data-mention href="./#c1131-yi-chu-onecampusapps-zhong-hua-lian-jiao-shi-quan-xian-de-xiang-guan-luo-ji">#c1131-yi-chu-onecampusapps-zhong-hua-lian-jiao-shi-quan-xian-de-xiang-guan-luo-ji</a></td><td>後端</td><td><a href="https://redmine.bonio.com.tw/issues/38450">https://redmine.bonio.com.tw/issues/38450</a></td></tr><tr><td><a data-mention href="./#d1131-yi-chu-hua-lian-ji-you-jiao-cai-shou-quan-gui-ze">#d1131-yi-chu-hua-lian-ji-you-jiao-cai-shou-quan-gui-ze</a></td><td>後端</td><td><a href="https://redmine.bonio.com.tw/issues/38451">https://redmine.bonio.com.tw/issues/38451</a></td></tr><tr><td><a data-mention href="./#e-1131-xin-zeng-hao-xue-zhuan-shu-shi-jie-gui-ze">#e-1131-xin-zeng-hao-xue-zhuan-shu-shi-jie-gui-ze</a></td><td>後端</td><td><a href="https://redmine.bonio.com.tw/issues/38452">https://redmine.bonio.com.tw/issues/38452</a></td></tr><tr><td><a data-mention href="./#f-ban-ji-zi-dong-tui-chu-yu-feng-cun-ji-zhi">#f-ban-ji-zi-dong-tui-chu-yu-feng-cun-ji-zhi</a></td><td>後端</td><td><a href="https://redmine.bonio.com.tw/issues/38590">https://redmine.bonio.com.tw/issues/38590</a></td></tr><tr><td><a data-mention href="./#g1131-xin-zeng-hao-xue-guan-li-hou-tai">#g1131-xin-zeng-hao-xue-guan-li-hou-tai</a></td><td>後端</td><td>SP235 開工</td></tr><tr><td><a data-mention href="./#g1131-xin-zeng-hao-xue-guan-li-hou-tai">#g1131-xin-zeng-hao-xue-guan-li-hou-tai</a></td><td>前端</td><td>SP236 開工</td></tr></tbody></table>

## A：112-2 與 113-1 機制並存處理 <a href="#id-1" id="id-1"></a>

1. 雖然[教育部規定](https://edu.law.moe.gov.tw/LawContent.aspx?id=FL008424)每年 8/1，各縣市需要將師生學籍資料更新至新學年，但因各學校有不同的需求（如暑假作業、較晚排定課表等），所以導致各學校更新速度不一，我們會在新學期之後遇到登入的師生們，有些還在 112-2 學期，但有些已經更新為 113-1 的情況
2. 使用者採用澔學登入的核心規則為：當 API 的資料跟 PaGamO 當前學年學期資料一致時，就會執行 「PaGamO 當前學年學期」所屬學年學期的流程（實作細節相對複雜，RD整理在：[slack](https://bonio.slack.com/archives/C04QF8AATS8/p1721124495748819?thread_ts=1721114842.754819\&cid=C04QF8AATS8))
   1. &#x20;112-2 的師生維持使用既有機制([澔學帳號登入現況](../si-qi-ta-xiang-guan-nei-rong/hao-xue-zhang-hao-deng-ru-xian-kuang.md))
   2. &#x20;113-1 的師生則走新上線的機制

<details>

<summary>Q：為什麼要只有 API 跟當前學期一致，系統才會動作？</summary>

1. 即使不一致可以加入世界也沒有班級/教材授權，實際對教學一樣是有問題
2. 現在我們對縣市說法都是資料一定要正確，有請數辦要求學校開學階段要盡力做好更新，我們也搭配教師公告通知學校。跟過去相比，資料錯誤的情況，113-1時，我們也比較有能力跟學校溝通

討論串：[slack](https://bonio.slack.com/archives/C04QF8AATS8/p1721275114213059?thread_ts=1721212038.489819\&cid=C04QF8AATS8)

</details>

## B：113-1 新增公開世界建班的機制 <a href="#id-1" id="id-1"></a>

1. 112-2 國中小師生透過澔學登入時，屬於新北的師生會依據年段在不同公開世界建班，但花蓮不會。
2. 113-1 也會維持現況，但會將澔學師生是否在公開世界建班的機制，作為後續可讓運營控制的開關。
3. 當使用者關閉時不會在公開世界建立班級，打開時則會依據年段在不同公開世界建立班級
   1. 1-6 年級：對應國小天地
   2. 7-9年級：對應國中世界
4. 與後端葉子在討論過程中有提到可以在 one\_campus\_app 中設定使用者對應的世界

{% embed url="https://www.figma.com/board/q93nPzlkCkL1u37WI8xCsd/%E6%BE%94%E5%AD%B8%E4%B8%B2%E6%8E%A5%E6%A9%9F%E5%88%B6%E8%A6%8F%E5%8A%83?node-id=893-2009&t=PHWwqvflBV3EcSSb-1" %}

## C：113-1 移除 one\_campus\_apps 中花蓮教師權限的相關邏輯

1. 在教師更新流程中，有一段「該 one\_campus\_apps 所對應的學校為花蓮公校?」然後再做老師權限的設定等機制，就直接全部移除。
2. 這邊的機制會在 [#e1-jia-ru-zhuan-shu-shi-jie-yu-ban-ji](./#e1-jia-ru-zhuan-shu-shi-jie-yu-ban-ji "mention")中補回

{% embed url="https://www.figma.com/board/q93nPzlkCkL1u37WI8xCsd/%E6%BE%94%E5%AD%B8%E4%B8%B2%E6%8E%A5%E6%A9%9F%E5%88%B6%E8%A6%8F%E5%8A%83?node-id=893-1921&t=3pcirVamNl1M0Kra-0" %}

## D：113-1 移除花蓮既有教材授權規則

1. 既有流程有一段花蓮授權邏輯，請直接移除（以下為現況的邏輯內容）
2. 移除的教材授權規則，會在 [#e-1131-xin-zeng-hao-xue-zhuan-shu-shi-jie-gui-ze](./#e-1131-xin-zeng-hao-xue-zhuan-shu-shi-jie-gui-ze "mention")中補回

{% embed url="https://www.figma.com/board/q93nPzlkCkL1u37WI8xCsd/%E6%BE%94%E5%AD%B8%E4%B8%B2%E6%8E%A5%E6%A9%9F%E5%88%B6%E8%A6%8F%E5%8A%83?node-id=831-1388&t=3pcirVamNl1M0Kra-0" %}

## E： 113-1 新增澔學專屬世界規則

### E1：加入專屬世界與班級

1. 規則主要參考教育雲 113-1  的做法：[Figma](https://www.figma.com/board/43zueGdZWB4MMHGDT0yjsg/%E6%95%99%E8%82%B2%E9%9B%B2%E4%B8%B2%E6%8E%A5%E6%A9%9F%E5%88%B6\(112-1%E9%96%8B%E5%A7%8B\)?node-id=1562-2486\&t=boWaSNV3gp9teLJw-0)，但並沒有納入教育雲在113-1 新增的私校功能，完整流程請參考如下：

{% embed url="https://www.figma.com/board/q93nPzlkCkL1u37WI8xCsd/%E6%BE%94%E5%AD%B8%E4%B8%B2%E6%8E%A5%E6%A9%9F%E5%88%B6%E8%A6%8F%E5%8A%83?node-id=799-2303&t=4QCt2BHUJzrMDAFv-0" %}

2. 流程中有關老師角色與老師角色所帶資料（職稱），會來自不同 API，請注意使用：
   1. 新北：my\_principal/get\_role
   2. 花蓮：getTeacher/get\_role
3. 注意職稱因為是人工輸入，所以處理職稱前，要去除空白轉小寫
   1. 花蓮：PaGamO管理者
4. 後續這邊跟教育雲一樣都從後台設定職稱關鍵字，職稱有包含該關鍵字就當成校管。後續上線預期設定：
   1. 花蓮：教務主任、校長、教導主任、教學組長、教務組長、pagamo管理者
   2. 新北：教務主任、校長、組長
5. 校管帳號清單（採用跟教育雲一樣的[清單格式](https://boniotw-my.sharepoint.com/:x:/r/personal/bonio_share_bonio_com_tw/_layouts/15/Doc.aspx?sourcedoc=%7B8109B0EB-C9C9-4C3B-9743-FBD0F30769CC%7D\&file=%E7%AF%84%E4%BE%8B_OO%E7%B8%A3%E5%B8%82_%E6%A0%A1%E7%AE%A1%E5%B8%B3%E8%99%9F%E6%B8%85%E5%96%AE_v2.xlsx\&action=default\&mobileredirect=true\&wdsle=0)）：
   1. 將用指定「管理者帳號」登入老師加入指定學校代碼的的（指定）學校班級
      1. 因澔學在不同縣市的帳號有不同domain（xxx@domain.com），只取前綴xxx可能有問題，所以管理者帳號必須填寫完整（教育雲也是取完整帳號）
      2. 僅限加入與「當前學年學期」相符合的 PaGamO 班級，舉例：
         1. 現在當前學年學期是 113-1，PaGamO 有 112-2\_501, 113-1\_601。清單上面 A 老師有寫 112-2 501, 113-1 601，老師就只會加入 113-1 601
   2. 如清單上未指定學校班級，則老師則可加入該學校代碼的所有班級。
   3. 學校班級驗證規則：總共可能是數3-4  位數，3位數字第一位是年級，後二是班級，例如 601。4位數前二位是年級，數字後兩位是班級，例如1001。

<details>

<summary>為什麼會有加入指定學校，然後再指定班級的需求？</summary>

1. 指定學校：當澔學資料有誤或老師同時任教兩個學校，但只有一間學校資料時，我們可以即時協助老師加入指定學校班級，而不用請老師回頭去找人修改資料
2. 指定班級：最初是加入指定學校的所有班級，但有時候老師只是缺少一兩個班級，他對自己能看到全校資料也會有疑慮，所以才新增此功能，完整說明可參考：會有指定班級的需求原因：[https://redmine.bonio.com.tw/issues/37690](https://redmine.bonio.com.tw/issues/37690)

</details>



### E2：授權與移除使用教材

#### 規則主要參考教育雲 112-2  的做法：[Figma](https://www.figma.com/board/43zueGdZWB4MMHGDT0yjsg/%E6%95%99%E8%82%B2%E9%9B%B2%E4%B8%B2%E6%8E%A5%E6%A9%9F%E5%88%B6\(112-1%E9%96%8B%E5%A7%8B\)?node-id=1377-2017\&t=boWaSNV3gp9teLJw-0)澔學調整後的流程如下：

{% embed url="https://www.figma.com/board/q93nPzlkCkL1u37WI8xCsd/%E6%BE%94%E5%AD%B8%E4%B8%B2%E6%8E%A5%E6%A9%9F%E5%88%B6%E8%A6%8F%E5%8A%83?node-id=893-3893&t=4QCt2BHUJzrMDAFv-0" %}

#### 澔學採用的授權清單格式新版範例：[Link](https://boniotw-my.sharepoint.com/:x:/r/personal/bonio_share_bonio_com_tw/_layouts/15/Doc.aspx?sourcedoc=%7B676b5ec6-0650-4a69-8d00-420d7f3dc597%7D\&action=editnew)

1. 學校聯絡人分頁單純運營紀錄使用，不特別處理
2. sheey\_name 必須為「中文教材班級申請表」或「英文教材班級申請表」才會做教材授權
3. 中文教材班級申請表、英文教材班級申請表分頁則需處理：
   1. 「該班主要推動教師」欄位系統實際不用用來做任何判斷，僅是方便運營人工辨識
   2. 依據學年度、學期、學校代碼、年級、班級，將 API 有對應班級資料的師生加入班級
   3. 依據學年度、學期、學校代碼、年級、班級、中文(英文)素養教材欄位，授權教材給班級內的學生
      1. 中文(英文)素養教材欄位是對應到[管理後台商品列表](https://www.pagamo.org/admin/products/subscribe_products)中的商品名稱



## F：班級自動退出與封存機制

1. 教育雲 113-1也有針對校管權限的教師退出班級做出調整，所以澔學開發過程參考教育雲時，建議與開發新版教育雲班級自動退出與封存機制的後端 RD 一起協作

## G：113-1 新增澔學管理後台

1. 流程中有關年級、GC到期日、年段授權、班級授權清單、特殊學校清單、特殊職稱、班級授權清單等都預計會是後台功能，
2. 上線時啟用狀態均為關閉。
3. 縣市名稱與課程代碼對應關係：
   1. 新北市：ntpc
   2. 花蓮縣：hlcrc
4. 可以參照既有教育雲後台設定：
5. 完整細節可參考： [guan-li-hou-tai-hao-xue-xiang-guan-she-ding-ye-mian.md](guan-li-hou-tai-hao-xue-xiang-guan-she-ding-ye-mian.md "mention") <mark style="color:red;">（想順便測試 PM 寫起來的感覺，以及前後端閱讀的感覺如何）</mark>

<figure><img src="../.gitbook/assets/image (3).png" alt=""><figcaption><p><a href="https://www.pagamo.org/admin/city_gov_case">https://www.pagamo.org/admin/city_gov_case</a></p></figcaption></figure>







