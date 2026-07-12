# 一楼墙面防潮防水综合治理方案 - Design Spec

> Human-readable design narrative — rationale, audience, style, color choices, content outline. 
> Machine-readable execution contract: `spec_lock.md`.

## I. Project Information

| Item | Value |
| ---- | ----- |
| **Project Name** | 一楼墙面防潮防水综合治理方案 |
| **Canvas Format** | PPT 16:9 (1280×720) |
| **Page Count** | 10 pages |
| **Design Style** | A) General Versatile + 清爽工程风（Clean Construction） |
| **Target Audience** | 业主 / 装修师傅 / DIY 爱好者 |
| **Use Case** | 家庭装修参考、施工指导、方案汇报 |
| **Created Date** | 2026-07-03 |

---

## II. Canvas Specification

| Property | Value |
| -------- | ----- |
| **Format** | PPT 16:9 |
| **Dimensions** | 1280×720px |
| **viewBox** | `0 0 1280 720` |
| **Margins** | left/right 60px, top 50px, bottom 40px |
| **Content Area** | 1160×630px (from 60,50) |

---

## III. Visual Theme

### Theme Style

- **Style**: A) General Versatile + 清爽工程风
- **Theme**: Light theme
- **Tone**: 专业、清晰、值得信赖 — 工程感但不冰冷，亲和但不随意

### Color Scheme

| Role | HEX | Purpose |
| ---- | --- | ------- |
| **Background** | `#FFFFFF` | 页面主背景 |
| **Secondary bg** | `#F0F4F8` | 卡片背景、区块背景 |
| **Primary** | `#0D4F8B` | 标题装饰、重点区块、图标 |
| **Accent** | `#E8612C` | 数据高亮、关键信息、警示标记 |
| **Secondary accent** | `#0891B2` | 渐变过渡、辅助高亮 |
| **Body text** | `#1A1A2E` | 主文本 |
| **Secondary text** | `#5B6E7D` | 标注、说明 |
| **Border/divider** | `#D0D8E0` | 卡片边框、分割线 |
| **Success** | `#0D8C5E` | 正面指标 |
| **Warning** | `#E8612C` | 警示标记（复用 Accent） |

### AI Image Strategy

- **Image Rendering**: `vector-illustration`
- **Image Palette**: `cool-corporate`

### Gradient Scheme

```xml
<!-- Title gradient -->
<linearGradient id="titleGradient" x1="0%" y1="0%" x2="100%" y2="100%">
  <stop offset="0%" stop-color="#0D4F8B"/>
  <stop offset="100%" stop-color="#0891B2"/>
</linearGradient>

<!-- Background decorative gradient -->
<radialGradient id="bgDecor" cx="85%" cy="15%" r="45%">
  <stop offset="0%" stop-color="#0D4F8B" stop-opacity="0.08"/>
  <stop offset="100%" stop-color="#0D4F8B" stop-opacity="0"/>
</radialGradient>

<!-- Card hover / accent gradient -->
<linearGradient id="accentBar" x1="0%" y1="0%" x2="0%" y2="100%">
  <stop offset="0%" stop-color="#E8612C"/>
  <stop offset="100%" stop-color="#0D4F8B"/>
</linearGradient>
```

---

## IV. Typography System

### Font Plan

**Typography direction**: 现代 CJK 无衬线 — 统一、清晰、工程气质

| Role | Chinese | English | Fallback tail |
| ---- | ------- | ------- | ------------- |
| **Title** | `"Microsoft YaHei", "PingFang SC"` | `Arial` | `sans-serif` |
| **Body** | `"Microsoft YaHei", "PingFang SC"` | `Arial` | `sans-serif` |
| **Emphasis** | `"Microsoft YaHei", "PingFang SC"` | `Georgia` | `serif` |
| **Code** | — | `Consolas, "Courier New"` | `monospace` |

**Per-role font stacks**:

- Title: `"Microsoft YaHei", "PingFang SC", Arial, sans-serif`
- Body: `"Microsoft YaHei", "PingFang SC", Arial, sans-serif`
- Emphasis: `Georgia, "Microsoft YaHei", serif` (数字/价格/关键数据使用衬线体强调)
- Code: `Consolas, "Courier New", monospace`

### Font Size Hierarchy

**Baseline**: Body font size = 20px (中等密度，兼顾文字说明和材料表格)

| Purpose | Ratio to body | Value @ body=20 | Weight |
| ------- | ------------- | --------------- | ------ |
| Cover title (hero headline) | 2.5-5x | 56-72px | Bold |
| Chapter / section opener | 2-2.5x | 40-48px | Bold |
| Page title | 1.5-2x | 30-36px | Bold |
| Hero number (KPIs) | 1.5-2x | 30-40px | Bold |
| Subtitle | 1.2-1.5x | 24-28px | SemiBold |
| **Body content** | **1x** | **20px** | Regular |
| Annotation / caption | 0.7-0.85x | 14-16px | Regular |
| Page number / footnote | 0.5-0.65x | 10-12px | Regular |

---

## V. Layout Principles

### Page Structure

- **Header area**: 页标题区，top 50px，高度 ~60px，包含装饰色条 + 标题文字
- **Content area**: 从 y≈120 到 y≈670，高度 ~550px
- **Footer area**: 底部 40px，页码 + 项目名

### Layout Pattern Library

| Pattern | Suitable Scenarios |
| ------- | ----------------- |
| **Single column centered** | 封面 (P01)、结尾 (P10) |
| **Symmetric split (5:5)** | 方案对比 (P03) |
| **Top-bottom split** | 流程步骤 + 底部说明 |
| **Three/four column cards** | 辅助措施 (P09)、品牌推荐 (P08) |
| **Full-bleed + floating text** | 封面全幅背景 |
| **Negative-space-driven** | 结尾总结页 |

### Spacing Specification

**Universal**:

| Element | Value |
| ------- | ----- |
| Safe margin from canvas edge | 60px |
| Content block gap | 32px |
| Icon-text gap | 12px |

**Card-based layouts**:

| Element | Value |
| ------- | ----- |
| Card gap | 24px |
| Card padding | 24px |
| Card border radius | 12px |
| Three-column card width | ~360px each |

---

## VI. Icon Usage Specification

### Source

- **Built-in icon library**: `chunk-filled` — 填充风格，直线几何，厚重扎实，适合工程建筑主题
- **Usage method**: SVG placeholder `<use data-icon="chunk-filled/icon-name" .../>`

### Recommended Icon List

| Purpose | Icon Path | Page |
| ------- | --------- | ---- |
| 房屋/家 | `chunk-filled/home` | P01, P10 |
| 防水保护 | `chunk-filled/shield-check` | P03, P10 |
| 水滴/防水 | `chunk-filled/droplet` | P02, P04, P05 |
| 施工工具 | `chunk-filled/toolbox` | P04, P05 |
| 涂刷 | `chunk-filled/paint-roller` | P05, P07 |
| 外墙建筑 | `chunk-filled/building` | P04 |
| 检查清单 | `chunk-filled/clipboard` | P02, P05 |
| 材料表格 | `chunk-filled/table` | P06 |
| 预算 | `chunk-filled/dollar` | P08 |
| 提示 | `chunk-filled/lightbulb` | P09 |
| 完成确认 | `chunk-filled/badge-check` | P05, P10 |
| 图层结构 | `chunk-filled/layers` | P03, P07 |
| 信息 | `chunk-filled/circle-info` | P09 |
| 警告 | `chunk-filled/triangle-exclamation` | P09 |
| 步骤1-7 | `chunk-filled/circle-number-1` ~ `circle-number-7` | P05 |
| 搜索/诊断 | `chunk-filled/search` | P02 |

---

## VII. Visualization Reference List

Catalog read: 71 templates

| Page | Template | Path | Summary-quote (verbatim) | Usage |
| ---- | -------- | ---- | ------------------------ | ----- |
| P04 | numbered_steps | `templates/charts/numbered_steps.svg` | "Pick for 3-6 horizontal sequential steps with numeric emphasis — how-it-works section, getting-started guide, methodology overview, implementation phases. Skip if steps need connector arrows (use process_flow) or named output artifacts (use pipeline_with_stages)." | 外墙防水3步施工流程 |
| P05 | numbered_steps | `templates/charts/numbered_steps.svg` | "Pick for 3-6 horizontal sequential steps with numeric emphasis — how-it-works section, getting-started guide, methodology overview, implementation phases. Skip if steps need connector arrows (use process_flow) or named output artifacts (use pipeline_with_stages)." | 内墙防水7步施工流程 |
| P06 | basic_table | `templates/charts/basic_table.svg` | "Pick for plain tabular text/number grid, 3-8 columns. Skip if cells need visual bars (use consulting_table) or qualitative scores (use harvey_balls_table)." | 材料清单与用量表 |

**Runners-up considered**:

- `process_flow` | rejected for P04/P05: 施工步骤不需要箭头连接，强调独立步骤编号
- `comparison_table` | rejected for P06: 材料表是清单而非功能对比
- `vertical_list` | rejected for P05: 7步流程更适合水平编号步骤展示

---

## VIII. Image Resource List

| Filename | Dimensions | Ratio | Purpose | Type | Layout pattern | Acquire Via | Status | Reference | text_policy | page_role |
| -------- | --------- | ----- | ------- | ---- | -------------- | ----------- | ------ | --------- | ----------- | --------- |
| cover_bg.png | 1280×720 | 1.78 | 封面全幅背景——防水涂料施工场景氛围图，画面中央区域留白用于标题叠加 | Background | #1 full-bleed background with floating title + #29 two-stop scrim | ai | Pending | Professional waterproofing construction scene with clean composition; worker applying coating on exterior wall with roller; calm sky-blue and white tones; central area kept quiet for title overlay | none | hero_page |
| wall_layers.png | 1280×720 | 1.78 | 墙面防水层次结构示意图——展示从基层到面层的7层防水体系 | Diagram | #44 background image + native network/architecture diagram | ai | Pending | Cross-section diagram of a wall showing multiple waterproofing layers from base to surface; clean architectural style; layers clearly differentiated by subtle color variations; labels to be overlaid as SVG text | none | local |

---

## IX. Content Outline

### Part 1: 封面与诊断

#### Slide 01 - 封面

- **Layout**: Full-screen background image (cover_bg.png) + centered title with gradient scrim
- **Title**: 一楼墙面防潮防水综合治理方案
- **Subtitle**: 内外兼治 · 一步到位 · 告别返潮发霉
- **Info**: 2026年7月 · 家庭装修实用指南

#### Slide 02 - 问题诊断：你家墙面是哪种潮湿？

- **Layout**: 2×2 四象限卡片布局
- **Title**: 先诊断，再施工 — 四种墙面潮湿类型
- **Content**:
  - 左上卡片（地下毛细渗透）：墙根30cm内起皮、鼓包、黑绿色霉斑 → 图标 droplet
  - 右上卡片（冷凝结露）：全墙挂水珠、梅雨季加重 → 图标 search
  - 左下卡片（外墙渗漏）：雨天加重、有水流痕迹 → 图标 building
  - 右下卡片（管道串水）：厨卫相邻墙、管道附近 → 图标 wrench
- **Takeaway**: 一楼墙面通常是「毛细渗透 + 冷凝结露」叠加，需综合治理

### Part 2: 方案详解

#### Slide 03 - 方案总览：内外兼治双方案

- **Layout**: 左右对称分栏（5:5）— 左：方案二（外墙优先），右：方案一（内墙跟进）
- **Title**: 治水之道：先外后内，双管齐下
- **Content**:
  - 左栏（方案二 — 外墙正水面防水）：
    - ① 清洁修补 → ② 丙烯酸弹性涂料 → ③ 墙角加强
    - 耗时约1-2天 | 优先级：★★★
  - 右栏（方案一 — 内墙背水面综合治理）：
    - 铲除→杀菌→封闭→防水→腻子→底漆→面漆 七步流程
    - 耗时约5-7天 | 优先级：★★☆
- **Visualization**: 双列对比，中间竖线分隔

#### Slide 04 - 方案二：外墙正水面防水（3步）

- **Layout**: 水平三步骤编号 + 每步详细说明卡片
- **Title**: 方案二：外墙正水面防水 — 优先执行
- **Visualization**: numbered_steps (3步)
- **Content**:
  - 步骤1：清洁外墙表面 + 修补裂缝（高压水枪冲洗 / 水泥砂浆填补裂缝）
  - 步骤2：涂刷丙烯酸弹性防水涂料 2遍（间隔4-6小时，覆盖率3-5㎡/kg）
  - 步骤3：墙角与地面交接处加强处理（向上翻起20-30cm）
- **Callout**: ⚠ 外墙处理好后再做内墙，等于白做！

#### Slide 05 - 方案一：内墙背水面综合治理（7步）

- **Layout**: 水平七步骤编号（紧凑排列）+ 底部关键要诀
- **Title**: 方案一：内墙背水面综合治理 — 七步到位
- **Visualization**: numbered_steps (7步)
- **Content**:
  - ① 铲除霉变层（超出霉变区30cm）
  - ② 杀菌消毒（84消毒液1:10湿敷10-15分钟）
  - ③ 基层封闭（防水型墙固封闭毛细孔）
  - ④ 防水层（渗透结晶防水涂料2遍+养护48h）
  - ⑤ 腻子层（N型耐水腻子2遍，间隔24h）
  - ⑥ 底漆（抗碱防潮底漆1遍）
  - ⑦ 面漆（防霉乳胶漆/无机涂料2遍）
- **Callout**: 🔑 关键：必须用N型水泥基耐水腻子（JG/T 298-2010），普通腻子=白做！

### Part 3: 材料与预算

#### Slide 06 - 材料清单与用量详表

- **Layout**: 全宽表格 + 表头上方标题
- **Title**: 材料清单与用量（按100㎡墙面计算）
- **Visualization**: basic_table
- **Content**:
  - 8行材料：84消毒液 / 防水型墙固 / 渗透结晶防水涂料 / N型耐水腻子 / 抗碱防潮底漆 / 防霉乳胶漆 / 丙烯酸弹性防水涂料(外墙) / 外墙透明防水胶(备选)
  - 列：材料名称 | 用量(100㎡) | 用法要诀 | 参考品牌 | 京东搜索关键词
- **Annotation**: 以上为材料费估算，人工费另计。建议京东/天猫品牌旗舰店购买

#### Slide 07 - 关键材料用法详解

- **Layout**: 三列卡片（每列一个关键材料）
- **Title**: 三大关键材料 · 用法详解
- **Content**:
  - 卡片1：水泥基渗透结晶防水涂料 — 粉:水≈1:0.3搅拌 / 横竖交叉2遍 / 总厚≥1.5mm / 养护48h
  - 卡片2：N型水泥基耐水腻子 — 认准JG/T 298-2010 N型 / 粉:水≈1:0.35 / 批刮2遍 / 每遍1-2mm
  - 卡片3：丙烯酸弹性防水涂料(外墙) — 开桶即用 / 辊涂2遍 / 间隔4-6h / 覆盖率3-5㎡/kg
- **Callout**: 京东搜索对应关键词即可找到品牌旗舰店正品

#### Slide 08 - 预算估算与品牌推荐

- **Layout**: 左：费用饼图分区 + 右：品牌推荐表
- **Title**: 预算估算与品牌推荐
- **Content**:
  - 材料费总计：约 2,500-4,000 元（100㎡墙面）
  - 分项估算：外墙材料 800-1,500元 / 内墙基层处理 500-800元 / 防水涂料 600-1,000元 / 腻子+漆面 600-1,200元
  - 品牌推荐：东方雨虹 / 德高K11 / 科顺 / 青龙（防水涂料）；美巢 / 德高（耐水腻子）；多乐士 / 立邦（乳胶漆）
- **Callout**: 💡 人工费约材料费的1-1.5倍，总计预算约5,000-10,000元

### Part 4: 辅助与总结

#### Slide 09 - 辅助配套措施 + 避坑清单

- **Layout**: 左：辅助措施（3列图标卡片）+ 右：避坑清单
- **Title**: 辅助配套 + 避坑清单
- **Content**:
  - 辅助措施（3卡片）：
    - 除湿机 — 湿度>65%开启，南方一楼必备
    - 通风策略 — 晴天中午大通风 / 阴雨天紧闭门窗
    - 家具摆放 — 离墙5-10cm留通风间隙
  - 避坑清单（5条）：
    - ❌ 返潮墙面直接刷漆覆盖 → ✅ 先铲除→杀菌→防水→再刷
    - ❌ 用普通石膏基腻子 → ✅ 必须N型水泥基耐水腻子
    - ❌ 只刷表面防水涂料 → ✅ 必须先做渗透型防水
    - ❌ 回南天开窗通风 → ✅ 紧闭门窗+开除湿机
    - ❌ 不处理外墙只做内墙 → ✅ 外墙优先→内墙配合
- **Visualization**: icon_grid (辅助措施) + vertical_list (避坑清单)

#### Slide 10 - 结尾总结

- **Layout**: 居中单列 + 背景装饰渐变
- **Title**: 一楼防潮防水 · 核心要点
- **Content**:
  - 🏠 诊断先行：搞清楚潮湿类型再动手
  - 🧱 先外后内：外墙防水优先，内墙跟进配合
  - 🔑 材料关键：N型耐水腻子是底线，渗透结晶是核心
  - 💡 习惯辅助：除湿机 + 正确通风 + 家具离墙
  - 一句话：好的防水是系统工程，不是一瓶涂料能解决的
- **Footer**: 祝施工顺利！墙面干爽，家更舒适 🏠

---

## X. Speaker Notes Requirements

One speaker note file per page, saved to `notes/`:

- **Filename**: match SVG name (e.g., `01_cover.md`)
- **Content**: script key points, timing cues, transition phrases
- **Style**: 口语化讲稿，每页1-2段，总时长约8-10分钟
- **Language**: 中文

---

## XI. Technical Constraints Reminder

### SVG Generation Must Follow:

1. viewBox: `0 0 1280 720`
2. Background uses `<rect>` elements
3. Text wrapping uses `<tspan>` (`<foreignObject>` FORBIDDEN)
4. Transparency uses `fill-opacity` / `stroke-opacity`; `rgba()` FORBIDDEN
5. FORBIDDEN: `mask`, `<style>`, `class`, `foreignObject`
6. FORBIDDEN: `textPath`, `animate*`, `script`
7. Text characters: write typography & symbols as raw Unicode; HTML named entities FORBIDDEN
8. `clipPath` conditionally allowed only on `<image>` elements

### PPT Compatibility Rules:

- `<g opacity="...">` FORBIDDEN; set on each child element individually
- Image transparency uses overlay mask layer
- Inline styles only; external CSS and `@font-face` FORBIDDEN
