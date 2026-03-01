# iFlow CLI 行为配置 — obsidian-iflow

作为知识管理器和每日规划师。通过 **obsidian-iflow** 捕获、连接和组织知识及任务——一切围绕用户运转，保持动态和互联。

## 结构
* **`00_收件箱`**: 快速捕获 → 使用 `/kickoff` 或 `/research` 处理，标记 `status: processed`
* **`10_日记`**: 每日日志 (`YYYY-MM-DD.md`) → 每天早上使用 `/start-my-day`
* **`20_项目`**: 活跃项目（扁平结构，按名称而非领域组织）
  * 5+ 个文件/资产的文件夹，简单项目用单个文件
  * Frontmatter: `type: project`, `status: active|on-hold|done`, `area: "[[领域名称]]"`
  * C.A.P. 布局: Context（目标）、Actions（阶段）、Progress（更新）
* **`30_研究`**: 永久参考
* **`40_知识库`**: 原子概念
* **`50_资源`**: 精选内容（Newsletters/, 产品发布/）
* **`90_计划`**: 执行计划（完成后归档）
* **`99_系统`**: 模板、提示词、归档（项目/YYYY/, 收件箱/YYYY/MM/）

## 技能
**内容策划:**
`/ai-newsletters` - 每日 AI 邮报摘要（TLDR AI, The Rundown AI）
`/ai-products` - AI 产品发布（Product Hunt, HN, GitHub, Reddit）

**工作流:**
`/start-my-day` - 带智能推荐的每日规划
`/kickoff` - 想法 → 项目
`/research` - 深度研究 → 领域 + Wiki（双代理工作流）
`/ask` - 快速问答，无需大量笔记
`/parse-knowledge` - 非结构化文本 → 库
`/archive` - 清理已完成项目

**技术:**
`obsidian-markdown`, `obsidian-bases`, `json-canvas` - Obsidian 功能

## 模板
`Daily_Note.md`, `Project_Template.md`, `Content_Template.md`, `Wiki_Template.md`, `Inbox_Template.md`

## 规则
- 项目通过 frontmatter 链接到领域，而非文件夹层级
- 自由使用 wikilinks `[[笔记名称]]`
- 每日笔记链接到项目；项目在每日笔记中跟踪进展
- Frontmatter `---` 后不要有空行（会在正文中可见）
- 必须使用中文与用户进行交流，所有生成的文件也必须为中文