# 图标语义映射与风格渲染策略

当生成 SVG 节点时，根据节点文本语义自动匹配 FontAwesome 图标，并根据当前风格的 `decoration.icons` 策略决定图标的渲染方式。

---

## 一、语义关键词 → FontAwesome 图标映射

根据节点标题/标签中的关键词，自动匹配对应的 FontAwesome 6 Free Solid 图标。匹配时优先匹配更具体的关键词（如"Redis"优先于"数据库"）。

### 人员与角色

| 语义关键词 | FA Unicode | 渲染示例 |
|---|---|---|
| 用户、客户、Customer、User | `&#xf007;` |  |
| 团队、部门、Group、Team | `&#xf0c0;` |  |
| 管理员、Admin | `&#xf505;` |  |
| 开发者、工程师、Developer、Engineer | `&#xf121;` |  |
| 产品经理、PM | `&#xf3ed;` |  |
| 设计师、Designer | `&#xf1fc;` |  |
| CEO、领导、Director | `&#xf507;` |  |
| HR、人事、Recruiter | `&#xf0b1;` |  |

### 基础设施与计算

| 语义关键词 | FA Unicode | 渲染示例 |
|---|---|---|
| 数据库、Database、DB、MySQL、PostgreSQL、Redis、MongoDB | `&#xf1c0;` |  |
| 服务器、Server | `&#xf233;` |  |
| 云、Cloud、AWS、阿里云、腾讯云 | `&#xf0c2;` |  |
| 容器、Docker、Container、K8s、Kubernetes | `&#xf434;` |  |
| 网络、Network、CDN | `&#xf6ff;` |  |
| 存储、Storage、OSS、S3 | `&#xf1c1;` |  |
| 防火墙、Firewall | `&#xf132;` |  |
| 负载均衡、Load Balancer、LB | `&#xf0e8;` |  |
| 缓存、Cache | `&#xf017;` |  |

### 通信与交互

| 语义关键词 | FA Unicode | 渲染示例 |
|---|---|---|
| 邮件、Email、Mail | `&#xf0e0;` |  |
| 消息、聊天、Chat、Message | `&#xf075;` |  |
| 通知、Notification、Alert | `&#xf0f3;` |  |
| 电话、Phone、Call | `&#xf095;` |  |
| API、接口、Endpoint | `&#xf13b;` |  |
| Webhook | `&#xf0c1;` |  |
| 推送、Push | `&#xf10d;` |  |

### 数据与分析

| 语义关键词 | FA Unicode | 渲染示例 |
|---|---|---|
| 图表、Chart、报表 | `&#xf080;` |  |
| 分析、Analytics、BI | `&#xf201;` |  |
| 仪表盘、Dashboard | `&#xf3fd;` |  |
| 搜索、Search | `&#xf002;` |  |
| 日志、Log | `&#xf15c;` |  |
| 监控、Monitor | `&#xf26c;` |  |
| 指标、Metrics | `&#xf200;` |  |

### 开发与部署

| 语义关键词 | FA Unicode | 渲染示例 |
|---|---|---|
| 代码、Code、Git | `&#xf121;` |  |
| 构建、Build、CI | `&#xf1b3;` |  |
| 部署、Deploy、CD | `&#xf135;` |  |
| 测试、Test | `&#xf492;` |  |
| Bug、缺陷 | `&#xf188;` |  |
| 配置、Config、Settings | `&#xf013;` |  |
| 环境、Environment | `&#xf0ac;` |  |
| 版本、Version、Release | `&#xf1d8;` |  |
| 分支、Branch | `&#xf126;` |  |
| 合并、Merge | `&#xf0c5;` |  |

### 安全与认证

| 语义关键词 | FA Unicode | 渲染示例 |
|---|---|---|
| 安全、Security、安全组 | `&#xf132;` |  |
| 锁、Lock、加密 | `&#xf023;` |  |
| 密钥、Key、Token | `&#xf084;` |  |
| 认证、Auth、登录、Login | `&#xf2f6;` |  |
| 权限、Permission、RBAC | `&#xf505;` |  |
| 证书、Certificate、SSL | `&#xf0a3;` |  |

### 业务与流程

| 语义关键词 | FA Unicode | 渲染示例 |
|---|---|---|
| 订单、Order | `&#xf0d6;` |  |
| 支付、Payment | `&#xf09d;` |  |
| 退款、Refund | `&#xf3e5;` |  |
| 库存、Inventory | `&#xf498;` |  |
| 审批、Approve | `&#xf058;` |  |
| 签约、Contract | `&#xf15b;` |  |
| 营销、Marketing | `&#xf0a1;` |  |
| 运营、Operation | `&#xf085;` |  |

### AI 与智能

| 语义关键词 | FA Unicode | 渲染示例 |
|---|---|---|
| AI、智能、Intelligence | `&#xf544;` |  |
| 模型、Model、LLM、GPT | `&#xf538;` |  |
| 训练、Training | `&#xf6e2;` |  |
| 推理、Inference | `&#xf0eb;` |  |
| 数据集、Dataset | `&#xf1c0;` |  |
| 向量、Embedding | `&#xf1ec;` |  |
| Prompt、提示词 | `&#xf075;` |  |

### 通用功能

| 语义关键词 | FA Unicode | 渲染示例 |
|---|---|---|
| 首页、Home | `&#xf015;` |  |
| 设置、Settings | `&#xf013;` |  |
| 文件、File | `&#xf15b;` |  |
| 文件夹、Folder | `&#xf07b;` |  |
| 日历、Calendar、Schedule | `&#xf073;` |  |
| 时钟、Time、Duration | `&#xf017;` |  |
| 位置、Location | `&#xf3c5;` |  |
| 链接、Link、URL | `&#xf0c1;` |  |
| 图片、Image、Photo | `&#xf03e;` |  |
| 视频、Video | `&#xf03d;` |  |
| 音频、Audio、Music | `&#xf001;` |  |
| 标签、Tag | `&#xf02c;` |  |
| 书签、Bookmark | `&#xf02e;` |  |
| 星标、Star | `&#xf005;` |  |
| 心、Heart、Like | `&#xf004;` |  |
| 下载、Download | `&#xf019;` |  |
| 上传、Upload | `&#xf093;` |  |
| 分享、Share | `&#xf1e0;` |  |
| 复制、Copy | `&#xf0c5;` |  |
| 删除、Delete、Trash | `&#xf1f8;` |  |
| 编辑、Edit | `&#xf044;` |  |
| 添加、Add、New | `&#xf067;` |  |
| 搜索、Search | `&#xf002;` |  |
| 过滤、Filter | `&#xf0b0;` |  |
| 排序、Sort | `&#xf0dc;` |  |

### 状态指示

| 语义关键词 | FA Unicode | 渲染示例 |
|---|---|---|
| 成功、Success、完成、Done | `&#xf058;` |  |
| 失败、Error、错误 | `&#xf057;` |  |
| 警告、Warning | `&#xf071;` |  |
| 信息、Info | `&#xf05a;` |  |
| 进行中、Running、Loading | `&#xf110;` |  |
| 暂停、Pause | `&#xf04c;` |  |
| 停止、Stop | `&#xf04d;` |  |
| 待处理、Pending | `&#xf017;` |  |
| 问号、Unknown | `&#xf059;` |  |

---

## 二、图标风格渲染策略

每个风格的 `decoration.icons` 值对应不同的图标渲染方式。在生成 SVG 时，按以下策略控制图标的外观。

### 策略定义

| icons 值 | 所属风格 | 渲染策略 |
|---|---|---|
| `none` | `notion`、`minimal` | **不使用图标**。节点只包含文字，不加任何图标元素 |
| `minimal` | `vercel` | **极简线条图标**。尺寸 12px，颜色取 `palette.textSecondary`，无填充，仅线条 |
| `sf-style` | `apple` | **圆润清晰**。尺寸 14px，颜色取 `palette.textSecondary`，圆角感，精致细腻 |
| `colored-dots` | `figma` | **彩色圆点替代图标**。用 8px 彩色圆形 `<circle>` 替代，颜色从 `headerColors` 数组轮转取值 |
| `hand-drawn` | `excalidraw` | **手绘风格**。尺寸 16px，颜色取 `palette.text`，用 FA 图标但配合手绘边框风格 |
| `colored-emoji` | `miro` | **彩色活泼**。尺寸 16px，使用 `palette.accent` 或 `stickyColors` 轮转着色，醒目突出 |
| `material-icons` | `material` | **Material 风格**。尺寸 16px，颜色取 `palette.primary`，填充式图标 |
| `ant-icons` | `ant-design` | **专业克制**。尺寸 14px，颜色取 `palette.primary`，线条式，统一蓝色系 |
| `octicons` | `github` | **GitHub 小型图标**。尺寸 12px，颜色取 `palette.textSecondary`，紧凑简洁 |
| `stripe-style` | `stripe` | **精致现代**。尺寸 14px，颜色取 `palette.accent`，带轻微装饰感 |
| `linear-icons` | `linear` | **暗色极简**。尺寸 12px，颜色取 `palette.textSecondary`，深色背景上低对比度 |
| `whimsical-style` | `whimsical` | **柔和圆润**。尺寸 14px，颜色从 `softColors` 轮转，圆润亲切 |
| `standard` | `lucidchart` | **标准企业**。尺寸 14px，颜色取 `palette.textSecondary`，中规中矩 |
| `light-on-dark` | `dark-mode` | **暗底亮色**。尺寸 14px，颜色取 `palette.primary`（淡色），确保深色背景可读 |
| `futuristic` | `neon` | **霓虹发光**。尺寸 16px，颜色从 `neonColors` 轮转，用叠加矩形模拟发光效果 |
| `technical` | `blueprint` | **蓝图技术**。尺寸 14px，颜色取 `palette.border`（浅蓝），白色线条风格 |
| `rounded` | `pastel` | **圆润柔和**。尺寸 14px，颜色从 `pastelColors` 轮转，温暖可爱 |
| `formal` | `corporate` | **正式克制**。尺寸 12px，颜色取 `palette.accent`（金色），小而精致 |
| `line-only` | `monochrome` | **纯线条**。尺寸 14px，颜色取 `palette.text`，无填充 |
| `isometric-blocks` | `isometric` | **3D 方块替代**。用倾斜 `<rect>` 模拟 3D 图标，颜色从 `isoColors` 取值 |
| `silhouettes` | `duotone` | **双色剪影**。尺寸 14px，颜色取 `palette.primary`（主色）和 `duoColor`（副色）双色填充 |
| `terminal-style` | `claude-code` | **终端风格**。尺寸 14px，颜色取 `palette.accent`（暖橙），等宽字体感 |
| `google-style` | `google` | **品牌四色**。尺寸 14px，颜色从 `brandColors` 轮转，活泼多彩 |
| `fluent-style` | `microsoft` | **Fluent 简洁**。尺寸 14px，颜色取 `palette.accent`，专业蓝色系 |
| `meta-style` | `meta` | **社交蓝**。尺寸 14px，颜色取 `palette.primary`（渐变蓝），现代社交感 |
| `aws-style` | `amazon` | **云服务**。尺寸 14px，颜色取 `palette.accent`（橙色），云计算主题 |
| `cinematic` | `netflix` | **电影感**。尺寸 14px，颜色取 `palette.accent`（红色），戏剧化 |
| `music-style` | `spotify` | **音乐感**。尺寸 14px，颜色取 `palette.accent`（绿色），活力 |
| `engineering` | `tesla` | **工程精密**。尺寸 12px，颜色取 `palette.textSecondary`，极简克制 |
| `minimal-ai` | `openai` | **AI 优雅**。尺寸 14px，颜色取 `palette.accent`（柔和绿），理性克制 |
| `tiktok-style` | `bytedance` | **双色活力**。尺寸 16px，颜色从 `brandColors` 轮转（粉/青/白），年轻活力 |

### 颜色轮转规则

当策略中提到"从数组轮转取值"时，按节点在图表中出现的顺序依次取颜色数组中的值，循环使用：

```
nodes[0] → colors[0]
nodes[1] → colors[1]
...
nodes[n] → colors[n % colors.length]
```

---

## 三、SVG 图标注入模板

### 基本结构

每个包含图标的节点，其内部 SVG 结构为：

```xml
<g transform="translate(X, Y)">
  <!-- 图标区域 -->
  <text font-family="'Font Awesome 6 Free'" font-weight="900"
        font-size="ICON_SIZE" fill="ICON_COLOR"
        x="PADDING" y="ICON_BASELINE">&#xf0e0;</text>
  <!-- 文字区域（图标右侧偏移） -->
  <text font-family="sans-serif" font-size="TEXT_SIZE" font-weight="TEXT_WEIGHT"
        fill="TEXT_COLOR" x="ICON_X + ICON_SIZE + GAP" y="TEXT_BASELINE">节点标题</text>
</g>
```

### 尺寸与间距规则

| 参数 | 计算方式 |
|---|---|
| `ICON_SIZE` | 取策略表中的尺寸值 |
| `ICON_COLOR` | 取策略表中的颜色值 |
| `ICON_BASELINE` | 节点垂直居中 + `ICON_SIZE × 0.35` |
| `ICON_X` | 节点左内边距，通常为 `8~12` |
| `GAP` | 图标与文字间距，通常为 `6~8` |
| `TEXT_BASELINE` | 与 `ICON_BASELINE` 对齐 |

### colored-dots 模板（Figma 风格）

用彩色圆点替代 FA 图标：

```xml
<circle cx="CX" cy="CY" r="4" fill="COLOR_FROM_HEADER_COLORS" />
```

### isometric-blocks 模板（等距风格）

用倾斜矩形模拟 3D 图标：

```xml
<polygon points="X,Y X+10,Y-5 X+20,Y X+10,Y+5" fill="COLOR_FROM_ISO_COLORS" opacity="0.8" />
```

### silhouettes 模板（双色调）

用两个叠加的 FA 图标模拟双色：

```xml
<!-- 副色层（偏移 1px 模拟阴影） -->
<text font-family="'Font Awesome 6 Free'" font-weight="900"
      font-size="14" fill="DUO_COLOR" x="X+1" y="BASELINE+1">&#xf007;</text>
<!-- 主色层 -->
<text font-family="'Font Awesome 6 Free'" font-weight="900"
      font-size="14" fill="PRIMARY_COLOR" x="X" y="BASELINE">&#xf007;</text>
```

### futuristic 模板（霓虹发光）

用叠加矩形模拟发光效果：

```xml
<!-- 发光层（大尺寸、半透明、偏移） -->
<text font-family="'Font Awesome 6 Free'" font-weight="900"
      font-size="18" fill="NEON_COLOR" opacity="0.3" x="X-1" y="BASELINE-1">&#xf007;</text>
<!-- 主图标 -->
<text font-family="'Font Awesome 6 Free'" font-weight="900"
      font-size="16" fill="NEON_COLOR" x="X" y="BASELINE">&#xf007;</text>
```

---

## 四、图标注入决策流程

生成 SVG 节点时，按以下流程决定是否注入图标：

```
1. 检查 decoration.icons 值
   ├─ "none" → 跳过，不注入图标
   └─ 其他值 → 继续

2. 检查节点文本是否匹配语义关键词
   ├─ 匹配成功 → 使用匹配的 FA Unicode
   └─ 无匹配 → 不注入图标（保持纯文字节点）

3. 根据 icons 策略值确定渲染参数
   ├─ 从策略表取 SIZE 和 COLOR 规则
   └─ 计算颜色（固定色 or 轮转色 or 调色板取值）

4. 选择对应的 SVG 注入模板
   ├─ 通用模板 → 大部分风格
   ├─ colored-dots → figma
   ├─ isometric-blocks → isometric
   ├─ silhouettes → duotone
   └─ futuristic → neon

5. 将图标元素插入节点 SVG 中
   └─ 调整文字位置，为图标腾出空间
```

### 何时必须注入图标

- **技术架构图**：每个组件节点都应尝试匹配图标
- **流程图**：关键处理节点（审批、发送、存储等）应有图标
- **组织架构图**：人员节点应有用户图标

### 何时可以省略图标

- **思维导图**：叶子节点如果语义泛化（如"其他"、"备注"），可不加图标
- **数据图表**（饼图、柱状图）：这类图表本身不适合注入图标
- **甘特图/时间线**：里程碑节点可加图标，普通时间条不加
