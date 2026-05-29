# MOC · Projects 项目索引

> Map of Content — 所有活跃项目的导航地图

---

## 🔴 进行中

```dataview
TABLE priority, deadline, area
FROM "02-Projects"
WHERE type = "project" AND status = "进行中"
SORT priority ASC
```

| 项目 | 优先级 | 截止日期 | 领域 |
|------|--------|----------|------|
| | P1 | | |

---

## 🟡 规划中

```dataview
TABLE priority, deadline, area
FROM "02-Projects"
WHERE type = "project" AND status = "规划中"
SORT priority ASC
```

---

## ⏸️ 暂停

```dataview
LIST
FROM "02-Projects"
WHERE type = "project" AND status = "暂停"
```

---

## ✅ 最近完成

```dataview
TABLE updated AS "完成日期"
FROM "02-Projects"
WHERE type = "project" AND status = "完成"
SORT updated DESC
LIMIT 5
```

---

## 按领域

### AI 开发

- 

### 工业数字孪生

- 

### 个人 IP

- 

### 财富积累

- 

---

## 项目管理原则

1. **同时进行中 ≤ 3 个**
2. **每个项目有明确的 + 可衡量的成功标准**
3. **Weekly Review 时更新此页**
4. **完成 30 天后移入 [[Archive/Projects|Archive]]**

→ [[02-Projects/README|Projects 说明]] | [[00-Dashboard/Home|Dashboard]]
