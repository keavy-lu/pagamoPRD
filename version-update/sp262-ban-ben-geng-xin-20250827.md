# SP262 版本更新(2025/08/27)

### 【重點功能】

1. 電競優化
   1. 報名流程加上賽場名稱和暱稱欄位 [#43244](https://redmine.bonio.com.tw/issues/43244)
   2. 競賽之盾即時排名與按鈕調整 [#43344](https://redmine.bonio.com.tw/issues/43344)
2. 計算紙功能優化 [#43627](https://redmine.bonio.com.tw/issues/43627)
   1. 調整畫筆和文字縮放、移動不能超出整張畫布邊界
   2. 將計算紙的memubar從覆蓋畫布改為相鄰，避免擋住畫布
   3. 優化計算紙打字功能，從固定座標改成隨畫布來移動
3. AI 申論題批改優化
   1. 教師批閱 - 學生訊息通知（班級任務）[#43506](https://redmine.bonio.com.tw/issues/43506)
   2. 使用者離開網頁或關閉作答時，如帳號/裝置/任務不變且未逾時，再次進入作答畫面可復原未送出的作答內容 [#43042](https://redmine.bonio.com.tw/issues/43042)
   3. 不同 AI 批改模型能設定不同的最低字數標準，並調整教師後台批改方式的顯示文字 [#43160](https://redmine.bonio.com.tw/issues/43160)
   4. 使用者題目開始AI批改後，如前往其他題再返回時，如有批改結果都應優先跳出 [#43171](https://redmine.bonio.com.tw/issues/43171)
   5. 答題介面答題時，新增「題目顯示學生上一次作答內容」的情境 [#43689](https://redmine.bonio.com.tw/issues/43689)
   6. 清除素養任務答題紀錄時，同時處理申論題答題與教師批閱紀錄 [#42888](https://redmine.bonio.com.tw/issues/42888)
   7. 申論題批閱頁面，最新回答與AI批閱建議欄位，如過長才會出現+號 [#43371](https://redmine.bonio.com.tw/issues/43371)
   8. 調整教師批閱頁面相關「批閱提示」的彈窗內容（前端）[#43368](https://redmine.bonio.com.tw/issues/43368)
   9. 移除舊版批閱功能，僅保留查看與下載功能 [#43166](https://redmine.bonio.com.tw/issues/43166)



### 【依平台介面】

1. PaGamO 首頁：
   1. 登入流程整合 reCAPTHCA 機制 [#43522](https://redmine.bonio.com.tw/issues/43522)
   2. 幫助中心改為新版連結、「企業 CSR」連結更新（首頁 [#43624](https://redmine.bonio.com.tw/issues/43624), 教師後台 [#43624](https://redmine.bonio.com.tw/issues/43624)）
2. 教師後台：
   1. 教育雲和澔學班級拿掉班級代碼、新增、匯入學生功能 [https://redmine.bonio.com.tw/issues/42645](https://redmine.bonio.com.tw/issues/42645)
   2. 教師後台「使用教學」連結更新為新版幫助中心連結 [#43624](https://redmine.bonio.com.tw/issues/43624)
3. 學習中心優化 [#41904](https://redmine.bonio.com.tw/issues/41904)
   1. 答題介面答題時，新增「題目顯示學生上一次作答內容」的情境
   2. 題組申論子題支援 AI 批改 [#42575](https://redmine.bonio.com.tw/issues/42575)
4. 管理後台：
   1. 優化「新增引用題庫」的搜尋提示 [#43364](https://redmine.bonio.com.tw/issues/43364)
   2. 課程世界自動綁定指定素養任務 [#43073](https://redmine.bonio.com.tw/issues/43073)
5. 地形：
   1. 調整金字塔地形 [#43616](https://redmine.bonio.com.tw/issues/43616)
   2. 星球地形：逆行衛星，道具：涅普頓的三叉戟 [#43424](https://redmine.bonio.com.tw/issues/43424)
   3. 魔法學院地形：神秘魔法門，道具：魔門之眼 [#43431](https://redmine.bonio.com.tw/issues/43431)
   4. 台南文資地形：大南門，道具：小西門 [#43646](https://redmine.bonio.com.tw/issues/43646)
   5. 道具卡地形：土地訓練卡，道具：升級御守 [#43654](https://redmine.bonio.com.tw/issues/43654)
   6. 道具卡地形：超級訓練卡，道具：滿等御守 [#43660](https://redmine.bonio.com.tw/issues/43660)
   7. 慈濟地形： 氣候時鐘，道具名稱：溫控之石 [#43673](https://redmine.bonio.com.tw/issues/43673)
   8. 慈濟地形：地球儀，道具：冰融之時 [#43675](https://redmine.bonio.com.tw/issues/43675)
   9. 台灣小吃地形：「中」於有太陽餅，道具：太陽餅 [#43680](https://redmine.bonio.com.tw/issues/43680)
   10. 台灣小吃地形：「南」忘牛肉湯，道具：牛肉湯 [#43683](https://redmine.bonio.com.tw/issues/43683)
   11. 調整地形道具文字（需統一取代）[#43363](https://redmine.bonio.com.tw/issues/43363)
