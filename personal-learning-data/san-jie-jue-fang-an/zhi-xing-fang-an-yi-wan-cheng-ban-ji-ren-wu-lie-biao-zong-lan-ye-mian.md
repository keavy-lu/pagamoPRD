# 執行方案-已完成班級任務列表(總覽頁面)

## 相關連結

FIGMA：[連結](https://www.figma.com/design/5Ehb22klJf7mV08SJ9asYe/-%E5%80%8B%E4%BA%BA%E5%AD%B8%E7%BF%92%E6%95%B8%E6%93%9A-%E7%8F%AD%E7%B4%9A%E4%BB%BB%E5%8B%99?node-id=2003-37846\&p=f\&t=M7UAY4CJKKcMVmIH-0)

## 需求目標&#x20;

1. 個人學習數據 『 已完成任務列表 』 文案改為 『 已完成素養任務列表 』 。
2. 個人學習數據新增 『 已完成班級任務列表 』 的分頁。
3. 已完成班級任務列表，內容如下
   1. 可查看一般任務列表總覽。(沿用目前學習數據 『 [已完成任務列表 ](https://www.pagamo.org/learning_data/student/4174052/finished_missions)』 設計方式)
   2. 可查看測驗任務列表總覽。(沿用目前學習數據 『 [已完成任務列表](https://www.pagamo.org/learning_data/student/4174052/finished_missions) 』 設計方式)
   3. 上述皆可透過 『日期區間』 和 『課程世界』 進行篩選。

## 執行方案

1. 用戶登入後 -> 頭像內選學習數據 ，增加和調整分頁名稱，改動內容如下
   1. 新增 『 已完成班級任務列表 』 的分頁。
   2. 修改文案原本的 『 已完成任務列表 』 調整為 『 已完成素養任務級列表 』。

<figure><img src="../.gitbook/assets/image (6).png" alt=""><figcaption><p>示意圖</p></figcaption></figure>



2.  『 已完成班級任務 』 總覽相關規則如下。

    1. 排序相關規則
       1. 會針對一般模式、測驗模式、魔王模式、競賽之盾進行分類。
       2. 會預設近一年的資訊。
       3. 每頁最多10筆，超過就會分頁。
       4. 預設由任務完成時間近到遠進行排序。
       5. 可選擇**正確率**或**任務完成時間**進行排序。
    2. 一般模式，總覽上會顯示的資訊
       1. 任務完成時間。(yyyy/mm/dd hh:mm)
       2. 任務名稱。
       3. 任務來自的**課程世界**和**班級**。
       4. 任務正確率。(首次答對題數/答題數)。
    3. 測驗模式，總覽上會顯示的資訊(測驗模式只要答題完成就會顯示，不用點擊完成任務)
       1. 答題完成時間。(yyyy/mm/dd hh:mm)
       2. 任務名稱。
       3. 任務來自的**課程世界**和**班級**。
       4. 任務正確率。(首次答對題數/答題數)。

    <figure><img src="../.gitbook/assets/image (5).png" alt=""><figcaption><p>示意圖</p></figcaption></figure>
3. 可以透過 『任務完成日的日期區間』 進行篩選，規則如下
   1. 任務完成的日期區間，最長可選區間為一年。
   2. 預設為近期一年。

<figure><img src="../.gitbook/assets/image (18).png" alt=""><figcaption><p>示意圖</p></figcaption></figure>
