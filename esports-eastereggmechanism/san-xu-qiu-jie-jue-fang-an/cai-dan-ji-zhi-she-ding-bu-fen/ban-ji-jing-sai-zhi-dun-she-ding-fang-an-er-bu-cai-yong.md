---
hidden: true
---

# 班級競賽之盾設定(方案二)-不採用

{% hint style="info" %}
**此方案已確定不採用，僅提供參考。**
{% endhint %}

{% hint style="warning" %}
設定頁面位置：教師後台->彩蛋題班級競賽之盾

備註ㄧ：彩蛋題班級競賽之盾，是本次開發新增的功能。

備註二：主要把賽事設定從遊戲內改到教師後台，設定完主辦方一樣到遊戲介面開始競賽。
{% endhint %}

## 參考連結：

FIGMA連結：後補

## 需求目標：

當[課程世界有啟動彩蛋題機制](guan-li-zhe-jie-mian-jin-jie-she-ding-shi-zuo-fang-xiang.md)時，可以從教師後台開設有彩蛋題的班級競賽之盾。

## 實作方向：&#x20;

1. 教師後台新增**彩蛋班級競賽之盾設定，**&#x4E3B;要用來**新增**和**查看**建立的賽事。
   * 查看建立的賽事，主要有尚未結束賽事和已結束賽事2個分類，欄位列表如下

<table data-full-width="false"><thead><tr><th width="178">賽事地圖號碼</th><th width="243">賽事名稱</th><th>賽事開始時間</th></tr></thead><tbody><tr><td>1955031</td><td>慈濟彩蛋題初賽</td><td>2025/5/20 10:00</td></tr></tbody></table>

<figure><img src="../../.gitbook/assets/image (15).png" alt=""><figcaption><p>尚未結束賽事</p></figcaption></figure>

<table data-full-width="false"><thead><tr><th width="178">賽事地圖號碼</th><th width="243">賽事名稱</th><th>賽事開始時間～結束時間</th></tr></thead><tbody><tr><td>1955031</td><td>慈濟彩蛋題初賽</td><td>2025/5/20 10:00～2025/6/20 11:00</td></tr></tbody></table>

<figure><img src="../../.gitbook/assets/image (52).png" alt=""><figcaption><p>已結束賽事</p></figcaption></figure>

2. 教師後台新增**彩蛋班級競賽之盾設定，**&#x53EF;以新增彩蛋班級競賽之盾的比賽，需設定的欄位如下：
   * 建立後代表開放比賽，玩家已經可以透過地圖號碼進場等待。
   * 建立後就無法進行刪除，如要刪除可開有教師權限的帳號進入遊戲結束比賽，或是等6小時後地圖自動消滅。
   * 最多只能新增一場比賽，不能同時存在兩場未結束的比賽。

| 設定欄位         | 元件類型   | 選項                       | 是否必填          | 欄位說明                |
| ------------ | ------ | ------------------------ | ------------- | ------------------- |
| 名稱           | 文字輸入框  | -                        | 必填            | -                   |
| 模式           | 下拉選單   | <p>1.大亂鬥</p><p>2.團體戰</p> | 必填            | -                   |
| 人數           | 文字輸入框  | -                        | 模式選大亂鬥必填，否則反灰 | -                   |
| 隊伍數          | 文字輸入框  | -                        | 模式選團體戰必填，否則反灰 | -                   |
| 各隊人數         | 文字輸入框  | -                        | 模式選團體戰必填，否則反灰 | -                   |
| 每天可獲得的能量藥水上限 | 文字輸入框  | -                        | 必填            | 請填入每天因彩蛋題而獲得的能量藥水上限 |
| 能量值上限        | 文字輸入框  | -                        | 必填            | 答題會消耗能量值，設定該賽場的能量上限 |
| 能量值回復速度      | 文字輸入框  | -                        | 必填            | -                   |
| 帳號           | 搜尋框    | -                        | 必填            | -                   |
| 題目集          | 下拉選單   | 教師後台裡設定為競賽之盾的作業          | 必填            | -                   |
| 彩蛋題目集        | 下拉選單   | 來源帳號裡的所有作業               | 必填            | -                   |
| 積分比例         | slider | 土地數＆答對數積分比例              | 必填            | -                   |
| 名次獎勵         | 下拉選單   | 該世界有開放的道具                | 非必填           | -                   |

<figure><img src="../../.gitbook/assets/image (44).png" alt=""><figcaption><p>彩蛋題班級競賽之盾設定</p></figcaption></figure>

3. 設定[完成後就能在列表上看到競賽地圖號碼](ban-ji-jing-sai-zhi-dun-she-ding-fang-an-er-bu-cai-yong.md#shi-zuo-fang-xiang)，將號碼給參賽的玩家，就能從遊戲進入參加比賽。

<figure><img src="../../.gitbook/assets/截圖 2024-09-11 上午11.22.44.png" alt=""><figcaption><p>輸入號碼進入比賽</p></figcaption></figure>

4. 比賽開始時，主辦方一樣到遊戲介面中啟動競賽，比照本來的班級競賽之盾流程

<figure><img src="../../.gitbook/assets/image (10).png" alt=""><figcaption><p>設定完後主辦方可以到遊戲開始競賽</p></figcaption></figure>
