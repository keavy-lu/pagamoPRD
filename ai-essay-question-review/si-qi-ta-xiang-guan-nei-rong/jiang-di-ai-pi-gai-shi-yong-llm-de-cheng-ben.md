---
description: 批改的成本成本
---

# 降低 AI 批改使用 LLM 的成本

## 114-1 學期估算約為：NTD$36,000（0.016 \* 30 \* 25000 \* 3）

1. 目前 chatGPT 4o-mini, 改用 ChatGPT 4o 會增加 10 倍 ([link](https://openai.com/api/pricing/))
2. 單題成本約USD$0.0005/ NTD$ 0.016 (USD$1＝NTD$32)
3. 每學期任務總數：30 (雙週 1 篇，每學期約 10 篇。分初中高階）
4. 單一任務最高答題人數：25,000
5. 單一任務平均送 LLM 次數：3



## 降低成本的可行機制：

### 已執行：

1. system+assistant prompt 內容統一，做 context cached&#x20;

### 其他可能方案：

1. 降低申論題預設文字上限(9999 > 500)，出題者有需要再自行提高
2. 答案通過 AI 批改後，就禁止/減少使用者再次修改送出
3. 測試其他模型 ([https://openrouter.ai/google/gemini-2.0-flash-lite-001](https://openrouter.ai/google/gemini-2.0-flash-lite-001))&#x20;
