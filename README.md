# Agent Failure Predictor

**Predict how your AI agent will fail — before it happens.**

---

### What it actually does

给你的 Agent 几个关键结构信息，它会告诉你：

- 这个系统最可能以哪种方式崩溃
- 崩溃大概会出现在哪个阶段
- 导致崩溃的核心结构原因是什么

它不帮你优化性能，也不教你写更好的 Prompt。  
它只做一件事：**提前告诉你系统会怎么坏掉**。

---

### Supported Failure Types

- **Explosion**：复杂度失控，资源或调用迅速爆炸
- **Loop**：陷入反复震荡或死循环
- **Drift**：目标逐渐偏离，慢慢跑偏
- **Collapse**：控制力丧失，突然失效
- **Stable**：目前结构相对稳定（但仍可能有隐患）

---

### How to use

你只需要选择或描述几个结构维度：

- Memory 使用方式
- Tool Usage 强度
- Reflection / Self-check 是否开启
- Goal 定义的清晰程度
- Execution Depth（调用层级）
- External Exposure（对外暴露程度）

系统会自动分析这些结构的组合，预测最可能的失败路径。

---

### Example

**输入：**
- Tool Usage: High
- Memory: None
- Reflection: Off
- Depth: Unbounded

**输出：**
- **Prediction**: Explosion（高概率）
- **Stage**: Early to Mid
- **Why**: 缺少 Reflection + 无界限的 Tool 调用，导致复杂度快速失控
- **Suggested focus**: 增加调用深度限制和反思机制

---

### Core Philosophy

Agent 的失败不是随机的，而是**结构性的**。

当某些结构维度组合不当时，系统会自然走向特定的失败吸引子。我们只是把这个过程提前说出来。

数学模型只用来在后台计算轨迹，不出现在用户界面上。

我们追求的不是最高精度，而是**清晰、可理解、能指导行动**的预测。

---

### Current Status

- 支持 5 种主要失败类型预测
- 支持结构输入 → 失败命运映射
- 支持简单轨迹模拟
- 支持因果解释（保持简洁）

仍在快速迭代中，欢迎真实使用后的反馈。

---

### Vision

希望有一天，每个重要的 AI Agent 在上线前，都会先问自己：

“它会以哪种方式失败？”

而这个工具，就是用来回答这个问题的。

---

### Contributing

目前还处于早期实验阶段。

如果你有使用中的案例、发现的 bug，或者对失败模式的看法，欢迎 Issue 或 Pull Request。

---

**Made with focus on clarity over complexity.**