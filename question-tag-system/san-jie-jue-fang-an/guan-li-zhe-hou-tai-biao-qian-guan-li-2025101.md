# 管理者後台-標籤管理 (2025/10/1)

## 參考連結

FIGMA：[點我](https://www.figma.com/design/YB9WjpbdDWB5mCT6bGx4qu/%E9%A1%8C%E7%9B%AE%E6%A8%99%E7%B1%A4%E5%8A%9F%E8%83%BD?node-id=108-13\&p=f\&t=qRz8RQFQ7IkoDPKw-0)

## 需求目標

1. 管理者後台新增 『 **標籤管理** 』 的功能
   * 管理者可以新增或刪除標籤
   * 管理者可以設定標籤適合的課程世界
2. **標籤格式相關定義**
   1. 是樹狀結構但是非階層標籤，<mark style="color:$danger;">**只有最底層是標籤**</mark>，其餘的<mark style="color:$danger;">**中間階層**</mark>都只是分類，可以不斷展開分類。
   2. root的命名可以重複，能設定description進行說明。
   3. 標籤命名可以重複，能設定description進行說明。
   4. 樹狀階層要一致，標籤不可以散布不同階層，需統一最底層為標籤。
   5. 標籤要標註在q\_info不要標註在question上。
3.  **標籤格式相關範例**

    1. 正確範例：如下圖所示，標籤統一在第三層，第一層是名稱其餘都只是分類而已。

    <figure><img src="../.gitbook/assets/image (48).png" alt="" width="375"><figcaption></figcaption></figure>

    b. 錯誤範例：如下圖所示，標籤不可散布於不同階層，需同步在最底層，否則無法建立。

    <figure><img src="../.gitbook/assets/截圖 2025-10-04 凌晨1.09.34.png" alt="" width="563"><figcaption></figcaption></figure>

## 實作方向

1. 管理者後台->產品管理->教案資源下新增 『 標籤管理 』

<figure><img src="../.gitbook/assets/image (44).png" alt=""><figcaption><p>新增標籤管理</p></figcaption></figure>

2. 標籤管理總覽介面，排序和顯示規則如下。

* 排序規則：標籤建立日期由新到舊。
* 標籤顯示數量：10筆/頁。
* 總覽頁面會顯示下列欄位。

<table><thead><tr><th width="144" align="center">欄位名稱</th><th width="292" align="center">資料來源</th><th align="center">其他備註</th></tr></thead><tbody><tr><td align="center">標籤名稱</td><td align="center">建立標籤時的Root節點</td><td align="center">-</td></tr><tr><td align="center">標籤描述</td><td align="center">建立標籤時，需要一併建立</td><td align="center">-</td></tr><tr><td align="center">適用課程世界</td><td align="center">建立標籤時，能設定可以使用的世界</td><td align="center">-</td></tr><tr><td align="center">建立人員</td><td align="center">建立該標籤的帳號</td><td align="center">-</td></tr><tr><td align="center">標籤建立日期</td><td align="center">建立該標籤的日期 (YYYY/MM/DD)</td><td align="center">-</td></tr><tr><td align="center">操作</td><td align="center">-</td><td align="center">『 刪除 』 或是 『 編輯查看 』 標籤</td></tr></tbody></table>

<figure><img src="../.gitbook/assets/image (49).png" alt=""><figcaption></figcaption></figure>

3. 管理者可建立新的標籤，相關步驟如下。

* 第一步驟：點擊新增標籤按鈕，需建立標籤名稱、標籤描述、適用課程世界。

<table><thead><tr><th width="131" align="center">欄位名稱</th><th width="89" align="center">是否必填</th><th width="267" align="center">用途</th><th align="center">其他備註</th></tr></thead><tbody><tr><td align="center">標籤名稱</td><td align="center">必填</td><td align="center">設定後下一步建立標籤時，標籤名稱會是 Root 節點</td><td align="center">屆時在<mark style="color:red;">標注題目</mark>或<mark style="color:red;">篩選題目</mark>時，都會用此標籤名稱做類別分類。</td></tr><tr><td align="center">標籤描述</td><td align="center">非必填</td><td align="center">標籤名稱重複命名時，可填描述來協助判斷。</td><td align="center">-</td></tr><tr><td align="center">適用課程世界</td><td align="center">非必填</td><td align="center">設定後，標籤才能在該課程世界使用</td><td align="center">-</td></tr></tbody></table>

<figure><img src="../.gitbook/assets/image (50).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (14).png" alt=""><figcaption></figcaption></figure>

* 第二步驟：設定完標籤名稱和描述後，會自動建立<mark style="color:blue;">**標籤名稱Root**</mark>，並且可在該名稱底下新增Node分類
  * 每個節點都能透過移動連結線去做階層的區分
  * 如果刪除上層的分類，仍然會保留他下層，只是管理者須重新拉連結線去關連。

<figure><img src="../.gitbook/assets/image (15).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (16).png" alt=""><figcaption></figcaption></figure>

* 第三步驟，按下新增建立後，就能成功建立標籤，並且回到標籤總覽頁面。
  * 如果所有分類的階層不一致，則會建立失敗，因為<mark style="color:$danger;">**標籤不可以散布不同階層，需統一最底層為標籤**</mark>

