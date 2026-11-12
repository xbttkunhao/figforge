# FigForge

把凝聚态物理论文做成能在组会上讲清楚的 PPT。

FigForge 是面向超导、强关联和 RIXS 组会的 Agent Skill。它先提交汇报主线和原图选用方案，再用 SeaSlides 制作 Typst/PDF 和可编辑 PowerPoint。逐页中文备注包含完整讲稿，默认每篇约 15 分钟。

## 使用

1. 将本仓库克隆到 Agent 的技能目录下，文件夹名用 `figforge`。Codex 可放到 `~/.codex/skills/figforge`。
2. 配置 `seaslides-typst-slides-skill` 及其 Typst/Touying 和 PPTX 导出依赖。
3. 把论文交给 Agent，并明确调用 `$figforge`。例如「用 $figforge 把这篇论文做成 15 分钟组会汇报，先给我主线和选图。」

制作时优先用原文图，清楚标注图号和出处，按证据需要讲解实验、拟合和反演。输出后对照检查 Typst PDF 和 PowerPoint 实际渲染。

## 运行依赖

- SeaSlides 与其 Typst/Touying 编译环境。
- 可编辑 PPTX 导出需要 `typst-ts-cli` 和 `typ2pptx`。
- 默认版式使用宋体（SimSun）和 Times New Roman。完整导出验收需要 Microsoft PowerPoint，用于打开 PPTX 并检查实际版式、原生文字和备注。

## 发布包内容

- `SKILL.md` 定义从论文、选图提案到制作和视觉验收的工作流。
- `README.md` 说明安装、调用方式和依赖。
