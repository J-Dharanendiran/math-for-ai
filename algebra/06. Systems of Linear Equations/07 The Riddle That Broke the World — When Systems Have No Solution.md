# 🍎 The Fruit That Couldn't Be Priced — Inconsistent Systems of Equations

> *"Sometimes, the most powerful answer mathematics can give you is not a number — it's a contradiction."*

---

## 🏰 The Kingdom, The Advisor, and The Riddle

Imagine you are inside a medieval kingdom. You have already proven your worth to the king by solving mathematical puzzles. But not everyone is pleased.

**Arbegla, the king's jealous advisor**, steps forward with a smirk and presents what he calls the *"Riddle of the Fruit Prices."*

The riddle is simple on the surface:

> *"Two visits were made to the market. Find the price per pound of apples and bananas."*

Here is what the market visits recorded:

1. **Visit 1** — 2 pounds of apples and 1 pound of bananas cost **$3**
   → Written as: `2a + b = 3`

2. **Visit 2** — 6 pounds of apples and 3 pounds of bananas cost **$15**
   → Written as: `6a + 3b = 15`

*Simple enough, right?*

You pick up your quill, confident. You've done this before.

---

## ⚔️ The Battle with Algebra

You decide to use the **elimination method** — a clean, reliable technique for solving two equations at once. The goal is to **cancel out one variable** so the other reveals itself.

Here's what you do:

1. Multiply the first equation by **−3**:
   `2a + b = 3` becomes `−6a − 3b = −9`

2. Now **add** this to the second equation:
   `(6a + 3b) + (−6a − 3b) = 15 + (−9)`

3. The `a` terms cancel. The `b` terms cancel too. And what remains is...

> **`0 = 6`**

You stare at the parchment.

*Zero equals six?*

That is not a strange answer. That is **no answer at all.** It is a mathematical impossibility — a contradiction written in ink.

---

## 🤔 "But Wait... Why Are We Even Comparing These?"

This is the exact moment where your instincts, as a curious learner, kick in — and they should.

You might think:

> *"The values changed between visits. Why are we trying to equate them in the first place?"*

This is a **brilliant question**, and it points directly to the heart of what systems of equations are really doing.

Here is the key insight: **we are not assuming the data is correct. We are *testing* whether it can be.**

When you write the two equations together as a *system*, you are essentially asking:

> *"Is there a single pair of prices — one for apples, one for bananas — that could explain both market visits?"*

If the prices stayed the same across both visits, a consistent pair should exist. **The algebra is your detective tool.** When it returns `0 = 6`, it is not failing — it is *telling you something crucial*:

> 💡 *"The information you were given cannot all be true at the same time."*

This is not a flaw in math. This is math working perfectly.

---

## 🗺️ When the Bird Says "Draw It"

A wise bird in the story advises you to **graph the equations** to understand what went wrong. You take its advice, and rewrite each equation in slope-intercept form (`b = ma + c`):

- Equation 1: `b = −2a + 3`
- Equation 2: `b = −2a + 5`

And something remarkable jumps out immediately.

**Both lines have the exact same slope: −2.**

But their *intercepts* differ — one starts at 3, the other at 5.

*What does that mean geometrically?*

It means these two lines are **parallel.** They run beside each other forever, always the same distance apart, **never intersecting.**

> *"Two parallel roads never meet — no matter how far you travel."*

And the solution to a system of equations is the **intersection point** — the one `(a, b)` pair that satisfies *both* equations simultaneously. If the lines never meet, **that point does not exist.**

---

## 🔍 The Deeper Truth About Variables

Here is where your intuition gets really sharp — and a little philosophical.

You notice something uncomfortable:

> *"When we write `b = −2a + 3`, we are treating `b` as the dependent variable. But in reality, neither apple price nor banana price depends on the other. So why are we doing this?"*

This is **not confusion** — this is *mathematical maturity in the making.*

The honest answer is that **the words "dependent" and "independent" here are a plotting convention, not a causal claim.**

When we write `b = −2a + 3`, we are not saying *"banana prices are caused by apple prices."* We are saying:

> *"If you pick any value for `a`, this equation tells you what `b` would have to be — in a world where this constraint is satisfied."*

It is a way to **visualize a constraint on a 2D graph.** Nothing more, nothing less. You could just as easily write `a = (3 − b) / 2` and put `b` on the horizontal axis instead. The mathematics is *symmetric.* The "dependency" is a **perspective**, not a law of causation.

---

## 🧪 What a System Is Really Doing

Now we arrive at the deepest idea in this entire story.

**A single equation in two unknowns** does not give you one answer. It gives you a *line* — infinitely many valid pairs. For `2a + b = 3`, here are just a few:

| `a` (apples) | `b` (bananas) |
|:---:|:---:|
| 0 | 3 |
| 1 | 1 |
| 2 | −1 |
| −1 | 5 |

Every one of these satisfies the rule. So one visit alone tells you nothing definitive about prices — it only tells you the *relationship* between them.

When you **add a second equation**, you are introducing a *second constraint.* Now the system asks a much sharper question:

> 🎯 *"Which pair satisfies BOTH constraints simultaneously?"*

Think of each equation as a **filter.** Filter 1 keeps only pairs where `2a + b = 3`. Filter 2 keeps only pairs where `2a + b = 5`. The system asks which pairs pass both filters at once. In this case — none, because no number can be both 3 and 5 at the same time.

---

## 📐 The Three Fates of Any System

After all this, the lesson crystallizes into three possible outcomes for any system of two linear equations.

**One Solution** *(Consistent — Independent)*: The two lines have different slopes, so they cross at exactly one point. A unique pair exists.

> *"Two roads converging at a single crossroads."*

**Infinitely Many Solutions** *(Consistent — Dependent)*: Both equations describe the same line, so every point on that line is a valid solution. The second equation added no new information.

> *"Two travelers walking the exact same path — they agree on everything."*

**No Solution** *(Inconsistent)*: The lines are parallel — same slope, different intercepts. No intersection exists, and the constraints contradict each other.

> *"Two roads running side by side, never meeting, no matter how far you go."*

The fruit riddle falls squarely into the **third fate.**

---

## 🧬 The Hypothesis Connection

You begin to sense something beyond the math here. You say:

> *"This feels like testing a hypothesis — we assume something, then check whether the math breaks."*

You are *exactly right*, and the insight is deeper than it first appears.

What the system implicitly assumed was that prices were constant across both visits and that the data from both visits is accurate. What the math discovered was that under those assumptions, a contradiction emerges — and therefore at least one assumption must be false.

This is the same logic structure as **hypothesis testing** in science and statistics: assume a hypothesis is true, derive what the data should look like, compare to actual observations, and if a contradiction arises, reject the hypothesis.

In the fruit story, the "hypothesis" is that prices were consistent. The math rejects it.

> 💡 *This is not just algebra. This is the logic that powers machine learning, regression analysis, and scientific reasoning.*

---

## 🎓 The Conclusion That Unifies Everything

Let's step back and look at the full picture.

**What a system of equations really is:** a consistency test for information. It asks whether multiple constraints about the same unknowns can all be true simultaneously.

**What "no solution" really means:** the constraints contradict each other. The information you were given cannot all be correct at the same time. The solution set is empty — written as ∅.

**Why the intercept matters:** when both equations simplify to the same left-hand side (`2a + b`) but demand different right-hand sides (3 vs. 5), they are forcing the same quantity to be two different values. That is inherently impossible. The different intercepts on the graph are just the *visual expression* of this algebraic impossibility.

**The fastest way to detect it:** if the coefficients on the left are proportional across equations, but the constants on the right are *not* proportional in the same ratio — you have an inconsistent system. Check: `6a + 3b = 15` is `3×` the left side of `2a + b = 3`. But `15 ≠ 3 × 3 = 9`. **Inconsistent.**

---

## 🌟 One-Line Takeaway

> **"Each equation is a rule. The system asks whether a world exists where all rules are obeyed at once. Sometimes — no such world exists."**

---

*And as for Arbegla's riddle?*

The real answer was never a number. The real answer was:

> *"Your data is inconsistent. No solution exists — and the mathematics proves it."*

**That** is what it means to solve a system of equations. 🎯

---

*— Lesson 7 of the Systems of Linear Equations series. Connects directly to Lessons 1–6: The Troll's Riddle, Lauren's Café, The Art of the Setup, Solving by Substitution, A Conceptual Journey, and Worked Examples & Exercises.*
