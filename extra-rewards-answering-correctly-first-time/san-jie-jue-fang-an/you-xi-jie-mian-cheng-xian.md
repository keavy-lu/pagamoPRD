---
description: 遊戲介面呈現
---

# 遊戲介面呈現

第一版不做任何動畫，若該題組首次全對，直接傷害力數字x2



<figure><img src="../.gitbook/assets/截圖 2024-12-17 下午2.00.17.png" alt=""><figcaption></figcaption></figure>

全對題組總傷害力公式：

&#x20;1\.  題組係數\
於管理者後台設定「題組防刷分錯題次數」後，若錯題次數高於此參數，將「係數」設為 0

&#x20; \- 若未套用上述功能，題組係數公式為:\
0.8+0.2x子題數＝理論值\
答對題數/總題數＝答對率\
理論值x答對率\*\*2＝題組係數

* 係數乘以各項傷害後，會再四捨五入

2. 題組各項傷害加成\
   (題組係數 \* 基礎傷害) + (題組係數 \* 難度加成) + (題組係數 \* 答題速度加成) + (題組係數 \* 爆擊傷害) + (題組係數 \* 題目集加成)＝題組各項傷害加成<br>
3. 題組總傷害力\
   題組各項傷害加成 + 角色額外傷害 + 道具效果 - 減傷效果＝題組總傷害力<br>
4. **全對題組總傷害力（本機制新增）**\
   題組總傷害力x2＝全對題組總傷害力\
   \
   如下圖範例：原始傷害力 107，經判斷是題組 + 首次全對 + 該課程開啟開關，\
   會加上題組加成：107，最後得到 214 的新傷害力<br>
5. 更詳細戰鬥相關公式請參考：[總整理\_戰鬥傷害計算機制](https://boniotw-my.sharepoint.com/:w:/g/personal/bonio_share_bonio_com_tw/Ef4VYbF3RmlKvbA7nQEsJfMBYT5DNKDO_mpBzJG0Mctzkw?e=xj8RZ6)

<figure><img src="../.gitbook/assets/image (23).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/截圖 2025-01-03 下午6.28.24.png" alt=""><figcaption></figcaption></figure>
