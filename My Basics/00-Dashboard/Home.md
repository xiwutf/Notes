---
type: dashboard
tags: [dashboard, home]
updated: 2026-05-26
---

# 🧠 第二大脑 · Dashboard

> AI 开发 · 工业数字孪生 · 长期成长 · 个人 IP · 财富积累

---

## 📌 今日重点

> [!important] 今天最重要的一件事
> - [ ] 

**今日任务**

- [ ] 
- [ ] 
- [ ] 

→ 打开 [[08-Daily/<% tp.date.now("YYYY-MM-DD") %>|今日 Daily Note]] *(需 Templater)*

---

## 🚀 当前项目

```dataview
TABLE status, priority, deadline
FROM "02-Projects"
WHERE type = "project" AND status = "进行中"
SORT priority ASC
LIMIT 5
```

> 无 Dataview 时手动维护：

| 项目 | 状态 | 下一步 |
|------|------|--------|
| | 进行中 | |
| | 进行中 | |
| | 进行中 | |

→ [[02-Projects/MOC-Projects|全部项目]]

---

## 💭 最近思考

```dataview
LIST
FROM "03-Knowledge/Thinking"
WHERE type = "thinking"
SORT file.mtime DESC
LIMIT 5
```

> 手动备选：

- [[03-Knowledge/Thinking/THK-系统思维与长期主义|系统思维与长期主义]]
- 

→ [[03-Knowledge/MOC-Knowledge|知识网络]]

---

## 🤖 AI 系统入口

| 入口 | 说明 |
|------|------|
| [[06-AI-System/Prompts/Prompt-索引\|Prompt 库]] | 按场景选用 Prompt |
| [[06-AI-System/Workflows/AI-工作流索引\|AI 工作流]] | 标准化 AI 协作流程 |
| [[06-AI-System/Obsidian插件推荐\|插件配置]] | Dataview / Templater 等 |
| [[认知系统说明书\|认知系统说明书]] | 系统使用手册 |

---

## 🧭 快速导航

| 区域 | 入口 | 用途 |
|------|------|------|
| 📥 | [[01-Inbox/README\|Inbox]] | 快速捕获 |
| 📋 | [[02-Projects/README\|Projects]] | 项目管理 |
| 📚 | [[03-Knowledge/README\|Knowledge]] | 知识网络 |
| 🌱 | [[04-Life/README\|Life]] | 生活成长 |
| 💎 | [[05-Assets/README\|Assets]] | 输出资产 |
| 🤖 | [[06-AI-System/README\|AI System]] | AI 增强 |
| 📅 | [[08-Daily/README\|Daily]] | 每日记录 |
| 📎 | [[Attachments/README\|Attachments]] | 附件 |
| 🗄️ | [[Archive/README\|Archive]] | 归档 |

---

## 📊 系统状态

```dataview
TABLE length(rows) AS "数量"
FROM ""
WHERE type != null
GROUP BY type
```

---

## 🔄 日常节奏

```
晨 → Dashboard → Daily Note → 处理 Inbox → 推进项目
      ↓
工 → 记录思考 → 更新 Knowledge → 使用 AI 工作流
      ↓
晚 → Daily 回顾 → 更新项目状态 → 准备明日重点
      ↓
周日 → Weekly Review → 整理 Knowledge → 规划下周
```

---

*最后更新：2026-05-26*
