<!-- SVENKUNKKA-README-NAV:BEGIN -->
[中文项目说明](#project-overview-zh) · [English overview](#project-overview-en) · [维护者 X / Maintainer on X](https://x.com/Svenu1s5)
<!-- SVENKUNKKA-README-NAV:END -->

# Anthropic Agent Skills

This repository is a public fork of [Anthropic's official Agent Skills repository](https://github.com/anthropics/skills). It contains reusable Claude skills, Claude Code plugin definitions, document-processing tools, skill-authoring examples, Claude API guidance, and the Agent Skills specification.

> **Fork notice:** Anthropic and the respective contributors are the original authors. This fork may not always match the latest upstream revision; check [`anthropics/skills`](https://github.com/anthropics/skills) when you need the newest version.

Skills are folders of instructions, scripts, and resources that Claude loads dynamically to improve performance on specialized tasks. They teach Claude how to complete repeatable workflows such as creating documents, following brand guidelines, analyzing data, testing web apps, and building MCP servers.

For information about the open Agent Skills standard, see [agentskills.io](https://agentskills.io).

For more information, check out:
- [What are skills?](https://support.claude.com/en/articles/12512176-what-are-skills)
- [Using skills in Claude](https://support.claude.com/en/articles/12512180-using-skills-in-claude)
- [How to create custom skills](https://support.claude.com/en/articles/12512198-creating-custom-skills)
- [Equipping agents for the real world with Agent Skills](https://anthropic.com/engineering/equipping-agents-for-the-real-world-with-agent-skills)

# About This Repository

This repository contains skills that demonstrate what's possible with Claude's skills system. These skills range from creative applications (art, music, design) to technical tasks (testing web apps, MCP server generation) to enterprise workflows (communications, branding, etc.).

Each skill is self-contained in its own folder with a `SKILL.md` file containing the instructions and metadata that Claude uses. Browse through these skills to get inspiration for your own skills or to understand different patterns and approaches.

Many skills in this repo are open source (Apache 2.0). We've also included the document creation & editing skills that power [Claude's document capabilities](https://www.anthropic.com/news/create-files) under the hood in the [`skills/docx`](./skills/docx), [`skills/pdf`](./skills/pdf), [`skills/pptx`](./skills/pptx), and [`skills/xlsx`](./skills/xlsx) subfolders. These are source-available, not open source, but we wanted to share these with developers as a reference for more complex skills that are actively used in a production AI application.

## Disclaimer

**These skills are provided for demonstration and educational purposes only.** While some of these capabilities may be available in Claude, the implementations and behaviors you receive from Claude may differ from what is shown in these skills. These skills are meant to illustrate patterns and possibilities. Always test skills thoroughly in your own environment before relying on them for critical tasks.

# Skill Sets
- [./skills](./skills): Skill examples for Creative & Design, Development & Technical, Enterprise & Communication, and Document Skills
- [./spec](./spec): The Agent Skills specification
- [./template](./template): Skill template

# Try in Claude Code, Claude.ai, and the API

## Claude Code
You can register this repository as a Claude Code Plugin marketplace by running the following command in Claude Code:
```
/plugin marketplace add anthropics/skills
```

Then, to install a specific set of skills:
1. Select `Browse and install plugins`
2. Select `anthropic-agent-skills`
3. Select `document-skills` or `example-skills`
4. Select `Install now`

Alternatively, directly install either Plugin via:
```
/plugin install document-skills@anthropic-agent-skills
/plugin install example-skills@anthropic-agent-skills
```

After installing the plugin, you can use the skill by just mentioning it. For instance, if you install the `document-skills` plugin from the marketplace, you can ask Claude Code to do something like: "Use the PDF skill to extract the form fields from `path/to/some-file.pdf`"

## Claude.ai

These example skills are all already available to paid plans in Claude.ai. 

To use any skill from this repository or upload custom skills, follow the instructions in [Using skills in Claude](https://support.claude.com/en/articles/12512180-using-skills-in-claude#h_a4222fa77b).

## Claude API

You can use Anthropic's pre-built skills, and upload custom skills, via the Claude API. See the [Skills API Quickstart](https://docs.claude.com/en/api/skills-guide#creating-a-skill) for more.

# Creating a Basic Skill

Skills are simple to create - just a folder with a `SKILL.md` file containing YAML frontmatter and instructions. You can use the **template-skill** in this repository as a starting point:

```markdown
---
name: my-skill-name
description: A clear description of what this skill does and when to use it
---

# My Skill Name

[Add your instructions here that Claude will follow when this skill is active]

## Examples
- Example usage 1
- Example usage 2

## Guidelines
- Guideline 1
- Guideline 2
```

The frontmatter requires only two fields:
- `name` - A unique identifier for your skill (lowercase, hyphens for spaces)
- `description` - A complete description of what the skill does and when to use it

The markdown content below contains the instructions, examples, and guidelines that Claude will follow. For more details, see [How to create custom skills](https://support.claude.com/en/articles/12512198-creating-custom-skills).

# Partner Skills

Skills are a great way to teach Claude how to get better at using specific pieces of software. As we see awesome example skills from partners, we may highlight some of them here:

- **Notion** - [Notion Skills for Claude](https://www.notion.so/notiondevs/Notion-Skills-for-Claude-28da4445d27180c7af1df7d8615723d0)


---

<!-- SVENKUNKKA-PROJECT-INFO:BEGIN -->

<a id="project-overview-zh"></a>
## 中文项目说明

[Anthropic 官方 Skills 仓库](https://github.com/anthropics/skills)的分支，收录 Claude 技能示例、Claude Code 插件、文档处理工具、技能模板及 Agent Skills 规范；原作者为 Anthropic 和各贡献者。

**使用入口：** 从 [skills](skills/)、[template](template/) 与 [spec](spec/) 浏览内容；README 提供 Claude Code、Claude.ai 及 API 的使用入口。

**范围说明：** 各技能许可证不同，文档技能属于源码可见，并非全部采用开源许可证；本分支也未必与上游最新版本同步。

<a id="project-overview-en"></a>
## English project overview

A fork of [Anthropic’s official Skills repository](https://github.com/anthropics/skills), containing Claude skill examples, Claude Code plugins, document tools, templates and the Agent Skills specification. Original authorship belongs to Anthropic and the respective contributors.

**Getting started:** Browse [skills](skills/), [template](template/) and [spec](spec/); the README explains access through Claude Code, Claude.ai and the API.

**Scope:** Licenses vary by skill. Document skills are source-available rather than all being open source, and this fork may lag behind upstream.

**本 Fork 的维护者 / Maintainer of this fork:** [SvenKunkka](https://github.com/SvenKunkka) · [X / Twitter](https://x.com/Svenu1s5)

**上游项目 / Upstream:** [anthropics/skills](https://github.com/anthropics/skills)。保留原作者署名与原许可证 / Original authorship and license notices are retained.

<!-- SVENKUNKKA-PROJECT-INFO:END -->
