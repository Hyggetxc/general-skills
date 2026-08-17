---
name: skill-design
description: Use when creating, updating, renaming, reviewing, or refactoring local Codex skills, skill repositories, skill routing rules, skill descriptions, references, evals, or agents/openai.yaml metadata.
---

# Skill 设计

创建、更新和审查本地 skill，保证触发准确、单一权威、渐进式披露、完成标准清楚、验证可运行。

## 执行原则

1. 先判断是否需要独立 skill。只在跨项目复用、触发明确、职责独立时新增；项目专属规则优先放项目 SOP 或 AGENTS.md。
2. `description` 是触发器，只写适用场景和不适用场景；不要把完整流程写进 description。
3. `SKILL.md` 放核心流程；分支规则、模板和长示例放 `references/`。
4. 同一规则只放一个权威位置。其他 skill 只引用，不复制。
5. 每个实质步骤要有完成标准。
6. 改名必须同步目录名、frontmatter `name`、互相引用、`agents/openai.yaml`、eval、脚本和 README。
7. 修改后必须验证；不能只凭阅读宣称完成。

## 工作流

1. 盘点现状：读取目标 skill、引用它的文件、eval、脚本和元数据。
2. 设计范围：说明新增、更新、改名或删除的理由和边界。
3. 编辑 skill：保持主文件简洁，按分支拆引用文件。
4. 同步元数据：检查 `agents/openai.yaml` 的名称、描述和 default prompt。
5. 验证：读取 `references/skill-quality-gates.md`。
6. 输出结果：列出修改文件、验证证据、仍需人工检查项。

## 边界

1. 不安装外部 skill 包，除非用户明确要求。
2. 不提交、不推送、不发布。
3. 不把一次性工作过程写成通用 skill。
4. 不把业务事实写进通用 skill。

## 资源导航

- `references/skill-quality-gates.md`：skill 审查与验证门禁。
