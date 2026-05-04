# Visual Taste Lab

让 AI 先学会视觉身份，再开始写页面。  
Make AI understand visual identity before it starts writing webpages.

[Public Preview / 在线预览](https://siuserxiaowei.github.io/visual-taste-lab/) · [Skill File / Skill 文件](visual-taste-lab/SKILL.md)

## 中文介绍

Visual Taste Lab 是一个给 Codex / Claude Code 这类编程 Agent 使用的 UI/UX 审美 Skill。

它不是网页模板，也不是一句“做得高级一点”的提示词。它的目标是让 AI 在写页面之前，先完成一轮视觉身份判断：

- 这个品牌的 Logo / 字标给了什么视觉线索？
- 主色、辅色、强调色、中性色分别承担什么角色？
- 这个页面是公司官网、产品页、交易工具、内容品牌页，还是后台系统？
- 访客进入页面 5 秒内应该理解什么、相信什么？
- 页面最不应该像什么？

很多 AI 生成网页的问题，不是代码不能跑，而是太早开始写页面。Visual Taste Lab 把“审美”拆成可执行的步骤：先做 VI 审计，再提炼 design language，最后再进入页面和组件实现。

## 适合什么场景

- 公司官网改版
- 产品落地页
- 投资人页面
- 内容品牌页
- 作品集 / Portfolio
- 交易型工具页面
- 管理后台 / Dashboard
- 任何你觉得“功能能跑，但页面有 AI 味”的项目

## 工作流

1. **收集参考**  
   使用截图、URL、品牌名、现有页面或代码库作为输入。

2. **VI 审计**  
   识别 Logo、主色、辅色、强调色、字体气质、图像风格和组件形态。

3. **判断站点类型**  
   区分公司官网、产品页、交易工具、内容品牌页、后台系统等不同页面任务。

4. **提炼设计语言**  
   输出颜色、字号、间距、圆角、卡片、按钮、表格、CTA、图片气质和反模式。

5. **再开始改页面**  
   在明确的视觉规则里修改代码，而不是让 AI 临场发挥。

## 安装方式

把 `visual-taste-lab` 文件夹复制到你的 Skills 目录。

Codex:

```bash
cp -R visual-taste-lab ~/.codex/skills/
```

Claude Code 风格的本地 Skills 目录，如果你的环境支持：

```bash
cp -R visual-taste-lab ~/.claude/skills/
```

安装后，在对话里通过 `$visual-taste-lab` 调用。

## 使用示例

```text
/goal 使用 $visual-taste-lab 优化当前网站 UI/UX。

不要直接开始改页面。先做 VI 审计：
1. 识别 Logo / 字标及其视觉锚点
2. 判断主色、辅色、强调色、中性色和语义色
3. 判断站点类型：公司官网 / 产品页 / 交易工具 / 内容品牌 / 后台系统 / 其他
4. 说明访客 5 秒内应该理解什么、相信什么
5. 提炼 design language：颜色、字体、间距、圆角、按钮、卡片、表格、CTA、图片气质
6. 明确反模式：这个网站最不应该像什么

确认视觉语言后，再修改页面和组件。
要求：
- 不套通用模板
- 不编造客户、案例、数据
- 不把公司官网误做成产品页
- 保持移动端无横向溢出
- 修改后运行构建或测试
- 输出改动说明和下一步建议
```

## 文件结构

```text
visual-taste-lab/
├── SKILL.md
├── agents/
│   └── openai.yaml
└── references/
    ├── archetypes.md
    └── design-language-template.md
```

- `SKILL.md`：核心工作流、设计标准、反模式和输出要求。
- `references/archetypes.md`：不同站点类型对应的视觉原型。
- `references/design-language-template.md`：设计语言输出模板。
- `agents/openai.yaml`：Skill 在界面中的展示信息。

## 隐私说明

这个仓库里的 Demo 使用虚构品牌和通用场景，不包含客户资料、业务细节或私有项目素材。实际用于项目时，请先清理敏感信息，再把截图、URL 或代码库交给 AI 分析。

---

## English Introduction

Visual Taste Lab is a UI/UX design-language skill for Codex, Claude Code, and similar coding agents.

It is not a webpage template, and it is not a vague “make it look premium” prompt. Its purpose is to make an AI agent understand visual identity before it writes page code.

Before redesigning a page, the skill asks:

- What does the logo or wordmark suggest?
- What are the brand primary, secondary, accent, neutral, and semantic colors?
- Is this a company website, product page, transactional utility, content brand, dashboard, or portfolio?
- What should a visitor understand and trust within five seconds?
- What should this page definitely not look like?

Many AI-generated webpages are not broken. They just look generic because the agent starts designing too early. Visual Taste Lab turns “taste” into an executable workflow: audit the visual identity, distill a design language, then implement the page.

## Use Cases

- Company websites
- Product landing pages
- Investor pages
- Content brand sites
- Portfolios
- Transactional utility pages
- Dashboards and admin tools
- Any project where the UI works but still feels AI-generated

## Workflow

1. **Collect references**  
   Use screenshots, URLs, brand names, existing pages, or the current codebase.

2. **Run a VI audit**  
   Identify logo cues, primary colors, secondary colors, accent colors, typography, imagery, and component geometry.

3. **Classify the site type**  
   Separate company sites, product pages, transactional utilities, content brands, dashboards, and portfolios.

4. **Distill a design language**  
   Define colors, type scale, spacing, radius, cards, buttons, tables, CTAs, imagery, and anti-patterns.

5. **Implement after the system is clear**  
   Update pages and components inside a coherent visual system instead of letting the agent improvise module by module.

## Installation

Copy the `visual-taste-lab` folder into your local Skills directory.

For Codex:

```bash
cp -R visual-taste-lab ~/.codex/skills/
```

For Claude Code-style local Skills, if your environment supports it:

```bash
cp -R visual-taste-lab ~/.claude/skills/
```

Then invoke it in a task with `$visual-taste-lab`.

## Example Prompt

```text
/goal Use $visual-taste-lab to improve this project visually.

Do not redesign immediately. Start with a VI audit:
1. Identify the logo or wordmark and its visual anchor.
2. Identify or propose primary, secondary, accent, neutral, and semantic colors.
3. Classify the site type: company site, product page, transactional utility, content brand, dashboard, portfolio, or other.
4. Explain what visitors should understand and trust within five seconds.
5. Distill the design language: colors, typography, spacing, radius, buttons, cards, tables, CTAs, and imagery.
6. Define anti-patterns: what this website should not look like.

After that, update the relevant pages and components.
Requirements:
- Do not apply a generic template.
- Do not invent customers, case studies, or metrics.
- Do not turn a company website into a product landing page by accident.
- Keep mobile layouts free of horizontal overflow.
- Run build or tests when applicable.
- Summarize changes and recommended next steps.
```

## Repository Structure

```text
visual-taste-lab/
├── SKILL.md
├── agents/
│   └── openai.yaml
└── references/
    ├── archetypes.md
    └── design-language-template.md
```

- `SKILL.md`: Core workflow, design standards, anti-patterns, and output contract.
- `references/archetypes.md`: Visual archetypes for different site types.
- `references/design-language-template.md`: Template for the design-language output.
- `agents/openai.yaml`: Display metadata for the skill UI.

## Privacy Note

The public demo uses fictional brands and generic scenarios. It does not include real clients, real businesses, or private project materials. When applying this skill to real work, remove sensitive information before sharing screenshots, URLs, or code with an AI agent.
