# Research Paper Writing — Claude Code Plugin

[中文介绍](./README_zh.md)

## Attribution

> **Most writing knowledge and methodology in this repository comes from Prof. Peng Sida (彭思达)'s open study notes:**
> - Notion: https://pengsida.notion.site/c1a22465a0fa4b15a12985223916048e
> - GitHub: https://github.com/pengsida/learning_research
>
> I sincerely thank Prof. Peng for openly sharing these valuable experiences.
> My contribution is organization, structured adaptation, and packaging as a Claude Code plugin.

## What This Plugin Does

A Claude Code plugin that improves academic paper writing quality for ML/CV/NLP-style papers. It provides structured guidance for:

- Drafting or rewriting Abstract / Introduction / Related Work / Method / Experiments / Conclusion
- Improving paragraph flow and section logic
- Checking claim-evidence alignment
- Polishing figures and tables
- Running pre-submission self-review from a reviewer mindset

## Installation

### Option 1: Install from local clone

```bash
git clone https://github.com/Master-cai/Research-Paper-Writing-Skills.git
cd Research-Paper-Writing-Skills
```

Then use with Claude Code:

```bash
# Test with --plugin-dir
claude --plugin-dir .

# Or copy to your project
cp -R . /path/to/your-project/.claude-plugin/research-paper-writing
```

### Option 2: Install as Claude Code skill (legacy)

If you prefer the simpler skill-based installation:

```bash
# Global installation
mkdir -p "$HOME/.claude/skills"
cp -R skills/research-paper-writing "$HOME/.claude/skills/"

# Or project-level installation
mkdir -p .claude/skills
cp -R skills/research-paper-writing .claude/skills/
```

## Plugin Structure

```
research-paper-writing/
├── .claude-plugin/
│   └── plugin.json          # Plugin manifest
├── skills/
│   └── research-paper-writing/
│       ├── SKILL.md         # Core workflow and rules
│       └── references/      # Section-specific guides
│           ├── abstract.md
│           ├── introduction.md
│           ├── method.md
│           ├── experiments.md
│           ├── related-work.md
│           ├── conclusion.md
│           ├── paper-review.md
│           ├── does-my-writing-flow-source.md
│           └── examples/    # Annotated templates from real papers
├── README.md
├── README_zh.md
└── LICENSE
```

## Usage

Once installed, the skill activates automatically when you ask about paper writing tasks. Examples:

- "Help me write the Introduction section"
- "Improve the flow of my Abstract"
- "Check claim-evidence alignment in my paper"
- "Review my paper before submission"
- "Rewrite the Method section with better motivation"

## Credits

- **Writing methodology:** Prof. Peng Sida (彭思达) — [GitHub](https://github.com/pengsida/learning_research)
- **Plugin packaging:** Master-cai — [GitHub](https://github.com/Master-cai)

## License

This project is licensed under the MIT License. See [LICENSE](./LICENSE).
