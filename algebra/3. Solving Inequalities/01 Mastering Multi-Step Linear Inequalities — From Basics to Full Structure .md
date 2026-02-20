# Multi-Step Linear Inequalities — From Basics to Full Structure

By the end of this lesson, you will understand not just *how* to solve inequalities, but *why* the algebra behaves the way it does — including the one critical exception that separates inequalities from equations. You will move from a single variable-on-both-sides case, through distribution, all the way to heavy multi-step problems, and you will be able to express, graph, and interpret every solution as a region — not just a number.

---

## 🔰 Part 1 — Variables on Both Sides (Core Mechanics)

### 1️⃣ The Problem

```
-3p - 7 < p + 9
```

**Goal:** Isolate `p` and determine the full set of values that make this statement true.

This is not asking "what is p?" It is asking "for which values of p is the left side strictly less than the right side?" That shift in framing matters — you are solving for a region, not a point.

---

### 2️⃣ Step-by-Step Solution

**Step 1 — Move variable terms to one side.**

Subtract `p` from both sides to collect all `p` terms on the left:

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
p > -4
```

**Step 4 — Flip the sign.**

Because you divided by a **negative number**, the inequality sign reverses. `<` becomes `>`. This is not optional — skipping this step produces a completely wrong solution set.

---

### ⚠️ Critical Rule

> **Whenever you multiply or divide both sides of an inequality by a negative number, you must flip the inequality sign. This is the only place where inequality algebra differs from equation algebra.**

Here is the intuition behind it. On the number line, `3 < 5` is true. Multiply both sides by `-1` and you get `-3` and `-5`. Now `-3 > -5` — the order reversed. Multiplying by a negative reflects both values across zero, and reflection swaps left and right. The flip preserves truth; skipping it destroys it.

---

### 📈 Graphing the Solution

The solution `p > -4` means every real number to the **right** of `-4` on the number line, not including `-4` itself.

```
←————————o══════════════════→
        -4
```

- **Open circle** at `-4` — because `>` is strict, `-4` is not included. If the inequality were `≥`, you would use a **closed (filled) circle**.
- **Shading goes right** — toward larger values, because those are the values that satisfy `p > -4`.

**Verification check:** Substitute `p = -3` (inside the region) into the original:

```
-3(-3) - 7 < (-3) + 9
9 - 7 < 6
2 < 6  ✓
```

Substitute `p = -5` (outside the region):

```
-3(-5) - 7 < (-5) + 9
15 - 7 < 4
8 < 4  ✗
```

The algebra is confirmed. Testing values is not optional busywork — it is how you verify that your region interpretation is correct.

---

### 🧠 Key Takeaways

- An inequality has the same algebraic engine as an equation — move terms, isolate, simplify — with one exception.
- Dividing or multiplying by a negative number flips the inequality sign. This is the only structural difference.
- The solution is a **set** — infinitely many values — not a single number.
- The boundary point is where the inequality becomes equality. Whether it is included depends on whether the sign is strict (`<`, `>`) or non-strict (`≤`, `≥`).
- Always verify by testing one value inside and one value outside the solution region.

---

### 🚀 Follow-Up Prompt

Before moving on, solve this on your own:

```
-5q + 3 > q - 9
```

Work through every step. Check whether you need to flip the sign. Graph it. If you can do this cleanly without hesitation, you are ready for Part 2.

**Part 2 introduces distribution inside an inequality** — which forces you to simplify before you can even begin isolating. The complexity increases, but the structure stays the same.

---

## 🔰 Part 2 — Distribution + Positive Division Case

### 1️⃣ The Problem

```
5x + 7 > 3(x + 1)
```

**Goal:** Expand the right side, then isolate `x`. Notice that the right side has parentheses — you cannot move terms until you distribute first. Order of operations applies to inequalities exactly as it does to equations.

---

### 2️⃣ Step-by-Step Solution

**Step 1 — Distribute.**

Expand `3(x + 1)` on the right side:

```
5x + 7 > 3x + 3
```

**Step 2 — Combine like terms.**

Both sides are already simplified. No combining needed here — move straight to collecting variables.

**Step 3 — Move variable terms to one side.**

Subtract `3x` from both sides:

```
5x + 7 - 3x > 3x + 3 - 3x
2x + 7 > 3
```

**Step 4 — Move constants to the other side.**

Subtract `7` from both sides:

```
2x + 7 - 7 > 3 - 7
2x > -4
```

**Step 5 — Isolate the variable.**

Divide both sides by `2`:

```
x > -2
```

**No sign flip** — because `2` is positive. The direction of the inequality is preserved.

---

### ⚠️ Structural Insight

> **Inequalities behave identically to equations at every step — until you divide or multiply by a negative. That is the only fork in the road. Distribution, combining like terms, adding and subtracting — all of it follows the same rules as equations.**

This is worth internalizing deeply. Students often feel that inequalities are a completely different system. They are not. They are linear equations with one additional rule attached: preserve order when you scale by a negative.

This example is valuable specifically because there is **no sign flip** — which means your brain now has both cases on record. Positive divisor: keep the sign. Negative divisor: flip the sign. That contrast is what makes the rule automatic.

---

### 📈 Graph + Interval Form

**Number line:**

```
←————————o══════════════════→
        -2
```

- Open circle at `-2` — strict inequality, `-2` is excluded.
- Shading goes right.

**Interval notation:**

```
(-2, +∞)
```

The parenthesis on `-2` confirms it is excluded. The parenthesis on `+∞` is always used because infinity is not a real number you can reach — it is never "included."

**Verification:** Test `x = 0`:

```
5(0) + 7 > 3(0 + 1)
7 > 3  ✓
```

Test `x = -3`:

```
5(-3) + 7 > 3(-3 + 1)
-15 + 7 > 3(-2)
-8 > -6  ✗
```

Confirmed.

---

### 🧠 Key Takeaways

- **Distribute before anything else.** You cannot collect or isolate variables that are still locked inside parentheses. Expansion comes first.
- **Positive divisor = no flip.** The sign flip rule only activates on negative scaling. Not every inequality requires it.
- **Region thinking.** The solution `x > -2` is not one answer — it is an infinite set of answers expressed as a direction on the number line.
- Interval notation is the formal way to write that region: `(-2, +∞)` means all real numbers greater than `-2`.

---

### 🚀 Follow-Up Prompt

Here is the natural next question to sit with:

> *What would have happened if the divisor in Step 5 had been negative instead of positive?*

Think it through before looking at Part 3. Specifically: would the answer still be `x > -2`, or would the direction reverse?

**Part 3 is the full consolidation.** It combines distribution on *both* sides, negative division, and careful sign management — all in one problem. If Parts 1 and 2 felt solid, Part 3 will feel like a natural conclusion.

---

## 🔰 Part 3 — Full Multi-Step + Both Cases Combined

### 1️⃣ The Complex Example

```
8x - 5(4x + 1) ≥ -1 + 2(4x - 3)
```

This is the pressure test. You have distribution on both sides, a negative coefficient in front of a bracket, variables that will need to be consolidated across sides, and a division by a negative at the end. Every skill from Parts 1 and 2 is required here simultaneously.

---

### 2️⃣ Full Solution Walkthrough

**Step 1 — Distribute carefully on both sides.**

Left side: distribute `-5` across `(4x + 1)`:

```
8x - 5(4x + 1) = 8x - 20x - 5
```

Right side: distribute `2` across `(4x - 3)`:

```
-1 + 2(4x - 3) = -1 + 8x - 6
```

The inequality now reads:

```
8x - 20x - 5 ≥ -1 + 8x - 6
```

**Step 2 — Combine like terms on each side independently.**

Left side: `8x - 20x = -12x`, constant is `-5`:

```
-12x - 5
```

Right side: `8x` stays, `-1 - 6 = -7`:

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

**Step 5 — Divide by the coefficient.**

Divide both sides by `-20`:

```
x ≤ 1/10
```

**Step 6 — Flip the sign.**

Because you divided by `-20` (a negative number), the inequality flips. `≥` becomes `≤`.

The solution is:

```
x ≤ 1/10
```

---

### ⚠️ Common Mistakes Section

**Mistake 1 — Forgetting to distribute the negative.**

When you see `-5(4x + 1)`, the `-5` multiplies *both* terms inside. A common error is writing `-5(4x + 1) = -20x + 1` instead of `-20x - 5`. The negative carries through to every term in the bracket, not just the first one.

**Mistake 2 — Forgetting to flip the sign after negative division.**

After arriving at `-20x ≥ -2`, dividing by `-20` without flipping gives `x ≥ 1/10` — which is the exact opposite of the correct answer. This is the most consequential algebraic error in inequality solving, because it reverses the entire solution set.

**Mistake 3 — Mixing inequality directions mid-problem.**

Some students start with `≥` and accidentally write `>` partway through, especially when rewriting lines. Keep the original sign consistent until you reach the division step — the only moment it changes.

---

### 📈 Graph + Interval Notation

**Number line:**

```
←══════════════════●————————→
                  1/10
```

- **Closed (filled) circle** at `1/10` — because `≤` is non-strict, `1/10` is included.
- **Shading goes left** — toward smaller values, because those are the values satisfying `x ≤ 1/10`.

**Interval notation:**

```
(-∞, 1/10]
```

The square bracket on `1/10` confirms it is included. The parenthesis on `-∞` is always used.

**Verification:** Test `x = 0` (inside the region):

```
8(0) - 5(4(0) + 1) ≥ -1 + 2(4(0) - 3)
0 - 5(1) ≥ -1 + 2(-3)
-5 ≥ -1 - 6
-5 ≥ -7  ✓
```

Test `x = 1` (outside the region):

```
8(1) - 5(4(1) + 1) ≥ -1 + 2(4(1) - 3)
8 - 5(5) ≥ -1 + 2(1)
8 - 25 ≥ -1 + 2
-17 ≥ 1  ✗
```

Confirmed.

---

### 🧠 Mastery Summary

**Algebra reliability.** Complex inequalities do not require new rules — they require clean, disciplined execution of the rules you already know. Every mistake at this level is an algebra execution error, not a conceptual failure. Distribution errors and sign flip omissions are the two biggest offenders.

**Order preservation.** The inequality sign is a statement about order on the number line. Every step you take must preserve that order relationship. Addition and subtraction preserve it automatically. Multiplication and division preserve it only when the scaling factor is positive — negative scaling reverses order, and the flip restores it.

**Boundary understanding.** The solution always has a boundary point — the value where the two sides are exactly equal. Whether that point is included in the solution depends on the sign: strict (`<`, `>`) excludes the boundary, non-strict (`≤`, `≥`) includes it. This is why the circle on the graph is either open or closed.

---

### 🚀 Final Reader Challenge

Solve this completely. No calculator. Show every step.

```
6 - 2(3x - 4) < 5x + 8
```

Distribute, collect, isolate, decide whether to flip, graph it, write the interval notation, and verify with one test value inside and one outside.

> **If you can work through this cleanly — without hesitation, without skipping steps, and with the correct direction on the number line — you are solid on multi-step linear inequalities.**

---

## 🏁 Final Consolidation Section

### What You Now Understand

**Inequalities = balance + order.**
Equations preserve equality. Inequalities preserve equality *and* order — the relationship between left and right must remain directionally correct through every transformation.

**Solution = region, not a single value.**
When you solve an equation, you find the point where two expressions are equal. When you solve an inequality, you find the entire region where one expression dominates the other. That region is infinite, and it is expressed as a direction on the number line or as an interval.

**Sign flip logic.**
The flip is not a rule to memorize — it is a geometric fact. Negative scaling reflects the number line. Left becomes right. Smaller becomes larger. The flip in the inequality sign is what preserves truth after that reflection. It happens exactly once: when you divide or multiply by a negative number.

**Graph interpretation.**
The number line is not decoration. It is a visual map of the solution set. The open circle marks an excluded boundary. The closed circle marks an included one. The shaded direction tells you which values make the original statement true.

---

> *"You don't solve for x. You solve for when the statement is true."*

This reframe is the deepest lesson here. An inequality is not asking you to find a value — it is asking you to find a truth condition. The algebra is just the tool that maps out where that truth lives on the number line.

---

### Why This Structure Works

This lesson was built in three deliberate layers — not because the math requires three separate topics, but because your brain needs complexity introduced gradually to internalize it as one unified system.

**Part 1** gave you the core mechanics with one challenge: variables on both sides. It forced you to confront the sign flip in its simplest context.

**Part 2** added distribution — which means you cannot even begin isolating until you expand. It also showed the *opposite* of Part 1's sign flip scenario, so your brain now holds both cases side by side.

**Part 3** stacked everything. Distribution on both sides, negative coefficients, careful combining, and a negative divisor requiring a flip. This is not a new topic — it is Parts 1 and 2 applied simultaneously under pressure.

Each part ended with a practice prompt so the knowledge does not stay passive. Each section built directly on the one before it, with no gaps and no redundancy. And the final consolidation exists not to repeat information, but to name what you have actually built — a complete mental model of inequalities as a system.

This is how algebra fluency is built: not by memorizing rules in isolation, but by seeing the same structure survive at every level of complexity.

---

*Next: Compound Inequalities — where two inequality conditions must be satisfied simultaneously, and the solution becomes an intersection or union of regions.*
