# 教師後台-原章節出題方式，新增標籤進階篩選

## 參考連結

FIGMA：[點我](https://www.figma.com/design/YB9WjpbdDWB5mCT6bGx4qu/%E9%A1%8C%E7%9B%AE%E6%A8%99%E7%B1%A4%E5%8A%9F%E8%83%BD?node-id=2877-16551\&p=f\&m=draw)

## 需求目標

1. 教師使用章節找題目出作業時，當選擇完題目後，仍可利用[適用此課程的進階標籤做篩選](guan-li-zhe-hou-tai-biao-qian-guan-li-2025101.md)，把適合的題目篩選出來進行作業設定。

## 實作方向

1. 教師後台新增作業，當老師選擇用章節新增題目時

<figure><img src="../.gitbook/assets/image (5).png" alt=""><figcaption></figcaption></figure>

2. 選擇出題方式，這裡比照原本邏輯就好，只調整部分UI呈現方式。

<figure><img src="../.gitbook/assets/image (51).png" alt=""><figcaption></figcaption></figure>

2. 題目預覽時，[如管理者後台有開啟，『 章節出題(原出題方式)，開啟標籤篩開關](guan-li-zhe-hou-tai-xin-zeng-biao-qian-shai-xuan-ti-mu-kai-guan.md)，且同時滿足下列條件，則可以用標籤篩出自己需要的題目，題目預覽也能看到該題目有被標註的標籤。
   1. **需有課程題庫來的題目，不能全部都是個人題庫的題目。**
   2. **該課程世界需有進階標籤可以使用。**
3. 每個類型的標籤都可以進行複選。
   * 範例：適合對象內有<mark style="color:red;">**一年級**</mark>和<mark style="color:red;">**二年級**</mark>2個標籤，使用者可以一次選2個進行篩選
4. 每個同類型內的標籤如果有複選會是聯集，不同類型的標籤篩選則會是交集。
   *   範例：假設適合對象類型選了<mark style="color:red;">**一年級**</mark>和<mark style="color:red;">**二年級**</mark>標籤，學習領域選了<mark style="color:red;">**數學**</mark>的標籤，預期呈現的篩選結果會是

       (適合對象=一年級 <mark style="color:blue;">**OR**</mark> 二年級) <mark style="color:blue;">**AND**</mark> (學習領域=數學)

<figure><img src="../.gitbook/assets/image (8).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (9).png" alt=""><figcaption></figcaption></figure>

6. 後續流程就比照原本的新增作業方式邏輯，不用進行調整。
