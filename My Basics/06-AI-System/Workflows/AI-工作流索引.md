# AI 工作流索引

> 标准化的 AI 协作流程 — 输入明确、步骤清晰、输出归档

---

## 工作流设计原则

1. **输入标准化**：明确从哪个目录取什么类型的笔记
2. **步骤可重复**：同一流程至少执行 3 次后才固化为 Workflow
3. **输出有归档**：AI 产出必须存入指定目录，经人工审核
4. **Prompt 引用**：每个 Workflow 链接到 [[06-AI-System/Prompts/Prompt-索引|Prompt 库]] 中的具体 Prompt

---

## WF-01 · 思考深化

**场景**：有一个初步想法，需要深度思考

```
触发：Inbox 中出现值得深化的想法
  ↓
输入：Inbox 条目
  ↓
步骤：
  1. 复制「深度思考引导」Prompt
  2. 与 AI 对话 2-3 轮
  3. 使用 [[07-Templates/Thinking Template|Thinking Template]] 创建笔记
  4. 链接至少 2 条已有笔记
  5. 更新 [[03-Knowledge/Thinking/MOC-Thinking|MOC-Thinking]]
  ↓
输出：03-Knowledge/Thinking/THK-xxx.md
```

---

## WF-02 · 知识内化

**场景**：读了一篇文章/书/课程，需要转化为个人知识

```
触发：阅读完成，Inbox 中有摘要
  ↓
输入：原始材料 + Inbox 摘要
  ↓
步骤：
  1. 使用「知识内化」Prompt 提取核心
  2. 使用 [[07-Templates/Knowledge Template|Knowledge Template]] 创建笔记
  3. 填写「我的理解」（必须用自己的话）
  4. 链接相关笔记，更新领域 MOC
  5. 标记 status: 种子
  ↓
输出：03-Knowledge/{领域}/KNW-xxx.md
```

---

## WF-03 · 内容创作

**场景**：从成熟知识笔记产出一篇对外内容

```
触发：Knowledge 笔记 status = 成熟，tags 含「可输出」
  ↓
输入：1-3 条相关 Knowledge 笔记
  ↓
步骤：
  1. 使用「文章大纲」Prompt 生成大纲
  2. 人工审校大纲
  3. 使用「技术博客」Prompt 生成初稿
  4. 人工编辑润色
  5. 创建 Assets 笔记，标注来源
  ↓
输出：05-Assets/AST-xxx.md
```

---

## WF-04 · 项目启动

**场景**：Inbox 中的想法值得作为一个项目推进

```
触发：Inbox 条目评估为「可行动的项目」
  ↓
输入：Inbox 条目 + 相关 Knowledge
  ↓
步骤：
  1. 使用「项目规划」Prompt 生成框架
  2. 使用 [[07-Templates/Project Template|Project Template]] 创建项目
  3. 设定里程碑和成功标准
  4. 更新 [[02-Projects/MOC-Projects|MOC-Projects]]
  5. 在 Daily Note 中添加项目任务
  ↓
输出：02-Projects/PRJ-xxx.md
```

---

## WF-05 · 每周复盘

**场景**：Weekly Review

```
触发：每周日
  ↓
输入：本周 Daily Notes + 项目状态 + Inbox
  ↓
步骤：
  1. 使用 [[07-Templates/Weekly Review Template|Weekly Review Template]]
  2. 使用「Weekly Review」Prompt 辅助分析
  3. 更新所有 MOC 索引
  4. 清空 Inbox
  5. 规划下周 Top 3
  ↓
输出：08-Daily/Reviews/YYYY-Www.md
```

---

## WF-06 · 个人 RAG 查询

**场景**：基于个人知识库回答问题（需外部工具）

```
触发：需要回忆/查找已有知识
  ↓
输入：自然语言问题
  ↓
步骤：
  1. 使用 Obsidian 搜索 / Dataview 查询
  2. （进阶）向量化笔记库，使用 RAG 检索
  3. 引用相关笔记链接
  ↓
输出：答案 + 来源笔记链接
```

---

## 工作流迭代日志

| 日期 | 工作流 | 变更 |
|------|--------|------|
| 2026-05-26 | 全部 | 初始版本 |

→ [[06-AI-System/Prompts/Prompt-索引|Prompt 库]] | [[06-AI-System/README|AI System]]
