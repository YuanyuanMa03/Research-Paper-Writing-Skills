# Research Paper Writing — Claude Code 插件

[English](./README.md)

## 归属说明

> **本仓库中的大部分写作经验与方法论来自彭思达老师公开的学习笔记：**
> - Notion: https://pengsida.notion.site/c1a22465a0fa4b15a12985223916048e
> - GitHub: https://github.com/pengsida/learning_research
>
> 衷心感谢彭思达老师把这些宝贵经验公开分享出来。
> 我主要做了资料整理、结构化适配，以及 Claude Code 插件封装。

## 插件功能

这是一个 Claude Code 插件，用于提升 ML/CV/NLP 类学术论文的写作质量。提供以下结构化指导：

- 撰写或重写 Abstract / Introduction / Related Work / Method / Experiments / Conclusion
- 改善段落衔接与章节逻辑
- 做 claim-evidence 对齐检查
- 优化图表质量
- 提交前从 reviewer 视角进行自审

## 安装方式

### 方式一：本地克隆安装

```bash
git clone https://github.com/Master-cai/Research-Paper-Writing-Skills.git
cd Research-Paper-Writing-Skills
```

然后配合 Claude Code 使用：

```bash
# 使用 --plugin-dir 测试
claude --plugin-dir .

# 或复制到你的项目中
cp -R . /path/to/your-project/.claude-plugin/research-paper-writing
```

### 方式二：作为 Claude Code skill 安装（传统方式）

```bash
# 全局安装
mkdir -p "$HOME/.claude/skills"
cp -R skills/research-paper-writing "$HOME/.claude/skills/"

# 或项目级安装
mkdir -p .claude/skills
cp -R skills/research-paper-writing .claude/skills/
```

## 插件结构

```
research-paper-writing/
├── .claude-plugin/
│   └── plugin.json          # 插件清单
├── skills/
│   └── research-paper-writing/
│       ├── SKILL.md         # 核心流程与规则
│       └── references/      # 按章节拆分的写作指南
│           ├── abstract.md
│           ├── introduction.md
│           ├── method.md
│           ├── experiments.md
│           ├── related-work.md
│           ├── conclusion.md
│           ├── paper-review.md
│           ├── does-my-writing-flow-source.md
│           └── examples/    # 来自真实论文的标注模板
├── README.md
├── README_zh.md
└── LICENSE
```

## 使用方式

安装后，当你询问论文写作相关任务时，插件会自动激活。例如：

- "帮我写 Introduction 部分"
- "改善我的 Abstract 的流畅度"
- "检查论文中的 claim-evidence 对齐"
- "提交前帮我 review 一下论文"
- "重写 Method 部分，加强 motivation"

## 致谢

- **写作方法论：** 彭思达老师 — [GitHub](https://github.com/pengsida/learning_research)
- **插件封装：** Master-cai — [GitHub](https://github.com/Master-cai)

## 许可证

本项目采用 MIT License，详见 [LICENSE](./LICENSE)。
