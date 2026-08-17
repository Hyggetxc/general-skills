# Skill 质量门禁

## 结构检查

1. 目录名、frontmatter `name` 一致。
2. `description` 能触发正确场景，并排除相邻 skill。
3. `SKILL.md` 只包含核心流程和资源导航。
4. `references/` 文件由 `SKILL.md` 直接指向，不做深层追引用。
5. 没有无关 README、安装指南、变更日志等辅助文件。

## 内容检查

1. 是否存在双权威。
2. 是否重复了环境中能直接查到的信息。
3. 是否把项目事实写成通用规则。
4. 是否有明确完成标准。
5. 是否过度使用禁止句，而没有说明目标行为。
6. 是否保留了可验证证据要求。

## 改名检查

1. 目录名。
2. `SKILL.md` frontmatter。
3. `agents/openai.yaml` default prompt。
4. README 或安装说明。
5. 其他 skill 的引用。
6. eval、脚本和 fixtures。
7. 运行时副本。
8. SOP 和 AGENTS.md 兼容审查。

## 验证建议

1. 运行 quick validate。
2. 运行 skill 自带 eval。
3. 扫描旧名称残留。
4. 扫描断裂路径。
5. 对复杂 skill 用真实任务做 forward-test；如会耗时或修改外部系统，先请求用户确认。
