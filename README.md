# Agent Failure Predictor

**Predict how your AI agent will fail — before it happens.**

---

### 核心理念

Agent 的失败不是随机的，而是由结构决定的。

这个工具不帮你优化性能，也不教你写更好的 Prompt。

它只做一件事：

**提前告诉你，你的 Agent 最可能以哪种方式崩溃，以及为什么。**

---

### 支持的失败类型

- **Explosion**：复杂度或工具调用失控爆炸
- **Loop**：陷入反复震荡或死循环
- **Drift**：目标逐渐偏离，最终跑偏
- **Collapse**：控制力突然丧失
- **Stable**：目前结构相对稳定（但仍可能存在隐患）

---

### 如何使用

你只需要选择或描述几个关键结构维度：

- Tool Usage（工具使用强度）
- Memory（是否有记忆机制）
- Reflection（是否有反思/自检）
- Goal Clarity（目标是否清晰）
- Depth Limit（调用深度是否有界限）
- External Exposure（对外暴露程度）

系统会自动分析这些结构的组合，预测最可能的失败路径。

---

### 示例

**输入结构：**
- Tool Usage: High
- Memory: None
- Reflection: Off
- Depth: Unbounded

**预测结果：**
- **Failure Type**: Explosion（高概率）
- **Stage**: Early–Mid
- **Core Reason**: 无反思机制 + 无界限的工具调用，导致复杂度快速失控
- **Suggestion**: 立即增加调用深度限制和反思步骤

---

### 实时演示

👉 **[https://failure-predictor-web.vercel.app/](https://failure-predictor-web.vercel.app/)**

---

### 当前状态

- 支持 5 种主要失败类型预测
- 支持结构输入 → 失败命运映射
- 支持简单轨迹模拟与解释
- 仍在快速迭代

欢迎真实使用后提出反馈。

---

### 联系我

有任何想法、案例或合作意向，欢迎邮件联系：  
**kingtmn1@gmail.com**

---

### Contributing

目前还处于早期实验阶段。

如果你有使用中的案例、发现的 bug，或者对失败模式的看法，欢迎 Issue 或 Pull Request。
https://failure-predictor-web.vercel.app/

---

**Made with focus on clarity over complexity.**
=======
**Made to understand failure, not just optimize performance.**
>>>>>>> 7a7506a (Update README.md with clearer product positioning and live demo link)
