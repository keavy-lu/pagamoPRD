# 執行方案-課程＆個人題庫

## 參考連結

FIGMA連結：[點我](https://www.figma.com/design/iJbnctZW6p1Qd9HLVJ41j1/%E5%A2%9E%E5%8A%A0%E6%95%B8%E5%AD%B8%E7%B4%A0%E9%A4%8A%E5%B0%8D%E9%A1%8C%E5%9E%8B%E5%87%BA%E9%A1%8C%E7%9A%84%E6%94%AF%E6%8F%B4?node-id=89-136\&p=f\&t=DRU3Y1FlNvJkCZHY-0)

## 需求目標

<mark style="color:red;">**個人題庫**</mark>和<mark style="color:red;">**課程題庫**</mark>，新增出題方式

1. 題型 『 填充題 』 新增開啟數學鍵盤功能。
2. 題組的子題，新增 『 填充題 』 的出題方式。
3. 數學鍵盤需支援，加減乘除、分數、根號、次方，不等式、幾何。
   * 可能涵蓋的符號有：`> <＋ ± － × ÷ ± ＝ ≠ ≒ ≦ ≧ ⊥ ∠ ° △` 。
4. 題目總覽預覽，新增填充題預覽時有數學鍵盤的畫面。
5. 題目總覽預覽，新增題組中有子題有填充題的畫面。
6. 題目總覽，如題目有開啟虛擬鍵盤，會顯示特殊icon提醒。

## 實作方向-填充題新增開啟數學鍵盤

1. [當課程世界有開啟『 填充題答題時支援開啟數學鍵盤 』 的權限](zhi-xing-fang-an-quan-xian-kong-guan.md)，出填充題時可以選擇玩家答題是否開啟數學鍵盤，反之如果權限沒開啟則會Disable，數學鍵盤相關規則如下
   1. 如數學鍵盤切換為開啟，會強制答案欄位需使用數學鍵盤。
   2. 只要有切換數學鍵盤的按鈕，皆會強制清空 『 答案內容 』 欄位的值。
   3. 開啟數學鍵盤，會隱藏 『是否區分大小寫』 的選項，反之則會顯示。

<figure><img src="../../.gitbook/assets/image (13).png" alt=""><figcaption><p>玩家答題是否開啟數學鍵盤示意圖</p></figcaption></figure>

2. 當出題者開啟數學鍵盤，輸入答案內容時，會強制使用mathfield的虛擬鍵盤套件。
   * 如有開啟虛擬鍵盤作答，輸入答案時會強制disable實體鍵盤和原生鍵盤。

<figure><img src="../../.gitbook/assets/image (12).png" alt=""><figcaption><p>新增答案內容會強制使用虛擬鍵盤</p></figcaption></figure>

3. 如有開啟數學鍵盤確認出題後，玩家屆時答題時就會出現有數學符號的鍵盤。

## 實作方向-題組的子題新增出題方式

1. [當課程世界有開啟題組子題支援 『 填充題 』 的相對應權限時](zhi-xing-fang-an-quan-xian-kong-guan.md)，題組子題出題時就可以進行選擇。

<figure><img src="../../.gitbook/assets/image (55).png" alt=""><figcaption><p>題組子題開啟填充題示意圖</p></figcaption></figure>

2. 子題選擇 『 填充題 』，[如課程世界有開啟『 填充題答題時支援開啟數學鍵盤 』](zhi-xing-fang-an-quan-xian-kong-guan.md) 的權限，也能選擇玩家答題是否開啟數學鍵盤，反之如果權限沒開啟則會Disable，數學鍵盤相關規則如下。
   1. 如數學鍵盤切換為開啟，會強制答案欄位需使用數學鍵盤。
   2. 只要有切換數學鍵盤的按鈕，皆會強制清空 『 答案內容 』 欄位的值。
   3. 開啟數學鍵盤，會隱藏 『是否區分大小寫』 的選項，反之則會顯示。

<figure><img src="../../.gitbook/assets/image (14).png" alt=""><figcaption><p>玩家答題是否開啟數學鍵盤示意圖</p></figcaption></figure>

3. 當出題者開啟數學鍵盤，輸入答案內容時，會強制使用mathfield的虛擬鍵盤套件。

<figure><img src="../../.gitbook/assets/image (15).png" alt=""><figcaption><p>新增答案內容會強制使用虛擬鍵盤</p></figcaption></figure>

4. &#x20;如有開啟數學鍵盤確認出題後，玩家屆時答題時就會出現有數學符號的鍵盤。

## 實作方向-題目總覽介面調整

1. 如題目有開啟虛擬鍵盤，則會出先特殊icon提醒管理者，icon顯示規則如下
   1. 填充題如有開啟數學鍵盤。
   2. 題組裡的子題，任一題有開啟數學鍵盤。

<figure><img src="../../.gitbook/assets/image (58).png" alt=""><figcaption><p>題目總覽icon示意圖</p></figcaption></figure>

2. 題目總覽預覽，新增填充題預覽有數學鍵盤開啟畫面。

<figure><img src="../../.gitbook/assets/image (26).png" alt=""><figcaption><p>填充題預覽有數學鍵盤開啟 示意圖</p></figcaption></figure>

3. 題目總覽預覽和編輯，新增題組中有子題有填充題的畫面。

<figure><img src="../../.gitbook/assets/image (48).png" alt=""><figcaption><p>題組中有子題有填充題的畫面 示意圖</p></figcaption></figure>
