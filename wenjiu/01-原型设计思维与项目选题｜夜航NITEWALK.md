# 01 原型设计思维与项目选题

> 项目：夜航 NITEWALK —— 面向城市独居青年与夜间创作者的情绪漫游 / 轻社交 App
>
> 研究日期：2026-08-26｜画布：375 × 812 pt｜交付：Figma 12 页原型

## 一、项目结论

### 1. 为什么选“夜间情绪漫游”

夜间散步、短时离线、声音陪伴和低压力社交，是一个能同时展示视觉表现力与完整 UX 的交叉垂类：

- **业务价值**：以“今晚想要什么状态”作为入口，连接城市路线、声音内容和小型活动；后续可扩展会员路线、独立创作者内容与线下品牌合作。
- **用户价值**：用户不需要经营人设，也不需要完成高强度任务，只需选择情绪、时间和安全偏好，就能得到一条可执行的夜间方案。
- **作品集价值**：既能做 P1 的沉浸式 3D 月相 / 玻璃材质，也能展示搜索、推荐、记录、隐私与安全等全链路设计。

### 2. 2026 设计趋势转译

Apple 当前设计指南强调统一平台语言、内容优先、可适应尺寸与可访问性；其 Liquid Glass 使用分层、半透明、动态光泽，并允许用户降低透明度或动效。[Apple WWDC26 Design Guide](https://developer.apple.com/wwdc26/guides/design/)｜[Adopting Liquid Glass](https://msc-kobol-public-prod.apple.com/documentation/technologyoverviews/adopting-liquid-glass)

Google 的 Material 3 Expressive 将“表达性”建立在研究之上，重点包含情绪化设计、动态色彩、灵活排版、对比形状与更有意图的动效。[Google Expressive Design Research](https://design.google/library/expressive-material-design-google-research?pubDate=20250521)｜[Material 3 Expressive](https://developer.android.com/design/ui/wear/guides/get-started/levels-expression?hl=en)

本项目的具体取舍：

1. **P1 使用表达性**：深夜蓝黑底、暖橙月相、3D 玻璃月亮、轻微光晕与呼吸动效。
2. **P2 使用可解释的情绪推荐**：展示“为什么推荐这条路线 / 声音”，避免 AI 黑箱。
3. **P3 使用降噪功能界面**：黑白灰为主，仅以橙色表示当前状态；玻璃效果不进入表单、支付和安全页。
4. **AI 只做陪伴与整理**：帮助生成路线摘要、整理夜记，不替代心理诊断；所有个性化入口提供关闭和清除数据选项。

## 二、产品定位与用户

### 一句话定位

**在城市还没睡着的时候，给你一段刚刚好的独处。**

### 核心用户

| 用户 | 场景 | 关键诉求 |
|---|---|---|
| 独居青年 | 下班后脑内过载，不想回家立刻刷短视频 | 低门槛、短时、可随时结束 |
| 夜间创作者 | 灵感枯竭，想寻找声音与街景 | 有氛围的路线、声音和收藏 |
| 轻社交用户 | 想认识同频的人，但拒绝公开社交压力 | 匿名、弱关系、可控可退出 |

### 核心主链路

`选择今晚状态 → 获取 20/40/60 分钟方案 → 查看路线与声音 → 开始漫游 → 留下一句夜记 → 复盘与收藏`

## 三、视觉策略：P1 / P2 / P3

| 等级 | 页面 | 视觉强度 | 设计策略 |
|---|---|---:|---|
| P1 | 开屏、首页、漫游进行中、个人月相 | 80–90% | 3D 月相、渐变、玻璃层、动态光晕；只突出一个主动作 |
| P2 | 路线详情、声音详情、发现 Feed、夜记发布、结果反馈 | 40–60% | 大图 / 局部渐变 / 精致卡片；信息层级优先于装饰 |
| P3 | 搜索筛选、路线确认、历史记录、隐私安全 | 10–20% | 中性底、严谨表单、状态色；减少透明与阴影，保证效率 |

## 四、基础设计规范

- 画布：**375 × 812 pt**；安全边距 16 pt；主要间距采用 4 / 8 / 12 / 16 / 24 / 32。
- 字体：中文优先使用 **PingFang SC**；英文 / 数字使用 **SF Pro Display / SF Pro Text**。
- 正文不低于 14 pt；辅助文字 12 pt；重要操作热区不低于 44 × 44 pt。
- 底部导航：4 个 Tab，图标盒子 32 × 32 pt；高度 56 pt，不含 Home Indicator。
- 颜色：`Ink #0C1020`、`Night #161C3A`、`Moon #F4C57A`、`Signal #FF7A59`、`Mist #DDE6FF`、`Fog #8D96B3`。
- 玻璃卡片：白色 12–18% 透明度 + 背景模糊 + 1 px 白色 20% 描边；文字与背景对比度优先。
- 动效：P1 呼吸光晕 4–6 s；页面转场 240–360 ms；提供“减少透明度 / 减少动效”开关。

## 五、12 个页面原型清单

| 编号 | 页面 | 等级 | 页面任务 | 关键组件 |
|---:|---|---|---|---|
| 01 | 开屏 / 情绪引导 | P1 | 建立品牌氛围并进入状态选择 | 3D 月相、主 CTA、跳过 |
| 02 | 今晚首页 | P1 | 选择状态并看到个性化方案 | 情绪球、推荐卡、Tab Bar |
| 03 | 漫游进行中 | P1 | 实时陪伴与安全确认 | 路线进度、声音控制、结束按钮 |
| 04 | 我的月相 | P1 | 查看连续记录与个人状态 | 月相日历、状态统计、IP 卡 |
| 05 | 路线详情 | P2 | 评估路线是否适合今晚 | 地图占位、时长、安静度、安全提示 |
| 06 | 声音详情 | P2 | 试听并加入漫游方案 | 专辑卡、波形、播放控制 |
| 07 | 发现 Feed | P2 | 浏览城市夜间灵感 | 内容卡、标签、收藏 |
| 08 | 夜记发布 | P2 | 用一句话结束漫游 | 情绪标签、输入框、公开范围 |
| 09 | 漫游反馈结果 | P2 | 复盘并获得下一步建议 | 结束状态、AI 摘要、再来一次 |
| 10 | 搜索与筛选 | P3 | 找到路线 / 声音 / 主题 | 搜索框、筛选 Chip、结果列表 |
| 11 | 我的记录 | P3 | 管理历史漫游与收藏 | 列表、时间筛选、批量管理 |
| 12 | 隐私与安全 | P3 | 管理位置、数据与退出机制 | 开关、权限说明、删除数据 |

## 六、10 张风格参考 / Moodboard

> 不是照搬界面，而是分别提取材质、层级、色彩、动效或排版语言。

1. [Apple WWDC26 Design Guide](https://developer.apple.com/wwdc26/guides/design/)：平台级材质与内容优先。
2. [Apple Adopting Liquid Glass](https://msc-kobol-public-prod.apple.com/documentation/technologyoverviews/adopting-liquid-glass)：透明度、动效和无障碍降级。
3. [Apple iOS 26 features PDF](https://www.apple.com/hk/en/os/pdf/All_New_Features_iOS_26_Sept_2025.pdf)：动态 Tab Bar、层叠玻璃与内容聚焦。
4. [Google Expressive Design Research](https://design.google/library/expressive-material-design-google-research?pubDate=20250521)：情绪化表达必须服务于使用场景。
5. [Material 3 Expressive Levels](https://developer.android.com/design/ui/wear/guides/get-started/levels-expression?hl=en)：从基础到转化级的表达强度分层。
6. [Figma UI/UX Blog](https://www.figma.com/blog/ui-ux/)：AI 让工具更接近自然语言与协作式创作。
7. [Liquid Glass Animation Playground](https://liquidglassdesign.com/gallery/liquid-glass-animation-playground)：玻璃、柔光、景深与动效实验参考。
8. [Figma Mobile App Showcase](https://forum.figma.com/showcase-your-work-14/mobile-app-37819)：留白、字体与移动端密度参考。
9. [Apple Design Resources](https://developer.apple.com/design/resources/)：原生控件、SF Symbols 与平台尺寸参考。
10. [Google Material 3](https://m3.material.io/)：色彩角色、状态和组件可用性参考。

## 七、10 个功能竞品 / 截图采集任务

> 交作业时在 Figma 中把下列产品的对应页面截图放入“竞品参考”区，并按“借鉴 / 不借鉴”标注。本作业原型画布已按相同信息架构预留分析逻辑。

| 竞品 | 建议截图页面 | 借鉴点 | 本项目的差异 |
|---|---|---|---|
| Headspace | 首页 / AI guidance / Sleep | 内容分层、专家内容、AI 陪伴 | 从“练习”转为“出门前方案” |
| Calm | 首页 / Sleep Stories | 夜间氛围、内容入口 | 增加城市路线与空间安全 |
| Finch | 首页 / 虚拟宠物 | 轻量激励、情绪反馈 | 不采用强养成，避免任务压力 |
| Daylio | Mood tracking / Statistics | 情绪记录与趋势 | 用月相视觉代替传统图表 |
| Stoic | Journal / Reflection | 低压力 journaling | 只要求一句夜记，降低输入成本 |
| AllTrails | Explore / Navigate / Activity | 搜索、记录、个人户外历史 | 聚焦城市夜行，不做专业户外 |
| Strava | Feed / Activity detail | 活动流、路线与轻社交 | 不强调排名，不公开实时位置 |
| Komoot | Discover / Route planning | 路线发现、兴趣点与规划 | 用“安静度 / 光线 / 人流”做筛选 |
| Spotify | Home / Now playing | 沉浸播放、内容卡片 | 声音是漫游的陪伴层，不是主产品 |
| Locket | Home / Share | 低压力、弱关系分享 | 采用匿名夜记与可控公开范围 |

功能依据：Headspace 官方页面明确覆盖引导冥想、AI 支持与睡眠内容；AllTrails 官方帮助中心将产品拆为 Explore、Saved、Navigate、Activity、Profile 五个核心入口；Strava 强调活动记录、路线与社区发现；Komoot强调发现、规划与分享。[Headspace](https://www.headspace.com/app)｜[AllTrails](https://support.alltrails.com/hc/en-gb/articles/44409942124052-Understanding-the-AllTrails-App)｜[Strava](https://www.strava.com/)｜[Komoot](https://www.komoot.com/?page=home)

## 八、UX 取舍与评分快速对照

| 评分项 | 本项目做法 | 占比 |
|---|---|---:|
| 信息架构 | 以“状态 → 方案 → 漫游 → 复盘”为主链路，5 个入口以内 | 30% |
| 页面层级 | 4 个 P1、5 个 P2、3 个 P3，明确视觉发力边界 | 30% |
| 栅格规范 | 375 × 812、16 边距、4/8 栅格、44 pt 热区 | 20% |
| 真机舒适度 | Figma Mirror 检查字号、对比度、拇指区和 Home Indicator | 20% |

## 九、风险与验证计划

- **风险：玻璃效果抢过内容。** 验证：关闭背景图与透明效果后，主任务仍可完成。
- **风险：夜间定位带来隐私和安全问题。** 验证：默认不公开实时位置；开始漫游前展示权限与安全出口。
- **风险：AI 推荐显得玄学。** 验证：每条推荐展示依据（时长、光线、安静度、用户偏好），允许重新生成。
- **风险：情绪记录变成负担。** 验证：首版只要求选一个状态或写一句话，连续记录不设置惩罚。

## 十、参考来源

- [Apple WWDC26 Design Guide](https://developer.apple.com/wwdc26/guides/design/)
- [Apple Human Interface Guidelines](https://developer.apple.com/design/human-interface-guidelines?lang=en)
- [Adopting Liquid Glass](https://msc-kobol-public-prod.apple.com/documentation/technologyoverviews/adopting-liquid-glass)
- [Google Expressive Design Research](https://design.google/library/expressive-material-design-google-research?pubDate=20250521)
- [Material 3 Expressive Levels](https://developer.android.com/design/ui/wear/guides/get-started/levels-expression?hl=en)
- [Headspace App](https://www.headspace.com/app)
- [AllTrails App Structure](https://support.alltrails.com/hc/en-gb/articles/44409942124052-Understanding-the-AllTrails-App)
- [Strava](https://www.strava.com/)
- [Komoot](https://www.komoot.com/?page=home)

