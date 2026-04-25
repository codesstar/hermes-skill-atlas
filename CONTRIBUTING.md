# Contributing to Hermes Skill Atlas

Thanks for helping grow the atlas! Here's how to add or update skills.

## Adding a New Skill

1. Fork this repo
2. Edit `data/skills.json`
3. Add your skill entry to the appropriate category
4. Submit a PR

### Skill Entry Format

```json
{
  "name": "my-skill",
  "source": "community",
  "description": "One-line description (keep it under 50 chars)",
  "install": "git clone https://github.com/user/my-skill ~/.hermes/skills/my-skill",
  "repo": "https://github.com/user/my-skill",
  "detail": "Longer description. What does it do? What are the prerequisites?",
  "stars": "42",
  "isNew": true
}
```

### Field Reference

| Field | Required | Description |
|-------|----------|-------------|
| `name` | Yes | Skill identifier (lowercase, hyphens) |
| `source` | Yes | One of: `builtin`, `hub`, `community`, `official`, `cyc` |
| `description` | Yes | Short description shown on the card |
| `install` | Yes | Install command. Use `内置 Skill，无需安装` for builtins |
| `repo` | No | GitHub repo URL |
| `detail` | No | Longer description shown in the modal |
| `stars` | No | GitHub star count (e.g. `"1.2K"`) |
| `isNew` | No | Set `true` to show a NEW badge |

### Source Types

| Source | Meaning |
|--------|---------|
| `builtin` | Ships with Hermes, no install needed |
| `hub` | Available via `hermes skills install` |
| `official` | Official Nous Research skill |
| `community` | Community-contributed, install from GitHub |
| `cyc` | Made by 奇思妙想CYC |

### Categories

| ID | Name |
|----|------|
| `productivity` | 日常生产力 |
| `search` | 搜索与研究 |
| `memory` | 记忆与上下文 |
| `writing` | 写作与内容 |
| `automation` | 任务编排 |
| `creative` | 创意可视化 |
| `agents` | AI Agent 联动 |
| `developer` | 开发者工具 |
| `comm` | 通讯社交 |
| `security` | 安全红队 |
| `fun` | 娱乐游戏 |
| `gui` | 工作区 GUI |
| `cyc` | 奇思妙想CYC |

## Updating an Existing Skill

Find the skill in `data/skills.json` and update the relevant fields. Common updates:
- Star count changed
- Repo URL changed
- New features added to description

## PR Guidelines

- One skill per PR (unless batch-adding a new category)
- Include a brief description of the skill in the PR body
- If adding a community skill, make sure the repo exists and is public
- Keep descriptions concise -- the card UI has limited space

## Proposing a New Category

Open an issue with the `[category]` tag. Include:
- Category name (Chinese + English)
- Category ID (lowercase)
- At least 3 skills that would belong in it
