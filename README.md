# General Skills

General-purpose skills for source-backed research, plain-language rewriting, skill design, and guided teaching workspaces.

These skills are intentionally not tied to any company, product, private repository, or domain-specific workflow.

## Skills

| Skill | Purpose |
| --- | --- |
| `source-research` | Check facts with primary sources and report evidence boundaries without making business decisions. |
| `human-language` | Rewrite content in plain Chinese while preserving facts and terminology; review-only requests do not trigger a rewrite, and code or structured data stays unchanged. |
| `skill-design` | Create, update, or audit skills, routing, metadata, and checks; verify source-to-runtime synchronization and require explicit authorization before publishing. |
| `teach` | Run a stateful learning workspace with missions, resources, lessons, reference documents, and learning records. |

## Install

Clone the repository:

```bash
git clone https://github.com/Hyggetxc/general-skills.git
```

Copy the skills you want into your skills directory:

```bash
mkdir -p ~/.codex/skills
cp -R source-research ~/.codex/skills/
cp -R human-language ~/.codex/skills/
cp -R skill-design ~/.codex/skills/
cp -R teach ~/.codex/skills/
```

Or copy them into a project-level skills directory:

```bash
mkdir -p "<project>/.codex/skills"
cp -R source-research "<project>/.codex/skills/"
cp -R human-language "<project>/.codex/skills/"
cp -R skill-design "<project>/.codex/skills/"
cp -R teach "<project>/.codex/skills/"
```

## Scope

- Keep these skills generic and reusable.
- Do not add private business logic, client names, internal repository paths, credentials, tokens, or environment-specific workflow rules.
- Put project-specific rules in that project's `AGENTS.md`, SOP, or project-local skill instead.
- Before publishing changes, run structure validation and scan for sensitive local content.
- Existing project glossaries or knowledge bases are optional context, not bundled dependencies. No additional skill is required for terminology maintenance.

## Validation

Validate a skill with the skill validator if available:

```bash
python3 ~/.codex/skills/.system/skill-creator/scripts/quick_validate.py source-research
python3 ~/.codex/skills/.system/skill-creator/scripts/quick_validate.py human-language
python3 ~/.codex/skills/.system/skill-creator/scripts/quick_validate.py skill-design
python3 ~/.codex/skills/.system/skill-creator/scripts/quick_validate.py teach
```

Also scan for accidental local or private content before publishing:

```bash
rg -n "(HOME_DIR|token|secret|credential|client-name|customer-name)" .
```
