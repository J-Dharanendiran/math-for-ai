# When "AND" Creates a Bounded Region — The Structure Behind Chain Inequalities

In the previous file, you saw how OR combines two inequality regions into a union — and how, under the right structural conditions, that union can expand to cover the entire number line with no gaps. This file flips that logic entirely. AND compound inequalities do not expand — they **restrict**. Instead of asking "which numbers satisfy at least one condition," you are now asking "which numbers satisfy both conditions simultaneously." The result is always an intersection, and intersections can only be equal in size or smaller than either region alone.

---

## 🔗 Where This Connects

In the OR file, the word "or" was doing set union — a number qualified for the solution set by passing either test. The answer could be two disconnected regions, one continuous region, or the entire number line, depending on whether the regions overlapped.

AND works as set intersection — a number only qualifies if it passes **both** tests at once. This is a fundamentally stricter condition. The solution cannot be larger than either individual region, and it can shrink all the way down to a single point or disappear entirely if the two regions have no overlap.

This is also why AND inequalities are often written as a **chain** — a compressed notation that makes the intersection structure visually explicit.

---

## 🎬 The Given Compound Inequality

$$-10 \leq 2x - 4 < 6$$

This is a chain inequality. It looks like one expression, but it is actually two conditions fused together:

$$-10 \leq 2x - 4 \quad \textbf{and} \quad 2x - 4 < 6$$

In plain language: the expression $2x - 4$ must live **between** $-10$ and $6$ — at or above $-10$, and strictly below $6$. The chain notation is just a shorthand that keeps both conditions in view at once, which makes it easier to see the bounded region you are solving for.

---

## Step 1 — Operate on All Three Parts Simultaneously

This is the key mechanical insight of chain inequalities. Because both conditions share the same middle expression, you can isolate $x$ by performing the same operation on all three parts at once — left, middle, and right. This is legal for the same reason that doing the same thing to both sides of an equation preserves balance: order-preserving operations applied uniformly do not disturb the relationships.

**Eliminate the constant first.** Add 4 to all three parts:

$$-10 + 4 \leq 2x - 4 + 4 < 6 + 4$$

$$-6 \leq 2x < 10$$

**Isolate $x$.** Divide all three parts by 2 — a positive number, so no sign flip:

$$\frac{-6}{2} \leq \frac{2x}{2} < \frac{10}{2}$$

$$\boxed{-3 \leq x < 5}$$

That is the complete solution. Every real number between $-3$ and $5$, including $-3$ and excluding $5$.

---

## ⚠️ The Sign Flip Rule Inside a Chain

Because you divided by $+2$, no flip was needed here. But it is worth understanding precisely what would happen if the divisor were negative — because this is the most common place students lose points.

Suppose the final step required dividing by $-2$ instead. You would flip **both** inequality signs simultaneously:

$$-6 \leq 2x < 10 \quad \xrightarrow{\div (-2)} \quad 3 \geq x > -5$$

Which you would then rewrite in standard left-to-right order as $-5 < x \leq 3$. Both signs flipped, and the direction of the entire chain reversed. Miss either flip and the answer is wrong. The rule is the same as in single inequalities — negative scaling reverses order — but in a chain, it applies to both boundary relationships at once.

---

## 🧠 The Structural Question

With OR, the structural question was: *do the regions leave a gap?* If not, the answer is all real numbers.

With AND, the structural question is the opposite: *do the regions overlap at all?* The solution is exactly the overlapping portion — nothing more.

Here, the first condition gives $x \geq -3$ and the second gives $x < 5$. These two regions share every number between $-3$ and $5$. That shared stretch is the intersection, and it is a **bounded region** — it has a definite left boundary and a definite right boundary. This is the structural signature of AND: it produces a finite interval rather than an infinite one.

What would cause the intersection to shrink further? If the two boundaries crossed in the wrong direction. For instance, if the first condition gave $x \geq 7$ and the second gave $x < 3$, there would be no overlap — no number is simultaneously at least 7 and less than 3. The intersection would be empty, and the answer would be "no solution." That is the AND counterpart to the "all real numbers" outcome in OR: a complete collapse rather than complete coverage.

---

## 📉 Visualizing the Region

```
First condition   (x ≥ -3):
————————————●══════════════════════→
            -3

Second condition  (x < 5):
←══════════════════════○————————————
                       5

Intersection (AND — both must hold):
————————————●══════════○————————————
            -3         5
```

The closed circle at $-3$ reflects the $\leq$ sign — the boundary is included. The open circle at $5$ reflects the $<$ sign — the boundary is excluded. The shaded region is finite and bounded on both sides. This is what AND always produces when the two regions genuinely overlap: a segment of the number line, not a ray extending to infinity.

**Interval notation:** $[-3, 5)$

The square bracket on $-3$ confirms it is included. The parenthesis on $5$ confirms it is excluded. If both boundaries were included, you would write $[-3, 5]$. If neither were, you would write $(-3, 5)$.

---

## 🔍 Verifying the Boundaries

Testing boundary and interior points is not optional — it is how you confirm that the algebra was clean and the interval notation is correct.

**At $x = -3$** (left boundary, should be included):

$$2(-3) - 4 = -10 \quad \Rightarrow \quad -10 \leq -10 < 6 \quad \checkmark$$

Both conditions hold. $-3$ is in the solution set.

**At $x = 5$** (right boundary, should be excluded):

$$2(5) - 4 = 6 \quad \Rightarrow \quad -10 \leq 6 < 6$$

The left condition holds, but $6 < 6$ is false. $5$ is correctly excluded.

**At $x = 0$** (interior, should be included):

$$2(0) - 4 = -4 \quad \Rightarrow \quad -10 \leq -4 < 6 \quad \checkmark$$

Both conditions hold. $0$ is in the solution set.

If any of these checks had failed, it would signal either an algebra error in the solving steps or an error in how the interval notation was written.

---

## 🔁 Structural Parallel to Everything Before

Step back and look at the full progression your files have built:

In the linear equations files, you learned that two linear expressions can relate to each other in exactly three ways — they meet at one point, never meet, or are identical everywhere. The outcome depends on whether their slopes and constants match.

In the inequalities files, you are discovering a parallel structure. Two inequality regions can relate to each other in ways that produce complete coverage (OR with overlap), a partial union with a gap (OR without overlap), a bounded intersection (AND with overlap), or no solution at all (AND without overlap). The outcome depends on where the boundary points sit relative to each other.

The chain inequality $-10 \leq 2x - 4 < 6$ produced a bounded region because its two boundary points, after solving, created an interval with genuine width. That is not luck — it is a structural consequence of the original constants being set up so that $-3 < 5$. If those had been reversed, no intersection would exist.

---

## 🧪 Test Yourself — The Flip Case

Now try a problem where the chain contains a negative coefficient, forcing a sign flip:

$$-6 \leq -3x + 1 < 3$$

Work through it completely: subtract 1 from all three parts, then divide by $-3$ and flip both signs. Rewrite the result in standard order, draw the number line, write the interval notation, and verify both boundary points.

If you arrive at $-\frac{2}{3} < x \leq \frac{7}{3}$, your algebra and sign discipline are solid. If you get the boundaries right but the interval notation wrong (or vice versa), that is the specific thing to fix before moving on.

---

> *"AND narrows. OR expands. The word connecting two conditions tells you whether you are building walls or tearing them down."*

---

*Next: Absolute Value Inequalities — where the distance interpretation of absolute value turns a single inequality into a compound one automatically, and the structure you built here becomes the tool you use to solve it.*
