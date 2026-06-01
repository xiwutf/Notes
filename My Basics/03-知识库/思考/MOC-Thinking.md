# MOC · 深度思考

> 原创洞察、观点、思维模型

---

## 思维模型

- [[THK-系统思维与长期主义]]
- [[THK-复利思维实践]]
- 

---

## 最近思考

```dataview
TABLE status, created
FROM "03-知识库/思考"
WHERE type = "thinking"
SORT file.mtime DESC
LIMIT 10
```

---

## 待输出

> 标记为「可输出」的思考，优先转化为 Assets

```dataview
LIST
FROM "03-知识库/思考"
WHERE contains(tags, "可输出")
```

→ [[03-知识库/MOC-Knowledge|知识网络总索引]] | [[05-输出/说明|Assets]]
