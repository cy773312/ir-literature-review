# IR 文献综述 Skill

<p align="center">
  <strong>面向国际关系（IR）文献综述写作的 Codex Skill</strong><br />
  中文优先，英文可选。先搭论证骨架，再把已核实文献嵌入推理，避免机械罗列。
</p>

<p align="center">
  <a href="./README.en.md">English Version</a> ·
  <a href="./SKILL.md">查看 SKILL.md</a>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Codex-Skill-111827?style=flat-square" alt="Codex Skill" />
  <img src="https://img.shields.io/badge/主页-中文优先-0f766e?style=flat-square" alt="中文优先" />
  <img src="https://img.shields.io/badge/英文-可选-1d4ed8?style=flat-square" alt="英文可选" />
  <img src="https://img.shields.io/badge/检索-GS%20%2B%20CNKI-7c3aed?style=flat-square" alt="GS and CNKI" />
</p>

<p align="center">
  <sub>English readers can use <a href="./README.en.md">README.en.md</a>.</sub>
</p>

## 一句话介绍

`ir-literature-review` 是一个专门服务于 **国际关系（IR）文献综述** 的 Claude Code skill。

它的目标不是“把很多论文说一遍”，而是让 agent 更稳定地做到：

- 先识别研究问题与核心张力
- 先确认骨架，再展开成文
- 用已核实文献支撑论证，而不是堆作者名
- 默认输出符合学术排版要求的 `.docx`

## 适合什么场景

这个 skill 特别适合：

- 你已经有论文框架，但还需要把综述写扎实
- 你有大致检索方向，希望先出骨架再展开
- 你想写安全研究、IPE、外交政策分析、国际组织、比较威权、信息政治、建构主义等 IR 主题
- 你需要把“研究空缺”写成从已有研究局限中自然长出来的缺口
- 你希望最终交付的不只是纯文本，而是可直接使用的 `.docx`

它**不主要用于**：

- 普通论文式背景介绍
- 机械化的文献清单
- 不需要综述结构的泛化写作

## 你会得到什么

| 产出 | 说明 |
|---|---|
| 文献综述骨架草案 | 先给结构，确认方向后再展开 |
| 正式综述正文 | 围绕争论、机制和缺口成文 |
| 参考文献 + `.docx` | 直接交付可用稿件 |

## 默认执行流程

1. 结构化提取研究问题、机制、方法范围与竞争文献
2. 检索并核实文献（Google Scholar / CNKI 路径）
3. 输出“文献综述骨架草案”并等待确认
4. 按选定策略展开正式写作
5. 输出带引用、参考文献和排版的 `.docx`

## 检索依赖

这个 skill 在文献检索阶段会结合两个外部 skill：

- [gs-skills](https://github.com/cookjohn/gs-skills)
- [cnki-skills](https://github.com/cookjohn/cnki-skills)

它们分别用于英文 IR 文献和中文 IR 文献的检索、核实与补充阅读。

## 核心能力

| 能力 | 作用 |
|---|---|
| 张力优先 | 不做逐篇总结，而是围绕争论、机制和缺口组织文献 |
| 骨架先行 | 先确认论证结构，再进入展开写作 |
| 核实优先 | 未核实文献不得当作确定性证据使用 |
| 交付优先 | 默认要生成可直接使用的 `.docx` |
| 中文优先 | 默认先给中文界面与中文输出，英文作为可选项 |

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

1. 在 Claude Code 中打开这个仓库
2. 提供论文框架和大致检索方向
3. 先确认文献综述骨架
4. 再展开成完整正文
5. 最终导出 `.docx`

## 示例提示词

- “基于我的论文框架，写一版国际关系文献综述，先给骨架再展开。”
- “围绕威慑失效机制做问题拆解式综述，重点比较竞争性解释。”
- “最终输出 docx，中文宋体、西文 Times New Roman，小四、首行缩进 2 字符、1.5 倍行距。”

## 设计原则

- 文献综述是论证，不是文献目录
- 研究缺口应从既有研究局限中长出来
- 评价要有力、要有据、要有针对性
- 段落过渡应由逻辑推进，而不是靠空泛连接词

## 相关文件

- 主要技能文件：[SKILL.md](./SKILL.md)
- 英文说明：[README.en.md](./README.en.md)
- 质量检查清单：[references/quality-checklist.md](./references/quality-checklist.md)
- 写作策略说明：[references/writing-strategies.md](./references/writing-strategies.md)

## 维护状态

持续维护中。

当前版本已支持：

- 文内引用与参考文献生成
- 默认 `.docx` 交付
- 学术排版默认值自动落实
