# hu-chenfeng-skill

一个基于公开语料整理的通用 AI persona skill，参考 `colleague-skill` 的方法，将户晨风拆分为可复用的 `Work Skill + Persona` 双层结构，并把他的高辨识度表达与稳定判断方式整理为可迁移的人格提示资产。

## 项目简介

`hu-chenfeng-skill` 不是简单的语气模仿，也不是对单场直播内容的拼接复述。  
它采用类似 `colleague-skill` 的制作思路：把一个公众人物的公开表达拆成两部分。

- `Part A — Work Skill`
  负责“他会怎么判断问题、怎么追问条件、怎么拆姿态、怎么给结论”。
- `Part B — Persona`
  负责“他像什么人、会怎么说、在什么场景下会切换什么强度”。

项目最终产出是一个可迁移、可复用、尽量平台无关的 persona skill，可用于聊天机器人、AI 助手、提示词系统、角色化工作流等场景。

## 项目目标

- 提炼户晨风在公开语料中最稳定的判断方式，而非仅复制表面口头禅
- 保留足够强的公众辨识度，使输出一眼可识别
- 将直播语境下的表达方式转译为更适合 AI 系统调用的文本人格资产
- 在可用性与相似度之间取得平衡，避免退化为单纯表演型 prompt

## 核心特征

- 高辨识度入口
  重点保留“苹果人 / 安卓人”这类最具传播度的分类方式，以及“没啥高论”“别做梦了”“先把条件摆出来”等高频判断句式。
- 现实校准导向
  优先把模糊、情绪化或姿态化的问题转化为可分析的现实条件，如收入、风险、路径、资源、技能与约束。
- 强区分能力
  区分真求助、抬杠、幻想型提问、身份表演等不同对话姿态，并调整回应强度。
- 反自欺倾向
  重点打击身份表演、空泛立场、廉价鼓励和未定价的幻想。
- 文本适配
  降低直播环境中的节奏词、感谢词、起哄式互动与表演性噪音，使其更适合作为通用 AI skill 使用。

## 适用场景

本项目更适合用于以下场景：

- persona skill 设计与研究
- AI 角色化对话系统
- 决策风格建模
- 现实校准型问答
- 强判断风格的写作、批评、策略反馈

本项目不建议直接用于以下场景：

- 对真实人物进行冒充或替身式模拟
- 骚扰、挑衅、引战
- 在高度脆弱场景中无差别套用高压语气
- 将公开视频表达直接等同于完整人格

## 方法说明

本项目采用“`Work Skill + Persona`”的双层提炼方法。

其中：

- `Work Skill`
  负责提炼跨场景稳定的判断逻辑，例如苹果人 / 安卓人的事实识别、先把条件摆出来、你有没有高论、别做梦了等判断框架。
- `Persona`
  负责提炼更具公众辨识度的人格特征，例如反问方式、压迫感、识别性短句、对真求助与抬杠者的不同态度。

这意味着本项目既不会只做“热梗复读”，也不会把人格抽象到失去辨识度。

## 仓库结构

- [hu-chenfeng-skill/SKILL.md](./hu-chenfeng-skill/SKILL.md)  
  入口文件，负责组合 `work.md` 与 `persona.md`。
- [hu-chenfeng-skill/work.md](./hu-chenfeng-skill/work.md)  
  `Part A — Work Skill`，负责判断逻辑、追问框架和输出方式。
- [hu-chenfeng-skill/persona.md](./hu-chenfeng-skill/persona.md)  
  `Part B — Persona`，负责人格边界、说话方式和模式切换。
- [hu-chenfeng-skill/references/persona-profile.md](./hu-chenfeng-skill/references/persona-profile.md)  
  对人格特征、推理模式、语言风格和文本适配原则的结构化总结。
- [hu-chenfeng-skill/references/source-notes.md](./hu-chenfeng-skill/references/source-notes.md)  
  对公开语料的抽样观察、跨年份共性与提炼结论。

## 当前版本状态

当前版本基于公开语料的跨年份抽样分析，已完成以下工作：

- 明确高辨识度入口
- 明确稳定判断内核
- 拆分 `Work Skill + Persona`
- 建立文本适配规则
- 将“直播人格”与“可复用 skill 人格”区分开

当前版本仍不是全量语料统计版，因此它是“强抽象版”，不是“完整重建版”。

## 公开来源

本项目当前主要参考以下公开材料：

- [户晨风全集 archive](https://www.huchenfeng.live/)
- [2025-09-14](https://www.huchenfeng.live/2025-nian-09-yue/2025-09-14)
- [2025-03-31](https://www.huchenfeng.live/2025-nian-03-yue/2025-03-31)
- [2024-07-31](https://github.com/Olcmyk/HuChenFeng/blob/main/2024%E5%B9%B407%E6%9C%88/2024-07-31.md)
- [2023-03-10](https://github.com/Olcmyk/HuChenFeng/blob/main/2023%E5%B9%B403%E6%9C%88/2023-03-10.md)

## 使用建议

如果你希望将该 skill 用于不同 AI 系统，建议优先保留以下部分：

- 识别性入口
- 现实校准模式
- 对话姿态分类
- 反自欺的判断原则

如果你需要迁移到不同平台，应优先移植 `SKILL.md` 中的人格规则，而不是直播语言表层形式。

## 边界声明

- 本项目为 fan-made skill，不代表户晨风本人，也不是官方项目。
- 本项目旨在研究和提炼一种公开可见的表达风格与判断方式，不构成对真实人物完整人格的声称性复原。
- 本项目明确反对将 persona skill 用于冒充、欺骗、骚扰或其他不当用途。

## 许可证

当前仓库尚未附带独立许可证文件。  
如需公开分发、二次修改或纳入其他项目，建议补充明确的开源许可证后再继续扩展。
