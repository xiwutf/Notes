# 07-Templates

## 用途

Templates 存放所有**标准化笔记模板**。通过 Templater 插件一键生成，确保每条笔记结构一致、元数据完整、可被 Dataview 检索。

## 模板清单

| 模板 | 用途 | 目标目录 |
|------|------|----------|
| [[Daily Note Template]] | 每日记录 | 08-Daily |
| [[Project Template]] | 项目启动 | 02-Projects |
| [[Thinking Template]] | 深度思考 | 03-Knowledge/Thinking |
| [[Knowledge Template]] | 知识沉淀 | 03-Knowledge |
| [[Weekly Review Template]] | 每周复盘 | 08-Daily |

## 使用建议

1. **Templater 配置**：将此目录设为 Templates folder
2. **快捷键绑定**：为常用模板设置热键（如 `Ctrl+Shift+D` → Daily）
3. **不修改模板原件**：生成后在新文件中编辑，模板保持干净
4. **按需扩展**：发现重复结构时，新增模板而非复制粘贴
5. **Frontmatter 规范**：所有模板包含统一元数据字段，便于 Dataview 查询

## Templater 配置参考

```
Settings → Templater → Template folder location → 07-Templates
Settings → Templater → Trigger Templater on new file creation → ON
```

## 元数据字段标准

```yaml
---
type: daily | project | thinking | knowledge | review
status: 
tags: []
created: 
updated: 
---
```
