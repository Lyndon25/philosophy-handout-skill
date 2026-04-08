# Philosophy Handout Skill

从哲学论文原文出发制作高质量学术报告 handout 的专业技能。

## 简介

本 Skill 用于指导 Claude 从一篇哲学论文原文出发，制作出符合分析哲学规范的高质量学术报告 handout。输出为 **LaTeX 源文件**（.tex），可编译为专业排版的 PDF。

### 核心理念

- **Markdown 极简风格**：无彩色框、无线框装饰，纯文字层次结构
- **极高信息密度**：每页包含尽可能多的关键信息
- **双独立版本**：英文完整版 + 中文完整版，结构平行、内容对应

## 文件结构

```
philosophy-handout/
├── _meta.json              # Skill 元数据配置
├── SKILL.md                # 主要技能文档（含完整方法论）
├── README.md               # 本文件
└── references/
    ├── latex-template.tex  # LaTeX 模板文件
    ├── style-guide.md      # 风格指南（排版、表格、论证图）
    └── argument-patterns.md # 分析哲学常见论证模式
```

## 使用方法

### 触发方式

当用户输入包含以下关键词时，Claude 会自动触发本 Skill：

- handout / 读书报告 / 论文汇报
- presentation handout / 哲学论文 / 学术报告
- 论文展示 / 课程展示材料

### 工作流程

本 Skill 采用**七阶段工作流**：

1. **文本解析与论点提取**：通读论文，提取核心论题、理论对手、论证结构
2. **概念定义清单编制**：列出所有关键术语及其定义
3. **论证结构形式化**：将关键论证转化为形式化表达
4. **Handout 宏观结构设计**：双独立版本结构
5. **LaTeX 编写实施**：基于模板编写 handout
6. **论证图绘制**：使用 TikZ 绘制论证结构图
7. **质量检查与完善**：逐项检查结构完整性、形式化、写作质量

## 依赖要求

### 必需软件

- **XeLaTeX**：用于编译 LaTeX 源文件（通过 TeX Live 或 MiKTeX 安装）

### 必需宏包

本 Skill 使用的 LaTeX 宏包包括：

- `ctex` - 中文支持
- `amsmath`, `amssymb`, `amsthm` - 数学与逻辑符号
- `booktabs` - 专业表格线
- `tikz` - 绘图（论证图）
- `enumitem` - 自定义列表
- `tabularx` - 弹性宽度表格
- 其他辅助宏包

## 输出格式

生成的 Handout 包含：

1. **英文完整版**：完整呈现所有内容，包含详细论证、形式化表达、页码引用
2. **中文完整版**：完整翻译所有内容，结构平行
3. **论证结构图**：TikZ 绘制的核心论证图

## 编译说明

```bash
# 编译 LaTeX 文件（需编译两次以获得正确交叉引用）
xelatex handout.tex
xelatex handout.tex
```

## 相关参考

- `SKILL.md` - 完整技能文档，含详细方法论和写作规范
- `references/style-guide.md` - 风格指南（排版、表格、论证图）
- `references/argument-patterns.md` - 分析哲学常见论证模式
- `references/latex-template.tex` - LaTeX 模板文件

## 版本信息

- **版本**: 1.0.0
- **作者**: Skill Creator
- **标签**: philosophy, academic, latex, handout, analytic-philosophy

## 适用场景

适用于分析哲学各子领域的论文，包括：

- 心灵哲学 (Philosophy of Mind)
- 知识论 (Epistemology)
- 形而上学 (Metaphysics)
- 语言哲学 (Philosophy of Language)
- 伦理学 (Ethics)
- 行动哲学 (Philosophy of Action)

---

*本 Skill 旨在帮助用户高效制作符合学术规范的分析哲学论文 handout。*
