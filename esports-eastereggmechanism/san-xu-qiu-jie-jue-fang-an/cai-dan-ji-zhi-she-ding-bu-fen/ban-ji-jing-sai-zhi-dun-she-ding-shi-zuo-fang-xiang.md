# 班級競賽之盾設定-實作方向

{% hint style="info" %}
&#x20;設定頁面位置：遊戲世界>競賽之盾->官方競賽之盾->教師設定

備註：非全部新功能，是由舊的功能延伸更多欄位來做設定。
{% endhint %}

## 參考連結：

FIGMA連結：[點我](https://www.figma.com/design/4WC1ZRNPDfJtorzHdSbj6U/%2339820-%E9%9B%BB%E7%AB%B6%E6%96%B0%E7%8E%A9%E6%B3%95-%E5%BD%A9%E8%9B%8B%E6%A9%9F%E5%88%B6?node-id=0-1\&node-type=canvas\&t=FZI1VRQztxTDuwQQ-0)

## 需求目標：

當[課程世界有啟動彩蛋題機制](guan-li-zhe-jie-mian-jin-jie-she-ding-shi-zuo-fang-xiang.md)時，可以在班級競賽之盾加入彩蛋題玩法。

## 實作方向：

1. 當[課程世界有啟動彩蛋題機制](guan-li-zhe-jie-mian-jin-jie-she-ding-shi-zuo-fang-xiang.md)時，遊戲內設定班級競賽之盾，會出現 『彩蛋玩法』 設定按鈕，點擊後會新增3 個設定選項。

| 彩蛋玩法按鈕                                                                       | 說明           | 點擊後動作      |
| ---------------------------------------------------------------------------- | ------------ | ---------- |
| <img src="../../.gitbook/assets/image (42).png" alt="" data-size="original"> | 灰燈：代表彩蛋玩法未開啟 | 開啟彩蛋玩法設定畫面 |
| <img src="../../.gitbook/assets/image (43).png" alt="" data-size="original"> | 綠燈：代表彩蛋玩法已開啟 | 開啟彩蛋玩法設定畫面 |

<table><thead><tr><th width="131">新增的設定</th><th width="128.31072998046875"> 元件類型</th><th>元件畫面</th><th>選項</th><th>是否必填</th><th>欄位說明</th></tr></thead><tbody><tr><td>彩蛋玩法</td><td>Switch按鈕</td><td><img src="../../.gitbook/assets/image (3).png" alt="" data-size="original"></td><td><ol><li>開</li><li>關</li></ol></td><td>必填</td><td>開啟後，賽事會加入彩蛋機制玩法。</td></tr><tr><td>設定彩蛋題目</td><td>下拉選單</td><td><img src="../../.gitbook/assets/image (5).png" alt="" data-size="original"></td><td><p>來源帳號有設定為競賽之盾</p><p>的所有作業</p></td><td>如果有開放彩蛋玩法則必填，如沒開放就反灰</td><td>出題規則：<br>未答題過先隨機出題->答錯的題目隨機出題->都答過後全部隨機重複出題</td></tr><tr><td>每天能量藥水上限</td><td>文字輸入框</td><td><img src="../../.gitbook/assets/image (6).png" alt="" data-size="original"></td><td>-</td><td>如果有開放彩蛋玩法則必填，如沒開放就反灰</td><td>請填入每天因彩蛋題而獲得的能量藥水上限</td></tr></tbody></table>

<figure><img src="../../.gitbook/assets/image (39).png" alt=""><figcaption><p>課堂班級競賽之盾彩蛋玩法設定按鈕</p></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (41).png" alt=""><figcaption><p>課堂班級競賽之盾彩蛋玩法設定畫面</p></figcaption></figure>

2. 設定完成後將號碼給參賽的玩家，就能從遊戲進入比賽。

<figure><img src="../../.gitbook/assets/截圖 2024-09-11 上午11.22.44.png" alt=""><figcaption><p>輸入號碼進入比賽</p></figcaption></figure>



