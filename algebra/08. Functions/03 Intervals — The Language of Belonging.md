# 📏 Intervals — The Language of Belonging

> *"Mathematics is the art of giving the same name to different things — and different names to the same thing."*
> — Henri Poincaré

---

## 🌉 Where the Last Story Left Us

In the last lesson, you learned to ask a precise question about any equation: *does it define a function?* And the moment you asked that question seriously, you immediately needed to talk about **domains** — the set of inputs a function is allowed to receive. You restricted the domain of `y² = x` to `x ≥ 0` so that the square root branch became a valid function. You mentioned `[−5, 5]` as the domain of the top semicircle.

But here is the thing: we used those notations *without ever stopping to explain them.*

That moment has arrived. Before we can talk fluently about functions — their domains, their ranges, their behaviour on different stretches of the number line — we need a shared vocabulary for describing **which real numbers belong to a set**. That vocabulary is called **interval notation**, and this lesson is devoted entirely to mastering it.

> *"Interval notation is not a new topic. It is the missing grammar of everything you have already been doing."*

---

## 🗺️ The Problem Interval Notation Solves

Suppose someone asks: *"For which values of `x` is the expression `√(x + 3)` defined?"*

You work it out: the square root requires the inside to be non-negative, so `x + 3 ≥ 0`, which means `x ≥ −3`. Simple enough. But now how do you *write* that answer?

You could write `x ≥ −3`. That works, but it's verbose, and when answers become complicated — *all real numbers except `x = 2`*, or *`x` between `−1` and `4` but not including `4`* — the inequality notation becomes unwieldy fast.

What mathematicians settled on instead is a compact, elegant shorthand that communicates two things at once: **where the set starts and ends**, and **whether those endpoints are included or excluded**. That shorthand is the interval.

---

## 🔒 Closed Intervals — When the Endpoints Belong

A **closed interval** is one where both boundary points are *included* in the set. The name "closed" is deliberate — the set is closed around its endpoints, like a sealed container that keeps them inside.

We write a closed interval using **square brackets**:

$$[-3, 2]$$

This reads: *"all real numbers `x` such that `x` is greater than or equal to `−3` and less than or equal to `2`."* In set-builder notation, the same idea is written:

$$\{x \in \mathbb{R} \mid -3 \leq x \leq 2\}$$

On a number line, closed endpoints are shown as **filled-in (solid) dots** — because the point is *included*, it gets to be coloured in.

The square bracket and the filled dot are telling you the same thing. **They are two dialects of the same sentence.**

---

## 🔓 Open Intervals — When the Endpoints Are Excluded

An **open interval** excludes its endpoints entirely. The boundary values are *approached* but never *reached*.

We write an open interval using **parentheses** (round brackets):

$$(−1, 4)$$

This reads: *"all real numbers `x` strictly greater than `−1` and strictly less than `4`."* The endpoints `−1` and `4` themselves are not in the set. On a number line, open endpoints are shown as **hollow (open) circles** — because the point is *not included*, it remains empty.

The inequality signs mirror the bracket choice perfectly:

- Square bracket `[` or `]` ↔ `≤` or `≥` (endpoint **included**)
- Round bracket `(` or `)` ↔ `<` or `>` (endpoint **excluded**)

*If you ever mix these up — writing a square bracket with a strict inequality or a round bracket with `≤` — you have stated a contradiction.* The notation and the symbol must agree.

---

## 🔀 Mixed Intervals — Half-Open, Half-Closed

Real life (and mathematics) often demands more nuance. Sometimes one endpoint belongs to the set and the other does not. These are called **half-open** or **half-closed** intervals, depending on your mood.

For example:

$$(-4, -1]$$

This means: `x` is *strictly greater than* `−4` (so `−4` is excluded) but *less than or equal to* `−1` (so `−1` is included). On a number line you would draw an open circle at `−4` and a filled dot at `−1`, with a solid line connecting them.

The bracket on each side works **independently**. You read the left side and the right side as two separate decisions:

- *Left endpoint `−4` — is it in or out?* Round bracket → out.
- *Right endpoint `−1` — is it in or out?* Square bracket → in.

This independence is what gives interval notation its flexibility.

---

## 🌍 Set-Builder Notation — The More Formal Voice

Alongside interval notation, mathematicians use a more formal language called **set-builder notation**. You will encounter it in textbooks, proofs, and higher-level courses, so it is worth knowing fluently.

The structure looks like this:

$$\{x \in \mathbb{R} \mid -3 \leq x \leq 2\}$$

Reading it aloud: *"the set of all `x` that are members of the real numbers, such that `x` is between `−3` and `2` inclusive."*

Three symbols carry all the meaning here:

- **`∈`** (the Greek letter epsilon, or the membership symbol) — means *"is a member of"* or *"belongs to"*. So `x ∈ ℝ` means "`x` is a real number."
- **`ℝ`** — the set of all real numbers (the entire number line).
- **`|`** (the vertical bar) — means *"such that"*. It separates the description of the variable from the condition it must satisfy.

The interval notation and the set-builder notation are *interchangeable* — they describe the same set. Interval notation is faster to write; set-builder notation is more explicit about what the condition actually is. In practice, you will move between them fluidly.

| Interval Notation | Set-Builder Notation | In Plain Words |
|---|---|---|
| `[−3, 2]` | `{x ∈ ℝ \| −3 ≤ x ≤ 2}` | From −3 to 2, both ends included |
| `(−1, 4)` | `{x ∈ ℝ \| −1 < x < 4}` | Between −1 and 4, neither end included |
| `(−4, −1]` | `{x ∈ ℝ \| −4 < x ≤ −1}` | Greater than −4, up to and including −1 |
| `[0, ∞)` | `{x ∈ ℝ \| x ≥ 0}` | Zero and everything to the right |

---

## ♾️ Infinity — The Horizon You Never Reach

Here is a rule that has no exceptions: **infinity always takes a parenthesis. Never a bracket.**

The reason is conceptual, not arbitrary. A square bracket says: *"this endpoint is included in the set."* But infinity is not a number. It is not a point on the number line that you can reach and include. It is a *direction* — a statement that the set continues without bound. You cannot include something that never arrives.

So the domain of `f(x) = √x` is written `[0, ∞)` — square bracket at `0` because zero *is* included, parenthesis at `∞` because there is no upper boundary to include.

Similarly, the set of all negative numbers is `(−∞, 0)` — parenthesis on both ends, because neither `−∞` nor `0` belongs to this particular set.

> *"Writing `[0, ∞]` is not just wrong notation — it is a category error. You would be claiming to include something that does not exist as a point. Always use a parenthesis at infinity."*

---

## ✂️ Excluding a Single Value — The Union

Now consider a slightly different problem. What is the domain of `f(x) = 1/(x − 2)`?

The function is defined for every real number *except* `x = 2`, where the denominator becomes zero. The domain is: *all real numbers except `2`.* How do you write that as an interval?

The answer is that you cannot write it as a single interval — because a single interval is always a *connected* stretch of the number line, and removing one point from the middle of the line leaves two disconnected pieces. So you write it as a **union** of two intervals:

$$(-\infty, 2) \cup (2, \infty)$$

The symbol `∪` means *"union"* — *"take everything in the first set and everything in the second set together."* The two open parentheses at `2` confirm that `2` itself is in neither piece.

This is the standard technique for any domain that requires excluding a finite number of points:

- Domain of `1/(x − 2)`: $(-\infty, 2) \cup (2, \infty)$
- Domain of `√(x + 3)`: $[-3, \infty)$
- Domain of `1/(x² − 1)` (exclude `x = ±1`): $(-\infty, -1) \cup (-1, 1) \cup (1, \infty)$

Each union joins pieces that individually cannot contain the excluded values.

---

## 🎯 Why Endpoints Are Not Pedantic — They Change Everything

It is tempting to treat the distinction between `[a, b]` and `(a, b)` as a minor technicality — a footnote. It is not. The difference between including and excluding an endpoint has real mathematical consequences.

Consider the **Extreme Value Theorem**: if a function is continuous on a *closed* interval `[a, b]`, then it is guaranteed to reach both a maximum value and a minimum value somewhere inside. This guarantee *evaporates* on an open interval `(a, b)`. The function `f(x) = x` on the open interval `(0, 1)` never actually reaches `0` or `1` — so it has no minimum and no maximum on that interval, despite being perfectly continuous.

The filled dot versus the hollow circle is not aesthetic. It is a statement about theorems that hold or fail.

> *"In mathematics, precision at the boundary is not obsessive tidiness — it is the difference between a theorem being true and being false."*

---

## 🚧 The Mistakes Worth Warning You About

Before moving on, here are the confusions that catch almost every student at least once:

- **Writing `∞` with a square bracket**, like `[0, ∞]` — this is always wrong. Infinity takes a parenthesis, no exceptions.
- **Mismatching the bracket and the inequality sign** — if you write `[a, b)` but then translate it to `a ≤ x ≤ b`, you have made an error. The round bracket on the right means `x < b`, not `x ≤ b`. Always check that every bracket corresponds to the right inequality symbol.
- **Forgetting the union when excluding a point** — writing `x ≠ 2` is fine informally, but in interval notation you must write `(−∞, 2) ∪ (2, ∞)`. A single interval cannot represent a set with a hole in the middle.
- **Reading a hollow dot as included** on a graph — always check the dot. A hollow circle is an excluded endpoint, regardless of how close it looks to being filled.

---

## 🧾 Everything Tied Together

The story of this lesson has one throughline: **every set of real numbers you care about in mathematics can be described precisely using intervals**, and that precision matters because endpoints carry real mathematical weight.

A **closed interval** `[a, b]` includes both boundaries — square brackets, filled dots, `≤` signs. An **open interval** `(a, b)` excludes both — round brackets, hollow circles, `<` signs. A **half-open interval** mixes the two, deciding each endpoint independently. **Infinity always wears a parenthesis**, because it is a direction, not a destination. And when a set has gaps — points removed from its middle — you express it as a **union** of intervals joined by `∪`.

Set-builder notation `{x ∈ ℝ | condition}` says the same thing in a more explicit voice, spelling out the membership symbol `∈` and the *"such that"* bar `|` to make the logic fully transparent.

These tools will appear in every lesson that follows — in domains of functions, in solution sets of inequalities, in statements about continuity and limits, and eventually in the language of calculus itself. You now have the grammar. The sentences it will build are waiting just ahead.

---

> *"An interval is not just a pair of numbers with brackets around them. It is a precise claim about belonging — about which points on the number line are inside the conversation and which are not. Get this right, and every door in mathematics opens a little more cleanly."* 📏

---

*This lesson continues the Functions series. It establishes interval notation and set-builder notation as the foundational language for describing domains, ranges, and solution sets in all lessons ahead.*
