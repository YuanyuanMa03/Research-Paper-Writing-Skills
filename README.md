# Paper Writing Skills Marketplace — Claude Code Plugin Marketplace

[中文介绍](./README_zh.md)

## Attribution

> **Most writing knowledge and methodology in this repository comes from Prof. Peng Sida (彭思达)'s open study notes:**
> - Notion: https://pengsida.notion.site/c1a22465a0fa4b15a12985223916048e
> - GitHub: https://github.com/pengsida/learning_research
>
> I sincerely thank Prof. Peng for openly sharing these valuable experiences.
> My contribution is organization, structured adaptation, and packaging as a Claude Code plugin marketplace.

## What This Marketplace Provides

A Claude Code plugin marketplace for paper writing skills. Currently includes:

- **research-paper-writing** — Academic paper writing guidance for ML/CV/NLP-style papers

## Installation

### Add the marketplace

```bash
/plugin marketplace add YuanyuanMa03/paper-writing-skills-marketplace
```

### Install plugins

```bash
/plugin install research-paper-writing@paper-writing-skills-marketplace
```

### Update

```bash
/plugin marketplace update paper-writing-skills-marketplace
```

## Marketplace Structure

```
paper-writing-skills-marketplace/
├── .claude-plugin/
│   └── marketplace.json              # Marketplace registry
├── plugins/
│   └── research-paper-writing/       # Plugin
│       ├── .claude-plugin/
│       │   └── plugin.json           # Plugin manifest
│       └── skills/
│           └── research-paper-writing/
│               ├── SKILL.md          # Core workflow and rules
│               └── references/       # Section-specific guides
│                   ├── abstract.md
│                   ├── introduction.md
│                   ├── method.md
│                   ├── experiments.md
│                   ├── related-work.md
│                   ├── conclusion.md
│                   ├── paper-review.md
│                   └── examples/     # Annotated templates
├── README.md
├── README_zh.md
└── LICENSE
```

## Usage

Once installed, the skill activates automatically when you ask about paper writing tasks:

- "Help me write the Introduction section"
- "Improve the flow of my Abstract"
- "Check claim-evidence alignment in my paper"
- "Review my paper before submission"
- "Rewrite the Method section with better motivation"

## Adding Your Own Plugins

To contribute a plugin to this marketplace:

1. Create your plugin in `plugins/your-plugin-name/`
2. Add a `.claude-plugin/plugin.json` manifest
3. Add an entry to `.claude-plugin/marketplace.json`
4. Submit a pull request

## Credits

- **Writing methodology:** Prof. Peng Sida (彭思达) — [GitHub](https://github.com/pengsida/learning_research)
- **Plugin packaging:** Master-cai — [GitHub](https://github.com/Master-cai)

## License

This project is licensed under the MIT License. See [LICENSE](./LICENSE).
