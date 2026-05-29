# MOC · Knowledge 知识网络

> 认知系统的核心索引 — 连接所有知识领域的枢纽

---

## 领域地图

| 领域 | MOC | 说明 |
|------|-----|------|
| AI 开发 | [[03-Knowledge/AI/MOC-AI\|AI]] | LLM、Agent、RAG、工程实践 |
| 工业数字孪生 | [[03-Knowledge/Digital-Twin/MOC-Digital-Twin\|Digital Twin]] | 架构、同步、仿真、可视化 |
| 工程方法论 | [[03-Knowledge/Engineering/MOC-Engineering\|Engineering]] | 架构、工具、最佳实践 |
| 深度思考 | [[03-Knowledge/Thinking/MOC-Thinking\|Thinking]] | 洞察、观点、原创思考 |

---

## 最近更新

```dataview
TABLE domain, status, updated
FROM "03-Knowledge"
WHERE type = "knowledge" OR type = "thinking"
SORT file.mtime DESC
LIMIT 10
```

---

## 成熟知识（可输出）

```dataview
LIST
FROM "03-Knowledge"
WHERE type = "knowledge" AND status = "成熟"
SORT file.name ASC
```

---

## 种子知识（待深化）

```dataview
LIST
FROM "03-Knowledge"
WHERE type = "knowledge" AND status = "种子"
SORT file.mtime DESC
```

---

## 核心概念枢纽

> 知识网络中连接度最高的概念，定期维护

- [[KNW-系统思维]]
- [[KNW-长期主义]]
- [[KNW-复利效应]]
- [[KNW-AI-Agent架构]]
- [[KNW-数字孪生核心概念]]

---

## 知识 → 资产 流水线

```
Knowledge (status: 成熟) → 选取素材 → Assets (加工) → 外部发布
```

→ [[05-Assets/README|Assets 库]] | [[03-Knowledge/README|Knowledge 说明]]

---

## 维护规则

1. 新笔记至少链接 2 条已有笔记
2. 每个领域超过 5 条笔记时更新领域 MOC
3. 每月检查「孤儿笔记」（无入链也无出链）
4. 成熟知识标记 `status: 成熟`，触发输出流程
