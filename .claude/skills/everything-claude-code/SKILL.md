---
name: everything-claude-code-conventions
description: Development conventions and patterns for everything-claude-code. JavaScript project with conventional commits.
---

# Everything Claude Code Conventions

> Generated from [affaan-m/everything-claude-code](https://github.com/affaan-m/everything-claude-code) on 2026-03-24

## Overview

This skill teaches Claude the development patterns and conventions used in everything-claude-code.

## Tech Stack

- **Primary Language**: JavaScript
- **Architecture**: hybrid module organization
- **Test Location**: separate

## When to Use This Skill

Activate this skill when:
- Making changes to this repository
- Adding new features following established patterns
- Writing tests that match project conventions
- Creating commits with proper message format

## Commit Conventions

Follow these commit message conventions based on 500 analyzed commits.

### Commit Style: Conventional Commits

### Prefixes Used

- `feat`
- `fix`
- `docs`
- `test`

### Message Guidelines

- Average message length: ~62 characters
- Keep first line concise and descriptive
- Use imperative mood ("Add feature" not "Added feature")


*Commit message example*

```text
feat: add everything-claude-code ECC bundle (.claude/commands/add-or-update-skill.md)
```

*Commit message example*

```text
perf(hooks): move post-edit-format and post-edit-typecheck to strict-only (#757)
```

*Commit message example*

```text
fix: safe Codex config sync — merge AGENTS.md + add-only MCP servers (#723)
```

*Commit message example*

```text
docs(zh-CN): translate code block(plain text) (#753)
```

*Commit message example*

```text
security: remove supply chain risks, external promotions, and unauthorized credits
```

*Commit message example*

```text
feat: add everything-claude-code ECC bundle (.claude/commands/feature-development.md)
```

*Commit message example*

```text
feat: add everything-claude-code ECC bundle (.claude/commands/database-migration.md)
```

*Commit message example*

```text
feat: add everything-claude-code ECC bundle (.claude/enterprise/controls.md)
```

## Architecture

### Project Structure: Single Package

This project uses **hybrid** module organization.

### Configuration Files

- `.github/workflows/ci.yml`
- `.github/workflows/maintenance.yml`
- `.github/workflows/monthly-metrics.yml`
- `.github/workflows/release.yml`
- `.github/workflows/reusable-release.yml`
- `.github/workflows/reusable-test.yml`
- `.github/workflows/reusable-validate.yml`
- `.opencode/package.json`
- `.opencode/tsconfig.json`
- `.prettierrc`
- `eslint.config.js`
- `package.json`

### Guidelines

- This project uses a hybrid organization
- Follow existing patterns when adding new code

## Code Style

### Language: JavaScript

### Naming Conventions

| Element | Convention |
|---------|------------|
| Files | camelCase |
| Functions | camelCase |
| Classes | PascalCase |
| Constants | SCREAMING_SNAKE_CASE |

### Import Style: Relative Imports

### Export Style: Mixed Style


*Preferred import style*

```typescript
// Use relative imports
import { Button } from '../components/Button'
import { useAuth } from './hooks/useAuth'
```

## Testing

### Test Framework

No specific test framework detected — use the repository's existing test patterns.

### File Pattern: `*.test.js`

### Test Types

- **Unit tests**: Test individual functions and components in isolation
- **Integration tests**: Test interactions between multiple components/services

### Coverage

This project has coverage reporting configured. Aim for 80%+ coverage.


## Error Handling

### Error Handling Style: Try-Catch Blocks


*Standard error handling pattern*

```typescript
try {
  const result = await riskyOperation()
  return result
} catch (error) {
  console.error('Operation failed:', error)
  throw new Error('User-friendly message')
}
```

## Common Workflows

These workflows were detected from analyzing commit patterns.

### Database Migration

Database schema changes with migration files

**Frequency**: ~2 times per month

**Steps**:
1. Create migration file
2. Update schema definitions
3. Generate/update types

**Files typically involved**:
- `migrations/*`

**Example commit sequence**:
```
Add Turkish (tr) docs and update README (#744)
docs(zh-CN): translate code block(plain text) (#753)
fix(install): add rust, cpp, csharp to legacy language alias map (#747)
```

### Feature Development

Standard feature implementation workflow

**Frequency**: ~26 times per month

**Steps**:
1. Add feature implementation
2. Add tests for feature
3. Update documentation

**Files typically involved**:
- `manifests/*`
- `**/*.test.*`
- `**/api/**`

**Example commit sequence**:
```
Merge pull request #736 from pvgomes/docs/add-brazilian-portuguese-translation
fix: bump plugin.json and marketplace.json to v1.9.0
Add Turkish (tr) docs and update README (#744)
```

### Add Or Update Skill

Adds or updates a skill, including its documentation and configuration.

**Frequency**: ~2 times per month

**Steps**:
1. Create or update .claude/commands/add-or-update-skill.md
2. Create or update .claude/skills/<skill-name>/SKILL.md
3. Optionally update .agents/skills/<skill-name>/SKILL.md
4. Optionally update .agents/skills/<skill-name>/agents/*.yaml

**Files typically involved**:
- `.claude/commands/add-or-update-skill.md`
- `.claude/skills/*/SKILL.md`
- `.agents/skills/*/SKILL.md`
- `.agents/skills/*/agents/*.yaml`

**Example commit sequence**:
```
Create or update .claude/commands/add-or-update-skill.md
Create or update .claude/skills/<skill-name>/SKILL.md
Optionally update .agents/skills/<skill-name>/SKILL.md
Optionally update .agents/skills/<skill-name>/agents/*.yaml
```

### Add Or Update Command Documentation

Adds or updates documentation for a CLI command or workflow.

**Frequency**: ~3 times per month

**Steps**:
1. Create or update .claude/commands/<command-name>.md

**Files typically involved**:
- `.claude/commands/*.md`

**Example commit sequence**:
```
Create or update .claude/commands/<command-name>.md
```

### Add Or Update Database Migration Patterns

Adds or updates database migration patterns or documentation.

**Frequency**: ~2 times per month

**Steps**:
1. Create or update .claude/commands/database-migration.md
2. Create or update skills/database-migrations/SKILL.md

**Files typically involved**:
- `.claude/commands/database-migration.md`
- `skills/database-migrations/SKILL.md`

**Example commit sequence**:
```
Create or update .claude/commands/database-migration.md
Create or update skills/database-migrations/SKILL.md
```

### Add Or Update Team Or Identity Config

Adds or updates team configuration or identity files.

**Frequency**: ~2 times per month

**Steps**:
1. Create or update .claude/team/everything-claude-code-team-config.json
2. Create or update .claude/identity.json

**Files typically involved**:
- `.claude/team/everything-claude-code-team-config.json`
- `.claude/identity.json`

**Example commit sequence**:
```
Create or update .claude/team/everything-claude-code-team-config.json
Create or update .claude/identity.json
```

### Add Or Update Guardrails Or Controls

Adds or updates project guardrails, rules, or enterprise controls.

**Frequency**: ~2 times per month

**Steps**:
1. Create or update .claude/rules/everything-claude-code-guardrails.md
2. Create or update .claude/enterprise/controls.md

**Files typically involved**:
- `.claude/rules/everything-claude-code-guardrails.md`
- `.claude/enterprise/controls.md`

**Example commit sequence**:
```
Create or update .claude/rules/everything-claude-code-guardrails.md
Create or update .claude/enterprise/controls.md
```

### Add Or Update Agent Config

Adds or updates agent configuration TOML files.

**Frequency**: ~2 times per month

**Steps**:
1. Create or update .codex/agents/*.toml

**Files typically involved**:
- `.codex/agents/*.toml`

**Example commit sequence**:
```
Create or update .codex/agents/*.toml
```

### Add Or Update Research Playbook

Adds or updates research playbooks or process documentation.

**Frequency**: ~2 times per month

**Steps**:
1. Create or update .claude/research/everything-claude-code-research-playbook.md

**Files typically involved**:
- `.claude/research/everything-claude-code-research-playbook.md`

**Example commit sequence**:
```
Create or update .claude/research/everything-claude-code-research-playbook.md
```

### Add Or Update Ecc Tools Config

Adds or updates ECC tools configuration.

**Frequency**: ~2 times per month

**Steps**:
1. Create or update .claude/ecc-tools.json

**Files typically involved**:
- `.claude/ecc-tools.json`

**Example commit sequence**:
```
Create or update .claude/ecc-tools.json
```


## Best Practices

Based on analysis of the codebase, follow these practices:

### Do

- Use conventional commit format (feat:, fix:, etc.)
- Follow *.test.js naming pattern
- Use camelCase for file names
- Prefer mixed exports

### Don't

- Don't write vague commit messages
- Don't skip tests for new features
- Don't deviate from established patterns without discussion

---

*This skill was auto-generated by [ECC Tools](https://ecc.tools). Review and customize as needed for your team.*
