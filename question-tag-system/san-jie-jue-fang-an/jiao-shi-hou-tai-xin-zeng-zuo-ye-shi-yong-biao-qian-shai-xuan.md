# 教師後台-新增作業使用標籤篩選

## 參考連結

FIGMA：[點我](https://www.figma.com/design/YB9WjpbdDWB5mCT6bGx4qu/%E9%A1%8C%E7%9B%AE%E6%A8%99%E7%B1%A4%E5%8A%9F%E8%83%BD?node-id=2877-16551\&p=f\&m=draw)

## 需求目標

1. 教師出作業時，可利用[適用此課程的進階標籤做篩選](guan-li-zhe-hou-tai-biao-qian-guan-li-2025101.md)，把適合的題目從不同題庫中篩選出來進行作業設定。

## 實作方向

1. [如管理者後台有開啟標籤篩選功能](guan-li-zhe-hou-tai-xin-zeng-biao-qian-shai-xuan-ti-mu-kai-guan.md)，且同時滿足下述條件時，教師後台新增作業時，增加用進階標籤，跨題庫篩選題目的選項，否則即時有開啟仍會隱藏。
   * 該課程世界需有課程題庫可以使用。
   * 該課程世界需有進階標籤可以使用。
2. 題目出題方式 UI/UX 呈現規則如下
   1. 僅有 1 種篩選方式時
      1. 預設展開
      2. 不需要收合功能
   2. 有超過 1 種篩選方式時
      1. 預設全部收合
      2. 僅允許同時間展開 1 種，若使用者展開另一種篩選方式，先前展開的會自動收合

<figure><img src="../.gitbook/assets/image (27).png" alt=""><figcaption></figcaption></figure>

2. 可以篩選要找尋的題目
   * 先選擇要找尋題目的題目來源。(可跨題庫找尋)
     1. 只會顯示課程題庫，因為題目標籤篩選暫時不支持個人題庫。
   * 可以透過[適用此課程世界的標籤](guan-li-zhe-hou-tai-biao-qian-guan-li-2025101.md)篩選該題庫內的題目。
     1. 每個類型的標籤都可以進行複選。
        * 範例：適合對象內有<mark style="color:red;">**一年級**</mark>和<mark style="color:red;">**二年級**</mark>2個標籤，使用者可以一次選2個進行篩選
     2. 每個同類型內的標籤如果有複選會是聯集，不同類型的標籤篩選則會是交集。
        *   範例：假設適合對象類型選了<mark style="color:red;">**一年級**</mark>和<mark style="color:red;">**二年級**</mark>標籤，學習領域選了<mark style="color:red;">**數學**</mark>的標籤，預期呈現的篩選結果會是

            (適合對象=一年級 <mark style="color:blue;">**OR**</mark> 二年級) <mark style="color:blue;">**AND**</mark> (學習領域=數學)

<figure><img src="../.gitbook/assets/image (28).png" alt=""><figcaption></figcaption></figure>

3. 選擇出題方式，這裡比照原本邏輯就好，只調整部分UI呈現方式。

<figure><img src="../.gitbook/assets/image (29).png" alt=""><figcaption></figcaption></figure>

4. 題目預覽時，題目來源新增適用此課程的進階標籤篩選，可以篩出自己需要的題目，題目預覽也能看到該題目有被標註的標籤。
   1. 每個類型的標籤都可以進行複選。
      * 範例：適合對象內有<mark style="color:red;">**一年級**</mark>和<mark style="color:red;">**二年級**</mark>2個標籤，使用者可以一次選2個進行篩選
   2. 每個同類型內的標籤如果有複選會是聯集，不同類型的標籤篩選則會是交集。
      *   範例：假設適合對象類型選了<mark style="color:red;">**一年級**</mark>和<mark style="color:red;">**二年級**</mark>標籤，學習領域選了<mark style="color:red;">**數學**</mark>的標籤，預期呈現的篩選結果會是

          (適合對象=一年級 <mark style="color:blue;">**OR**</mark> 二年級) <mark style="color:blue;">**AND**</mark> (學習領域=數學)

<figure><img src="../.gitbook/assets/image (31).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (32).png" alt=""><figcaption></figcaption></figure>

4. 後續流程就比照原本的新增作業方式邏輯，不用進行調整。
