# 分析哲学常见论证模式及其形式化方法

本参考文件列出了分析哲学中最常见的论证类型及其形式化表示方法，供制作 handout 时参考。

---

## 一、演绎论证 \engterm{Deductive Argument}

### 1.1 肯定前件式（Modus Ponens）

**模式**：若 $p \rightarrow q$ 且 $p$，则 $q$。

**形式化**：
$$\frac{p \rightarrow q \qquad p}{q}$$

**哲学应用示例**：
- P1: 如果信念由推论角色构成，那么不在推论网络中的状态不是信念
- P2: 训练有素的鹦鹉的反应不在推论网络中
- C: 因此鹦鹉的反应不是信念

### 1.2 否定后件式（Modus Tollens）

**模式**：若 $p \rightarrow q$ 且 $\neg q$，则 $\neg p$。

**形式化**：
$$\frac{p \rightarrow q \qquad \neg q}{\neg p}$$

**哲学应用示例**：
- P1: 如果所有认知过程都在头部内，则外部工具的使用不是认知过程
- P2: 外部工具的使用（如纸笔计算）是认知过程（反例）
- C: 因此"所有认知过程都在头部内"为假

### 1.3 假言三段论（Hypothetical Syllogism）

**模式**：若 $p \rightarrow q$ 且 $q \rightarrow r$，则 $p \rightarrow r$。

### 1.4 归谬法（Reductio ad Absurdum）

**模式**：假设 $p$，推出矛盾 $\bot$，因此 $\neg p$。

**形式化**：
$$\frac{p \vdash \bot}{\neg p}$$

**哲学应用**（布兰顿对单调性论证的批评即隐含归谬）：
- 假设所有实践推理都是单调的
- 则需要列举无穷多种 ceteris paribus 条件
- 但无穷列举在认知上不可行
- 因此并非所有实践推理都是单调的

---

## 二、归纳论证 \engterm{Inductive Argument}

### 2.1 枚举归纳

**模式**：观察到 $a_1, a_2, \ldots, a_n$ 都具有属性 $P$，且无反例，因此（可能）所有 $A$ 都具有 $P$。

**形式化**：
$$\frac{P(a_1) \land P(a_2) \land \cdots \land P(a_n)}{\forall x \, (A(x) \rightarrow P(x))} \quad \text{(概率性)}$$

### 2.2 最佳解释推理 \engterm{Inference to the Best Explanation} (IBE)

**模式**：在所有可能的解释 $H_1, H_2, \ldots, H_n$ 中，$H_k$ 最佳地解释了现象 $E$，因此 $H_k$ 为真（或最可能为真）。

**形式化**：
$$\frac{\text{Best}(H_k, \{H_1, \ldots, H_n\}, E)}{H_k} \quad \text{(概然性)}$$

**哲学应用示例**（Dennett 的解释性优势论证）：
- 现象：意向策略可以预测人类行为
- 可能解释：
  - H1: 人类确实具有信念和欲望（Dennett 的立场）
  - H2: 这只是预测工具，不对应真实心理状态
- H1 提供了更简洁、更自然的解释（chaining predictions, real pattern）
- 因此 H1 更可能是正确的

---

## 三、归谬与反例论证 \engterm{Reductio and Counterexample}

### 3.1 反例法

**模式**：声称 $\forall x \, (A(x) \rightarrow B(x))$，找到 $c$ 使得 $A(c) \land \neg B(c)$，因此该声称为假。

**形式化**：
$$\frac{A(c) \land \neg B(c)}{\neg \forall x \, (A(x) \rightarrow B(x))}$$

**哲学应用示例**（Twin Otto 案例）：
- 声称：信念在头部内（$\forall b, \text{InHead}(b)$）
- 反例：Twin Otto 的笔记本中的信念是外在的
- 结论：$\neg \forall b, \text{InHead}(b)$，即"信念不在头部内"

### 3.2 二难论证 \engterm{Dilemma}

**模式**：$p \lor q$（构造性）或 $\neg p \lor \neg q$（破坏性），且不论哪种选择都导致不受欢迎的结果。

**形式化**（构造性二难）：
$$\frac{p \rightarrow r \qquad q \rightarrow s \qquad p \lor q}{r \lor s}$$

---

## 四、溯因论证 \engterm{Abductive Argument}

### 4.1 假设-演绎法

**模式**：
1. 观察到现象 $O$
2. 假设 $H$ 可解释 $O$
3. 如果 $H$ 为真，则 $O$ 应当出现（$H \rightarrow O$）
4. $O$ 确实出现了
5. 因此 $H$ 可能是真的

**形式化**：
$$\frac{H \rightarrow O \qquad O}{H \text{ (可能为真)}}$$

---

## 五、概念论证 \engterm{Conceptual Argument}

### 5.1 概念分析

**模式**：通过分析概念 $C$ 的构成条件，揭示 $C$ 的必然属性或与其他概念的关系。

**形式化**：
$$C(x) \overset{\text{def}}{=} \varphi_1(x) \land \varphi_2(x) \land \cdots \land \varphi_n(x)$$

**哲学应用示例**（布兰顿对信念概念的分析）：
$$\text{Belief}(x) \overset{\text{def}}{=} \text{PremiseCapable}(x) \land \text{ConclusionCapable}(x) \land \text{ReasonSensitive}(x)$$

### 5.2 反映性论证 \engterm{Transcendental Argument}

**模式**：某现象 $F$ 的存在，必然预设了条件 $C$；$F$ 确实存在；因此 $C$ 为真。

**形式化**：
$$\frac{F \rightarrow_{\text{necessarily}} C \qquad F}{C}$$

---

## 六、论证强度评估框架

在评论章节中，可使用以下维度评估论证：

| 维度 | 评估问题 | 权重建议 |
|------|---------|---------|
| **前提可信度** | 前提是否有独立支持？是否为哲学共识？ | 高 |
| **逻辑有效性** | 推理形式是否正确？是否有隐含前提？ | 高 |
| **反驳回应力** | 对主要异议的回应是否充分？ | 中-高 |
| **概念清晰性** | 关键概念是否被精确定义？ | 中 |
| **理论统一性** | 是否与作者的其他理论承诺一致？ | 中 |
| **解释力** | 相比竞争理论，是否提供更好的解释？ | 中 |
| **简洁性** | 是否遵循奥卡姆剃刀原则？ | 低-中 |

**评分建议**：使用 1-5 分制，在 handout 中以表格形式呈现（见 style-guide.md 第四节"类型四"）。
