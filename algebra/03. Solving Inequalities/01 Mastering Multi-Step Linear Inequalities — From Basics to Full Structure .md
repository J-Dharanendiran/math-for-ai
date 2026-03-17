# 📐 Multi-Step Linear Inequalities — From Basics to Full Structure

> *"You don't solve for x. You solve for when the statement is true."*

By the end of this lesson, you will understand not just *how* to solve inequalities, but *why* the algebra behaves the way it does — including the one critical exception that separates inequalities from equations. You will move from a single variable-on-both-sides case, through distribution, all the way to heavy multi-step problems, and you will be able to express, graph, and interpret every solution as a **region** — not just a number.

---

## 🔰 Part 1 — Variables on Both Sides (Core Mechanics)

### The Problem

```
-3p - 7 < p + 9
```

**Goal:** Isolate `p` and determine the full set of values that make this statement true.

Before a single step of algebra, notice the framing shift happening here. This problem is *not* asking "what is p?" It is asking **"for which values of p is the left side strictly less than the right side?"** That distinction matters more than it sounds — you are solving for a *region*, not hunting for a single point. The answer will be a direction on the number line, not a lone number.

---

### Step-by-Step Solution

**Step 1 — Move all variable terms to one side.**

Subtract `p` from both sides to collect every `p` term on the left:

```
-3p - 7 - p < p + 9 - p
-4p - 7 < 9
```

**Step 2 — Move constants to the other side.**

Add `7` to both sides to isolate the variable term:

```
-4p - 7 + 7 < 9 + 7
-4p < 16
```

**Step 3 — Isolate the variable.**

Divide both sides by `-4` to get `p` alone:

```
-4p ÷ -4  <  16 ÷ -4
```

**Step 4 — ⚠️ Flip the inequality sign.**

Because you divided by a **negative number**, the inequality sign *must* reverse. `<` becomes `>`:

```
p > -4
```

This is not optional. Skipping this step does not produce a slightly wrong answer — it produces the *exact opposite* answer.

---

### ⚠️ The One Rule That Separates Inequalities from Equations

> *"Whenever you multiply or divide both sides of an inequality by a negative number, you must flip the inequality sign. This is the only place where inequality algebra differs from equation algebra."*

Here is the intuition that makes this feel inevitable rather than arbitrary. On the number line, `3 < 5` is true. Multiply both sides by `-1` and you get `-3` and `-5`. Now `-3 > -5` — the order has reversed. Multiplying by a negative **reflects** both values across zero, and reflection swaps left and right. The flip in the sign is what *preserves truth* after that reflection. Skipping it destroys it.

---

### 📈 Graphing the Solution

The solution `p > -4` means every real number to the **right** of `-4` on the number line, not including `-4` itself.

```
←————————o══════════════════→
        -4
```

Two things to notice on this graph:

- **Open circle** at `-4` — because `>` is a strict inequality, `-4` itself is *not* included. Had the sign been `≥`, you would use a **closed (filled) circle** instead.
- **Shading goes right** — toward larger values, because those are the values that satisfy `p > -4`.

**Verification — always check your work with test values:**

Substitute `p = -3` (inside the solution region) into the original:
```
-3(-3) - 7 < (-3) + 9
9 - 7 < 6
2 < 6  ✓
```

Substitute `p = -5` (outside the solution region):
```
-3(-5) - 7 < (-5) + 9
15 - 7 < 4
8 < 4  ✗
```

The algebra is confirmed. Testing values is not busywork — it is how you verify that your *interpretation* of the region is correct.

---

### 🧠 Key Takeaways — Part 1

- An inequality uses the same algebraic engine as an equation — move terms, isolate, simplify — with exactly one exception.
- **Dividing or multiplying by a negative flips the sign.** This is the only structural difference between inequality and equation algebra.
- The solution is a **set** containing infinitely many values, not a single number.
- The boundary point is where the inequality becomes equality. Whether it is *included* depends on whether the sign is strict (`<`, `>`) or non-strict (`≤`, `≥`).
- Always verify with one test value *inside* and one *outside* the solution region.

---

### 🚀 Try It Yourself — Before Moving On

Solve this completely on your own:

```
-5q + 3 > q - 9
```

Work through every step. Check whether you need to flip the sign. Graph it. If you can do this cleanly without hesitation, you are ready for Part 2.

*Part 2 introduces distribution inside an inequality — which forces you to simplify before you can even begin isolating. The complexity increases, but the structure stays exactly the same.*

---

## 🔰 Part 2 — Distribution + Positive Division Case

### The Problem

```
5x + 7 > 3(x + 1)
```

**Goal:** Expand the right side, then isolate `x`.

Notice that the right side has parentheses. This is the key constraint here: **you cannot move terms until you distribute first.** Order of operations applies to inequalities exactly as it does to equations. If you try to subtract `3x` before expanding `3(x + 1)`, you are operating on an expression that hasn't been simplified yet — and the result will be wrong.

---

### Step-by-Step Solution

**Step 1 — Distribute first, always.**

Expand `3(x + 1)` on the right side:

```
5x + 7 > 3x + 3
```

**Step 2 — Move variable terms to one side.**

Subtract `3x` from both sides:

```
5x + 7 - 3x > 3x + 3 - 3x
2x + 7 > 3
```

**Step 3 — Move constants to the other side.**

Subtract `7` from both sides:

```
2x + 7 - 7 > 3 - 7
2x > -4
```

**Step 4 — Isolate the variable.**

Divide both sides by `2`:

```
x > -2
```

**No sign flip** — because `2` is positive. The direction of the inequality is preserved.

---

### 💡 Structural Insight Worth Internalizing

> *"Inequalities behave identically to equations at every step — until you divide or multiply by a negative. That is the only fork in the road."*

Students often feel that inequalities are a completely different system requiring a new set of rules. They are not. Distribution, combining like terms, adding and subtracting — all of it follows the same rules as equation algebra. The one additional rule — the sign flip — only activates when you scale by a negative number.

This example is especially valuable because there is **no sign flip here** — which means your brain now holds *both* cases side by side. Positive divisor: keep the sign. Negative divisor: flip the sign. That contrast is what makes the rule feel automatic rather than memorized.

---

### 📈 Graph + Interval Notation

**Number line:**

```
←————————o══════════════════→
        -2
```

- Open circle at `-2` — strict inequality, `-2` is excluded.
- Shading goes right toward larger values.

**Interval notation:**

```
(-2, +∞)
```

The parenthesis on `-2` confirms it is excluded. The parenthesis on `+∞` is *always* used, because infinity is not a real number you can ever reach — it is never "included."

**Verification:**

Test `x = 0` (inside the region):
```
5(0) + 7 > 3(0 + 1)
7 > 3  ✓
```

Test `x = -3` (outside the region):
```
5(-3) + 7 > 3(-3 + 1)
-8 > -6  ✗
```

Confirmed.

---

### 🧠 Key Takeaways — Part 2

- **Distribute before anything else.** Variables locked inside parentheses cannot be collected or isolated until the brackets are cleared.
- **Positive divisor = no flip.** The sign flip rule only activates on negative scaling — not every problem requires it.
- **Region thinking.** The solution `x > -2` is not one answer. It is an *infinite set* of answers expressed as a direction on the number line.
- Interval notation `(-2, +∞)` is the formal written form of that region.

---

### 🚀 A Question to Sit With Before Part 3

> *What would have happened if the divisor in the final step had been negative instead of positive? Would the answer still be `x > -2`, or would the direction reverse?*

Think it through before reading on. **Part 3 is the full consolidation** — distribution on *both* sides, negative division, and careful sign management all in one problem. If Parts 1 and 2 felt solid, Part 3 will feel like a natural conclusion rather than a jump in difficulty.

---

## 🔰 Part 3 — Full Multi-Step: Both Cases Combined

### The Problem

```
8x - 5(4x + 1) ≥ -1 + 2(4x - 3)
```

This is the pressure test. Distribution on both sides. A negative coefficient in front of a bracket. Variables that need to be consolidated across sides. And a division by a negative at the end that demands a sign flip. **Every skill from Parts 1 and 2 is required here simultaneously.** Nothing new is introduced — but everything is tested at once.

---

### Full Solution Walkthrough

**Step 1 — Distribute carefully on both sides.**

Left side — distribute `-5` across `(4x + 1)`. Notice that the negative carries through to *both* terms:

```
8x - 5(4x + 1) = 8x - 20x - 5
```

Right side — distribute `2` across `(4x - 3)`:

```
-1 + 2(4x - 3) = -1 + 8x - 6
```

The inequality now reads:

```
8x - 20x - 5 ≥ -1 + 8x - 6
```

**Step 2 — Combine like terms on each side independently.**

Left side: `8x - 20x = -12x`, with constant `-5`:
```
-12x - 5
```

Right side: `8x` stays, and `-1 - 6 = -7`:
```
8x - 7
```

Updated inequality:
```
-12x - 5 ≥ 8x - 7
```

**Step 3 — Move all variable terms to one side.**

Subtract `8x` from both sides:

```
-12x - 5 - 8x ≥ 8x - 7 - 8x
-20x - 5 ≥ -7
```

**Step 4 — Move constants to the other side.**

Add `5` to both sides:

```
-20x - 5 + 5 ≥ -7 + 5
-20x ≥ -2
```

**Step 5 — Divide by the coefficient and flip the sign.**

Divide both sides by `-20`. Because this is a *negative* divisor, `≥` becomes `≤`:

```
x ≤ 1/10
```

The solution is `x ≤ 1/10` — every real number at or to the left of one-tenth.

---

### ⚠️ Common Mistakes — The Three to Watch For

**Mistake 1 — Forgetting to distribute the negative fully.**
When you see `-5(4x + 1)`, the `-5` multiplies *every* term inside the bracket. A frequent error is writing `-20x + 1` instead of `-20x - 5`. The negative carries all the way through — not just to the first term.

**Mistake 2 — Forgetting to flip the sign after negative division.**
After arriving at `-20x ≥ -2`, dividing by `-20` without flipping gives `x ≥ 1/10` — which is the *exact opposite* of the correct answer. This is the most consequential error in inequality solving. It reverses the entire solution set while looking algebraically clean.

**Mistake 3 — Drifting the sign mid-problem.**
Some students start with `≥` and accidentally write `>` partway through when rewriting lines. Keep the original sign consistent until you reach the division step — that is the *only* moment it legitimately changes.

---

### 📈 Graph + Interval Notation

**Number line:**

```
←══════════════════●————————→
                  1/10
```

- **Closed (filled) circle** at `1/10` — because `≤` is non-strict, `1/10` is *included* in the solution.
- **Shading goes left** — toward smaller values, because those are the values satisfying `x ≤ 1/10`.

**Interval notation:**

```
(-∞, 1/10]
```

The square bracket on `1/10` confirms inclusion. The parenthesis on `-∞` is always used — infinity is never a reachable endpoint.

**Verification:**

Test `x = 0` (inside the region):
```
8(0) - 5(4(0) + 1) ≥ -1 + 2(4(0) - 3)
-5 ≥ -7  ✓
```

Test `x = 1` (outside the region):
```
8(1) - 5(4(1) + 1) ≥ -1 + 2(4(1) - 3)
-17 ≥ 1  ✗
```

Confirmed.

---

### 🧠 Mastery Summary — Part 3

**Algebra reliability.** Complex inequalities do not require new rules. They require *clean, disciplined execution* of the rules you already know. Every mistake at this level is an algebra execution error, not a conceptual gap. Distribution errors and sign flip omissions are the two biggest offenders — and both are entirely preventable.

**Order preservation.** The inequality sign is a statement about *order* on the number line. Every step you take must preserve that order relationship. Addition and subtraction preserve it automatically. Multiplication and division preserve it only when the scaling factor is positive — negative scaling reverses order, and the flip restores it.

**Boundary understanding.** The solution always has a boundary point — the value where the two sides are exactly equal. Whether that point is *included* depends entirely on the sign: strict signs (`<`, `>`) exclude the boundary, non-strict signs (`≤`, `≥`) include it. That is why the graph circle is either open or closed.

---

### 🚀 Final Challenge — Prove It to Yourself

Solve this completely. No calculator. Show every step.

```
6 - 2(3x - 4) < 5x + 8
```

Distribute, collect, isolate, decide whether to flip, graph it, write the interval notation, and verify with one test value inside and one outside.

> *"If you can work through this cleanly — without hesitation, without skipping steps, and with the correct direction on the number line — you are solid on multi-step linear inequalities."*

---

## 🏁 Final Consolidation — What You Have Actually Built

### The Four Things You Now Understand Deeply

**📌 Inequalities = balance + order.**
Equations preserve equality. Inequalities preserve equality *and* order — the directional relationship between left and right must remain correct through every transformation you apply.

**📌 Solution = region, not a single value.**
When you solve an equation, you find the *point* where two expressions are equal. When you solve an inequality, you find the entire *region* where one expression dominates the other. That region is infinite, expressed as a direction on the number line or as an interval.

**📌 Sign flip logic.**
The flip is not a rule to memorize — it is a geometric fact. Negative scaling reflects the number line. Left becomes right. Smaller becomes larger. The flip in the inequality sign is what preserves truth after that reflection. It happens exactly *once* in any problem: when you divide or multiply by a negative number.

**📌 Graph interpretation.**
The number line is not decoration. It is a *visual map* of the solution set. The open circle marks an excluded boundary. The closed circle marks an included one. The shaded direction tells you which values make the original statement true.

---

### Why This Three-Part Structure Works

This lesson was built in three deliberate layers — not because the math requires three separate topics, but because understanding needs to be assembled gradually to feel like a *unified system* rather than a pile of disconnected rules.

**Part 1** gave you the core mechanics with one challenge: variables on both sides. It forced you to confront the sign flip in its simplest possible context.

**Part 2** added distribution — which means you cannot even begin isolating until you expand first. It also showed the *opposite* of Part 1's sign flip scenario, so your brain now holds both cases side by side in contrast.

**Part 3** stacked everything at once. Distribution on both sides, negative coefficients, careful combining, and a negative divisor requiring a flip. This is not a new topic — it is Parts 1 and 2 applied *simultaneously under pressure*.

Each part ended with a practice prompt so the knowledge never stayed passive. Each section built directly on the one before it. And this final consolidation exists not to repeat information, but to *name* what you have actually constructed — a complete mental model of inequalities as a system.

> *"This is how algebra fluency is built: not by memorizing rules in isolation, but by seeing the same structure survive at every level of complexity."*

---

*Next: Compound Inequalities — where two inequality conditions must be satisfied simultaneously, and the solution becomes an intersection or union of regions.*
