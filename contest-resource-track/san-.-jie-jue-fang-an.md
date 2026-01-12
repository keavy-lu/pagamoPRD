# 三. 解決方案

## 功能(Key Features)

1.  透過電競賽的報名頁網址設定不同參數用來追蹤報名來源，新增以下約定參數。

    * utm\_source
    * utm\_medium
    * utm\_campaign

    範例：[https://esports.pagamo.org/register/2018newhope3\_4/information](https://esports.pagamo.org/register/2018newhope3_4/information)<mark style="color:red;">**?utm\_source=xxxxx\&utm\_medium=xxxxx\&utm\_campaign=xxxxx，**</mark>參數內的xxxxx可由管理者自行命名。
2. 追蹤電競賽參賽玩家的組成。(新玩家或舊玩家)。

## 執行方案

### 後端項目

1. 電競賽[報名者管理的『](https://www.pagamo.org/esports/manage/course/contestant_management?course_id=1252)[下載回應』報表](https://www.pagamo.org/esports/manage/course/contestant_management?course_id=1252)內新增『 報名入口』、『 報名媒介 』、『 報名活動 』 的欄位，當玩家報名成功後，前端直接將參數存入新增的資料欄位，格式如下
   1. 只支援英文數字和下底線。
   2. 不必區分大小寫。
   3. 不可超過32個字。
   4. 可以是空值。
2. 上述3個參數，要先有『 報名入口 』，才可以使用『 報名媒介 』和『 報名活動 』，如沒有報名入口，就不會存入另外2個參數
3. 電競賽[報名者管理的『下載回應』報表](https://www.pagamo.org/esports/manage/course/contestant_management?course_id=1252)新增『 帳號註冊日期 』，格式如下
   * yyyy/mm/dd
   * 用 『申請註冊帳號的日期』 即可(users.created\_at)
4. 報名的 API 要支援紀錄以下參數。
   1. utm\_source
   2. utm\_medium
   3. utm\_campaign
5. 下載回應的報表新增的『 報名入口』、『 報名媒介 』、『 報名活動 』和『帳號註冊日期』，全部放在最後欄位就行。

### 前端項目

1. 管理者可在報名網址上加入事前約定好的字串並設定要追蹤的參數，當玩家報名成功後，前端直接將參數存入新增的資料欄位，參考範例如下。
   * 電競賽網址： [**https://esports.pagamo.org/register/2018newhope3\_4/information?utm\_source=xxxxx\&utm\_medium=xxxxx\&utm\_campaign=xxxxx**](https://esports.pagamo.org/register/2018newhope3_4/information?utm_source=xxxxx\&utm_medium=xxxxx\&utm_campaign=xxxxx) ，『utm\_source』『utm\_medium 』  『utm\_campaign』 為約定的參數，其中xxxxx可由管理者自行命名。
2. 在用戶送出報名時，如果網址帶有上述約定的參數，要一併打給後端。
3. 電競賽報名頁設定畫面，新增文字提醒，文案畫面如下。

<figure><img src=".gitbook/assets/image (4).png" alt=""><figcaption></figcaption></figure>
