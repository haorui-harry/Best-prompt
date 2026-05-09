# Benchmark Task Analysis

## 1. 数据格式
请说明 benchmark 的 task 数据长什么样：

例如：
- json
- yaml
- repo
- issue
- prompt
- environment state
- trajectory
- test case
- browser task
- API task
等。

并重点说明：
- 一个 task 包含哪些字段
- 输入是什么
- 输出是什么
- evaluator 如何读取 task
- 是否包含 hidden test
- 是否包含 execution environment

如果可能，请给一个真实 task 的结构示例（简化即可）。

---

## 2. 题目案例（详细展示一个）
请选择一个有代表性的 task，详细说明：

### Task 内容
- task instruction 是什么
- agent 需要完成什么

### Agent 实际会看到什么
- 能访问哪些文件/工具/环境
- 是否能看到 test

### Agent 需要执行什么
例如：
- 修改代码
- 调 API
- 浏览网页
- 修 bug
- 写测试
- 多步规划
- tool use
等。

### 最终如何判定成功
例如：
- unit test pass
- hidden test
- execution result
- reward
- human evaluation
等。

尽量让人能真正理解：
“agent 实际跑这个 task 时是什么体验”。

---

## 3. 这个题目具体在考察什么能力？
请总结：
- planning
- debugging
- retrieval
- reasoning
- memory
- tool use
- long-horizon execution
- browser interaction
- environment interaction
- code understanding
等。

并说明：
- 难点主要来自哪里
- agent 最容易失败在哪

---

## 4. 代表性题目（重点）
请挑选 10 个最有代表性的 task。

对于每个 task，请输出：

### Task 名称
### 仓库中的路径
（task 文件路径 / dataset 路径 / repo 路径）

### 为什么选这个题目
例如：
- 最能体现 benchmark 核心思想
- 最难
- 最真实
- 最典型
- 最依赖 tool use
- 最 long-horizon
等。

### 这个题目要求 Agent 做什么
请用简洁语言说明任务目标。

### 这个题目主要考察什么能力
例如：
- code repair
- planning
- debugging
- web navigation
- reasoning
- multi-step execution
- memory
等。

尽量覆盖不同难度和不同类型。

---

## 最后总结（研究视角）
请总结：

- 这个 benchmark 的 task design 最大特点是什么
- 哪类 task 最有研究价值
- 哪类 task 最能区分 agent 能力
- 哪些 task 设计最值得学习
- benchmark 的 task 是否真实、是否容易过拟合

输出要求：
- 多用 bullet points
- 不要大段复述论文
- 优先结合 GitHub 里的真实 task 分析
- 如果某些 task 在代码里找不到，请明确说明
