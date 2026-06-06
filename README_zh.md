# Paper Writing Skills Marketplace — Claude Code 插件市场

[English](./README.md)

## 归属说明

> **本仓库中的大部分写作经验与方法论来自彭思达老师公开的学习笔记：**
> - Notion: https://pengsida.notion.site/c1a22465a0fa4b15a12985223916048e
> - GitHub: https://github.com/pengsida/learning_research
>
> 衷心感谢彭思达老师把这些宝贵经验公开分享出来。
> 我主要做了资料整理、结构化适配，以及 Claude Code 插件市场封装。

## 市场功能

这是一个 Claude Code 插件市场，提供论文写作相关技能。目前包含：

- **research-paper-writing** — ML/CV/NLP 类学术论文写作指导

## 安装方式

### 添加市场

```bash
/plugin marketplace add YuanyuanMa03/paper-writing-skills-marketplace
```

### 安装插件

```bash
/plugin install research-paper-writing@paper-writing-skills-marketplace
```

### 更新

```bash
/plugin marketplace update paper-writing-skills-marketplace
```

## 市场结构

```
paper-writing-skills-marketplace/
├── .claude-plugin/
│   └── marketplace.json              # 市场注册表
├── plugins/
│   └── research-paper-writing/       # 插件
│       ├── .claude-plugin/
│       │   └── plugin.json           # 插件清单
│       └── skills/
│           └── research-paper-writing/
│               ├── SKILL.md          # 核心流程与规则
│               └── references/       # 按章节拆分的写作指南
│                   ├── abstract.md
│                   ├── introduction.md
│                   ├── method.md
│                   ├── experiments.md
│                   ├── related-work.md
│                   ├── conclusion.md
│                   ├── paper-review.md
│                   └── examples/     # 来自真实论文的标注模板
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

## 添加你的插件

向本市场贡献插件：

1. 在 `plugins/your-plugin-name/` 中创建你的插件
2. 添加 `.claude-plugin/plugin.json` 清单
3. 在 `.claude-plugin/marketplace.json` 中添加条目
4. 提交 Pull Request

## 致谢

- **写作方法论：** 彭思达老师 — [GitHub](https://github.com/pengsida/learning_research)
- **插件封装：** Master-cai — [GitHub](https://github.com/Master-cai)

## 许可证

本项目采用 MIT License，详见 [LICENSE](./LICENSE)。
