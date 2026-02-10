# 三. 解決方案

## 參考連結

FIGMA：[點我](https://www.figma.com/design/vkizwKYcDY9ODsBZGxJHhr/%E8%87%AA%E5%8B%95%E9%A0%90%E8%A8%AD%E5%A7%93%E5%90%8D%E6%9A%B1%E7%A8%B1%E5%8A%9F%E8%83%BD?node-id=26-90\&t=BE6hBnkLoxv5y0ho-0)

## 功能(Key Features)

1. 管理者後台->進階設定->新增關閉姓名和暱稱開關。
2. 當關閉姓名暱稱後，選角色時如系統檢查到該玩家尚無暱稱和姓名，會自動給預設的姓名和暱稱(隨機取名)。
3. 前台遊戲頭像內需增加暱稱修改的功能(只有系統自動產生的暱稱可進行修改)。
4. 個人設定頁面需增加暱稱和姓名修改的功能(只有系統自動產生的暱稱可進行修改)。

## 用戶流程(User Flow)

1. 玩家進入世界選角色時，系統會進行判斷，如後台有關閉暱稱或姓名，會自動給玩家預設的姓名或暱稱
2. 如果姓名或暱稱是系統自動產生，則玩家可以在頭像內進行修改。

<figure><img src=".gitbook/assets/image (21).png" alt=""><figcaption></figcaption></figure>

## 實作方向-管理者後台

1. 管理者後台->進階設定-世界設定區塊，新增以下2個開關。
   * 選角色後自動取姓名：開啟的話，玩家選角色後，如果尚未取姓名，系統會自動給預設值，玩家可隨時在個人設定內針對預設的姓名做修改
   * 選角色後自動取暱稱：開啟的話，玩家選角色後，如果尚未取暱稱，系統會自動給預設值，玩家可隨時在遊戲或個人設定內針對預設的暱稱做修改
2. 隨機命名規則：**玩家或系統預設選的 『遊戲角色名稱 』**  + **UID**

<figure><img src=".gitbook/assets/image (22).png" alt=""><figcaption></figcaption></figure>

## 實作方向-前台遊戲畫面&個人設定畫面

1. 玩家在遊戲頭像內可以針對**預設的暱稱**進行修改，如下圖
   * 只有預設的暱稱才可以修改，其餘則不會顯示修改的圖示。

<figure><img src=".gitbook/assets/image (19).png" alt=""><figcaption></figcaption></figure>

2. 玩家可以到首頁的個人設定，針對預設的姓名和暱稱進行修改。

<figure><img src=".gitbook/assets/image (20).png" alt=""><figcaption></figcaption></figure>
