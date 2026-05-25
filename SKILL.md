---
name: feishu-whiteboard-themes
version: 1.0.0
description: "飞书画板主题库：为 SVG/DSL 画板提供 32 种视觉风格模板，根据图表类型和用户场景自动推荐最佳风格。当用户画图时提到风格、设计语言、品牌风格、或要求美化/优化画板视觉时触发。"
---

# 飞书画板主题库

为飞书画板 SVG/DSL 创作提供可复用的视觉风格系统。覆盖 32 种风格，从极简到华丽，从商务到技术，一键切换。

## 触发时机

当以下任一条件满足时，主动读取本 skill 并应用：

1. 用户画图时指定了风格（"用 Vercel 风格"、"画个 Excalidraw 风格的"）
2. 用户提到品牌名（Notion、Figma、Apple 等）作为设计参考
3. 用户要求"美化"、"优化"、"换风格"、"好看一点"
4. 用户提供了参考截图要求复刻风格
5. 你在创建 SVG/DSL 画板时需要决定视觉风格

## 工作流

### Step 1：确定风格

按优先级从高到低判断使用哪个风格：

| 优先级 | 判断依据 | 示例 |
|---|---|---|
| 1 | 用户直接指定风格名 | "用 Vercel 风格" |
| 2 | 用户提到品牌关键词 | "Notion 那种感觉"、"Apple 风格" |
| 3 | 用户给了参考图 | 发截图说"类似这个" |
| 4 | 根据图表类型+场景自动推荐 | 见 `references/scene-style-mapping.md` |
| 5 | 默认风格 | `vercel`（极简专业） |

**风格匹配关键词表**（不区分中英文、大小写）：

| 关键词 | 风格 ID |
|---|---|
| vercel, Vercel, 维尔塞尔 | `vercel` |
| apple, 苹果, Apple | `apple` |
| notion, Notion, 诺申 | `notion` |
| figma, Figma, 菲格玛 | `figma` |
| excalidraw, Excalidraw, 手绘, 涂鸦, sketch | `excalidraw` |
| miro, Miro, 米罗, 白板 | `miro` |
| material, Material Design, 谷歌, Google | `material` |
| ant, Ant Design, 蚂蚁, 阿里 | `ant-design` |
| github, GitHub, 代码, 开发者 | `github` |
| stripe, Stripe, 支付, 渐变 | `stripe` |
| linear, Linear, 项目管理, 深色 | `linear` |
| whisk, whimsical, Whimsical, 清新 | `whimsical` |
| lucid, lucidchart, 企业, 流程 | `lucidchart` |
| dark, 暗黑, 深色, 夜间 | `dark-mode` |
| neon, 赛博, 赛博朋克, 发光, cyberpunk | `neon` |
| blueprint, 蓝图, 工程图, 建筑 | `blueprint` |
| pastel, 马卡龙, 柔和, 淡彩 | `pastel` |
| corporate, 商务, 公司, 正式 | `corporate` |
| minimal, 极简, 简约 | `minimal` |
| mono, 单色, 黑白 | `monochrome` |
| isometric, 等距, 2.5D, 立体 | `isometric` |
| duotone, 双色, 双色调 | `duotone` |
| claude, claude-code, Claude Code, anthropic | `claude-code` |
| google, 谷歌, Google | `google` |
| microsoft, 微软, Microsoft | `microsoft` |
| meta, facebook, Meta, Facebook, 脸书 | `meta` |
| amazon, aws, 亚马逊, Amazon | `amazon` |
| netflix, 奈飞, Netflix | `netflix` |
| spotify, Spotify, 声田 | `spotify` |
| tesla, Tesla, 特斯拉 | `tesla` |
| openai, chatgpt, OpenAI, GPT | `openai` |
| bytedance, tiktok, 字节, 抖音, TikTok | `bytedance` |

### Step 2：读取风格参数

从 `references/style-catalog.md` 中找到对应风格，提取以下参数应用到 SVG 代码中：

- **配色方案**（`palette`）：主色、背景色、边框色、文字色、强调色
- **形状参数**（`shape`）：圆角 `rx`、边框宽度、阴影
- **字体规范**（`typography`）：字号层级、字重、字间距、大小写
- **连线风格**（`connector`）：颜色、宽度、虚线/实线
- **装饰规则**（`decoration`）：是否允许渐变、图标风格、额外点缀

### Step 3：应用到 SVG/DSL

在写 SVG 代码时，严格使用 Step 2 提取的参数替换以下默认值：

```
背景填充 → palette.background
节点填充 → palette.card / palette.primary
文字颜色 → palette.text / palette.textSecondary / palette.textMuted
边框颜色 → palette.border
连线颜色 → connector.color
圆角半径 → shape.borderRadius
边框宽度 → shape.borderWidth
标题字重 → typography.titleWeight
正文字号 → typography.bodySize
```

**重要约束**（来自飞书画板限制）：
- 禁止使用 `<radialGradient>`、`<filter>`、`<pattern>`、`<clipPath>`、`<mask>`
- 线性渐变 `<linearGradient>` 可谨慎使用（确保画板兼容）
- 阴影效果用叠加半透明矩形模拟，不用 `<filter>`
- 文字必须用 `<text>`，不用 `<path>`

**图标使用**：
- 如需在节点中添加图标，使用 [FontAwesome](https://fontawesome.com/) 图标库
- 在 SVG 的 `<style>` 中通过 CDN 引入：
  ```xml
  @import url('https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.1/css/all.min.css');
  ```
- 图标用 `<text>` 元素渲染 FontAwesome 字体图标：
  ```xml
  <text font-family="'Font Awesome 6 Free'" font-weight="900" font-size="14" fill="#666">&#xf0e0;</text>
  ```
- 常用图标 Unicode：用户 `` (`&#xf007;`)、齿轮 `` (`&#xf013;`)、邮件 `` (`&#xf0e0;`)、数据库 `` (`&#xf1c0;`)、云端 `` (`&#xf0c2;`)、图表 `` (`&#xf080;`)

### Step 4：混合与定制

用户可以在基础风格上叠加定制：

- "Vercel 风格但用蓝色主题" → 用 vercel 的布局规则，但 `palette.primary` 改为蓝色系
- "Excalidraw 风格但要专业感" → 用 excalidraw 的手绘线条，但配色改深色系
- "Notion 风格 + 深色模式" → 用 notion 的布局 + dark-mode 的配色

## 与 lark-whiteboard skill 的协作

本 skill 是 `lark-whiteboard` 的**辅助 skill**，不替代其渲染流程。协作方式：

1. `lark-whiteboard` 负责画板创建、渲染、上传
2. 本 skill（`feishu-whiteboard-themes`）负责在 SVG/DSL 写入阶段提供视觉参数
3. 当本 skill 被触发时，同时读取 `lark-whiteboard` 的 `routes/svg.md` 确保不违反画板限制

## 风格一览

| # | 风格 ID | 名称 | 一句话描述 |
|---|---|---|---|
| 1 | `vercel` | Vercel 极简 | 黑白灰、零圆角、大写标签、工程师美学 |
| 2 | `apple` | Apple 简约 | 大圆角、毛玻璃感、SF 风格、精致留白 |
| 3 | `notion` | Notion 文档 | 超轻边框、小圆角、文档内嵌感、克制裁剪 |
| 4 | `figma` | Figma 设计 | 圆角卡片、彩色标签、网格系统、设计工具感 |
| 5 | `excalidraw` | Excalidraw 手绘 | 手绘线条、随意感、暖色调、白板协作感 |
| 6 | `miro` | Miro 协作白板 | 彩色便利贴、活泼配色、团队协作氛围 |
| 7 | `material` | Material Design | 谷歌设计语言、阴影层级、Material 色板 |
| 8 | `ant-design` | Ant Design 企业级 | 阿里设计体系、专业蓝、清晰层级 |
| 9 | `github` | GitHub 开发者 | 深色代码感、等宽字体风格、Green/Blue |
| 10 | `stripe` | Stripe 金融科技 | 精致渐变、圆角、科技紫、高端感 |
| 11 | `linear` | Linear 项目管理 | 深色背景、紫色调、现代项目管理感 |
| 12 | `whimsical` | Whimsical 清新 | 柔和圆角、淡彩配色、轻松愉悦 |
| 13 | `lucidchart` | Lucidchart 企业流程 | 标准流程图、蓝灰配色、企业级专业 |
| 14 | `dark-mode` | 深色模式 | 深色背景、高对比文字、护眼 |
| 15 | `neon` | 赛博朋克 | 深色底、霓虹发光色、未来感 |
| 16 | `blueprint` | 蓝图工程 | 深蓝底色、白色线条、工程图纸感 |
| 17 | `pastel` | 马卡龙柔和 | 柔和淡彩、圆润形状、温馨感 |
| 18 | `corporate` | 商务正式 | 深蓝金配色、稳重专业、正式场合 |
| 19 | `minimal` | 极简主义 | 白底、最少元素、最大留白 |
| 20 | `monochrome` | 单色黑白 | 纯黑白、无彩色、印刷感 |
| 21 | `isometric` | 等距 2.5D | 等距投影、立体感、技术插画 |
| 22 | `duotone` | 双色调 | 两色配色、高对比、海报感 |
| 23 | `claude-code` | Claude Code | 暖橙棕终端感、AI 原生 |
| 24 | `google` | Google | 四色品牌、Material You |
| 25 | `microsoft` | Microsoft | Fluent Design、专业四色方格 |
| 26 | `meta` | Meta/Facebook | 渐变蓝、现代社交科技 |
| 27 | `amazon` | Amazon/AWS | 深蓝橙、云计算企业级 |
| 28 | `netflix` | Netflix | 深黑红、电影感、沉浸式 |
| 29 | `spotify` | Spotify | 深绿黑、活力绿、音乐感 |
| 30 | `tesla` | Tesla | 极简黑白红、工程美学 |
| 31 | `openai` | OpenAI | 柔和绿、AI 前沿、理性优雅 |
| 32 | `bytedance` | ByteDance/TikTok | 黑白粉青、短视频活力 |

详细参数见 `references/style-catalog.md`。

## 参考文件

- [`references/style-catalog.md`](references/style-catalog.md) — 完整风格参数库（配色、形状、字体、连线）
- [`references/scene-style-mapping.md`](references/scene-style-mapping.md) — 图表类型 × 场景 × 推荐风格映射
