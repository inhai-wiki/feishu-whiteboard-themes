# 图表类型 × 场景 × 推荐风格映射

当用户没有指定风格时，根据图表类型和使用场景自动推荐最合适的风格。

## 映射表

| 图表类型 | 场景 | 推荐风格（优先级排序） | 理由 |
|---|---|---|---|
| **组织架构图** | 公司内部分享 | `vercel` > `ant-design` > `corporate` | 专业清晰、层级分明 |
| **组织架构图** | 对外展示/汇报 | `corporate` > `apple` > `stripe` | 正式稳重、有品牌感 |
| **组织架构图** | 团队轻松分享 | `whimsical` > `miro` > `excalidraw` | 轻松愉悦、协作氛围 |
| **技术架构图** | 技术文档/内部 | `github` > `vercel` > `dark-mode` | 开发者友好、代码感 |
| **技术架构图** | 对外演示 | `stripe` > `linear` > `figma` | 科技感、精致 |
| **技术架构图** | 3D/云架构 | `isometric` > `blueprint` > `dark-mode` | 立体感、工程感 |
| **流程图** | 业务流程 | `lucidchart` > `ant-design` > `notion` | 标准规范、清晰可读 |
| **流程图** | 产品流程 | `figma` > `whimsical` > `vercel` | 设计友好、现代感 |
| **流程图** | 开发者工作流 | `github` > `vercel` > `linear` | 代码感、简洁 |
| **思维导图** | 头脑风暴 | `excalidraw` > `miro` > `whimsical` | 自由随性、激发创意 |
| **思维导图** | 会议记录 | `notion` > `whimsical` > `miro` | 干净、易归档 |
| **思维导图** | 学习笔记 | `notion` > `pastel` > `minimal` | 轻松、易阅读 |
| **甘特图/时间线** | 项目管理 | `linear` > `ant-design` > `vercel` | 专业 PM 工具感 |
| **甘特图/时间线** | 产品路线图 | `stripe` > `apple` > `figma` | 精致、科技感 |
| **对比图** | 方案对比 | `figma` > `vercel` > `duotone` | 彩色区分、对比鲜明 |
| **对比图** | 竞品分析 | `corporate` > `duotone` > `dark-mode` | 正式、高对比 |
| **饼图/数据图** | 数据报告 | `corporate` > `figma` > `stripe` | 专业、可信 |
| **饼图/数据图** | 团队分享 | `figma` > `whimsical` > `pastel` | 活泼、易理解 |
| **鱼骨图** | 根因分析 | `lucidchart` > `notion` > `vercel` | 结构清晰、理性 |
| **泳道图** | 跨部门流程 | `lucidchart` > `ant-design` > `figma` | 规范、角色清晰 |
| **漏斗图** | 转化/销售 | `stripe` > `figma` > `duotone` | 商业感、渐变美感 |
| **金字塔图** | 层级结构 | `corporate` > `duotone` > `dark-mode` | 稳重、层级感强 |
| **飞轮图** | 增长模型 | `stripe` > `linear` > `figma` | 科技感、动感 |
| **里程碑图** | 版本规划 | `github` > `linear` > `vercel` | 开发者、版本感 |

## 特殊场景

| 场景 | 推荐风格 | 说明 |
|---|---|---|
| 暗色 PPT/汇报 | `dark-mode` / `linear` | 深色背景适合大屏展示 |
| 创意提案 | `neon` / `duotone` | 视觉冲击力强 |
| 打印/PDF | `monochrome` / `corporate` | 黑白打印友好 |
| 教育/培训 | `pastel` / `whimsical` | 温和友好、降低紧张感 |
| 工程/建筑 | `blueprint` / `isometric` | 技术感、专业感 |
| 演讲/大会 | `apple` / `stripe` | 精致高端、品牌感 |

## 用户画像匹配

| 用户类型 | 默认推荐 | 原因 |
|---|---|---|
| 工程师/开发者 | `vercel` / `github` | 简洁、代码感、高效 |
| 设计师 | `figma` / `apple` | 精致、设计工具熟悉感 |
| 产品经理 | `linear` / `figma` | 现代 PM 工具感 |
| 管理层/高管 | `corporate` / `apple` | 正式、专业、品牌感 |
| 教师/学生 | `notion` / `pastel` | 简洁、温和、易读 |
| 销售/市场 | `stripe` / `miro` | 科技感、活泼 |
