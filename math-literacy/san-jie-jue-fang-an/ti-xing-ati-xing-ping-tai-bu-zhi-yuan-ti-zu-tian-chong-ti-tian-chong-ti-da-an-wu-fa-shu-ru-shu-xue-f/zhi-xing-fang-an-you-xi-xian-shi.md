# 執行方案-遊戲顯示

{% hint style="info" %}
<mark style="color:red;">**支援系統：**</mark>

**APP、WEB、MOBILE。**
{% endhint %}

## 參考連結

FIGMA連結：[點我](https://www.figma.com/design/iJbnctZW6p1Qd9HLVJ41j1/%E5%A2%9E%E5%8A%A0%E6%95%B8%E5%AD%B8%E7%B4%A0%E9%A4%8A%E5%B0%8D%E9%A1%8C%E5%9E%8B%E5%87%BA%E9%A1%8C%E7%9A%84%E6%94%AF%E6%8F%B4?node-id=0-1\&p=f\&t=DRU3Y1FlNvJkCZHY-0)

## 需求目標

<mark style="color:red;">**遊戲內的答題介面調整**</mark>

1. 新增 『 填充題 』 且開啟**數學鍵盤**的題型答題介面。
2. 題組子題，新增 『 填充題 』 且開啟**數學鍵盤**的答題介面。
3. 題組子題，新增 『 填充題 』 的答題介面。
4. 上述相關答題介面，只支援新版遊戲答題介面。
5. 需支援測驗模式和一般模式

<mark style="color:red;">**遊戲內的詳解調整**</mark>

1. 題組子題，答題後詳解新增填充題的答案欄位
2. 需支援測驗模式和一般模式

## 實作方向-答題介面

1. 遊戲答題介面需能解析數學公式，之前[討論串](https://bonio.slack.com/archives/C040564MBPX/p1741167265458799)。
2. 新增題型 『 填充題 』 且開啟數學鍵盤的答題介面，點擊答題框會出現虛擬鍵盤。
   * 玩家只能使用虛擬鍵盤答題，會強制disable實體或原生鍵盤。
   * 使用虛擬鍵盤作答，不會限制字數。

<figure><img src="../../.gitbook/assets/image (30).png" alt=""><figcaption><p>題型-填充題且開啟數學鍵盤 示意圖</p></figcaption></figure>

3. 題組子題，新增 『 填充題』 且開啟數學鍵盤 的答題介面，點擊答題框會出現虛擬鍵盤。
   * 玩家只能使用虛擬鍵盤答題，會強制disable實體或原生鍵盤。
   * 使用虛擬鍵盤作答，不會限制字數。

<figure><img src="../../.gitbook/assets/image (36).png" alt=""><figcaption><p>題組子題-填充題且開啟數學鍵盤 示意圖</p></figcaption></figure>

4. 題組子題，需新增 『填充題』  的答題介面。

<figure><img src="../../.gitbook/assets/image (37).png" alt=""><figcaption><p>題組子題-填充題 示意圖</p></figcaption></figure>

## 實作方向-詳解介面

1. 題組子題，需新增 『填充題』 的詳解介面。

<figure><img src="../../.gitbook/assets/image (45).png" alt=""><figcaption><p>題組子題填充題詳解介面 示意圖</p></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (46).png" alt=""><figcaption><p>題組子題填充題，全對才顯示答案 示意圖</p></figcaption></figure>

2. 遊戲詳解介面需能解析數學公式，之前[討論串](https://bonio.slack.com/archives/C040564MBPX/p1741167265458799)。
