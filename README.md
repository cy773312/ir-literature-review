# IR 文献综述工具

<p align="center">
  <strong>面向国际关系（IR）文献综述写作的工具</strong><br />
  中文优先，英文可选。先做文献检索定位，再把已核实文献嵌入推理，避免机械罗列。
</p>

<p align="center">
  <a href="./README.en.md">English Version</a> ·
  <a href="./SKILL.md">查看 SKILL.md</a>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/主页-中文优先-0f766e?style=flat-square" alt="中文优先" />
  <img src="https://img.shields.io/badge/英文-可选-1d4ed8?style=flat-square" alt="英文可选" />
  <img src="https://img.shields.io/badge/检索-GS%20%2B%20CNKI-7c3aed?style=flat-square" alt="GS and CNKI" />
</p>

它强调“问题张力与研究定位”，而不是机械罗列文献；并支持：
- 基于已核实文献的文内引用；
- 自动生成参考文献列表；
- 按学术排版要求交付 `.docx` 文件；
- **跨用户/跨模型的一致性约束（固定输出协议 + 质量闸门）**；
- **中文为默认输出语言，用户可按需切换英文版**。

<p align="center">
  <sub>English readers can use <a href="./README.en.md">README.en.md</a>.</sub>
</p>

## 一句话介绍

`ir-literature-review` 是一个专门服务于 **国际关系（IR）文献综述** 的工具。

`ir-literature-review` 适用于以下场景：
- 你至少有文献检索范围；
- 你可选提供论文框架与初步文献（种子文献）；
- 你希望先完成文献检索定位，再进入综述写作。

技能执行流程：
1. 结构化提取检索边界、语种比例、纳排标准与种子文献；
2. 联动检索并核实文献（Google Scholar / CNKI）；
3. 先输出“文献检索范围与文献地图”并等待确认；
4. 再进行研究定位与综述写作（用户要求时可先给骨架）；
5. 输出带引用的正文、参考文献与 `.docx` 成稿。

## 核心能力

- **张力优先写作**：围绕理论困境/经验争论组织文献，不做流水账式总结。
- **双策略写作框架**：
  - 框架整合（Framework-first）
  - 问题拆解（Question-driven）
- **IR 子领域适配**：安全研究、IPE、外交政策分析、国际组织、比较威权/信息政治、建构主义等。
- **引用真实性约束**：
  - 禁止捏造文献；
  - 未核实信息必须标记；
  - 正文引用与文末参考文献一一对应。
- **稳健性机制**：
  - 质量档位（fast / standard / rigorous）控制检索深度；
  - 固定“检索日志 + 文献地图”输出协议；
  - 写作前必须通过证据/结构/定位三道质量闸门。
- **docx 优先交付**：默认不只给纯文本，直接交付可用文稿。

## 默认输出规范

除非用户另有说明，默认按以下规则交付：

| 项目 | 默认值 |
|---|---|
| 文内引用 | 作者-年份格式 |
| 参考文献 | 仅包含正文实际引用过的文献 |
| 中文字体 | 宋体 |
| 西文字体 / 数字 | Times New Roman |
| 字号 | 12pt |
| 首行缩进 | 2 个中文字符 |
| 行间距 | 1.5 倍 |
| 最终交付 | `.docx` |

如果用户提供学校或期刊模板，以模板要求优先。

## 快速开始

1. 在 Claude Code 中打开本仓库。
2. 提供你的文献检索范围（可附论文框架与初步文献）。
3. 先确认技能给出的“文献检索范围与文献地图”。
4. 再生成正文、引用与参考文献（需要时可先看骨架）。
5. 获取符合排版要求的 `.docx` 文件。

## 示例提示词

- “先按这个检索范围做文献搜索并给我文献地图：威慑失效机制、2015-2025、英文为主中文补充；我已有几篇初步文献会一起给你。”
- “结合我给的种子文献 + GS/CNKI 在线检索，先确认文献范围，再写一版问题拆解式综述。”
- “最终输出 docx，中文宋体、西文 Times New Roman，小四、首行缩进 2 字符、1.5 倍行距。”

## 设计原则

- 文献综述是论证，不是文献目录。
- 研究缺口应从已有研究局限中生长出来，而非外加结论。
- 评价应当有力（sharp）、有据（grounded）、有针对性（targeted）。
- 段落过渡依赖逻辑推进，而非形式化连接词。
- 为保证不同用户、agent、模型下质量接近，优先遵循固定协议与质量闸门，而不是依赖自由发挥。

## 相关文件

- 主要说明文件：[SKILL.md](./SKILL.md)
- 英文说明：[README.en.md](./README.en.md)
- 质量检查清单：[references/quality-checklist.md](./references/quality-checklist.md)
- 写作策略说明：[references/writing-strategies.md](./references/writing-strategies.md)

## 维护状态

持续维护中。

当前版本已支持：

- 文内引用与参考文献生成
- 默认 `.docx` 交付
- 学术排版默认值自动落实
