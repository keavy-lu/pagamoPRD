# 二：目標用戶與價值

## 目標用戶

2S、2G 世界中，會在**教師後台**使用**素養數據**頁的教師



112-1 學期（2024/2/16\~2024/6/30），GA4 相關數據：

<table><thead><tr><th width="115">世界</th><th width="235" data-type="number">進入教師後台的活躍人數</th><th width="247" data-type="number">進入素養數據頁的活躍人數</th><th>佔比</th></tr></thead><tbody><tr><td>2S 世界</td><td>293</td><td>261</td><td>89%</td></tr><tr><td>2G 世界</td><td>9051</td><td>5296</td><td>59%</td></tr></tbody></table>

<details>

<summary> 名詞、數據定義</summary>

* 世界：
  1. 2S 世界：參考 [metabase 列表](https://metabase-da.pagamo.org/question#eyJkYXRhc2V0X3F1ZXJ5Ijp7ImRhdGFiYXNlIjoyLCJxdWVyeSI6eyJzb3VyY2UtdGFibGUiOjE0fSwidHlwZSI6InF1ZXJ5In0sImRpc3BsYXkiOiJ0YWJsZSIsInZpc3VhbGl6YXRpb25fc2V0dGluZ3MiOnt9fQ==)（排除測試世界 & 一次性活動世界）
  2. 2G 世界：參考 [metabase 列表](https://metabase-da.pagamo.org/question#eyJkYXRhc2V0X3F1ZXJ5Ijp7ImRhdGFiYXNlIjozMCwidHlwZSI6InF1ZXJ5IiwicXVlcnkiOnsic291cmNlLXRhYmxlIjo1MzF9fSwiZGlzcGxheSI6InRhYmxlIiwidmlzdWFsaXphdGlvbl9zZXR0aW5ncyI6e319)
* 頁面：
  1. 教師後台：網址包含 “/teacher\_console”
  2. 素養數據頁：網址包含 “/teacher\_console/literacy“
* 活躍人數：GA4 中的[活躍使用者](https://support.google.com/analytics/answer/12253918?hl=zh-Hant) → 只要在 1 秒內偵測到 [user\_engagement](https://support.google.com/analytics/answer/9234069#user_engagement) 事件，系統就會將使用者視為活躍使用者。

</details>

## 主要問題定義

1. 目前素養任務**送出作答數據**至教師後台的時間點為「任務完成」時，此機制導致老師需等到學生**將任務中題目皆作答到全對**後，才有辦法在教師後台查看學生的作答數據。
2. 有些學生無法在課堂中作答到全對，導致上課過程中，作答數據始終不會出現在教師後台中，並衍生以下問題：
   1. 老師無法透過教師後台分辨學生在該任務是處於何種狀態，包含：未開始、已開始、完成首次作答。故老師僅能口頭向同學一一確認他們是否已開始作答、是否將所有題目皆已作答過一次
   2. 學生即使已將任務中的所有題目皆作答過一次，已經可計算正確率、答對題數、作答時間等數據，但若是尚未作答到全對，此時教師後台仍看不到這些數據。故老師便無法查看這些學生的作答狀&#x6CC1;**（這個時間點需要知道詳細數據嗎？還是只要知道學生「已完成首次作答」就好？）**

#### 補充資訊

1. 目前「任務完成」的定義為：
   1. 遊戲：任務中的題目做到全對後，並按下「完成任務」按鈕
   2. 學習中心：任務中的題目做到全對後
2. 參考數據：
   1. 112-2 學期（2024/2/16\~2024/6/30），2G 世界的所有作答記錄中（包含已完成、未完成任務），第一次作答就全對的人數佔比為 10.4%，老師可以在教師後台第一時間查看到學生的作答數據。故有 89.6% 的作答記錄是學生完成第一次作答後，教師後台仍無法查看作答數據（[撈數據票](https://redmine.bonio.com.tw/issues/40029)）

## 解決方向（High Level Approach）

當學生**首次完成任務中的所有題目**後，老師便可以在教師後台第一時間掌握學生的作答數據

## 目標與衡量指標

### 目標

1. 老師可以在學生將任務中的所有題目皆答過一次後（不論答對答錯，只要每一題皆有答題紀錄），便在教師後台看到**首次作答數據**（含正確率、作答時間等）
2. 老師可以透&#x904E;**「任務狀態」**&#x4F86;辨別學生在該任務的作答狀態。包含：
   1. 未收到任務
   2. 未開始
   3. 已開始
   4. 完成首次作答
   5. 完成任務
3. 因應目標 1，讓**平均正確率、平均作答時間**皆改為「完成首次作答」的任務都列入計算



### 非本次目標（產品目標之一，只是這次先不做）

### 成功的衡量方式

優化上線後，由運營協助向常使用素養數據頁的老師們，收集針對此優化的質性回饋

## 產品規劃時程

1. 預計交付時程：可能是合約相關、產品先訂的交付時間
2. 先粗估預計規劃、進到設計開發的時間

<table><thead><tr><th width="148">階段</th><th width="129">開始時間</th><th width="99">deadline</th><th width="115">時程原因</th><th>實際上線時間</th></tr></thead><tbody><tr><td>需求收斂</td><td>9/30</td><td></td><td></td><td></td></tr><tr><td>初版解決方案(Alan/Jeff/YuWen/Amy)</td><td></td><td></td><td></td><td></td></tr><tr><td>完整解決方案(預排會議）</td><td></td><td></td><td></td><td></td></tr><tr><td>設計</td><td></td><td></td><td></td><td><br></td></tr><tr><td>後端</td><td></td><td></td><td></td><td></td></tr><tr><td>前端</td><td></td><td></td><td></td><td></td></tr><tr><td>目標時程（上線）</td><td></td><td></td><td></td><td></td></tr></tbody></table>

## 共識取得

{% hint style="danger" %}
綠色圓圈 + V：代表跨部門主管均對此章節內容有共識

藍色圓圈 +！：代表正在共識會議的討論過程中

橙色圓圈 +！：代表 PM 已經完成一版，可作為共識會議前的閱讀資料

紅色三角形 +！：代表 PM 撰寫中，內容可能會極大的變化
{% endhint %}

| Role           | Reviewer(確認後簽名) |
| -------------- | --------------- |
| K12 PM窗口       |                 |
| PM Head        |                 |
| CTO            |                 |
| Design Head    |                 |
| Front-end Lead |                 |
