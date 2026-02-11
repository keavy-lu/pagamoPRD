---
description: 此方案暫時不考慮
hidden: true
---

# 執行方案(二)-課程＆個人題庫

## 參考連結

FIGMA連結

## 需求目標

<mark style="color:red;">**個人題庫**</mark>和<mark style="color:red;">**課程題庫**</mark>，新增出題方式

1. 題型新增 『 填充題(數學鍵盤) 』 的出題方式。
2. 題組的子題，新增 『 填充題 』 的出題方式。
3. 題組的子題，新增 『 填充題(數學鍵盤) 』 的出題方式
4. 數學鍵盤需支援，加減乘除、分數、根號、次方，不等式、幾何。
   * 可能涵蓋的符號有：`> <＋ ± － × ÷ ± ＝ ≠ ≒ ≦ ≧ ⊥ ∠ ° △` 。

## 實作方向-新增填充題(數學鍵盤)的出題方式

1. [當課程世界有開啟『 填充題(數學鍵盤) 』 的權限](zhi-xing-fang-an-quan-xian-kong-guan.md)，出題時會新增 『 填充題(數學鍵盤) 』 的出題方式。

<table><thead><tr><th width="159">題型</th><th width="149">元件類型</th><th>題型說明</th></tr></thead><tbody><tr><td>填充題(數學鍵盤)</td><td>RadioButton</td><td>讓學生自行填入答案，且可使用有數學符號的虛擬鍵盤</td></tr></tbody></table>

<figure><img src="../../.gitbook/assets/image (40).png" alt=""><figcaption><p>題型新增 『 填充題(數學鍵盤) 』 示意圖</p></figcaption></figure>

2. 輸入答案內容時，顯示虛擬的數學鍵盤。

<figure><img src="../../.gitbook/assets/image (41).png" alt=""><figcaption><p>輸入答案時數學鍵盤示意圖</p></figcaption></figure>

3. 確認出題後，玩家屆時答題時就會出現有數學符號的鍵盤。

## 實作方向-題組的子題新增出題方式

1. [當課程世界有開啟題組子題支援『 填充題 』 或 『 填充題(數學鍵盤) 』 的相對應權限時](zhi-xing-fang-an-quan-xian-kong-guan.md)，題組子題出題時就可以進行選擇。

<figure><img src="../../.gitbook/assets/image (42).png" alt=""><figcaption><p>題組子題開啟填充題和填充題(數學鍵盤)示意圖</p></figcaption></figure>

2. 子題選擇 『 填充題(數學鍵盤) 』，輸入答案內容時會顯示數學鍵盤，如選擇 『填充題』，輸入答案內容時則不會有數學鍵盤。

<figure><img src="../../.gitbook/assets/image (43).png" alt=""><figcaption><p>子題選擇 『 填充題(數學鍵盤) 』 示意圖</p></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (44).png" alt=""><figcaption><p>子題選擇 『 填充題 』 示意圖</p></figcaption></figure>

3. 確認出題後，玩家屆時答題時就會出現有數學符號的鍵盤。
