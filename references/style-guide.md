# 哲学 Handout 风格详细指南 (黑白紧凑版)

本指南是对 SKILL.md 中写作规范的补充，针对**黑白紧凑、数学风格**的排版需求提供细致的操作建议和示例。

---

## 一、黑白紧凑排版的核心原则

### 1.1 视觉层次通过结构而非颜色实现

**传统做法（避免）**：使用彩色区分不同类型的框（蓝色=论题，绿色=定义，红色=反驳）

**紧凑做法（采用）**：
- 通过**线框样式**区分（实线/虚线/双线）
- 通过**填充灰度**区分（纯白/浅灰/深灰）
- 通过**字体样式**区分（正体/斜体/粗体/小字号）
- 通过**留白与缩进**组织层次

### 1.2 密度最大化原则

1. **字号**：正文 10pt，脚注 8pt，表格 8-9pt
2. **行距**：1.05 倍行距，段落间距 0.3em
3. **边距**：2cm 边距，最大化内容区域
4. **列表**：紧凑列表，itemsep=1pt
5. **公式**：行内公式优先，行间公式尽量紧凑

### 1.3 数学论文风格要素

- **定理式编号**：论证、定义、思想实验等使用统一编号
- **形式化优先**：可形式化的内容尽量用符号表达
- **证明结构**：关键论证采用"前提 → 推理 → 结论"的演绎格式
- **引用精确**：页码标注使用上标形式，不干扰正文阅读

---

## 二、双语版本结构详解

### 2.1 文档结构

```
┌─────────────────────────────────────┐
│           Header (元信息)            │
│      (双语标题、作者、汇报人信息)     │
├─────────────────────────────────────┤
│          Thesis Box (核心论题)       │
│         (一句话概括，英中双语)         │
├─────────────────────────────────────┤
│  Part I: English Version (英文完整版) │
│  ├─ Background / 理论背景            │
│  ├─ Main Arguments / 核心论证        │
│  ├─ Key Definitions / 关键概念         │
│  ├─ Objections and Replies / 反驳与回应  │
│  └─ Commentary / 评论                 │
├─────────────────────────────────────┤
│ Part II: 中文摘要版 (Chinese Summary)  │
│  ├─ 背景概述                         │
│  ├─ 论证结构总结                      │
│  ├─ 关键概念表                        │
│  └─ 评论                             │
├─────────────────────────────────────┤
│  Appendix: Argument Map (论证图)      │
└─────────────────────────────────────┘
```

### 2.2 Part I (English) 写作要点

- **完整详细**：包含论文中的所有关键论证细节
- **形式化表达**：关键论证使用逻辑符号和 schema 表示
- **术语标注**：首次出现的哲学术语用 `\engterm{}` 标注，后文直接使用英文
- **页码引用**：使用 `\pagemark{}` 标注原文页码
- **双语提示**：节标题后可使用 `\zh{}` 添加中文翻译提示

### 2.3 Part II (中文摘要版) 写作要点

- **精简概括**：Part I 的精华提炼，篇幅控制在 1-2 页
- **结构化表达**：使用列表、表格呈现核心内容，减少段落
- **中文为主**：术语可保留英文但主要用中文表达
- **评论重点**：Part II 的评论可以更加概括性，指出主要贡献和局限

### 2.4 双语协调原则

1. **内容互补而非重复**：Part I 负责"完整"，Part II 负责"精要"
2. **术语一致**：同一术语在英文版和中文版中含义一致
3. **结构平行**：主要章节在两部分之间有对应关系
4. **评论侧重不同**：英文版评论可以更技术化，中文版评论可以更综合

---

## 三、形式化表达详细规范

### 3.1 逻辑符号体系

**命题逻辑**（按频率排序）：

| 符号 | LaTeX | 含义 | 使用场景 |
|------|-------|------|---------|
| $\rightarrow$ | `\rightarrow` | 实质蕴涵 | 条件句、推理规则 |
| $\leftrightarrow$ | `\leftrightarrow` | 等价 | 定义、充要条件 |
| $\land$ | `\land` | 合取 | 多前提并列 |
| $\lor$ | `\lor` | 析取 | 选言命题 |
| $\neg$ | `\neg` | 否定 | 否定命题 |
| $\vdash$ | `\vdash` | 逻辑后承 | 推理结论标记 |
| $\models$ | `\models` | 逻辑蕴涵（语义） | 有效性判断 |

**一阶逻辑**：

| 符号 | LaTeX | 含义 |
|------|-------|------|
| $\forall x$ | `\forall x` | 全称量化 |
| $\exists x$ | `\exists x` | 存在量化 |
| $=$ | `=` | 等词 |
| $\neq$ | `\neq` | 不等 |

**模态逻辑**（知识论、形而上学常用）：

| 符号 | LaTeX | 含义 |
|------|-------|------|
| $\Box \varphi$ | `\Box \varphi` | 必然 |
| $\Diamond \varphi$ | `\Diamond \varphi` | 可能 |

**认知逻辑**（心灵哲学、知识论常用）：

| 符号 | LaTeX | 含义 |
|------|-------|------|
| $K_a \varphi$ | `K_a \varphi` | a 知道 φ |
| $B_a \varphi$ | `B_a \varphi` | a 相信 φ |
| $J_a \varphi$ | `J_a \varphi` | a 有理由相信 φ |

### 3.2 形式化定义格式

**标准定义格式**：

```latex
\begin{defbox}{术语英文 \engterm{Term}}
  \textbf{定义：}[定义内容]\\
  \textbf{形式化：} $[符号表达式]$
\end{defbox}
```

**示例**：

```latex
\begin{defbox}{意向系统 \engterm{Intentional System}}
  \textbf{定义：}一个系统 $S$ 是意向系统，当且仅当 $S$ 的行为可以通过
  采用意向立场（赋予信念和欲望）得到成功预测。
  
  \textbf{形式化：}
  \[
    \text{IntentionalSystem}(S) \leftrightarrow 
    \text{PredictableByIntentionalStance}(S)
  \]
\end{defbox}
```

### 3.3 分类体系的形式化

**方法一：枚举 + 条件描述**（推荐用于大多数分类）

```latex
\textbf{实践推理的类型：}
\begin{enumerate}[label=(\alph*)]
  \item \textbf{审慎推理} \engterm{Prudential reasoning}：
        以主体的欲望/偏好为驱动条件
  \item \textbf{制度推理} \engterm{Institutional reasoning}：
        以社会制度身份为构成条件
  \item \textbf{无条件推理} \engterm{Unconditional reasoning}：
        不以任何欲望或制度身份为条件
\end{enumerate}
```

**方法二：条件矩阵**（推荐用于二元属性分类）

```latex
\begin{table}[h]
  \centering
  \small
  \begin{tabular}{@{}lcc@{}}
    \toprule
    & \textbf{依赖于欲望} & \textbf{依赖于社会身份} \\
    \midrule
    审慎推理 & 是 & 否 \\
    制度推理 & 否 & 是 \\
    无条件推理 & 否 & 否 \\
    \bottomrule
  \end{tabular}
\end{table}
```

**方法三：形式化定义**（当条件关系精确时）

```latex
设 $R$ 为推理模式，$D$ 为欲望条件，$I$ 为制度条件：
\begin{align*}
  R_{\text{prudential}} &= D \land \neg I \\
  R_{\text{institutional}} &= \neg D \land I \\
  R_{\text{unconditional}} &= \neg D \land \neg I
\end{align*}
```

---

## 四、表格设计规范

### 4.1 必须使用表格的场景

以下情况 **必须** 使用表格（而非纯文本列表）：

1. **两方以上观点对比**（如 Realism vs Interpretationism）
2. **概念分类及其属性枚举**
3. **思想实验索引**（名称 | 页码 | 目的 | 结论）
4. **判断标准或条件的罗列**（如"扩展信念的四条标准"）
5. **论证评估**（维度 | 评分 | 依据）

### 4.2 表格设计原则

1. **使用 booktabs 三线表**：`\toprule`, `\midrule`, `\bottomrule`。不使用竖线。
2. **紧凑列格式**：使用 `@{}` 去除列间多余间距，如 `@{}lXl@{}`
3. **小字号**：表格内容使用 `\small` 或 `\footnotesize`
4. **表题必备**：每个表格必须有 `\caption{}`（简短标题）
5. **表内文字左对齐**：内容列使用 `l` 或 `X`，仅序号列使用 `c`

### 4.3 表格类型模板

**类型一：对立观点对比表**

```latex
\begin{table}[h]
  \centering
  \small
  \begin{tabularx}{\textwidth}{@{}l X X@{}}
    \toprule
    & \textbf{实在论 \engterm{Realism}} 
      & \textbf{解释主义 \engterm{Interpretationism}} \\
    \midrule
    核心主张 & 信念是客观的内在事实 
             & 信念是基于解释的归因标签 \\
    认知方式 & 可靠地猜测内在状态 
             & 采取预测策略并评估其成功 \\
    代表人物 & Fodor, Dretske & Dennett, Davidson \\
    \bottomrule
  \end{tabularx}
\end{table}
```

**类型二：思想实验索引表**

```latex
\begin{table}[h]
  \centering
  \small
  \begin{tabularx}{\textwidth}{@{}l l X X@{}}
    \toprule
    \textbf{名称} & \textbf{页码} & \textbf{目的} & \textbf{关键结论} \\
    \midrule
    Inga-Otto & \pagemark{pp.12--13} 
      & 展示外部资源可构成非当下信念 
      & 信念由功能角色而非位置决定 \\
    Twin Otto & \pagemark{p.14} 
      & 证明信念不在头部 
      & 外在差异直接决定信念内容 \\
    \bottomrule
  \end{tabularx}
\end{table}
```

**类型三：条件判断矩阵**

```latex
\begin{table}[h]
  \centering
  \small
  \begin{tabular}{@{}p{3cm} p{3.5cm} p{3.5cm}@{}}
    \toprule
    \textbf{条件 A} & \textbf{条件 B} & \textbf{推论结果} \\
    \midrule
    系统行为可通过意向策略预测 
      & 预测依赖于信念-欲望归因 
      & $\rightarrow$ 是意向系统 \\
    存在外在资源耦合 
      & 资源具恒常性与直接可用性 
      & $\rightarrow$ 构成扩展信念 \\
    \bottomrule
  \end{tabular}
\end{table}
```

---

## 五、思想实验呈现规范

### 5.1 思想实验的结构化呈现

每个思想实验必须包含以下三个要素：

1. **设置（Setup）**：实验的具体情境描述
2. **目的（Purpose）**：该实验旨在证明或反驳什么
3. **结论（Conclusion）**：作者从该实验中提取的哲学结论

### 5.2 命名规范

- 如果原文已有名称（如 "Inga-Otto Case"），直接使用
- 如果原文没有名称，根据核心特征创造一个简短名称
- 始终保留英文名称，格式："[中文名称] \engterm{English Name}"

### 5.3 示例（黑白紧凑风格）

```latex
\begin{thoughtexp}[Inga-Otto 案例比较 \engterm{Inga-Otto Case}]
  \textbf{设置：}Inga 是普通认知主体，听说现代艺术博物馆有展览时，
  回忆起博物馆在第53街并前往该地。她拥有存储在生物记忆中的"既有信念"。

  Otto 是阿尔茨海默症患者，依赖随身携带的笔记本。新信息被记录其中，
  需要时查阅。笔记本功能等同于他的生物记忆。\pagemark{12--13}

  \textbf{目的：}通过平行对比展示：外部环境可以构成"非当下信念"，
  二者差异仅在于位置（内部记忆 vs 外部笔记本），而功能完全相同。

  \textbf{结论：}"Otto在查阅笔记本之前就相信博物馆在第53街"，
  因为"笔记本对Otto扮演了记忆对Inga所扮演的相同角色"。
\end{thoughtexp}
```

---

## 六、反驳-回应机制详细规范

### 6.1 反驳的识别与分类

在阅读论文时，注意识别以下类型的反驳：

| 类型 | 来源 | 特征 |
|------|------|------|
| 内部反驳 | 作者自己提出的 | "有人可能会反对……" |
| 外部反驳 | 作者引用的其他哲学家 | "X认为……" |
| 预设反驳 | 对理论预设的挑战 | "该论证依赖于……但这一前提可以质疑" |
| 类比反驳 | 通过类比案例挑战 | "如果我们接受这一论证，那么……" |

### 6.2 反驳-回应的呈现格式（黑白风格）

**基本格式**：使用 `objreply` 环境，包含 `\objection` 和 `\reply` 命令（均为黑色粗体）。

**多级反驳**：当反驳有多个子论点时，使用嵌套结构：

```latex
\begin{objreply}[异议：扩展认知依赖意识]
  \objection 认知过程本质上与意识相连，而外部过程不可能有意识，
  因此不可能构成认知过程。\pagemark{页码}

  \reply
  \begin{itemize}
    \item [$\triangleright$] 并非所有认知过程都是有意识的。
      无意识过程在认知中扮演重要角色。
    \item [$\triangleright$] 仅仅因为某过程是外在的，
      并不能否定其认知地位。
  \end{itemize}
\end{objreply}
```

---

## 七、论证图绘制指南 (黑白风格)

### 7.1 论证图的元素

| 元素 | TikZ 样式 | 含义 |
|------|-----------|------|
| 白色矩形+黑框 | `premise` | 前提 |
| 浅灰填充矩形 | `conclusion` | 结论 |
| 虚线框 | `objection` | 反驳 |
| 实线箭头 | `arrow` | 推理方向 |
| 虚线箭头 | `objarrow` | 反驳指向 |

### 7.2 论证图设计原则

1. **从上到下**：前提在上，结论在下
2. **同级前提**并排放置
3. **反驳**放在侧面，用虚线指向被反驳的前提
4. **黑白打印友好**：仅使用黑色线条和灰度填充
5. **字号统一**：图中文字使用 `\small` 或 `\footnotesize`

### 7.3 TikZ 模板 (黑白风格)

```latex
\begin{tikzpicture}[
  node distance=0.6cm and 1cm,
  premise/.style={
    rectangle, draw=black, fill=white, text width=4.5cm,
    minimum height=0.5cm, align=center, font=\small
  },
  conclusion/.style={
    rectangle, draw=black, fill=gray!15, text width=4.5cm,
    minimum height=0.5cm, align=center, font=\small\bfseries
  },
  objection/.style={
    rectangle, draw=black, fill=none, text width=3.5cm,
    minimum height=0.4cm, align=center, font=\small, dashed
  },
  arrow/.style={-{Stealth[length=2mm]}, thick},
  objarrow/.style={-{Stealth[length=2mm]}, thick, dashed}
]

% 节点
\node[premise] (p1) {P1: 前提一};
\node[premise, below=of p1] (p2) {P2: 前提二};
\node[conclusion, below=of p2] (c1) {C: 结论};

% 反驳
\node[objection, right=1.2cm of p1] (obj1) {异议};

% 箭头
\draw[arrow] (p1) -- (c1);
\draw[arrow] (p2) -- (c1);
\draw[objarrow] (obj1) -- (p1);

\end{tikzpicture}
```

---

## 八、评论章节写作指南

### 8.1 评论的结构建议

评论章节是 handout 中唯一完全由汇报者创作的内容，建议结构：

1. **论证强度评估**
   - 前提是否可信？
   - 推理是否有效？
   - 整体论证力度如何？

2. **未考虑的反驳**
   - 作者忽略了哪些可能的反对意见？
   - 这些反驳是否致命？

3. **理论影响与比较**
   - 该论证对相关领域的贡献
   - 与其他理论的比较

4. **开放问题**
   - 论文留下了哪些未解决的问题？

### 8.2 评论的语气规范

- 保持学术客观性
- 使用"笔者认为""值得注意""然而""可以质疑"等表达
- 不使用情感色彩词汇（"精彩""错误""荒谬"）
- 对作者的批评应具体且有据

---

## 九、常见错误规避

| 错误类型 | 表现 | 正确做法 |
|---------|------|---------|
| 颜色依赖 | 使用彩色区分信息 | 使用线框、填充、字体样式区分 |
| 过度留白 | 大段空行、宽行距 | 1.05倍行距、紧凑段落 |
| 字号不一致 | 表格、框内文字大小不一 | 统一使用 `\small` 或 `\footnotesize` |
| 内容重复 | 中英文部分完全重复 | 英文完整详细、中文精简概括 |
| 形式化不足 | 纯自然语言表述 | 关键论证使用逻辑符号和 schema |
| 页码缺失 | 未标注原文出处 | 使用 `\pagemark{}` 标注 |
| 表格滥用 | 简单列举也使用表格 | 仅在对比、分类时使用表格 |
| 表格不足 | 复杂对比用纯文本 | 多维对比必须用表格 |

---

## 十、中英双语处理细则

### 10.1 术语标注

- 首次出现：`规范语汇 \engterm{normative vocabulary}`
- 后续提及可直接使用中文；若上下文可能引起歧义，再次标注
- 论文标题保持原文语言

### 10.2 Part I (English) 术语处理

- 节标题后可使用 `\zh{}` 添加中文翻译提示：
  ```latex
  \subsection{Background \zh{理论背景}}
  ```
- 关键术语首次出现用 `\engterm{}`，后文直接使用英文

### 10.3 Part II (中文) 术语处理

- 以中文为主，关键术语保留英文标注
- 表格中可采用"术语 \engterm{Term}"格式
- 论证结构可以用中文简述

---

## 附录：紧凑排版参数速查

```latex
% 字号
\documentclass[10pt, a4paper]{article}  % 正文 10pt
\small                                   % 9pt
\footnotesize                            % 8pt
\scriptsize                              % 7pt

% 行距
\setstretch{1.05}                        % 1.05 倍行距
\setlength{\parskip}{0.3em}              % 段落间距 0.3em

% 边距
\usepackage[margin=2cm]{geometry}         % 2cm 边距

% 列表
\setlist[itemize]{leftmargin=1.5em, itemsep=1pt, parsep=0pt, topsep=2pt}
\setlist[enumerate]{leftmargin=2em, itemsep=1pt, parsep=0pt, topsep=2pt}

% 标题间距
\titlespacing*{\section}{0pt}{0.8em}{0.3em}
\titlespacing*{\subsection}{0pt}{0.5em}{0.2em}
\titlespacing*{\subsubsection}{0pt}{0.4em}{0.2em}

% 表格列格式 (紧凑)
\begin{tabular}{@{}lXl@{}}  % 去除左右间距
```
