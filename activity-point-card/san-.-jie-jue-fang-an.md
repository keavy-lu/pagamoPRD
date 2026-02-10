# 三. 解決方案

## 參考連結

FIGMA：[點我](https://www.figma.com/design/BcnmQGscCESMKxUcif1k6U/43069-%E4%BB%BB%E5%8B%99%E9%9B%86%E9%BB%9E%E5%8D%A1%E6%B4%BB%E5%8B%95?node-id=2170-4\&p=f\&t=u3Z7m4GyfGvlN0j6-0)

## 功能(Key Features)

1. 用WIX建立活動的landing page。
2. landing page的CTA會導到任務集點卡頁面。
3. 玩家可以登入查看目前的任務狀態和任務進度條。
4. 集點卡集滿後，可以讓工作人員進行線下核銷，兌換實體贈品。

## 用戶流程(User Flow)

1. 玩家現場掃描QRCODE開啟活動頁的Landing Page
2. 登入PaGamO帳號，查詢活動完成狀態或是接活動任務
3. 完成任務後在現場找工作人員進行現場核銷，核銷成功後可兌換實體贈品
4. 上述完整的FLOW可參考FIGMA：[點我](https://www.figma.com/design/BcnmQGscCESMKxUcif1k6U/43069-%E4%BB%BB%E5%8B%99%E9%9B%86%E9%BB%9E%E5%8D%A1%E6%B4%BB%E5%8B%95?node-id=12-2\&p=f\&t=u3Z7m4GyfGvlN0j6-0)

## 實作方向-任務集點卡頁面

1. 玩家掃描QR CODR後會先進到用WIX建立的Landing Page。
   1. Landing Page能放活動視覺和活動辦法，到時候由MK和廠商討論決定
   2. Landing Page會有CTA按鈕，主要用來連到任務集點卡頁面。
2. 任務集點卡頁面上的內容主要分為以下區塊

<figure><img src=".gitbook/assets/image (3).png" alt=""><figcaption></figcaption></figure>

* header banner，合作廠商可以放自己logo或是活動可兌換贈品。
  * 未來如果不同活動會透過OP上傳圖檔。
* 活動的進度條和登入區塊，內容如下。
  * 進度條由前端進行計算，後端不提供計算結果。

<table><thead><tr><th width="230">活動進度條(實際以設計為準)</th><th width="94">登入狀態</th><th>顯示內容</th></tr></thead><tbody><tr><td><div><figure><img src=".gitbook/assets/image (15).png" alt=""><figcaption></figcaption></figure></div></td><td>未登入</td><td><ol><li>會有登入按鈕</li></ol></td></tr><tr><td><div><figure><img src=".gitbook/assets/image (16).png" alt=""><figcaption></figcaption></figure></div></td><td>已登入</td><td><ol><li>會顯示玩家暱稱的任務集點卡</li><li>會有登出按鈕</li><li>會有集點卡當下的完成進度</li><li>當暱稱為空時，只顯示任務集點卡</li></ol></td></tr></tbody></table>

* 活動需完成的任務區塊，內容如下。
  * 未來如果有不同活動，可以透過OP上傳任務資料。
  * 前端會去監聽事件，當網頁從背景拉回來時，會自動進行重新取資料的動作。
  * loading 時會以固定數量的 skeleton 來顯示，然後 loading 的有無取決於登入與否
    1. 未登入：後端塞 prop 讓前端直接呈現任務名稱、任務id
    2. 已登入：前端自行 query 要呈現的所有資料。

<table><thead><tr><th width="213">任務卡(實際以設計為準)</th><th width="99">登入狀態</th><th width="117">任務卡狀態</th><th>備註</th></tr></thead><tbody><tr><td><div><figure><img src=".gitbook/assets/image (4).png" alt=""><figcaption></figcaption></figure></div></td><td>未登入</td><td>請登入查看</td><td>如果尚未登入，任務狀態會是請登入查看</td></tr><tr><td><div><figure><img src=".gitbook/assets/image (7).png" alt=""><figcaption></figcaption></figure></div></td><td>已登入</td><td>未完成</td><td>未完成的狀態，會有接任務按鈕，導引玩家進遊戲接任務</td></tr><tr><td><div><figure><img src=".gitbook/assets/image (8).png" alt=""><figcaption></figcaption></figure></div></td><td>已登入</td><td>已完成</td><td>已完成的任務狀態，會變換底色，並且蓋上印章。</td></tr></tbody></table>

* 兌獎換獎勵區塊，內容如下。
  * 兌換完成後，前端需把資料傳回後端紀錄。

<table><thead><tr><th width="167">兌換獎勵按鈕(實際以設計為準)</th><th width="99">登入狀態</th><th width="117">兌換狀態</th><th>備註</th></tr></thead><tbody><tr><td><div><figure><img src=".gitbook/assets/image.png" alt=""><figcaption></figcaption></figure></div></td><td>未登入</td><td>-</td><td>需登入才能查看兌換狀態</td></tr><tr><td><div><figure><img src=".gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure></div></td><td>已登入</td><td>尚未兌換</td><td>點擊兌換按鈕，會跳彈窗提醒是否真的要兌換，如還沒集滿任務，按鈕則disable。</td></tr><tr><td><div><figure><img src=".gitbook/assets/image (2).png" alt=""><figcaption></figcaption></figure></div></td><td>已登入</td><td>已兌換</td><td>兌換後，會押上兌換日期和時間。</td></tr></tbody></table>

## 實作方向-OP上傳內容

屆時集點卡的任務資料，會透過OP讓RD進行上傳，OP票內容如下

1. redmine票附上banner的圖片
2. redmine票附上集點卡的名稱(需為唯一值，不得和其他活動重複)。
3. 提供excel內容如下。
   1. courseID
   2. missionID

備註：如果不同couseID搭配一樣的missionID不會阻擋，玩家一樣可進行集點。

<figure><img src=".gitbook/assets/截圖 2025-08-07 下午3.51.44 (1).png" alt=""><figcaption></figcaption></figure>

