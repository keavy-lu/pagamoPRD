# 三、解決方案

## 1. 功能（Features）

1.  學習行為紀錄&#x20;

    <table data-header-hidden><thead><tr><th width="68"></th><th width="79"></th><th width="117"></th><th width="262"></th><th width="79"></th><th width="75"></th><th></th></tr></thead><tbody><tr><td>序號 </td><td>屬性名稱 </td><td>行為 </td><td>說明 </td><td>次數上限 </td><td>點數每次 </td><td>每天點數 </td></tr><tr><td>1 </td><td>耐力 </td><td>領取每日獎勵 </td><td>點擊每日獎勵機制，領取獎勵 </td><td>一天 1 次 </td><td>1 </td><td>1 </td></tr><tr><td>2 </td><td>智力 </td><td>作答訓練土地 10 次 </td><td>點擊自己領土訓練，答對題目10 題算完成一次 </td><td>一天 3 次 </td><td>2 </td><td>6 </td></tr><tr><td>3 </td><td>敏捷 </td><td>使用 1 個能量道具 </td><td>答題一次消耗6~15能量，使用能量藥水補充能量可答更多題目，使用 1 個能量類道具算完成 1 次 </td><td>一天 1 次 </td><td>1 </td><td>1 </td></tr><tr><td>4 </td><td>魅力 </td><td> 送 1 個好友能量 </td><td>在好友介面送能量值給遊戲內好友 </td><td>一天 3 次 </td><td>1 </td><td>3 </td></tr></tbody></table>

    1. 上述行為要處理為帳戶執行後，要記錄log，當超過當日限制次數就不再計
    2. 每天凌晨 00:00 重置，次數歸零
2. Api 介接&#x20;
   1. 將帳號完成的行為、獲取的屬性點數於執行當下傳送給新北，讓新北加上積點
   2. 介接[密鑰連結](https://boniotw-my.sharepoint.com/:w:/g/personal/bonio_share_bonio_com_tw/EQok3YoF4phHm9OZb7y73H0Brc1k0JsLBjZQyK4vjcjDqA?e=dEUHG6)&#x20;
   3. 相關[技術文件](https://boniotw-my.sharepoint.com/:f:/g/personal/bonio_share_bonio_com_tw/EkOkWMkV30lOnOnGzqZ2wSsB4wTKgIqHb-KvCVg-fihpNQ?e=yM7JiF)
3. 傳送失敗需進行補送機制&#x20;
   1. 當傳送失敗，要持續補送（沒有200就重傳）&#x20;
4. Log 查詢後台（metabase）&#x20;
   1. 搜尋UID或帳號，以及時間區間，可列出該時間段在哪個課程、執行哪些上述行為、執行的時間、
5. 統計數據&#x20;
   1. 平均使用率 ：機制開放前後新北用戶日/週/月平均上線次數，比較是否提升&#x20;
   2. 活躍度：機制開放前後新北用戶日周月活躍度，比較是否提升&#x20;
   3. 平均答題次數：選擇新北帳號，機制開放前後的日/週/月平均答題次數，比較是否提升&#x20;

## 2. 用戶流程(User Flow)&#x20;

1. 身為新北學生，我從親師生平台注意到 PaGamO 加入機積點趣玩法&#x20;
2. 感覺積點趣列出的四項行為活動，部分行為看似不難，很多是原本就會從事的遊戲行為&#x20;
3. 進入 PaGamO 準備執行積點行動&#x20;
4. 進入遊戲領取每日獎勵、送好友能量&#x20;
5. 執行幾題作答&#x20;
6. 使用能量道具補充（以上是沒時間又不想錯過積點趣的玩法）&#x20;
7. 若比較有時間，或有作答目標意願，會進行至少一輪(10次）土地訓練&#x20;
8. 之後上線都會順便進行這幾個積點行為&#x20;

## 3. 重要邏輯（Key Logics）&#x20;

1. 用戶行為完成後如何獲取新北點數&#x20;
   1. 四項行為任一執行完成後，先檢查是否為新北帳號、是否在次數上限內，&#x20;
      1. 若否，無作用&#x20;
      2. 若是，在十分鐘內要更新給新北&#x20;
   2. 執行行為不限新北專屬世界，而是該帳戶當日在任意世界（含電競課程）有執行完成就算數&#x20;
   3. 執行行為時需同步紀錄log，以供後續查詢&#x20;
2. 傳送失敗時的補傳送機制&#x20;
   1. 沒有200就重傳&#x20;
   2. 重傳一直未成功的處理（不處理靠查詢補給？重置時補給？這裡看看RD建議）&#x20;

## 4. 要交付時程與上線計畫（Key Logics）

<table data-header-hidden><thead><tr><th width="177"></th><th width="134"></th><th width="143"></th><th width="202"></th><th></th></tr></thead><tbody><tr><td>階段 </td><td>開始時間 </td><td>Deadline </td><td>原因 </td><td>實際上線日期 </td></tr><tr><td>需求收斂 </td><td>2024/7/1 </td><td>2024/7/19 </td><td> </td><td> </td></tr><tr><td>初版解決方案 </td><td> </td><td>2024/8/14 </td><td> </td><td> </td></tr><tr><td>完整解決方案 </td><td> </td><td> </td><td> </td><td> </td></tr><tr><td>設計 </td><td>Ｘ </td><td> </td><td> </td><td> </td></tr><tr><td>後端 </td><td> </td><td> </td><td> </td><td> </td></tr><tr><td>前端 </td><td> Ｘ</td><td> </td><td> </td><td> </td></tr><tr><td>APP </td><td> Ｘ</td><td> </td><td> </td><td> </td></tr><tr><td>目標時程 </td><td> </td><td>2024/10/15 </td><td> </td><td> </td></tr></tbody></table>

## 5. Checklists
