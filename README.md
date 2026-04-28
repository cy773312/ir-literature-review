# IR Literature Review

<p align="center">
  <strong>用 AI 写出顶刊水准的国际关系文献综述</strong><br />
  <sub>把既有文献变成有论证张力的综述成稿 · 自动引用 · 一键出 docx</sub>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/discipline-IR%20%7C%20国际关系-0f766e?style=flat-square" alt="IR" />
  <img src="https://img.shields.io/badge/output-docx-1d4ed8?style=flat-square" alt="docx" />
  <img src="https://img.shields.io/badge/language-中文%20%7C%20English-7c3aed?style=flat-square" alt="bilingual" />
  <img src="https://img.shields.io/badge/license-MIT-green?style=flat-square" alt="license" />
</p>

<p align="center">
  <a href="./README.en.md">English</a> ·
  <a href="./SKILL.md">SKILL.md</a> ·
  <a href="#快速开始">快速开始</a> ·
  <a href="#设计哲学">设计哲学</a>
</p>

---

## 这是什么

**IR Literature Review** 是一个 Claude Code Skill，专注于把国际关系领域的既有文献转化为高质量的文献综述。

你提供论文主题和已有文献（摘要、PDF、笔记、参考文献列表），它负责：

- 按功能分类、精读评价每一篇文献
- 识别研究张力，选择最优写作策略
- 写出有论证驱动力的综述正文
- 自动生成文内引用、参考文献列表
- 一键输出格式规范的 `.docx` 文件

> 这不是文献检索工具。如需检索文献，推荐配合 [gs-skills](https://github.com/cookjohn/gs-skills) 或 [cnki-skills](https://github.com/cookjohn/cnki-skills) 使用。

## 核心理念

<p align="center">
  <strong>文献不是单位，问题和张力才是单位。</strong>
</p>

好的 IR 文献综述读起来像一个论证，而不是一份目录。它不逐篇报告"谁说了什么"，而是用已有研究呈现一个结构性张力，并在这个张力中确立新研究的位置。

## 能力一览

- **张力优先写作** — 围绕理论困境、经验争论、概念模糊或方法缺口组织文献
- **双策略框架** — 框架整合（Framework-First）或问题拆解（Question-Driven），可混用
- **缺口三分法** — 共识区缺口、争论区缺口、空白区缺口，每种有不同写法
- **四维精读评价** — 假设 / 逻辑 / 证据 / 方法，精准定位文献贡献与局限
- **10 种评价路径** — 内置王凯、唐世平（2022）总结的解释性研究 10 种文献评价方式
- **引用真实性** — 禁止捏造文献；引用仅限用户提供的材料，一一对应
- **品质闸门** — 引用闸门、结构闸门、定位闸门，三道关口保证输出质量
- **自动 docx 交付** — 宋体 / Times New Roman，12pt，1.5 倍行距，首行缩进 2 字符
- **IR 子领域适配** — 安全研究、IPE、FPA、国际制度、比较威权/信息政治、建构主义

## 快速开始

1. 在 Claude Code 中打开本仓库
2. 提供论文主题 + 已有文献材料（摘要/PDF/笔记/参考文献列表）
3. Skill 先做文献地图与功能分类，确认后开始写作
4. 获取带完整引用和参考文献的 `.docx` 文件

**示例提示词**：

```
我要写一篇关于"数字威权主义如何影响跨国政治动员"的文献综述。
关键文献包括：Rosenfeld & Wallace (2024)、Guriev & Treisman (2022)、
Roberts (2018)。请先做文献分类和评价，再用问题拆解策略写综述。
```

```
我有几篇关于"联盟承诺可信度"的论文框架和摘要，帮我整理成一份
文献底稿，识别核心争论和缺口，为后续正式写作做准备。
```

## 方法论基础

本 Skill 的写作方法论建立在以下四项参考材料之上，经过系统提炼和嵌入：

| 来源 | 贡献 |
|---|---|
| **Knopf (2006)** *Doing a Literature Review* | 四任务框架、四维评价（假设/逻辑/证据/方法）、双圈文献结构、知识贡献框架 |
| **王凯、唐世平 (2022)** 第三章"如何进行文献评价" | 正当性/合理性框架、10 种解释性研究评价方式、质量四标准、常见错误清单 |
| **Clark, Dolan & Jost (2025)** *Bureaucratic Influence in International Politics* | 框架整合策略的完整示范 |
| **Rosenfeld & Wallace** *Information Politics and Propaganda in Authoritarian Societies* | 问题拆解策略的完整示范 |

## 设计哲学

- 文献综述是**论证**，不是文献目录
- 研究缺口应从已有研究的具体局限中**生长**出来，而非外加
- 批评应当 **sharp、grounded、targeted**
- 段落过渡依赖**逻辑推进**，不靠"此外""综上所述"
- 每个缺口必须回答：**从哪里来**（来源）？**会怎样**（后果）？
- 质量闸门抬高的**是下限**，不设上限

## 输出规范

| 项目 | 默认值 |
|---|---|
| 文内引用 | 作者-年份 |
| 参考文献 | 仅正文实际引用条目 |
| 中文字体 | 宋体 |
| 西文/数字 | Times New Roman |
| 字号 | 小四（12pt） |
| 首行缩进 | 2 字符 |
| 行间距 | 1.5 倍 |
| 交付格式 | `.docx` |

用户提供学校或期刊模板时，以模板优先。

## 项目文件

| 文件 | 说明 |
|---|---|
| [SKILL.md](./SKILL.md) | Skill 完整指令 |
| [README.en.md](./README.en.md) | English README |
| [references/quality-checklist.md](./references/quality-checklist.md) | 文献评价质量清单 |
| [references/writing-strategies.md](./references/writing-strategies.md) | 写作策略详细展开 |

---

<p align="center">
  <strong>🤝 加入我们，一起建设 IR × AI 的开源生态</strong>
</p>

国际关系研究正处于 AI 赋能的关键窗口期。文献综述只是第一步——事实检索、因果推断辅助、政策情景模拟、多语种情报分析……每一个环节都有巨大的工具化潜力。

但这个领域的 AI 工具建设，不能只靠少数人。IR 学者最懂自己的研究需求，工程师最懂技术实现，**只有当这两个群体在开源社区中持续对话，才能做出真正好用的东西**。

如果你：

- 用这个 Skill 写出了文献综述，欢迎分享你的使用体验和改进建议
- 想到了一个新的 IR 研究环节可以 AI 化，欢迎提 Issue 或直接 PR
- 已经自己写了一个 IR 相关的 Claude Code Skill（事实核查、理论推演、案例匹配……），欢迎告诉我们，互相连接
- 只是路过但觉得有意思，⭐ Star 一下就是最大的鼓励

<p align="center">
  <strong>AI 赋能国际关系研究，需要每一个你的参与。</strong>
</p>

---

<p align="center">
  <sub>MIT License · 持续维护中</sub>
</p>
