# Claude Code Skills

Custom skills for [Claude Code](https://claude.ai/code), organized and ready to install.

## What are Claude Code Skills?

Skills are markdown-based prompt extensions that give Claude specialized capabilities. Each skill lives in its own directory and contains a `SKILL.md` file (with YAML frontmatter) along with optional `references/` and `scripts/` subdirectories.

## Repository Structure

```
my_skills/
├── README.md
├── write-email/
│   ├── SKILL.md                  # Skill definition (required)
│   └── references/
│       └── tone-guide.md         # Supplementary reference material
├── your-skill/
│   ├── SKILL.md
│   ├── references/
│   │   └── ...
│   └── scripts/
│       └── ...
└── ...
```

## How to Install Skills

### Option 1: Copy to the default skills directory (Recommended)

Claude Code automatically loads skills from `~/.claude/skills/`. Simply copy or symlink the skill directory:

```bash
# Copy a skill
cp -r write-email ~/.claude/skills/

# Or create a symlink (easier to keep updated)
ln -s $(pwd)/write-email ~/.claude/skills/write-email
```

After copying, the skill will be available the next time you start a Claude Code session. You can invoke it with:

```
/write-email
```

### Option 2: Clone the entire repository

```bash
# Clone the repo
git clone https://github.com/Bohrium332/my_skills.git

# Symlink each skill you want to use
ln -s $(pwd)/my_skills/write-email ~/.claude/skills/write-email
```

### Option 3: Use with project-level skills

You can also place skills in a project-specific `.claude/skills/` directory:

```bash
# In your project root
mkdir -p .claude/skills
cp -r /path/to/my_skills/write-email .claude/skills/
```

This makes the skill available only when working in that specific project.

## How to Create a New Skill

1. Create a new directory under this repository:

```bash
mkdir -p my-new-skill/references
```

2. Create a `SKILL.md` with YAML frontmatter:

```markdown
---
name: my-new-skill
description: >
  One-line description of what this skill does and when to trigger it.
  Mention keywords that should activate it.
---

# Skill Title

Your skill instructions here...
```

3. (Optional) Add reference documents in `references/` and scripts in `scripts/`.

4. Install and test:

```bash
cp -r my-new-skill ~/.claude/skills/
```

## Skill Naming Conventions

- Use lowercase with hyphens (e.g., `write-email`, `jetson-bsp`)
- The directory name becomes the slash command name (`/write-email`)
- Keep names short and descriptive

## Available Skills

| Skill | Description |
|-------|-------------|
| [write-email](./write-email/) | Generate professional technical support emails for Seeed Jetson BSP |

## License

MIT
