# Benchmark Data & Evaluation Summary

## 1. 任务数据分布
请总结：
- task 数量
- 难度分布（easy / medium / hard 等）
- 类型/领域分布
  - coding
  - web
  - tool-use
  - reasoning
  - planning
  - SWE
  - math
  - embodied
  - browser-use
  等

如果论文有统计图或数据表，请提炼关键分布信息。

---

## 2. 每个 Task 的规模
请分析：
- 单个 task 的代码量/项目规模
- repo size
- 文件数量
- context 长度
- 平均执行步骤
- 平均耗时/周期
- 是否 long-horizon

重点说明：
- task 到底“小到什么程度”或“大到什么程度”

---

## 3. 数据是怎么构建的？
请总结：
- 数据来源是什么
- 从哪里收集的
- 是否来自真实世界
- 是否人工构建
- 是否自动生成
- 是否基于 GitHub / issue / PR / environment / simulator

并说明：
- 数据清洗方式
- 去污染(contamination)方式（如果有）
- train/test 划分方式（如果有）

---

## 4. Agent 实际可见的信息
请重点分析：

Agent 在运行时到底能看到什么？

例如：
- task description
- repository
- tools
- docs
- internet
- browser
- execution result
- unit test output
- hidden test
- public test

特别关注：
- test 是否可见
- evaluation script 是否可见
- 是否存在 hidden test
- 是否能访问 ground truth
- 是否允许多轮交互

请明确区分：
- Agent input
vs
- evaluator 内部信息

---

## 5. 评估指标 / 测试方式
请总结：
- success rate
- pass@k
- reward
- execution accuracy
- human evaluation
- LLM-as-a-judge
- sandbox execution
- unit test
- trajectory evaluation
等。

并说明：
- 最终是怎么判定成功的
- evaluator 如何工作
- 是否自动化评测
- 是否存在 flaky evaluation

---

## 6. 各 Agent 的表现
请总结：
- 哪些 agent/model 表现最好
- GPT-4 / Claude / open-source 的表现
- scaffold 是否显著提升
- tool-use / reflection / planning 是否有效

重点提炼：
- 实验结果真正说明了什么

不要只抄表格，要总结趋势。

---

## 7. Benchmark 的难点主要来自什么？
请重点总结 benchmark 的核心难度来源：

例如：
- long horizon
- sparse feedback
- environment interaction
- planning
- debugging
- retrieval
- memory
- tool selection
- partial observability
- noisy environment
- hidden tests
- large codebase
- ambiguous instruction
- multi-step reasoning
等。

并说明：
- agent 最容易失败在哪
- benchmark 真正卡 agent 的地方是什么

---

## 最后总结（研究视角）
请像 researcher 一样总结：

- 这个 benchmark 最值得学习的数据设计是什么
- 它最重要的 evaluation philosophy 是什么
- 它是否真的能有效衡量 agent 能力
- 它有哪些局限性

输出要求：
- 多用 bullet points
- 不要大段复述论文
- 优先提炼 benchmark design insight
- 如果 GitHub 有实现细节，请结合代码分析
- 如果某部分论文没有明确写，请明确说明
