# ✏️ Systems of Linear Equations — Worked Examples & Exercises

> *"Tell me and I forget. Teach me and I remember. Involve me and I learn."*
> — Benjamin Franklin

---

## 🗺️ How to Use This File

This document is the **practice companion** to `systems_of_equations_theory.md`. Where that file asks *why*, this file asks *how* — and more importantly, it asks *you* to try. Every worked example is followed by an explanation of what just happened, so the steps never feel arbitrary.

Work through the examples with a pencil. Cover the solutions. Struggle a little. Then check.

> *"The struggle is not a sign you're doing it wrong. It is the feeling of your brain building new connections."*

---

## 🔥 Warm-Up: One Equation, Infinite Solutions

Before we deal with systems, let's deeply feel what a *single* equation does.

**The equation:**
```
x + y = 6
```

**What it means:** For every real number you pick for `x`, there is exactly one `y` that makes the equation true. Specifically: `y = 6 − x`.

**The parametric solution** — letting `t` stand for any freely chosen real number:

```
x = t
y = 6 − t

→  (x, y) = (t,  6 − t)   for any real t
```

**Spot-checking three values:**

| `t` | `x` | `y = 6 − t` | Check: `x + y = 6`? |
|-----|-----|-------------|---------------------|
| 0   | 0   | 6           | 0 + 6 = 6 ✅         |
| 2   | 2   | 4           | 2 + 4 = 6 ✅         |
| -1  | -1  | 7           | -1 + 7 = 6 ✅        |

Every row is a valid solution. There are infinitely many. **One free parameter `t` = one degree of freedom = one line.**

> 💡 *Before you see the second equation, this is all you have: a line. Infinite possibilities. No single answer.*

---

## ⚔️ Example 1: Elimination (Clean Case)

**The system (from the Khan Academy balance-scale video):**
```
(1)  2X + Y = 8
(2)   X + Y = 5
```

**Why elimination works here:** Both equations contain the term `+Y` with the same coefficient (`1`). Subtracting equation (2) from equation (1) will make the `Y` terms cancel exactly.

**Step 1 — Subtract equation (2) from equation (1):**

```
Left side:   (2X + Y) − (X + Y)
           = 2X + Y − X − Y
           = (2X − X) + (Y − Y)
           = X + 0
           = X

Right side:  8 − 5 = 3
```

**Result:** `X = 3`

**Step 2 — Substitute `X = 3` back into equation (2):**
```
X + Y = 5
3 + Y = 5
    Y = 5 − 3
    Y = 2
```

**Step 3 — Verify in both original equations:**
```
Equation (1):  2(3) + 2 = 6 + 2 = 8  ✅
Equation (2):  3 + 2 = 5             ✅
```

**✅ The solution is `(X, Y) = (3, 2)`.**

> 🔍 *Notice what elimination actually did: it used the second equation as a "known weight" and removed it from the first. Because `X + Y = 5` is a true statement, subtracting it from both sides of the first equation kept everything balanced — and eliminated one unknown.*

---

## ⚙️ Example 2: Elimination With Scaling (One Equation)

> *"When the coefficients don't cooperate immediately, you don't wait — you create the conditions for cancellation."*

**The system:**
```
(1)  5x − 10y = 15
(2)  3x −   2y =  3
```

**The obstacle:** The `y` coefficients are `-10` and `-2`. They don't cancel by simple subtraction. We need to *manipulate* one equation so the `y` terms become equal in magnitude with opposite signs.

**Strategy:** Multiply equation (2) by `−5`, which will turn its `−2y` into `+10y`. Then when we add the two equations, `−10y + 10y = 0`.

**Step 1 — Multiply equation (2) by `−5`:**
```
−5 × (3x − 2y = 3)
  →   −15x + 10y = −15     ... (Equation 2, transformed)
```

> ⚠️ *Critical: multiply every term — including the right-hand side. The `3` on the right becomes `−15`.*

**Step 2 — Add the transformed equation to equation (1):**
```
    5x − 10y =  15
+  −15x + 10y = −15
──────────────────────
  −10x +   0 =   0
```

**Step 3 — Solve for `x`:**
```
−10x = 0
   x = 0
```

**Step 4 — Substitute `x = 0` into the original equation (2):**
```
3(0) − 2y = 3
      −2y = 3
        y = −3/2
```

**Step 5 — Verify in both original equations:**
```
Equation (1):  5(0) − 10(−3/2) = 0 + 15 = 15  ✅
Equation (2):  3(0) −  2(−3/2) = 0 +  3 =  3  ✅
```

**✅ The solution is `(x, y) = (0, −3/2)`.**

> 💡 *The transformed equation was scaffolding — we used it to find `x`, then immediately returned to the originals for back-substitution. Always go back to the originals. The transformed equations are working tools, not final references.*

---

## 🏆 Example 3: Elimination With Scaling (Both Equations — LCM Method)

> *"Sometimes neither equation will cooperate alone. Then you scale both — and let the LCM be your guide."*

**The system:**
```
(1)  5x + 7y = 15
(2)  7x − 3y =  5
```

**The obstacle:** The `x` coefficients are `5` and `7`. Neither is a multiple of the other. We need to find the **Least Common Multiple** so both equations can be scaled to the same `x` coefficient.

```
LCM(5, 7) = 35
```

We want one equation to have `+35x` and the other to have `−35x`. Then they cancel when added.

**Step 1 — Multiply equation (1) by `7` (to get 5×7 = 35x):**
```
7 × (5x + 7y = 15)
  →  35x + 49y = 105
```

**Step 2 — Multiply equation (2) by `−5` (to get 7×−5 = −35x):**
```
−5 × (7x − 3y = 5)
   →  −35x + 15y = −25
```

**Step 3 — Add the two transformed equations:**
```
   35x + 49y =  105
+  −35x + 15y =  −25
───────────────────────
      0 + 64y =   80
```

**Step 4 — Solve for `y`:**
```
64y = 80
  y = 80/64 = 5/4
```

**Step 5 — Substitute `y = 5/4` into original equation (2):**
```
7x − 3(5/4) = 5
7x − 15/4   = 5
7x           = 5 + 15/4 = 20/4 + 15/4 = 35/4
 x           = 35/28 = 5/4
```

**Step 6 — Verify in both original equations:**
```
Equation (1):  5(5/4) + 7(5/4) = 25/4 + 35/4 = 60/4 = 15  ✅
Equation (2):  7(5/4) − 3(5/4) = 35/4 − 15/4 = 20/4 =  5  ✅
```

**✅ The solution is `(x, y) = (5/4, 5/4)`.**

> 🌟 *Both unknowns share the same value — a beautiful coincidence. But notice what the LCM gave us: a systematic, guaranteed path to cancellation even when the numbers looked messy.*

---

## 🔄 Example 4: Substitution Method

> *"When one equation hands you a variable already solved, use it. That is an invitation you should never refuse."*

**The system:**
```
(1)  −3x − 4y = −2
(2)       y = 2x − 5
```

**Why substitution here:** Equation (2) already defines `y` in terms of `x`. It is saying: *"Wherever you see y, you may write 2x − 5 instead."* That is the substitution key.

**Step 1 — Substitute `y = 2x − 5` into equation (1):**
```
−3x − 4(2x − 5) = −2
```

> ⚠️ *The parentheses are not decoration. The entire expression `2x − 5` is multiplied by `−4`. Dropping them is the single most common error in substitution.*

**Step 2 — Distribute `−4` across the parenthesis:**
```
−3x − 4(2x) − 4(−5) = −2
−3x − 8x + 20        = −2
```

> 💡 *`−4 × (−5) = +20`, not `−20`. A negative times a negative is always positive. Take a breath at every sign.*

**Step 3 — Combine like terms:**
```
−11x + 20 = −2
```

**Step 4 — Isolate `x`:**
```
−11x = −2 − 20
−11x = −22
   x = −22 ÷ −11
   x = 2
```

**Step 5 — Back-substitute `x = 2` into equation (2):**
```
y = 2(2) − 5 = 4 − 5 = −1
```

**Step 6 — Verify in both original equations:**
```
Equation (1):  −3(2) − 4(−1) = −6 + 4 = −2  ✅
Equation (2):  −1 = 2(2) − 5 = 4 − 5 = −1   ✅
```

**✅ The solution is `(x, y) = (2, −1)`.**

> *"Substitution and elimination are different roads to the same city. The destination — the intersection of two lines — was always `(2, −1)`. The method only changed how we got there."*

---

## 🔍 Example 5: Diagnosing the Edge Cases

### 🔁 Case A — Infinite Solutions (Dependent Equations)

**The system:**
```
(1)   x + y = 5
(2)  2x + 2y = 10
```

**What happens if you try to eliminate:** Multiply equation (1) by `−2` and add to equation (2):
```
  2x + 2y =  10
+ −2x − 2y = −10
─────────────────
   0 + 0   =  0
```

The result `0 = 0` is always true — a **tautology**. This tells us the equations are **dependent**: the second equation is just `2 × (first equation)` in disguise. They describe the exact same line.

**The parametric solution:**
```
(x, y) = (t, 5 − t)   for any real t
```

DoF = 1. Infinitely many solutions.

---

### ❌ Case B — No Solution (Inconsistent Equations)

**The system:**
```
(1)   x + y = 5
(2)  2x + 2y = 11
```

**What happens if you try to eliminate:** Multiply equation (1) by `−2` and add to equation (2):
```
  2x + 2y =  11
+ −2x − 2y = −10
──────────────────
   0 + 0   =  1
```

The result `0 = 1` is **never true** — a **contradiction**. No pair `(x, y)` can satisfy both equations. The lines are parallel; they never intersect.

**Geometric picture:** Both lines have slope `−1`. But one has y-intercept `5`, the other has y-intercept `5.5`. Parallel. Separated. No meeting point.

---

### 📊 Diagnostic Table

| Result After Elimination | What It Means          | Number of Solutions |
|--------------------------|------------------------|---------------------|
| `x = number`             | Independent equations  | **Exactly one**     |
| `0 = 0`                  | Dependent equations    | **Infinitely many** |
| `0 = nonzero`            | Inconsistent equations | **None**            |

---

## 📊 Visualization: The Geography of Solutions

> *"A graph doesn't just show you the answer — it shows you the entire landscape of near-misses, close calls, and the one perfect spot."*

Consider Lauren's Café system:
```
x + y = 80       (Quantity line — Blue)
3x + 2y = 220    (Cost line — Green)
```

Think of the coordinate plane as a **map**. Each equation draws a boundary:

- **On the blue line:** exactly 80 kg ordered. Step off it in either direction — too much or too little.
- **On the green line:** exactly $220 spent. Step off it — over budget or under budget.
- **At their intersection:** both conditions satisfied. This single point `(60, 20)` is the only location on the map where both constraints hold simultaneously.

Points near the intersection are *almost* solutions — but "almost" is not good enough. A system demands perfect simultaneous satisfaction.

```
💡 To visualize any system interactively:
   → Go to desmos.com
   → Type each equation on its own line
   → Find the intersection point — that is your solution
```

---

## 🏋️ Exercises — Try These Yourself

**Instructions:** Solve each system using the method you feel is most appropriate. Identify whether the system has a unique solution, infinite solutions, or no solution. Verify every answer in both original equations.

---

**Exercise 1** *(Clean elimination — good starting point)*
```
2x + 3y = 12
 x + 3y =  9
```

---

**Exercise 2** *(Scaling required — one equation)*
```
4x −  y = 10
2x + 3y =  12
```

---

**Exercise 3** *(Substitution invitation)*
```
x = 3y − 1
2x + y = 12
```

---

**Exercise 4** *(LCM elimination — both equations need scaling)*
```
3x + 4y = 24
5x − 2y = 10
```

---

**Exercise 5** *(Diagnose: unique, infinite, or none?)*
```
6x − 4y = 8
3x − 2y = 4
```

---

**Exercise 6** *(Diagnose: unique, infinite, or none?)*
```
2x + 5y = 7
4x + 10y = 15
```

---

## ✅ Solutions

### Exercise 1

Subtract equation (2) from equation (1):
```
(2x + 3y) − (x + 3y) = 12 − 9
x = 3
```
Substitute into equation (2): `3 + 3y = 9 → 3y = 6 → y = 2`.

**Solution: `(3, 2)`** ✅

---

### Exercise 2

Multiply equation (2) by `−2`: `−4x − 6y = −24`. Add to equation (1):
```
4x −  y =  10
−4x − 6y = −24
─────────────────
   −7y = −14
     y = 2
```
Substitute into equation (1): `4x − 2 = 10 → 4x = 12 → x = 3`.

**Solution: `(3, 2)`** ✅

---

### Exercise 3

Substitute `x = 3y − 1` into the second equation:
```
2(3y − 1) + y = 12
6y − 2 + y    = 12
7y            = 14
 y            = 2
```
Then `x = 3(2) − 1 = 5`.

**Solution: `(5, 2)`** ✅

---

### Exercise 4

LCM(3, 5) = 15. Multiply equation (1) by 5: `15x + 20y = 120`. Multiply equation (2) by `−3`: `−15x + 6y = −30`. Add:
```
26y = 90
  y = 90/26 = 45/13
```
Substitute back into equation (2): `5x − 2(45/13) = 10 → 5x = 10 + 90/13 = 220/13 → x = 44/13`.

**Solution: `(44/13, 45/13)`** ✅

---

### Exercise 5

Equation (1) divided by 2: `3x − 2y = 4`. This is **identical** to equation (2). The equations are dependent.

**Result: Infinite solutions.** Parametric form: `(x, y) = (t, (3t − 4)/2)` for any real `t`. ♾️

---

### Exercise 6

Multiply equation (1) by 2: `4x + 10y = 14`. Compare to equation (2): `4x + 10y = 15`. Same left side, different right side — a contradiction: `14 ≠ 15`.

**Result: No solution.** The lines are parallel and never intersect. ❌

---

## 🔑 Method Selection Guide

> *"Mathematical fluency is not knowing one method perfectly — it is knowing which method to reach for, and why."*

Use this as your decision guide when approaching any system:

- **Reach for substitution** when one equation is already solved for a variable (e.g., `y = 3x + 2`), or can be isolated cleanly in one step.
- **Reach for elimination** when both equations are in standard form `ax + by = c` and the coefficients share an obvious common multiple.
- **Scale one equation** when only one coefficient needs adjustment to match the other.
- **Use LCM on both equations** when neither coefficient is a multiple of the other.
- **Check for edge cases first** — look at whether the ratio of `x`-coefficients equals the ratio of `y`-coefficients. If they do, prepare for dependence or inconsistency.

---

## 🏁 Final Reflection

You've now worked through the full arc:

1. 🔢 **Single equation** — a line, infinite possibilities, one free parameter.
2. ⚔️ **Two independent equations** — an intersection, one unique solution, no free parameters.
3. 🔄 **Substitution and elimination** — two roads to the same destination.
4. 🔍 **Edge cases** — when the system whispers `0 = 0` or shouts `0 = 1`.

> *"Every solved system is a small proof that the universe of mathematics is consistent — that when the constraints are right, there is exactly one truth hiding at their intersection. That truth was always there. You just learned how to find it."* 🌟

---

*📌 Return to: **`systems_of_equations_theory.md`** — for the deep conceptual explanation of why every step in this document is justified.*
