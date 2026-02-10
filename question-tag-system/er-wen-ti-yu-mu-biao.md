# 二、問題與目標

## 目標用戶&#x20;

* 老師：
  * 無法有效率地在平台上找到所需的題目時，可能轉用其它平台
    * 無法在單元下根據更小的知識單位篩選題目。
    * 教育部期望 114 年起計劃實施成效，希望老師在教學現場可以透過平台做前後測的成效檢核。
  * 使用素養教材意願低，影響到素養教材的作答狀況，此為付費簽約採購的參考指標之一
    * 難以將素養教材跟主科課程內容做連結，擔心使用素養教材會耽誤主科。
* 學生：無法有效率的自學，影響學習成效
  * 無法挑選適合程度的題目，學習成就低的學生遇到太難的題目，影響學習動力。
  * 無法快速辨識已熟悉與未掌握的知識點，需要做完整章節測驗，耗時費力。
* 內部：課程內容每學年微調，無法有效沿用舊題，需額外投入資源購買新題目。

<details>

<summary> 老師所需的知識點、測量向度的參考資料</summary>

**標記資料整理：**[https://boniotw-my.sharepoint.com/:x:/g/personal/reese\_chang\_bonio\_com\_tw/EbZmSzSNSTpAtnIMDgFVwJABlYuigyNWi3StSZq9uCrVtA?e=5oPKvJ](https://boniotw-my.sharepoint.com/:x:/g/personal/reese_chang_bonio_com_tw/EbZmSzSNSTpAtnIMDgFVwJABlYuigyNWi3StSZq9uCrVtA?e=5oPKvJ)

原始資料來源參考：

教育部課綱能力指標：[https://cirn.moe.edu.tw/WebContent/index.aspx?sid=11\&mid=363](https://cirn.moe.edu.tw/WebContent/index.aspx?sid=11\&mid=363)

學習扶助基本學習架構：[https://exam.tcte.edu.tw/tbt\_html/index.php?mod=instructionalresources](https://exam.tcte.edu.tw/tbt_html/index.php?mod=instructionalresources)

學力檢測評量架構：[https://saaassessment.ntcu.edu.tw/AssessmentFrame](https://saaassessment.ntcu.edu.tw/AssessmentFrame)

</details>

<details>

<summary>競爭者（類似功能舉例）</summary>

翰林雲端學苑

因材網

學習吧

酷英

均一

</details>



## 解決方向（High level Approach)&#x20;

**將題目所屬的「領域」、「適合對象」、「知識點」 標記在題目上，讓**使用者可以用「領域」、「適合對象」來找到所有符合教學範圍的題目，再用「知識點（學習內容、學習表現等等）」來快速分辨需要的題目。

1. 使用者可以用「領域」、「適合對象」的多種題目屬性來找到哪些題目符合教學範圍。
2. 讓使用者可以根據使用需求和情境，在題目上加上多種屬性的標記。
3. 讓使用者可以根據這些特徵，在不同題庫間找到擁有相同特徵的題目。



## 目標與衡量指標

### 目標&#x20;

簡潔明確說明此次要滿足的 User Stories ，不落入細節，依據重要程度排序

* 管理者可以在**管理者後台**管理「領域」、「適合對象」、「學習指標」 的內容項目，確保標籤系統的分類正確。
* 課程題庫管理者可以在**題庫管理後台**將題目設定「領域」、「適合對象」、「學習指標」 ，以便於更好地組織與檢索題目。
* 課程題庫管理者可以在**題庫管理後台**用「領域」、「適合對象」、「學習指標」 篩選出尚未標記的題目，以便快速將尚未標記的題目進行標記。
* 教師後台可以在打包作業時，用「領域」、「適合對象」、「學習指標」 篩選出符合學力檢測的題目

### 非本次目標&#x20;

簡述哪些範圍不是本次目標、這些範圍不是本次目標的原因

1. 非管理者，無法建立「領域」、「適合對象」、「知識點類型」標記，避免標籤過於混亂、難以查找
2. 非課程題庫管理者，無法對題目設定標記，等到此功能運作測試沒問題後，再逐步開放個人題庫或一般老師使用。



### 成功的衡量方式&#x20;

提供量化/質化的成功衡量方式（相關數據、訪談、問卷等協助描述）

* 第一階段功能滿足
  * **滿足數學素養教材的題目標記需求**
  * **滿足國語科學力檢測的題目標記需求**
*

## 產品規劃時程&#x20;

預計交付時程：可能是合約相關、產品先訂的交付時間 先粗估預計規劃、進到設計開發的時間



| 階段     | 開始時間      | Deadline   | 時程原因 | 實際上線時間 |
| ------ | --------- | ---------- | ---- | ------ |
| 需求收斂   | 2025/12/1 | 2025/12/31 |      |        |
| 初版解決方案 |           | 2025/3/31  |      |        |
| 完整解決方案 |           |            |      |        |
| 設計開發   |           |            |      |        |
| 完成上線   |           |            |      |        |



## 階段狀態&#x20;

❌ 本階段尚未取得共識，請勿往下一階段進行&#x20;

✅  代表跨部門主管均對此章節內容有共識



<table><thead><tr><th width="217">階段</th><th width="280">參與者</th><th>狀態</th></tr></thead><tbody><tr><td>PM 內部共識&#x26;Review</td><td>Alan, Miles</td><td>O</td></tr><tr><td>產品團隊問題目標共識</td><td>Alan, Jeff, Miles, Amy, Yuwen</td><td>❌</td></tr></tbody></table>





