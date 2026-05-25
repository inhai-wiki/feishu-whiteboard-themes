# 风格参数目录

每个风格包含 5 类参数：`palette`（配色）、`shape`（形状）、`typography`（字体）、`connector`（连线）、`decoration`（装饰）。直接复制对应参数到 SVG 代码中使用。

---

## 1. Vercel 极简 `vercel`

> 灵感：vercel.com — 工程师美学，零装饰，黑白灰为主

```yaml
palette:
  background: "#FAFAFA"
  card: "#FFFFFF"
  primary: "#000000"
  border: "#E5E5E5"
  text: "#000000"
  textSecondary: "#666666"
  textMuted: "#999999"
  accent: "#0070F3"        # Vercel 蓝，仅用于强调
shape:
  borderRadius: 0           # 零圆角
  borderWidth: 1
  shadow: none
typography:
  titleSize: 14
  titleWeight: 600
  bodySize: 13
  bodyWeight: 500
  labelSize: 10
  labelWeight: 500
  labelSpacing: 1           # letter-spacing: 1px
  labelCase: uppercase
connector:
  color: "#E5E5E5"
  width: 1
  style: solid
decoration:
  gradients: false
  icons: minimal
  extraEmbellishment: false
```

---

## 2. Apple 简约 `apple`

> 灵感：apple.com — 大圆角、精致留白、SF Pro 风格

```yaml
palette:
  background: "#F5F5F7"
  card: "#FFFFFF"
  primary: "#1D1D1F"
  border: "#D2D2D7"
  text: "#1D1D1F"
  textSecondary: "#6E6E73"
  textMuted: "#AEAEB2"
  accent: "#0071E3"         # Apple 蓝
shape:
  borderRadius: 16          # 大圆角
  borderWidth: 0.5
  shadow: soft              # 用半透明叠加矩形模拟
typography:
  titleSize: 16
  titleWeight: 600
  bodySize: 14
  bodyWeight: 400
  labelSize: 11
  labelWeight: 500
  labelSpacing: 0
  labelCase: normal
connector:
  color: "#D2D2D7"
  width: 1.5
  style: solid
decoration:
  gradients: false
  icons: sf-style
  extraEmbellishment: subtle
```

---

## 3. Notion 文档 `notion`

> 灵感：notion.so — 超轻边框、内嵌文档感、极克制

```yaml
palette:
  background: "#FFFFFF"
  card: "#FFFFFF"
  primary: "#2383E2"        # Notion 蓝
  border: "#E8E8E8"
  text: "#37352F"
  textSecondary: "#787774"
  textMuted: "#B4B4B0"
  accent: "#2383E2"
shape:
  borderRadius: 4           # 微圆角
  borderWidth: 0.5
  shadow: none
typography:
  titleSize: 14
  titleWeight: 600
  bodySize: 13
  bodyWeight: 400
  labelSize: 11
  labelWeight: 500
  labelSpacing: 0
  labelCase: normal
connector:
  color: "#E8E8E8"
  width: 1
  style: solid
decoration:
  gradients: false
  icons: none
  extraEmbellishment: false
```

---

## 4. Figma 设计 `figma`

> 灵感：figma.com — 彩色标签头、网格系统、设计工具感

```yaml
palette:
  background: "#F5F5F5"
  card: "#FFFFFF"
  primary: "#0D99FF"        # Figma 蓝
  border: "#E5E5E5"
  text: "#2C2C2C"
  textSecondary: "#6B6B6B"
  textMuted: "#ABABAB"
  accent: "#A259FF"         # Figma 紫
  headerColors: ["#0D99FF", "#A259FF", "#F24E1E", "#0ACF83"]  # 蓝/紫/红/绿
shape:
  borderRadius: 8
  borderWidth: 1
  shadow: soft
typography:
  titleSize: 12
  titleWeight: 600
  bodySize: 14
  bodyWeight: 500
  labelSize: 11
  labelWeight: 500
  labelSpacing: 0
  labelCase: normal
connector:
  color: "#CCCCCC"
  width: 1.5
  style: solid
decoration:
  gradients: false
  icons: colored-dots
  extraEmbellishment: color-coding
```

---

## 5. Excalidraw 手绘 `excalidraw`

> 灵感：excalidraw.com — 手绘线条、随意温暖、白板协作

```yaml
palette:
  background: "#FFFFFF"     # 纯白画布
  card: "#FFF9C4"           # 便签黄
  primary: "#1B1B1B"
  border: "#1B1B1B"
  text: "#1B1B1B"
  textSecondary: "#5C5C5C"
  textMuted: "#9B9B9B"
  accent: "#6965DB"         # Excalidraw 紫
  noteColors: ["#FFF9C4", "#FFD8A8", "#D3EAE5", "#F5C6EC", "#C7ECEE"]
shape:
  borderRadius: 6           # 不规则手绘感
  borderWidth: 2
  borderStyle: rough        # 用虚线/不规则 path 模拟
  shadow: none
typography:
  titleSize: 16
  titleWeight: 700          # 粗体手写感
  bodySize: 14
  bodyWeight: 400
  labelSize: 12
  labelWeight: 500
  labelSpacing: 0
  labelCase: normal
connector:
  color: "#1B1B1B"
  width: 1.5
  style: dashed             # 虚线模拟手绘
decoration:
  gradients: false
  icons: hand-drawn
  extraEmbellishment: sticky-notes
```

---

## 6. Miro 协作白板 `miro`

> 灵感：miro.com — 彩色便利贴、活泼、团队感

```yaml
palette:
  background: "#F5F5F0"
  card: "#FFFFFF"
  primary: "#FFD02F"        # Miro 黄
  border: "#E0E0E0"
  text: "#2D2D2D"
  textSecondary: "#6B6B6B"
  textMuted: "#A0A0A0"
  accent: "#FF6B6B"
  stickyColors: ["#FEF3C7", "#DBEAFE", "#FCE7F3", "#D1FAE5", "#EDE9FE", "#FEE2E2"]
shape:
  borderRadius: 4
  borderWidth: 1
  shadow: soft
typography:
  titleSize: 14
  titleWeight: 600
  bodySize: 13
  bodyWeight: 400
  labelSize: 11
  labelWeight: 500
  labelSpacing: 0
  labelCase: normal
connector:
  color: "#C4C4C4"
  width: 2
  style: solid
decoration:
  gradients: false
  icons: colored-emoji
  extraEmbellishment: sticky-notes
```

---

## 7. Material Design `material`

> 灵感：material.io — Google 设计语言、阴影层级

```yaml
palette:
  background: "#FAFAFA"
  card: "#FFFFFF"
  primary: "#6200EE"        # Material 紫
  border: "#E0E0E0"
  text: "#212121"
  textSecondary: "#757575"
  textMuted: "#BDBDBD"
  accent: "#03DAC6"         # Material 青
shape:
  borderRadius: 8
  borderWidth: 0
  shadow: elevation-1       # Material elevation 模拟
typography:
  titleSize: 16
  titleWeight: 500          # Medium
  bodySize: 14
  bodyWeight: 400
  labelSize: 12
  labelWeight: 400
  labelSpacing: 0.5
  labelCase: normal
connector:
  color: "#BDBDBD"
  width: 1.5
  style: solid
decoration:
  gradients: false
  icons: material-icons
  extraEmbellishment: ripple-effect
```

---

## 8. Ant Design 企业级 `ant-design`

> 灵感：ant.design — 阿里设计体系、专业蓝、规范严谨

```yaml
palette:
  background: "#F0F2F5"
  card: "#FFFFFF"
  primary: "#1677FF"        # Ant 蓝
  border: "#D9D9D9"
  text: "#000000E0"         # rgba(0,0,0,0.88)
  textSecondary: "#000000A0"
  textMuted: "#00000040"
  accent: "#1677FF"
shape:
  borderRadius: 8
  borderWidth: 1
  shadow: soft
typography:
  titleSize: 16
  titleWeight: 600
  bodySize: 14
  bodyWeight: 400
  labelSize: 12
  labelWeight: 400
  labelSpacing: 0
  labelCase: normal
connector:
  color: "#D9D9D9"
  width: 1.5
  style: solid
decoration:
  gradients: false
  icons: ant-icons
  extraEmbellishment: status-colors
```

---

## 9. GitHub 开发者 `github`

> 灵感：github.com — 深色代码感、等宽风、开发者友好

```yaml
palette:
  background: "#0D1117"
  card: "#161B22"
  primary: "#58A6FF"        # GitHub 蓝
  border: "#30363D"
  text: "#C9D1D9"
  textSecondary: "#8B949E"
  textMuted: "#6E7681"
  accent: "#3FB950"         # GitHub 绿
shape:
  borderRadius: 6
  borderWidth: 1
  shadow: none
typography:
  titleSize: 14
  titleWeight: 600
  bodySize: 13
  bodyWeight: 400
  labelSize: 11
  labelWeight: 500
  labelSpacing: 0.5
  labelCase: normal
connector:
  color: "#30363D"
  width: 1
  style: solid
decoration:
  gradients: false
  icons: octicons
  extraEmbellishment: code-blocks
```

---

## 10. Stripe 金融科技 `stripe`

> 灵感：stripe.com — 精致渐变、圆角、科技紫、高端感

```yaml
palette:
  background: "#F6F9FC"
  card: "#FFFFFF"
  primary: "#635BFF"        # Stripe 紫
  border: "#E3E8EE"
  text: "#1A1F36"
  textSecondary: "#697386"
  textMuted: "#A3ACB9"
  accent: "#635BFF"
shape:
  borderRadius: 12
  borderWidth: 1
  shadow: soft
typography:
  titleSize: 16
  titleWeight: 600
  bodySize: 14
  bodyWeight: 400
  labelSize: 11
  labelWeight: 500
  labelSpacing: 0.5
  labelCase: uppercase
connector:
  color: "#C1C9D2"
  width: 1.5
  style: solid
decoration:
  gradients: careful        # 谨慎使用 linearGradient
  icons: stripe-style
  extraEmbellishment: subtle-gradients
```

---

## 11. Linear 项目管理 `linear`

> 灵感：linear.app — 深色、紫色调、现代项目管理

```yaml
palette:
  background: "#0A0A0F"
  card: "#15151A"
  primary: "#5E6AD2"        # Linear 紫
  border: "#2A2A35"
  text: "#E2E2E8"
  textSecondary: "#8B8B96"
  textMuted: "#55555F"
  accent: "#5E6AD2"
shape:
  borderRadius: 8
  borderWidth: 1
  shadow: none
typography:
  titleSize: 14
  titleWeight: 500
  bodySize: 13
  bodyWeight: 400
  labelSize: 11
  labelWeight: 500
  labelSpacing: 0.5
  labelCase: normal
connector:
  color: "#2A2A35"
  width: 1
  style: solid
decoration:
  gradients: false
  icons: linear-icons
  extraEmbellishment: status-dots
```

---

## 12. Whimsical 清新 `whimsical`

> 灵感：whimsical.com — 柔和圆角、淡彩、轻松愉悦

```yaml
palette:
  background: "#F8F9FB"
  card: "#FFFFFF"
  primary: "#5B6BF0"        # Whimsical 紫
  border: "#E8EAF0"
  text: "#2D3142"
  textSecondary: "#73798C"
  textMuted: "#B0B5C4"
  accent: "#5B6BF0"
  softColors: ["#E8EAF8", "#E3F2FD", "#FFF3E0", "#E8F5E9", "#FCE4EC"]
shape:
  borderRadius: 12
  borderWidth: 1.5
  shadow: soft
typography:
  titleSize: 14
  titleWeight: 600
  bodySize: 13
  bodyWeight: 400
  labelSize: 11
  labelWeight: 500
  labelSpacing: 0
  labelCase: normal
connector:
  color: "#C8CCE0"
  width: 1.5
  style: solid
decoration:
  gradients: false
  icons: whimsical-style
  extraEmbellishment: soft-color-fill
```

---

## 13. Lucidchart 企业流程 `lucidchart`

> 灵感：lucidchart.com — 标准流程图、企业蓝灰

```yaml
palette:
  background: "#FFFFFF"
  card: "#FFFFFF"
  primary: "#2D6BE0"        # Lucidchart 蓝
  border: "#CCCCCC"
  text: "#333333"
  textSecondary: "#666666"
  textMuted: "#999999"
  accent: "#2D6BE0"
shape:
  borderRadius: 4
  borderWidth: 1.5
  shadow: none
typography:
  titleSize: 14
  titleWeight: 600
  bodySize: 12
  bodyWeight: 400
  labelSize: 10
  labelWeight: 400
  labelSpacing: 0
  labelCase: normal
connector:
  color: "#999999"
  width: 1.5
  style: solid
  arrows: true
decoration:
  gradients: false
  icons: standard
  extraEmbellishment: none
```

---

## 14. 深色模式 `dark-mode`

> 通用深色模式 — 深色背景、高对比、护眼

```yaml
palette:
  background: "#1E1E2E"     # Catppuccin Mocha 风格
  card: "#2A2A3C"
  primary: "#89B4FA"        # 淡蓝
  border: "#45475A"
  text: "#CDD6F4"
  textSecondary: "#A6ADC8"
  textMuted: "#6C7086"
  accent: "#CBA6F7"         # 淡紫
shape:
  borderRadius: 8
  borderWidth: 1
  shadow: none
typography:
  titleSize: 14
  titleWeight: 600
  bodySize: 13
  bodyWeight: 400
  labelSize: 11
  labelWeight: 500
  labelSpacing: 0
  labelCase: normal
connector:
  color: "#45475A"
  width: 1
  style: solid
decoration:
  gradients: false
  icons: light-on-dark
  extraEmbellishment: glow-edges
```

---

## 15. 赛博朋克 `neon`

> 灵感：赛博朋克 2077、Synthwave — 霓虹发光、未来感

```yaml
palette:
  background: "#0D0221"     # 深紫黑
  card: "#150734"
  primary: "#FF2A6D"        # 霓虹粉
  border: "#7B2FBE"
  text: "#05D9E8"           # 霓虹青
  textSecondary: "#D1F7FF"
  textMuted: "#7B2FBE"
  accent: "#05D9E8"         # 霓虹青
  neonColors: ["#FF2A6D", "#05D9E8", "#7B2FBE", "#D300C5"]
shape:
  borderRadius: 2
  borderWidth: 1.5
  shadow: glow              # 用叠加矩形模拟发光
typography:
  titleSize: 16
  titleWeight: 700
  bodySize: 13
  bodyWeight: 400
  labelSize: 11
  labelWeight: 600
  labelSpacing: 2
  labelCase: uppercase
connector:
  color: "#7B2FBE"
  width: 1.5
  style: solid
decoration:
  gradients: careful
  icons: futuristic
  extraEmbellishment: neon-glow-lines
```

---

## 16. 蓝图工程 `blueprint`

> 灵感：建筑蓝图、工程图纸 — 深蓝底、白色线条

```yaml
palette:
  background: "#0A3D7C"     # 蓝图蓝
  card: "#0E4A8F"
  primary: "#FFFFFF"
  border: "#6AADDE"
  text: "#FFFFFF"
  textSecondary: "#B8D8F0"
  textMuted: "#5A8EB0"
  accent: "#FFB347"         # 标注橙
shape:
  borderRadius: 0
  borderWidth: 1
  borderStyle: dashed       # 虚线框模拟工程线
  shadow: none
typography:
  titleSize: 14
  titleWeight: 600
  bodySize: 12
  bodyWeight: 400
  labelSize: 10
  labelWeight: 400
  labelSpacing: 1
  labelCase: uppercase
connector:
  color: "#6AADDE"
  width: 1
  style: dashed
decoration:
  gradients: false
  icons: technical
  extraEmbellishment: grid-lines
```

---

## 17. 马卡龙柔和 `pastel`

> 灵感：柔和水彩、马卡龙色系 — 温馨、可爱

```yaml
palette:
  background: "#FFF8F0"
  card: "#FFFFFF"
  primary: "#FFB5C2"        # 柔粉
  border: "#F0D9E0"
  text: "#5D4E60"
  textSecondary: "#8E7F92"
  textMuted: "#C0B4C4"
  accent: "#B5D8EB"         # 柔蓝
  pastelColors: ["#FFB5C2", "#B5D8EB", "#C4E6B0", "#FCE4A8", "#D4B5FF"]
shape:
  borderRadius: 16          # 超圆润
  borderWidth: 1.5
  shadow: soft
typography:
  titleSize: 14
  titleWeight: 600
  bodySize: 13
  bodyWeight: 400
  labelSize: 11
  labelWeight: 500
  labelSpacing: 0
  labelCase: normal
connector:
  color: "#E0D0D8"
  width: 1.5
  style: solid
decoration:
  gradients: false
  icons: rounded
  extraEmbellishment: soft-color-fill
```

---

## 18. 商务正式 `corporate`

> 灵感：咨询报告、企业年报 — 深蓝金配色、稳重

```yaml
palette:
  background: "#FFFFFF"
  card: "#FFFFFF"
  primary: "#003366"        # 深蓝
  border: "#CCCCCC"
  text: "#1A1A1A"
  textSecondary: "#666666"
  textMuted: "#999999"
  accent: "#C49A3C"         # 金色
shape:
  borderRadius: 4
  borderWidth: 1
  shadow: none
typography:
  titleSize: 16
  titleWeight: 700
  bodySize: 13
  bodyWeight: 400
  labelSize: 10
  labelWeight: 600
  labelSpacing: 1
  labelCase: uppercase
connector:
  color: "#CCCCCC"
  width: 1.5
  style: solid
decoration:
  gradients: false
  icons: formal
  extraEmbellishment: gold-accent-lines
```

---

## 19. 极简主义 `minimal`

> 灵感：Dieter Rams、MUJI — 最少元素、最大留白

```yaml
palette:
  background: "#FFFFFF"
  card: "#FFFFFF"
  primary: "#000000"
  border: "#E0E0E0"
  text: "#000000"
  textSecondary: "#888888"
  textMuted: "#CCCCCC"
  accent: "#000000"
shape:
  borderRadius: 0
  borderWidth: 0.5
  shadow: none
typography:
  titleSize: 12
  titleWeight: 600
  bodySize: 12
  bodyWeight: 400
  labelSize: 10
  labelWeight: 400
  labelSpacing: 0
  labelCase: normal
connector:
  color: "#E0E0E0"
  width: 0.5
  style: solid
decoration:
  gradients: false
  icons: none
  extraEmbellishment: none
```

---

## 20. 单色黑白 `monochrome`

> 灵感：报纸、印刷 — 纯黑白灰、无彩色

```yaml
palette:
  background: "#FFFFFF"
  card: "#F5F5F5"
  primary: "#000000"
  border: "#000000"
  text: "#000000"
  textSecondary: "#555555"
  textMuted: "#999999"
  accent: "#000000"
shape:
  borderRadius: 2
  borderWidth: 1.5
  shadow: none
typography:
  titleSize: 16
  titleWeight: 700
  bodySize: 13
  bodyWeight: 400
  labelSize: 10
  labelWeight: 700
  labelSpacing: 1
  labelCase: uppercase
connector:
  color: "#000000"
  width: 1
  style: solid
decoration:
  gradients: false
  icons: line-only
  extraEmbellishment: hatching
```

---

## 21. 等距 2.5D `isometric`

> 灵感：技术插画、信息图 — 等距投影、立体感

```yaml
palette:
  background: "#F0F4F8"
  card: "#FFFFFF"
  primary: "#4A90D9"
  border: "#B0C4DE"
  text: "#2C3E50"
  textSecondary: "#7F8C8D"
  textMuted: "#BDC3C7"
  accent: "#E74C3C"
  isoColors: ["#4A90D9", "#50C878", "#E74C3C", "#F5A623", "#9B59B6"]
shape:
  borderRadius: 2
  borderWidth: 1
  shadow: isometric         # 用平行四边形模拟 3D 效果
typography:
  titleSize: 14
  titleWeight: 600
  bodySize: 12
  bodyWeight: 400
  labelSize: 10
  labelWeight: 500
  labelSpacing: 0
  labelCase: normal
connector:
  color: "#B0C4DE"
  width: 1
  style: solid
decoration:
  gradients: careful
  icons: isometric-blocks
  extraEmbellishment: 3d-depth
```

---

## 22. 双色调 `duotone`

> 灵感：海报设计、Spotify Wrapped — 两色高对比

```yaml
palette:
  background: "#1A1A2E"     # 深色底
  card: "#16213E"
  primary: "#E94560"        # 红粉
  border: "#0F3460"
  text: "#E94560"
  textSecondary: "#F5F5F5"
  textMuted: "#0F3460"
  accent: "#E94560"
  duoColor: "#0F3460"       # 第二色：深蓝
shape:
  borderRadius: 4
  borderWidth: 2
  shadow: none
typography:
  titleSize: 18
  titleWeight: 800
  bodySize: 13
  bodyWeight: 400
  labelSize: 11
  labelWeight: 600
  labelSpacing: 2
  labelCase: uppercase
connector:
  color: "#0F3460"
  width: 2
  style: solid
decoration:
  gradients: careful        # 两色渐变
  icons: silhouettes
  extraEmbellishment: high-contrast
```

---

## 23. Claude Code `claude-code`

> 灵感：Anthropic Claude Code CLI — 暖橙棕色调、终端感、AI 原生

```yaml
palette:
  background: "#1C1917"       # 深棕黑（终端底色）
  card: "#292524"             # 深棕卡片
  primary: "#D97706"          # Claude 暖橙
  border: "#44403C"           # 石板棕边框
  text: "#FAFAF9"             # 暖白文字
  textSecondary: "#A8A29E"    # 暖灰
  textMuted: "#78716C"        # 暗暖灰
  accent: "#D97706"           # 橙色强调
  secondary: "#7C3AED"        # 紫色（Anthropic 品牌辅助）
shape:
  borderRadius: 8
  borderWidth: 1
  shadow: none
typography:
  titleSize: 14
  titleWeight: 600
  bodySize: 13
  bodyWeight: 400
  labelSize: 11
  labelWeight: 500
  labelSpacing: 0.5
  labelCase: normal
connector:
  color: "#44403C"
  width: 1
  style: solid
decoration:
  gradients: false
  icons: terminal-style
  extraEmbellishment: warm-terminal-glow
```

---

## 24. Google `google`

> 灵感：Google Material You — 四色品牌、圆润、友好

```yaml
palette:
  background: "#F8F9FA"
  card: "#FFFFFF"
  primary: "#1A73E8"          # Google 蓝
  border: "#DADCE0"
  text: "#202124"
  textSecondary: "#5F6368"
  textMuted: "#9AA0A6"
  accent: "#EA4335"           # Google 红
  brandColors: ["#4285F4", "#EA4335", "#FBBC04", "#34A853"]  # 蓝/红/黄/绿
shape:
  borderRadius: 12
  borderWidth: 1
  shadow: soft
typography:
  titleSize: 16
  titleWeight: 500
  bodySize: 14
  bodyWeight: 400
  labelSize: 12
  labelWeight: 500
  labelSpacing: 0
  labelCase: normal
connector:
  color: "#DADCE0"
  width: 1.5
  style: solid
decoration:
  gradients: false
  icons: google-style
  extraEmbellishment: four-color-accents
```

---

## 25. Microsoft `microsoft`

> 灵感：Microsoft Fluent Design — 四色方格、专业、清晰

```yaml
palette:
  background: "#F3F2F1"
  card: "#FFFFFF"
  primary: "#0078D4"          # Microsoft 蓝
  border: "#D2D0CE"
  text: "#323130"
  textSecondary: "#605E5C"
  textMuted: "#A19F9D"
  accent: "#0078D4"
  brandColors: ["#F25022", "#7FBA00", "#00A4EF", "#FFB900"]  # 红/绿/蓝/黄
shape:
  borderRadius: 4
  borderWidth: 1
  shadow: soft
typography:
  titleSize: 16
  titleWeight: 600
  bodySize: 14
  bodyWeight: 400
  labelSize: 12
  labelWeight: 400
  labelSpacing: 0
  labelCase: normal
connector:
  color: "#D2D0CE"
  width: 1.5
  style: solid
decoration:
  gradients: false
  icons: fluent-style
  extraEmbellishment: four-square-brand
```

---

## 26. Meta `meta`

> 灵感：Meta/Facebook — 渐变蓝、现代社交科技

```yaml
palette:
  background: "#F0F2F5"
  card: "#FFFFFF"
  primary: "#1877F2"          # Meta 蓝
  border: "#CED0D4"
  text: "#1C1E21"
  textSecondary: "#606770"
  textMuted: "#8A8D91"
  accent: "#1877F2"
  gradientColors: ["#0078FF", "#0066FF", "#0055FF"]  # 渐变蓝
shape:
  borderRadius: 12
  borderWidth: 0
  shadow: soft
typography:
  titleSize: 16
  titleWeight: 700
  bodySize: 14
  bodyWeight: 400
  labelSize: 12
  labelWeight: 500
  labelSpacing: 0
  labelCase: normal
connector:
  color: "#CED0D4"
  width: 1.5
  style: solid
decoration:
  gradients: careful          # 谨慎使用蓝色渐变
  icons: meta-style
  extraEmbellishment: gradient-headers
```

---

## 27. Amazon `amazon`

> 灵感：Amazon/AWS — 深蓝橙渐变、云计算、企业级

```yaml
palette:
  background: "#F2F3F3"
  card: "#FFFFFF"
  primary: "#232F3E"          # Amazon 深蓝
  border: "#D5DBDB"
  text: "#16191F"
  textSecondary: "#545B64"
  textMuted: "#879596"
  accent: "#FF9900"           # Amazon 橙
shape:
  borderRadius: 4
  borderWidth: 1
  shadow: soft
typography:
  titleSize: 16
  titleWeight: 700
  bodySize: 14
  bodyWeight: 400
  labelSize: 12
  labelWeight: 500
  labelSpacing: 0
  labelCase: normal
connector:
  color: "#D5DBDB"
  width: 1.5
  style: solid
decoration:
  gradients: false
  icons: aws-style
  extraEmbellishment: orange-underline
```

---

## 28. Netflix `netflix`

> 灵感：Netflix — 深黑红、电影感、沉浸式

```yaml
palette:
  background: "#141414"       # Netflix 黑
  card: "#1A1A1A"
  primary: "#E50914"          # Netflix 红
  border: "#333333"
  text: "#FFFFFF"
  textSecondary: "#B3B3B3"
  textMuted: "#666666"
  accent: "#E50914"
shape:
  borderRadius: 4
  borderWidth: 1
  shadow: none
typography:
  titleSize: 16
  titleWeight: 700
  bodySize: 14
  bodyWeight: 400
  labelSize: 11
  labelWeight: 600
  labelSpacing: 1
  labelCase: uppercase
connector:
  color: "#333333"
  width: 1.5
  style: solid
decoration:
  gradients: false
  icons: cinematic
  extraEmbellishment: red-accent-lines
```

---

## 29. Spotify `spotify`

> 灵感：Spotify — 深绿黑、活力绿、音乐感

```yaml
palette:
  background: "#121212"       # Spotify 深黑
  card: "#181818"
  primary: "#1DB954"          # Spotify 绿
  border: "#282828"
  text: "#FFFFFF"
  textSecondary: "#B3B3B3"
  textMuted: "#535353"
  accent: "#1DB954"
shape:
  borderRadius: 8
  borderWidth: 0
  shadow: none
typography:
  titleSize: 16
  titleWeight: 700
  bodySize: 14
  bodyWeight: 400
  labelSize: 11
  labelWeight: 500
  labelSpacing: 0
  labelCase: normal
connector:
  color: "#282828"
  width: 1.5
  style: solid
decoration:
  gradients: false
  icons: music-style
  extraEmbellishment: green-glow
```

---

## 30. Tesla `tesla`

> 灵感：Tesla — 极简黑白红、工程美学、未来汽车

```yaml
palette:
  background: "#FFFFFF"
  card: "#F5F5F5"
  primary: "#CC0000"          # Tesla 红
  border: "#E0E0E0"
  text: "#000000"
  textSecondary: "#666666"
  textMuted: "#999999"
  accent: "#CC0000"
shape:
  borderRadius: 2             # 几乎直角，工程感
  borderWidth: 1
  shadow: none
typography:
  titleSize: 14
  titleWeight: 700
  bodySize: 13
  bodyWeight: 400
  labelSize: 10
  labelWeight: 600
  labelSpacing: 2
  labelCase: uppercase
connector:
  color: "#E0E0E0"
  width: 1
  style: solid
decoration:
  gradients: false
  icons: engineering
  extraEmbellishment: red-detail-line
```

---

## 31. OpenAI `openai`

> 灵感：OpenAI — 柔和渐变、AI 前沿、理性优雅

```yaml
palette:
  background: "#FFFFFF"
  card: "#F7F7F8"
  primary: "#10A37F"          # OpenAI 绿
  border: "#E5E5E5"
  text: "#202123"
  textSecondary: "#6E6E80"
  textMuted: "#ACACBE"
  accent: "#10A37F"
  gradientColors: ["#10A37F", "#1A7F64", "#2D5E4E"]
shape:
  borderRadius: 12
  borderWidth: 1
  shadow: soft
typography:
  titleSize: 16
  titleWeight: 600
  bodySize: 14
  bodyWeight: 400
  labelSize: 11
  labelWeight: 500
  labelSpacing: 0
  labelCase: normal
connector:
  color: "#E5E5E5"
  width: 1
  style: solid
decoration:
  gradients: careful
  icons: minimal-ai
  extraEmbellishment: green-gradient-headers
```

---

## 32. ByteDance `bytedance`

> 灵感：字节跳动/TikTok — 黑白粉青、短视频活力

```yaml
palette:
  background: "#000000"
  card: "#161823"
  primary: "#FE2C55"          # TikTok 粉红
  border: "#2F3142"
  text: "#FFFFFF"
  textSecondary: "#A0A0B0"
  textMuted: "#4E4F60"
  accent: "#25F4EE"           # TikTok 青
  brandColors: ["#FE2C55", "#25F4EE", "#FFFFFF"]  # 粉/青/白
shape:
  borderRadius: 6
  borderWidth: 1
  shadow: none
typography:
  titleSize: 16
  titleWeight: 700
  bodySize: 14
  bodyWeight: 400
  labelSize: 11
  labelWeight: 600
  labelSpacing: 0
  labelCase: normal
connector:
  color: "#2F3142"
  width: 1.5
  style: solid
decoration:
  gradients: false
  icons: tiktok-style
  extraEmbellishment: pink-cyan-dual
```

---

## 混合定制示例

### Vercel + 蓝色主题
```yaml
# 基础: vercel
# 修改: palette.primary → "#0070F3", palette.accent → "#0050CC"
# 其余保持 vercel 参数
```

### Notion + 深色模式
```yaml
# 布局: notion（微圆角、超轻边框）
# 配色: dark-mode 的 palette
# 字体: notion 的 typography
```

### Excalidraw + 专业配色
```yaml
# 形状: excalidraw（手绘线条、虚线边框）
# 配色: 色系改为 ant-design 的专业蓝
# 连线: excalidraw 的 dashed 改为 solid
```
