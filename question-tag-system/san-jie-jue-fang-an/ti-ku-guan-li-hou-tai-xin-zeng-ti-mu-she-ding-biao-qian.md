# 題庫管理後台-新增題目設定標籤

## 參考連結

FIGMA：[點我](https://www.figma.com/design/YB9WjpbdDWB5mCT6bGx4qu/%E9%A1%8C%E7%9B%AE%E6%A8%99%E7%B1%A4%E5%8A%9F%E8%83%BD?node-id=2058-310\&t=qRz8RQFQ7IkoDPKw-0)

## 需求目標

1. 新增進階標籤篩選區塊，可以篩選[有設定適用此課程世界的標籤](guan-li-zhe-hou-tai-biao-qian-guan-li-2025101.md)。
2. 課程管理者出題時，可在[題目上標註適合此課程世界的標籤](guan-li-zhe-hou-tai-biao-qian-guan-li-2025101.md)。
   * 支援批量的方式標註標籤。

## 實作方向 - 題目總覽功能

1. 題目總覽，新增 『 進階標籤篩選 』 的區塊，裡面可篩選的標籤來自，[標籤管理](guan-li-zhe-hou-tai-biao-qian-guan-li-2025101.md)中有設定適用此課程的標籤。
   * 標籤的下拉選項中，除了有底下各階層的標籤，也會有 『 無 』 的選項，篩選無的話會把沒有標註過此類型的題目篩出來，讓管理者可以進行標注。
   * 標籤名稱的顯示順序，由建立日期新到舊排序
   * 每個類型的標籤都可以進行複選。
     * 範例：適合對象內有<mark style="color:red;">**一年級**</mark>和<mark style="color:red;">**二年級**</mark>2個標籤，使用者可以一次選2個進行篩選
   * 每個同類型內的標籤如果有複選會是聯集，不同類型的標籤篩選則會是交集。
     *   範例：假設適合對象類型選了<mark style="color:red;">**一年級**</mark>和<mark style="color:red;">**二年級**</mark>標籤，學習領域選了<mark style="color:red;">**數學**</mark>的標籤，預期呈現的篩選結果會是

         (適合對象=一年級 <mark style="color:blue;">**OR**</mark> 二年級) <mark style="color:blue;">**AND**</mark> (學習領域=數學)

<figure><img src="../.gitbook/assets/image (20).png" alt=""><figcaption></figcaption></figure>

2. 篩選題目時新增 『 新增進階標籤 』 和 『 刪除進階標籤 』 功能，課程管理者可以批量新增或刪除標籤。
   1. 開啟批量標註時不會呈現任何標籤的勾選狀態。
      1. 批量新增和刪除的範例如下，假設有A B C三題題目，各自標註不同標籤
         1. A: 『適合對象: 五年級』 + 『學習領域: 自然, 社會』
         2. B: 『適合對象: 六年級 』+ 『學習領域: 社會』
         3. C:  都沒標注任何標籤
      2. **呈上所述，新增標籤的範例**
         1. 如果選了 <mark style="color:red;">『適合對象: 六年級』</mark> 標籤，系統就標註A和C，因爲B已經有所以不用重複標註。
         2. 如果選的標籤，本身都已經標註在A B C上的話，就不需執行任何動作。
      3. **呈上所述，刪除標籤的範例**
         1. 管理者如果選了<mark style="color:red;">適合對象: 六年級</mark> ，就把B的<mark style="color:red;">適合對象: 六年級標籤</mark>進行刪除。
         2. 如果管理者要刪除的標籤，都沒有在題目上，就不需執行任何動作。
   2. 不論新增或刪除，標籤都可以複選。

<figure><img src="../.gitbook/assets/image (21).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (23).png" alt=""><figcaption></figcaption></figure>



3. 題目上標註的進階標籤，都會顯示在題目總覽的預覽上面，如示意圖。
   * 標籤上有hover，會顯示該標籤的上層結構會。

<figure><img src="../.gitbook/assets/image (36).png" alt=""><figcaption><p>標籤會顯示在題目預覽上</p></figcaption></figure>

<figure><img src="../.gitbook/assets/image (24).png" alt="hover會顯示上層節點"><figcaption><p>hover會顯示上層節點</p></figcaption></figure>

## 實作方向 - 新增題目功能

1. 新增題目時，在 『 難易度設定的區塊 』 下方，加入『 進階標籤設定區塊 』，課程管理者出題時可以[設定適用此課程世界的標籤](guan-li-zhe-hou-tai-biao-qian-guan-li-2025101.md)。
   1. 如果是題組，母題和子題都能建立標籤
   2. 標籤名稱的顯示順序，由建立日期新到舊排序

<figure><img src="../.gitbook/assets/image (38).png" alt=""><figcaption><p>新增題目設定進階標籤-示意圖</p></figcaption></figure>
