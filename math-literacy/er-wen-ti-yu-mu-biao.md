# 二、問題與目標



## 目標用戶&#x20;

所有國小、國中的學生與老師

## 主要問題定義

數學是科學之母，也是學校老師關注的學科之一，但 PaGamO 目前缺乏數學素養產品。今年產品與教研團隊訪談 5 位國中小數學老師，根據老師在數學與數位教學的經驗分享，評估平台若直接上線數學素養產品會遇到下列四類問題：

1. **題型：**
   1. 不支援題組-填充題：數學素養通常由 200 - 350 字的文本與 3 個以上的題目組成 ([數學素養題目](si-qi-ta-xiang-guan-nei-rong/shu-xue-su-yang-ti-mu.md))，如題目只有選擇題時，（中低程度）使用者很可能透過選項回推答案或直接猜題，故會需要透過填充題讓使用者填寫正確答案
   2. 填充題答案無法輸入數學符號：數學素養的答案會由數學符號或代數組成（舉例：⅔，√5等），但目前平台填充題僅支援純文字輸入
2. **答題過程：**
   1. 沒有「計算紙」功能：數學素養答題與檢討著重思考計算，使用者作答過程常會需要紙筆、尺、畫圓等工具輔助學習
   2. 缺少「答題引導」機制：數學素養著重思考邏輯，如答題過程中能逐步引導使用者解題，會比一次看完全部詳解更有助於思考學習
   3. 題組子題答對還要再答一次：在數學素養中，使用者如觀念與計算過程正確，答對後就幾乎不會再錯，再次填寫也會造成使用者要反覆填寫一樣答案的困擾
3. **持續學習：**
   1. 素養任務與學科題目之間缺少知識點連結：數學素養任務的知識點會對應至特定學科章節題目，但目前平台並未建立此連結，導致同學很難在平台中持續學習
4. **老師教學需求：**
   1. 老師很難了解同學的思考脈絡：假設平台有提供同學「計算紙」功能，如老師可以看到同學計算紙上的內容，更可以進一步了解同學的思考方式
   2. 老師很難了解同學對特定知識點的精熟程度：數學素養與學科章節題目會有相似的知識點，老師會想知道同學在特定知識點的學習成效

## 解決方向（High level Approach)&#x20;

產品會透過開發數學素養產品優化平台功能，第一階段會優先解決數學素養產品遇到的問題，再往下推動產品發展

{% content-ref url="san-jie-jue-fang-an/ti-xing-ati-xing-ping-tai-bu-zhi-yuan-ti-zu-tian-chong-ti-tian-chong-ti-da-an-wu-fa-shu-ru-shu-xue-f/" %}
[ti-xing-ati-xing-ping-tai-bu-zhi-yuan-ti-zu-tian-chong-ti-tian-chong-ti-da-an-wu-fa-shu-ru-shu-xue-f](san-jie-jue-fang-an/ti-xing-ati-xing-ping-tai-bu-zhi-yuan-ti-zu-tian-chong-ti-tian-chong-ti-da-an-wu-fa-shu-ru-shu-xue-f/)
{% endcontent-ref %}

{% content-ref url="san-jie-jue-fang-an/da-ti-guo-cheng-a+-jiao-xue-xu-qiu-aji-suan-zhi-gong-neng-lao-shi-hen-nan-liao-jie-tong-xue-de-si-ka.md" %}
[da-ti-guo-cheng-a+-jiao-xue-xu-qiu-aji-suan-zhi-gong-neng-lao-shi-hen-nan-liao-jie-tong-xue-de-si-ka.md](san-jie-jue-fang-an/da-ti-guo-cheng-a+-jiao-xue-xu-qiu-aji-suan-zhi-gong-neng-lao-shi-hen-nan-liao-jie-tong-xue-de-si-ka.md)
{% endcontent-ref %}

<details>

<summary>答題過程 b：缺少「答題引導」機制（非 must have）</summary>

**數學素養上線 must have：**

**無。原因：**

1. 涉及出題的題目設計，此階段無法確認出題者能滿足，且快速調整題目內容
2. 此機制評估適用所有素養商品，可思考更貼合遊戲的做法，以及如何筆記模式整合（擷取資訊：畫出官方重點），建議將此機制獨立處理，不要被數學素養時程限制

**產品長期：**

1. 素養題型會強調文本閱讀，須先花時間閱讀理解，且具備對應的知識能力後才能有效答題。要回答正確的投入心力與時間遠大於自選章節的簡短題目，預期有下列可提高素養任務的答題意願：
   1. 任務前引起興趣（故事、影片等）
   2. 確認應具備的能力（先備知識）
   3. 分階段答題引導
   4. 提高遊戲收益

***

補充：25年2月有將題組答題正確的攻擊力 x 2，可以觀察此遊戲機制的調整，對素養題組答題的影響

</details>

{% content-ref url="san-jie-jue-fang-an/da-ti-guo-cheng-cti-zu-zi-ti-da-dui-huan-yao-zai-da-yi-ci.md" %}
[da-ti-guo-cheng-cti-zu-zi-ti-da-dui-huan-yao-zai-da-yi-ci.md](san-jie-jue-fang-an/da-ti-guo-cheng-cti-zu-zi-ti-da-dui-huan-yao-zai-da-yi-ci.md)
{% endcontent-ref %}

{% content-ref url="san-jie-jue-fang-an/chi-xu-xue-xi-asu-yang-ren-wu-yu-xue-ke-ti-mu-zhi-jian-que-shao-zhi-shi-dian-lian-jie.md" %}
[chi-xu-xue-xi-asu-yang-ren-wu-yu-xue-ke-ti-mu-zhi-jian-que-shao-zhi-shi-dian-lian-jie.md](san-jie-jue-fang-an/chi-xu-xue-xi-asu-yang-ren-wu-yu-xue-ke-ti-mu-zhi-jian-que-shao-zhi-shi-dian-lian-jie.md)
{% endcontent-ref %}

<details>

<summary> 教學需求 b：老師很難了解同學對特定知識點的精熟程度（非 must have）</summary>

**數學素養上線 must have：**

**無。原因：**

1. 題目知識點標記須考量不同學科需求來設計架構，故不建議綁定數學素養的上線時程
2. 數學素養推薦章節機制上線後，後續可調整至推薦章節的指定題目
3. 推薦章節或題目都要搭配章節精熟機制，對使用者才有更高價值

**產品長期：**

1. 重新設計學生「定標」階段（學什麼？），預期涉及自選章節與任務書的調整
2. 老師能看到學生自選章節的表現，能看到針對特定知識點的綜合表現（自選章節、任務書）

</details>

## 目標與衡量指標

### 目標&#x20;

從產品整體需求出發規劃，確保在 114-1 學期完成數學素養會使用到的平台功能 (must have)

### 非本次目標&#x20;

\-

### 成功的衡量方式&#x20;

1. 在數學素養任務中，至少 30% 使用者使用過計算紙功能（再對標筆記模式）
2. 114-1 學年度數學素養營收達到預定目標（1600萬）

## 產品規劃時程&#x20;

| 階段    | 開始時間 | Deadline                        | 時程原因      | 實際上線時間 |
| ----- | ---- | ------------------------------- | --------- | ------ |
| 產品規劃  |      | <p>20250315-</p><p>20250415</p> | 不同問題有不同時間 |        |
| 設計    |      | 20250515                        |           |        |
| 開發完成  |      | 20250715                        |           |        |
| 測試修改完 |      | 20250815                        |           |        |
| 正式使用  |      | 20250901                        |           |        |



## 階段狀態&#x20;

❌ 本階段尚未取得共識，請勿往下一階段進行&#x20;

✅  代表跨部門主管均對此章節內容有共識



<table><thead><tr><th>階段</th><th width="280">參與者</th><th>狀態</th></tr></thead><tbody><tr><td>PM 內部共識&#x26;Review</td><td>Miles, Maggie, Alan, Seven, 峻賓, 羽慈, 姵儀</td><td>✅</td></tr><tr><td>K12PM 共識</td><td>Miles, Alan, 葉子, 思羽, Corrine</td><td>✅</td></tr><tr><td>產品團隊問題目標共識</td><td>Miles, Alan, Jeff, 昱雯, Elena, Seven, 峻賓</td><td>✅</td></tr></tbody></table>





