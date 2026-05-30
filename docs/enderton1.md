# A Mathematical Introduction to Logic



## First-Order Logic

**Expression.** An *expression* is any finite sequence of symbols.

**Term.** The set of *terms* is the set of *expressions* that can be built up from the *constant* symbols and *variables* by prefixing the *function* symbols.

**Atomic formula.** An *atomic formula* is an *expression* of the form $Pt_1 \dots t_n$, where $P$ is an $n$-place predicate symbol and $t_1, \dots , t_n$ are terms.

**WFF.** The *well-formed formulas* are those expressions that can be built up from the atomic formulas by use (zero or more times) of the *connective symbols* ($\neg, \to$) and the *quantifier symbol* ($\forall$).

**Free variables.** These rules define when a variable $x$ occurs **free** in a formula:

1. For atomic $\alpha$, $x$ occurs free in $\alpha$ iff $x$ occurs in (i.e., is a symbol of) $\alpha$.

2. $x$ occurs free in $(\neg \alpha)$ iff $x$ occurs free in $\alpha$.

3. $x$ occurs free in $(\alpha \rightarrow \beta)$ iff $x$ occurs free in $\alpha$ or in $\beta$.

4. $x$ occurs free in $\forall v_i \alpha$ iff $x$ occurs free in $\alpha$ and $x \neq v_i$.

**Sentence.** If no variable *occurs free* in the *wff* $α$, then $α$ is a *sentence*.

**Convention of alphabets. ** 

- **Predicate symbols**: Uppercase italic letters. Also $\in$, $<$.
- **Variables**: $v_i$, $u$, $v$, $x$, $y$, $z$.
- **Function symbols**: $f$, $g$, $h$. Also $\mathbf{S}$, $+$, etc.
- **Constant symbols**: $a$, $b$, $\ldots$. Also $\mathbf{0}$.
- **Terms**: $u$, $t$.
- **Formulas**: Lowercase Greek letters.
- **Sentences**: $\sigma$, $\tau$.
- **Sets of formulas**: Uppercase Greek letters, plus certain italic letters that pretend to be Greek, viz., $A$ (alpha) and $T$ (tau).
- **Structures**: Uppercase German (Fraktur) letters.

---

**Structure.** A *structure* $\mathfrak{A}$ is a function such that: 

| Symbol (Parameters)     | Refers to                                                    |
| ----------------------- | ------------------------------------------------------------ |
| $\forall$               | $|\mathfrak{A}|$, the universe/domain of $\mathfrak{A}$ (nonempty) |
| $n$-palce predicate $P$ | $P^{\mathfrak{A}}$, an $n$-ary relation, $P^{\mathfrak{A}} \subseteq |\mathfrak{A}|^n$ |
| constant $c$            | $c^{\mathfrak{A}} \in |\mathfrak{A}|$                        |
| $n$-place function $f$  | $f^{\mathfrak{A}}: |\mathfrak{A}|^n \to |\mathfrak{A}|$      |

**$\models_{\mathfrak{A}} \sigma$ ($\sigma$ is true in $\mathfrak{A}$ or $\mathfrak{A}$ is a model of $\sigma$).** Let

- $\varphi$ be a wff of our language,
- $\mathfrak{A}$ a structure for the language,
- $s: V \to |\mathfrak{A}|$ a function from the set $V$ of all variables into the universe $|\mathfrak{A}|$ of $\mathfrak{A}$.

Then $\models_{\mathfrak{A}} \varphi[s]$ (for $\mathfrak{A}$ to *satisfy* $\varphi$ with $s$) *if and only if* the translation of $\varphi$ determined by $\mathfrak{A}$, where the variable $x$ is translated as $s(x)$ wherever it occurs free, is true.

**THEOREM 22A.** Assume that $s_1$ and $s_2$ are functions from $V$ into $|\mathfrak{A}|$ which agree at all variables (if any) that occur free in the wff $\varphi$. Then
$$
\models_{\mathfrak{A}} \varphi[s_1] \quad \text{iff} \quad \models_{\mathfrak{A}} \varphi[s_2].
$$

> This theorem justifies the following notation: Suppose that $\varphi$ is a formula such that all variables occurring free in $\varphi$ are included among $v_1, \ldots, v_k$. Then for elements $a_1, \ldots, a_k$ of $|\mathfrak{A}|$, $$\models_{\mathfrak{A}} \varphi[\![a_1, \ldots, a_k]\!]$$ means that $\mathfrak{A}$ satisfies $\varphi$ with some (and hence with any) function $s: V \to |\mathfrak{A}|$ for which $s(v_i) = a_i$, $1 \leq i \leq k$.

**Logical implication.** Let $\Gamma$ be a set of wffs, $\varphi$ a wff. Then $\Gamma$ *logically implies* $\varphi$, written $\Gamma \models \varphi$, iff for every structure $\mathfrak{A}$ for the language and every function $s: V \to |\mathfrak{A}|$ such that $\mathfrak{A}$ satisfies every member of $\Gamma$ with $s$, $\mathfrak{A}$ also satisfies $\varphi$ with $s$.

**Tautology.** A wff $\varphi$ is **valid** iff $\emptyset \models \varphi$ (written simply "$\models \varphi$").
