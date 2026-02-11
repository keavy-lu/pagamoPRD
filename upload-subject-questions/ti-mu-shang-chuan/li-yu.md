# 力宇

學科題目所在位置：課程題庫（課程世界：官方上題修正用）

### API 匯入的處理流程：

1. 整理並且檢查 Excel 表格中螢光黃色欄的資料，是否是這個學期要匯入的範圍\
   Excel: [https://boniotw-my.sharepoint.com/:x:/g/personal/bonio\_share\_bonio\_com\_tw/Eaz13LD5AEZJsy41Wey6XsUBNf\_Pt\_C\_p\_jec\_x7J\_Rvog?e=wE3TXy\&nav=MTVfezdDMkUzOTg1LTQyMDItQTM0QS05QzM4LTk5MUMyQjFGMjg4Nn0](https://boniotw-my.sharepoint.com/:x:/g/personal/bonio_share_bonio_com_tw/Eaz13LD5AEZJsy41Wey6XsUBNf_Pt_C_p_jec_x7J_Rvog?e=wE3TXy\&nav=MTVfezdDMkUzOTg1LTQyMDItQTM0QS05QzM4LTk5MUMyQjFGMjg4Nn0)
2. 在這次要匯入的範圍的「票號」欄位填入票號
   1. 若力宇一次可以串接的範圍是齊全的，則票號都相同
   2. 若分批提供可串接的範圍，則在該次串接範圍的學年科目後方填入票號
3. RD 根據票號標示的範圍撈回題目，填入題數資料
   1. 題數不 OK ，運營向力宇詢問狀況
   2. 題數確認 OK 後，RD 匯入 Develop 機
4. PM 在 Develop 抽查不同學年科目的匯入狀況
   1. 冊次名稱、章節名稱、題目內容是否正常
5. 匯入正式機



### Word 匯入的處理流程

1. 請 RD 從力宇課版表撈回章節資料，運營將力宇章節名稱貼上 Excel，對應到現存的章節結構：\
   判斷章節的欄位：unit\_text, topic\_text

* 課版表撈回資料：[https://boniotw-my.sharepoint.com/:x:/g/personal/bonio\_share\_bonio\_com\_tw/Ec3L3Y9CrcdIuKgtH6QCTK0Bn25jK-CSmZ6aduGzEgMgaA?e=fx2HtZ](https://boniotw-my.sharepoint.com/:x:/g/personal/bonio_share_bonio_com_tw/Ec3L3Y9CrcdIuKgtH6QCTK0Bn25jK-CSmZ6aduGzEgMgaA?e=fx2HtZ)\
  注意：課版表在第一次撈回資料之後，可能更新變動，可以跟力宇確認已更新的範圍或變動完畢的時間
* 舊有的題庫架構可以從 [Metabase 出題商題目難易統計](https://metabase-da.pagamo.org/question/3172) 下載
* 製作章節結構對照：[https://boniotw-my.sharepoint.com/:x:/g/personal/bonio\_share\_bonio\_com\_tw/EUqfcJiqoJpLrs57m16dofMB\_3ZAxtV5ov20wxRdOYqtzA?e=177QJ7](https://boniotw-my.sharepoint.com/:x:/g/personal/bonio_share_bonio_com_tw/EUqfcJiqoJpLrs57m16dofMB_3ZAxtV5ov20wxRdOYqtzA?e=177QJ7)

<details>

<summary>原因：題庫已有舊題和統一的章節名稱格式，為避免上傳力宇的題目時建立新的力宇版本的章節名稱，此動作確保力宇的章節都可以對應並上傳到現存章節、若原本無該章節，則上傳時新增章節</summary>



</details>



2. 整理並且檢查 Excel 表格中螢光黃色欄的資料，是否是這個學期要匯入的範圍\
   Excel: [https://boniotw-my.sharepoint.com/:x:/g/personal/bonio\_share\_bonio\_com\_tw/Eaz13LD5AEZJsy41Wey6XsUBNf\_Pt\_C\_p\_jec\_x7J\_Rvog?e=wE3TXy\&nav=MTVfezdDMkUzOTg1LTQyMDItQTM0QS05QzM4LTk5MUMyQjFGMjg4Nn0](https://boniotw-my.sharepoint.com/:x:/g/personal/bonio_share_bonio_com_tw/Eaz13LD5AEZJsy41Wey6XsUBNf_Pt_C_p_jec_x7J_Rvog?e=wE3TXy\&nav=MTVfezdDMkUzOTg1LTQyMDItQTM0QS05QzM4LTk5MUMyQjFGMjg4Nn0)
3. 下載的 Word 檔案將 docx 轉檔成 doc（原因：）
4. 在這次要匯入的範圍的「票號」欄位填入票號
5. RD 根據票號標示的範圍，填入題數資料
   1. 題數不 OK ，運營向力宇詢問狀況
   2. 題數確認 OK 後（題數有少的話可以後續再另開票補），RD 匯出力宇章節名稱
6. RD 匯入 Develop 及「匯入結果明細」，標示出哪些題目匯入失敗，需要人工修正 （僅供檢查，不需要修正）[https://boniotw-my.sharepoint.com/:x:/g/personal/bonio\_share\_bonio\_com\_tw/EdiuRgQOPntHgOn7vzUIQGQBQdV\_Ewi-nyQyuDqv1QOpUQ?e=j8quvp](https://boniotw-my.sharepoint.com/:x:/g/personal/bonio_share_bonio_com_tw/EdiuRgQOPntHgOn7vzUIQGQBQdV_Ewi-nyQyuDqv1QOpUQ?e=j8quvp)
7. PM 在 Develop 抽查不同學年科目的匯入狀況：冊次名稱、章節名稱、題目內容是否正常，確認 OK 後通知 RD 匯入正式機，
   1. 轉檔成功的題目直接設定為上架；失敗的設定為下架(rejected)
   2. 時間設定為“四小時”
   3. 選項“隨機”
8. 匯入正式機及「匯入結果明細」，標示出哪些題目匯入失敗，需要人工修正，運營根據明細上的「PaGamO 題目 ID」從題庫搜尋到要修正的題目，從明細上的「力宇題目編號」可以找到力宇提供的「Word 檔案題目編號」，從 Word 原始檔判斷修改方式，修改後設定為上架

匯入流程可參考票：[https://redmine.bonio.com.tw/issues/38759](https://redmine.bonio.com.tw/issues/38759)

註：等所有題目上傳完畢後，一起處理 word 轉檔費用報帳事宜（由PM處理）

