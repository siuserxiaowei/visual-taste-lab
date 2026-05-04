# Visual Taste Lab

让 AI 先学会视觉身份，再开始写页面。  
Make AI understand visual identity before it starts writing webpages.

[Public Preview / 在线预览](https://siuserxiaowei.github.io/visual-taste-lab/) · [Skill File / Skill 文件](visual-taste-lab/SKILL.md) · [Examples / 示例](examples/)

## What It Is / 它是什么

Visual Taste Lab is a UI/UX design-language skill for Codex, Claude Code, and similar coding agents. It helps an agent pause before implementation, read the visual identity, classify the page type, and turn taste into reusable design rules.

Visual Taste Lab 是一个面向 Codex、Claude Code 等编程 Agent 的 UI/UX 审美 Skill。它让 Agent 在动手改页面前，先理解视觉身份、判断页面类型，并把“审美要求”转成可复用的设计语言。

It is not a template, theme pack, or one-line prompt like “make it premium.” The output should be a design direction the agent can apply across typography, color, spacing, surfaces, buttons, cards, forms, tables, imagery, and motion.

它不是网页模板、主题包，也不是一句“做得高级一点”的提示词。它希望产出的，是一套能落到字体、颜色、间距、界面表面、按钮、卡片、表单、表格、图片和动效里的视觉规则。

## Why / 为什么

AI-generated webpages often fail visually because the agent starts drawing screens before it understands the brand system. Visual Taste Lab makes the first step explicit:

AI 生成页面经常“不坏，但很模板化”，原因通常不是代码能力不足，而是 Agent 太早开始画页面。Visual Taste Lab 把第一步拆清楚：

- What visual cues already exist in the logo, wordmark, product, or references?
- Which colors are primary, secondary, accent, neutral, and semantic?
- Is the project a company site, product landing page, transactional utility, content site, dashboard, portfolio, or something else?
- What should a visitor understand and trust within five seconds?
- What should this interface definitely not look like?

- Logo、字标、产品或参考图里已经有哪些视觉线索？
- 主色、辅色、强调色、中性色和语义色分别是什么角色？
- 项目到底是公司官网、产品落地页、交易工具、内容站、后台、作品集，还是其他类型？
- 访客进入页面 5 秒内应该理解什么、相信什么？
- 这个界面最不应该像什么？

## Install / 安装

Clone or download this repository, then copy the skill folder into your local Skills directory.

克隆或下载本仓库，然后把 skill 文件夹复制到本地 Skills 目录。

For Codex:

```bash
cp -R visual-taste-lab ~/.codex/skills/
```

For Claude Code-style local Skills, if your environment supports it:

```bash
cp -R visual-taste-lab ~/.claude/skills/
```

Then invoke it in a task with `$visual-taste-lab`.

安装后，在对话里通过 `$visual-taste-lab` 调用。

## Usage / 使用方式

Use it when you want the agent to improve visual quality without drifting into a generic template.

当你希望 Agent 提升界面质感，但又不想套用通用模板时，可以这样调用：

```text
/goal Use $visual-taste-lab to improve this project visually.

Do not redesign immediately. First run a VI audit, classify the site type,
distill a design language, and only then update the relevant pages/components.

Constraints:
- Do not invent customers, case studies, or metrics.
- Do not delete unrelated files.
- Keep mobile layouts free of horizontal overflow.
- Run build or tests when applicable.
- Summarize changes and recommended next steps.
```

More copyable prompts are available in [examples/goal-prompts.md](examples/goal-prompts.md).

更多可复制 prompt 见 [examples/goal-prompts.md](examples/goal-prompts.md)。

## Workflow / 工作流

1. **Collect references / 收集参考**

   Use screenshots, URLs, brand names, existing pages, or the current codebase.

2. **Run a VI audit / 进行 VI 审计**

   Identify logo cues, color roles, typography, imagery style, and component geometry.

3. **Classify the project / 判断项目类型**

   Separate company sites, product pages, utilities, content sites, dashboards, portfolios, and other page types.

4. **Distill a design language / 提炼设计语言**

   Define color roles, type scale, spacing, radius, surfaces, cards, buttons, tables, CTAs, imagery, motion, and anti-patterns.

5. **Implement system-first / 先落系统，再改页面**

   Update shared tokens and components before polishing isolated sections.

6. **Verify / 验证**

   Build or test the project, check desktop and mobile layouts, and keep claims honest.

## Examples / 示例

- [Goal prompts / 目标 prompt](examples/goal-prompts.md): 6 copyable prompts for common UI improvement tasks.
- [Design language sample / 设计语言样例](examples/design-language-sample.md): a fictional output showing the kind of direction the skill can produce.

## Repository Structure / 仓库结构

```text
visual-taste-lab/
├── SKILL.md
├── agents/
│   └── openai.yaml
└── references/
    ├── archetypes.md
    └── design-language-template.md
```

- `SKILL.md`: core workflow, design standards, anti-patterns, and output contract.
- `references/archetypes.md`: visual archetypes for different site types.
- `references/design-language-template.md`: template for the design-language output.
- `agents/openai.yaml`: display metadata for the skill UI.

- `SKILL.md`：核心工作流、设计标准、反模式和输出要求。
- `references/archetypes.md`：不同站点类型对应的视觉原型。
- `references/design-language-template.md`：设计语言输出模板。
- `agents/openai.yaml`：Skill 在界面中的展示信息。

## Privacy / 隐私

This repository uses fictional examples and generic scenarios. It should not contain private project materials, confidential screenshots, customer data, internal metrics, or non-public strategy notes.

本仓库只使用虚构示例和通用场景，不应包含私有项目素材、保密截图、客户数据、内部指标或未公开策略记录。

When using the skill on your own work, remove sensitive information before sharing screenshots, URLs, documents, or code with an AI agent.

实际项目中使用时，请先清理敏感信息，再把截图、URL、文档或代码交给 AI Agent 分析。

## Links / 链接

- Public preview / 在线预览: [siuserxiaowei.github.io/visual-taste-lab](https://siuserxiaowei.github.io/visual-taste-lab/)
- Skill entry / Skill 入口: [visual-taste-lab/SKILL.md](visual-taste-lab/SKILL.md)
- Archetypes / 视觉原型: [visual-taste-lab/references/archetypes.md](visual-taste-lab/references/archetypes.md)
- Design language template / 设计语言模板: [visual-taste-lab/references/design-language-template.md](visual-taste-lab/references/design-language-template.md)

## License / 许可证

MIT. See [LICENSE](LICENSE).
