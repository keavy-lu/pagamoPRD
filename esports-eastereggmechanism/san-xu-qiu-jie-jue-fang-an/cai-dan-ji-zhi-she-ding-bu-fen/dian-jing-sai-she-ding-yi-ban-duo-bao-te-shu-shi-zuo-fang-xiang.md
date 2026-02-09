# 電競賽設定(一般、奪寶、特殊)-實作方向

{% hint style="info" %}
設定頁面位置：競賽管理介面->世界設定

備註：非全部新功能，是由舊的功能延伸更多欄位來做設定。
{% endhint %}

## 參考連結：

FIGMA連結：[點我](https://www.figma.com/design/4WC1ZRNPDfJtorzHdSbj6U/%2339820-%E9%9B%BB%E7%AB%B6%E6%96%B0%E7%8E%A9%E6%B3%95-%E5%BD%A9%E8%9B%8B%E6%A9%9F%E5%88%B6?node-id=0-1\&node-type=canvas\&t=FZI1VRQztxTDuwQQ-0)

## 需求目標：

一般、特殊、奪寶賽事地圖的電競賽加入彩蛋題玩法。

## 實作方向：

1. 競賽管理介面->世界設定，新增**彩蛋題機制設定的收合欄位**，展開後的內容如下

<table><thead><tr><th width="146">展開後的設定</th><th>元件類型</th><th>選項</th><th>是否必填</th><th>欄位說明</th><th>備註</th></tr></thead><tbody><tr><td>彩蛋玩法</td><td>switch</td><td>關閉或開啟(預設關閉)</td><td>-</td><td>開啟後，賽事會加入彩蛋機制玩法</td><td>-</td></tr><tr><td>每天可獲得能量藥水的上限</td><td>文字輸入框</td><td>-</td><td>如果有開放彩蛋玩法則必填，如沒開放就反灰</td><td>請填入每天因彩蛋題而獲得的能量藥水上限</td><td>當賽場有玩家加入後就不能進行修改</td></tr></tbody></table>

<figure><img src="../../.gitbook/assets/image (17).png" alt=""><figcaption><p><strong>彩蛋題機制設定的收合欄位</strong></p></figcaption></figure>

2. 競賽管理介面->世界設定裡的題目設定，**新增彩蛋機制的題目設定選項**。

<table><thead><tr><th width="148">新增的設定</th><th width="103">元件類型</th><th width="169">選項</th><th>是否必填</th><th>欄位說明</th></tr></thead><tbody><tr><td>設定彩蛋題目</td><td>下拉選單</td><td>來源帳號裡的所有作業</td><td>如果有開放彩蛋玩法則必填，如沒開放就反灰</td><td>出題規則：<br>未答題過先隨機出題->答錯的題目隨機出題->都答過後全部隨機重複出題</td></tr></tbody></table>

<figure><img src="../../.gitbook/assets/image (19).png" alt=""><figcaption><p><strong>新增彩蛋機制的題目設定選項</strong></p></figcaption></figure>

3. 設定完成後，就能成功建立有彩蛋機制的電競賽，後續就比照原本流程進行。
