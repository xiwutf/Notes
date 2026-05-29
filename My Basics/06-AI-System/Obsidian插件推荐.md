# Obsidian 插件推荐

> 本认知系统的核心插件配置指南

---

## 必装插件

### 1. Dataview

**用途**

将笔记元数据转化为动态查询——Dashboard 的项目列表、知识索引、系统状态统计都依赖 Dataview。没有它，MOC 和 Home 页面的自动聚合无法工作。

**安装方式**

1. Settings → Community Plugins → Turn on community plugins
2. Browse → 搜索 `Dataview` → Install → Enable

**推荐配置**

```
Settings → Dataview:
  ✅ Enable JavaScript Queries
  ✅ Enable Inline Queries
  ✅ Enable DataviewJS

常用查询语法：
  TABLE status, priority FROM "02-Projects" WHERE type = "project"
  LIST FROM "03-Knowledge" WHERE status = "种子"
  TABLE length(rows) AS "数量" FROM "" GROUP BY type
```

**在本系统中的用法**

- [[00-Dashboard/Home|Dashboard Home]] — 项目列表、最近思考、系统统计
- [[02-Projects/MOC-Projects|MOC-Projects]] — 按状态筛选项目
- [[03-Knowledge/MOC-Knowledge|MOC-Knowledge]] — 知识状态追踪

---

### 2. Templater

**用途**

模板引擎——创建 Daily Note、Project、Thinking 笔记时自动填充日期、生成 Frontmatter、插入双向链接。本系统所有 [[07-Templates|Templates]] 都使用 Templater 语法。

**安装方式**

1. Community Plugins → Browse → 搜索 `Templater` → Install → Enable

**推荐配置**

```
Settings → Templater:
  Template folder location: 07-Templates
  ✅ Trigger Templater on new file creation
  ✅ Enable Folder Templates:
     08-Daily/ → Daily Note Template
     02-Projects/ → Project Template
     03-Knowledge/Thinking/ → Thinking Template
     03-Knowledge/ → Knowledge Template
     08-Daily/Reviews/ → Weekly Review Template

Settings → Hotkeys:
  绑定常用模板快捷键，如 Ctrl+Shift+D → Daily Note Template
```

**语法示例**

```markdown
<% tp.date.now("YYYY-MM-DD") %>        → 2026-05-26
<% tp.file.title %>                     → 当前文件名
[[08-Daily/<% tp.date.now("YYYY-MM-DD", -1) %>|昨日]]  → 昨日链接
```

---

### 3. Tasks

**用途**

跨笔记任务管理——在 Daily Note、Project、Inbox 中创建的任务可以统一查询、按优先级排序、追踪完成状态。

**安装方式**

1. Community Plugins → Browse → 搜索 `Tasks` → Install → Enable

**推荐配置**

```
Settings → Tasks:
  Global Filter: 留空（或设置 path includes 08-Daily OR 02-Projects）
  
任务语法：
  - [ ] 普通任务
  - [ ] 任务 📅 2026-05-30        （截止日期）
  - [ ] 任务 ⏫                   （高优先级）
  - [ ] 任务 🔁 every week        （重复任务）
  - [x] 已完成任务 ✅ 2026-05-26  （完成日期）

Dashboard 查询示例：
  ```tasks
  not done
  due before tomorrow
  sort by priority
  limit 10
  ```
```

**在本系统中的用法**

- Daily Note 的「今日任务」区块
- Project 的「目标」和「里程碑」
- Dashboard Home 的「今日重点」

---

### 4. Calendar

**用途**

日历视图——可视化 Daily Notes，点击日期创建/打开对应笔记，直观看到记录连续性。

**安装方式**

1. Community Plugins → Browse → 搜索 `Calendar` → Install → Enable

**推荐配置**

```
Settings → Calendar:
  ✅ Show week numbers
  
Settings → Daily Notes（Core Plugin）:
  ✅ Enable Daily Notes
  New file location: 08-Daily
  Template file location: 07-Templates/Daily Note Template
  Date format: YYYY-MM-DD

Settings → Calendar → 建议固定在右侧边栏
```

**在本系统中的用法**

- 右侧边栏常驻，点击日期进入 Daily Note
- 可视化记录连续性（复利追踪）
- Weekly Review 时快速浏览一周 Daily Notes

---

### 5. Homepage

**用途**

启动页——打开 Obsidian 时自动显示 Dashboard Home，而非上次关闭的文件。确保每天从系统中枢开始。

**安装方式**

1. Community Plugins → Browse → 搜索 `Homepage` → Install → Enable

**推荐配置**

```
Settings → Homepage:
  Homepage file: 00-Dashboard/Home
  ✅ Open on startup
  ✅ Open on empty pane
  Open mode: Replace empty (或 Replace all)
```

---

## 推荐插件（可选）

| 插件 | 用途 | 优先级 |
|------|------|--------|
| **Periodic Notes** | 增强 Daily/Weekly/Monthly 笔记 | 高 |
| **Graph Analysis** | 分析知识网络连接度 | 中 |
| **Excalidraw** | 手绘架构图、思维导图 | 中 |
| **Advanced Tables** | 表格编辑增强 | 中 |
| **QuickAdd** | 快速捕获到 Inbox | 高 |
| **Tag Wrangler** | 标签管理 | 低 |
| **Obsidian Git** | 自动备份到 Git | 高 |

### QuickAdd 推荐配置

```
Macro: Quick Capture
  → Capture to 01-Inbox/README
  → Format: - {DATE} {VALUE}
  → Hotkey: Ctrl+Shift+I
```

---

## 插件安装清单

```
必装（5 个）：
  ✅ Dataview
  ✅ Templater
  ✅ Tasks
  ✅ Calendar
  ✅ Homepage

推荐（4 个）：
  ☐ Periodic Notes
  ☐ QuickAdd
  ☐ Obsidian Git
  ☐ Excalidraw
```

---

## Core Plugins 推荐开启

```
Settings → Core Plugins:
  ✅ Daily Notes
  ✅ Templates
  ✅ Backlinks
  ✅ Outgoing Links
  ✅ Graph View
  ✅ Tag Pane
  ✅ Page Preview
  ✅ File Recovery
```

---

→ [[00-Dashboard/Home|Dashboard]] | [[认知系统说明书|认知系统说明书]]
