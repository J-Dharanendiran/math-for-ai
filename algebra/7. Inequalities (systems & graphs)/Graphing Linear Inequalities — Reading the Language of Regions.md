# 🗺️ Graphing Linear Inequalities — Reading the Language of Regions

> *"An equation draws a line. An inequality draws a world."*

---

There is a moment in every algebra journey where the number line is no longer enough. You have been thinking in one dimension — a variable sliding left or right along a single axis. But the real world has two dimensions. Relationships between two variables need a **plane** to live in — a flat surface where every point is a pair $(x, y)$, and every inequality carves that surface into two territories: one where the rule holds, and one where it does not.

That is the entire idea behind graphing inequalities on the coordinate plane. Not solving for a single value of $x$. Not finding one point. But *painting a region* — marking every coordinate pair that satisfies the rule, all at once, visually and completely.

---

## 🖊️ The Boundary Line — Where Everything Begins

Before you can shade a region, you need to know where its edge is. And the edge of an inequality's solution region is always a **line** — specifically, the line you get when you replace the inequality symbol with an equals sign.

Take $y \leq 4x + 3$. Strip the inequality and you get $y = 4x + 3$. That line is the **boundary** — the precise border between the territory that satisfies the rule and the territory that does not. Everything below it might be the answer. Everything above it might be the answer. But the line itself is the dividing wall, and you draw it first before deciding anything else.

Now, that wall has two possible forms — and which one you draw tells the reader something critical.

---

## ✏️ Solid or Dashed — The Line's First Message

Imagine the line is a fence. Whether that fence is *part of your property* or merely *the property boundary* depends entirely on what the inequality symbol says.

When the symbol is $\leq$ or $\geq$ — *less than or equal to*, *greater than or equal to* — the boundary line **is** part of the solution. Points sitting exactly on the line satisfy the inequality. So you draw a **solid line**, a visual promise that says: *"I am included. Step on me freely."*

When the symbol is $<$ or $>$ — strictly less than or strictly greater than — the boundary line is **excluded**. Points on the line make the inequality false. You draw a **dashed line** instead, a visual warning: *"I mark the edge, but I am not yours."*

This is not decoration. When someone reads your graph, the solid or dashed line is the first signal they look for. It tells them immediately whether the boundary belongs to the solution before they even look at the shading.

| Symbol | What it means | Line to draw |
|--------|---------------|--------------|
| $\leq$ or $\geq$ | Boundary is *included* | **Solid** |
| $<$ or $>$ | Boundary is *excluded* | **Dashed** |

---

## 🔵 Walking Through the First Graph: $y \leq 4x + 3$

Start by identifying what you need to draw the boundary line. The equation $y = 4x + 3$ is already in slope-intercept form, so it hands you everything directly.

The **y-intercept** is $3$ — meaning the line crosses the $y$-axis at the point $(0, 3)$. Plant your first point there. The **slope** is $4$ — meaning for every 1 unit you move to the right, you climb 4 units upward. From $(0, 3)$, step right once and up four times to land at $(1, 7)$. You can also work backwards: step left once and drop four to land at $(-1, -1)$.

Connect those points and extend the line in both directions. Because the symbol is $\leq$, draw it **solid**.

Now the shading question: the inequality asks for $y$ to be *less than or equal to* the expression. For any fixed value of $x$, the $y$-values that satisfy this are the ones **below** the line — because those are the $y$-values smaller than $4x + 3$. So shade downward, covering everything beneath the solid line, stretching infinitely in every direction below it.

Every point in that shaded half-plane — every single coordinate pair $(x, y)$ — satisfies $y \leq 4x + 3$. Not a selection of points. Not a sample. *All of them.*

---

## 🟠 Walking Through the Second Graph: $y > -\frac{x}{2} - 6$

This example introduces both a negative slope and a strict inequality — which changes the graph in two important ways.

The boundary line is $y = -\frac{1}{2}x - 6$. The **y-intercept** is $-6$, so begin at $(0, -6)$ on the $y$-axis. The **slope** is $-\frac{1}{2}$, meaning for every 2 steps right, the line drops 1 step down. From $(0, -6)$, move right 2 and down 1 to reach $(2, -7)$. Alternatively, move left 2 and up 1 to reach $(-2, -5)$.

Because the symbol is strictly $>$, draw the boundary as a **dashed line**. The line exists only as a reference — it is not part of the answer.

Now the shading: $y$ must be *greater than* the expression, meaning we want $y$-values **above** the line for any given $x$. Shade the entire region above the dashed line. Everything above it is a valid solution. The dashed line itself is the one place in the entire plane that is explicitly excluded.

---

## 🧠 Why One Test Point Proves the Whole Region

This is the question worth sitting with, because it sounds like it should not work — and yet it does, completely and provably.

After drawing the boundary line, you know the plane is split into two halves. You do not yet know which half is the solution. So you pick a single test point, substitute it into the original inequality, and check whether it satisfies the rule. If it does, shade that side. If it does not, shade the other side.

But why does testing *one* point tell you about *infinitely many* others?

The answer lies in what a linear function actually does. Rewrite $y \leq 4x + 3$ as $f(x, y) = y - 4x - 3 \leq 0$. This function $f$ is continuous — it changes smoothly without jumping. On the boundary line, $f = 0$ exactly. Move to one side of the line and $f$ becomes negative. Move to the other side and $f$ becomes positive.

Here is the critical piece: *$f$ can only change sign by passing through zero.* And passing through zero means crossing the boundary line. So within a single half-plane — without crossing that line — $f$ never changes sign. If it is negative at one point in the region, it is negative at **every** point in that region.

| Point | $f(x,y) = y - 4x - 3$ | Result |
|-------|------------------------|--------|
| $(0, 0)$ — below the line | $0 - 0 - 3 = -3$ | ✅ Satisfies $\leq 0$ |
| $(0, 3)$ — on the line | $3 - 0 - 3 = 0$ | ✅ On the boundary |
| $(0, 5)$ — above the line | $5 - 0 - 3 = 2$ | ❌ Does not satisfy |

Testing $(0, 0)$ and finding it satisfies the inequality does not *guess* that the whole lower half satisfies it. It *confirms* something that was already guaranteed by the mathematics of linear functions. The test point is the final identification step, not a leap of faith.

> *"The test point does not represent the region. It names it."*

A practical note: $(0, 0)$ is almost always the easiest test point to use, because substituting zeros involves no arithmetic. The one exception is when the boundary line passes directly through the origin — in that case, choose a different point, like $(0, 1)$ or $(1, 0)$.

---

## 🔺 When Two Inequalities Share a Plane

A single inequality fills half the plane. But what happens when you graph two inequalities on the same coordinate system and ask: *where do both hold true at once?*

That overlap — the region where both shaded areas cover the same points — is called the **feasible region**. It is the geometric picture of AND logic: every point inside satisfies both rules simultaneously.

Consider three constraints working together on the same plane:

$$x \geq 0, \qquad y \geq 0, \qquad x + 2y \leq 10$$

The first says: stay to the right of the $y$-axis. The second says: stay above the $x$-axis. The third says: stay below the line $x + 2y = 10$. Each one shades a half-plane. Their intersection — the region where all three shadings overlap — is a **triangle** sitting in the first quadrant, bounded on three sides.

Every point inside that triangle satisfies all three rules at once. Points outside the triangle fail at least one of them. The triangle *is* the complete set of solutions to the system, expressed visually in one glance.

This is the geometry that powers **linear programming** — the technique used in manufacturing, logistics, finance, and machine learning to find the best solution within a set of constraints. The feasible region is always a polygon (or an unbounded region shaped like one), and the optimal point — whatever you are trying to maximize or minimize — always lives at one of its **corner points**. So instead of checking infinitely many possibilities, you check a handful of corners. The graph does the heavy lifting of narrowing the infinite down to the essential few.

---

## 🧭 The Three-Step Method — Made Permanent

No matter which inequality you face, the approach is always the same three moves:

**First**, draw the boundary line by treating the inequality as an equation. Use the $y$-intercept and slope to place it accurately. Decide immediately whether it should be solid or dashed based on the symbol.

**Second**, pick a test point not on the line — $(0, 0)$ whenever possible — and substitute into the original inequality. This single check tells you which half-plane is the solution.

**Third**, shade the correct half-plane. If the test point satisfied the inequality, shade toward it. If not, shade away from it.

> *"Algebra gives the boundary. Geometry splits the plane. The test point names the solution half."*

---

## ✨ What the Graph Is Actually Saying

It is worth stepping back and appreciating what a completed inequality graph communicates that an algebraic solution cannot.

An algebraic solution says: *"$x > -4$."* That is useful. But it is still abstract — a rule written in symbols.

A graph of $y > -\frac{x}{2} - 6$ says something richer. It shows the dashed line carving the plane in two. It shows the shaded territory above it, stretching infinitely upward and in every lateral direction. It makes visually obvious that the solution is not a line, not a handful of points, but an *entire half of the coordinate plane* — infinite in extent, bounded only by the line you drew.

Every coordinate pair in that shaded region is a valid answer. Every pair outside it fails. The graph makes that truth *visible*, which is something no equation can quite do on its own.

The solid and dashed lines, the shading above and below — these are not formatting conventions. They are a **visual language**, and once you learn to read and write it fluently, you can describe constraints, represent possibilities, and reason about regions in a way that words and symbols alone simply cannot match.

> *"The line divides. The shading includes. The test point decides. And the region — that beautiful shaded half-plane — is where all the answers live."*

---

*📘 This file is part of a series on inequalities. The solving mechanics — multi-step inequalities, compound inequalities, and absolute value — are covered in the companion files in this folder.*
