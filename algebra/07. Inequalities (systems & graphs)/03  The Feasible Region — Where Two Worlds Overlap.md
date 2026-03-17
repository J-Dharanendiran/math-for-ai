# 🗺️ The Feasible Region — Where Two Worlds Overlap

> *"One inequality fills half the plane. Two inequalities start a negotiation. The solution is wherever both sides agree."*

---

In the last lesson, you learned that a single inequality doesn't point to a spot on a map — it **paints an entire territory**. You drew a boundary, chose a test point, and watched an infinite half-plane come to life. Every coordinate pair inside the shading was a valid answer. Every pair outside was not.

That was one constraint working alone.

Now imagine two constraints. Two half-planes. Two rules that both demand to be satisfied *at the same time.* The question is no longer *"which side of this line is valid?"* — it becomes ***"where do both valid sides meet?"***

That meeting place has a name. It is called the **feasible region**, and learning to find it — graphically, algebraically, and logically — is one of the most powerful tools algebra has ever handed you.

---

## 🌍 Setting the Scene — Two Inequalities, One Plane

We will work through the following system throughout this lesson:

$$y > x - 8 \qquad \text{and} \qquad y < 5 - x$$

Read these two rules like two characters in the same story. The first says: *"I want* $y$ *to be above me — above the line* $y = x - 8$*."* The second says: *"I want* $y$ *to be below me — below the line* $y = 5 - x$*."*

Both characters speak simultaneously. Your job is to find every point in the plane that **listens to both at once**.

---

## ✏️ Step 1 — Draw Each Boundary Line

Before a single region can be shaded, both boundary lines must be drawn. Strip each inequality of its symbol and replace it with an equals sign.

**Boundary 1:** $y = x - 8$
This is in slope-intercept form. The **y-intercept** is $-8$, placing the starting point at $(0, -8)$ on the $y$-axis. The **slope** is $1$ — for every step right, the line climbs one step up. From $(0, -8)$, step right 1 and up 1 to reach $(1, -7)$. Extend in both directions.

**Boundary 2:** $y = 5 - x$, which is the same as $y = -x + 5$
The **y-intercept** is $5$, placing the starting point at $(0, 5)$. The **slope** is $-1$ — for every step right, the line drops one step down. From $(0, 5)$, step right 1 and down 1 to reach $(1, 4)$. Extend in both directions.

Now the critical question: **solid or dashed?**

Both original inequalities use strict symbols — $>$ and $<$, with no "equal to" component. This means neither boundary line belongs to the solution. Draw **both lines as dashed**. They are borders without citizenship — present only to define where the territory begins, not to be part of it.

---

## 🎨 Step 2 — Shade Each Half-Plane

With both lines drawn, each inequality now claims its half of the plane.

**For $y > x - 8$:** You want $y$-values *greater than* the boundary — meaning, for any fixed $x$, you want points that sit *above* the line $y = x - 8$. **Shade above the first dashed line.**

**For $y < 5 - x$:** You want $y$-values *less than* the boundary — meaning, for any fixed $x$, you want points that sit *below* the line $y = 5 - x$. **Shade below the second dashed line.**

> *"The first line says: rise above me. The second line says: stay beneath me. The feasible region is the territory that honours both commands."*

At this point, your graph has two overlapping shadings. The area covered by *both* — the doubly-shaded overlap — is the feasible region. Every point inside it satisfies both inequalities simultaneously. Every point outside fails at least one.

---

## 🔬 Step 3 — Describe the Overlap Algebraically

Graphing reveals the shape of the solution. But algebra **compresses it into language**.

If a point must simultaneously satisfy both inequalities, its $y$-coordinate must be *above* $x - 8$ and *below* $5 - x$. Stack those two demands into a single compound inequality:

$$x - 8 < y < 5 - x$$

This is the algebraic portrait of the feasible region. Read it as: *"$y$ must be squeezed between the two boundary expressions — always greater than* $x - 8$ *and always less than* $5 - x$*."*

This compact form is powerful because it tells you something immediately: **for any given** $x$, there is only a valid $y$-interval if the lower bound is *actually lower* than the upper bound. In other words, the two sides of the inequality must have room between them. That condition leads directly to the next step.

---

## 📍 Step 4 — Find the Intersection Point

The two boundary lines will eventually cross each other. That crossing point is where the "gap" between the two bounds collapses to zero — the precise location where the feasible region terminates. Finding it is essential.

Set the two boundary expressions equal to each other:

$$x - 8 = 5 - x$$

Add $x$ to both sides:

$$2x - 8 = 5$$

Add $8$ to both sides:

$$2x = 13$$

Divide both sides by $2$:

$$x = \frac{13}{2} = 6.5$$

Now substitute back to find $y$. Use either boundary equation — both must give the same answer at the crossing point:

$$y = x - 8 = 6.5 - 8 = -1.5$$

The two boundary lines meet at the point $\left(6.5,\ -1.5\right)$.

⚠️ **But here is a crucial detail:** because both inequalities are *strict* (no "equal to"), this intersection point is **not included** in the solution. It lives on both dashed lines simultaneously, which means it fails both inequalities — it neither satisfies $y > x - 8$ nor $y < 5 - x$. It marks the tip of the feasible region, not a member of it.

> *"The intersection point is the meeting of the fences — the corner post that belongs to neither yard."*

---

## 🔎 Step 5 — Determine the Domain: Where Does Overlap Exist?

The compound inequality $x - 8 < y < 5 - x$ only makes sense when its lower bound is actually *smaller* than its upper bound. If $x - 8 \geq 5 - x$, the "gap" vanishes or inverts — there is no $y$ that fits.

Solve for when the lower bound is strictly less than the upper bound:

$$x - 8 < 5 - x$$

Add $x$ to both sides:

$$2x - 8 < 5$$

Add $8$:

$$2x < 13$$

Divide by $2$:

$$x < 6.5$$

The feasible region only exists for $x < 6.5$. At $x = 6.5$, the two bounds are equal — no $y$ fits. For $x > 6.5$, the lower bound exceeds the upper bound — still no $y$ fits. The feasible region is **cut off at** $x = 6.5$, the $x$-coordinate of the intersection point.

This is not a coincidence. It is a consequence of the geometry: the two lines diverge to the left of their crossing and converge to the right. The overlap only exists in the diverging direction.

---

## 🧭 Step 6 — Is the Region Bounded or Unbounded?

Now look at the shape of the feasible region and ask: *does it close in on itself, or does it extend without limit?*

To the **right**, it is sealed off at $x = 6.5$ — the intersection point acts as a pointed tip, and no overlap exists beyond it.

To the **left**, both lines diverge endlessly. For smaller and smaller values of $x$, the gap between $y = x - 8$ (pulling down and left) and $y = 5 - x$ (pulling up and left) grows wider and wider. The feasible region **opens up infinitely** in the leftward direction.

Vertically, at each $x$-value, the valid $y$-values form an interval that also stretches — narrowing as $x$ approaches $6.5$ and widening as $x$ moves away.

**Conclusion:** the feasible region is **unbounded**. It widens indefinitely to the left, like a wedge-shaped opening. No walls close it off from the left, top, or bottom.

> *"The feasible region is not a room with walls on all sides. It is a corridor with one sealed end — pointing rightward at* $(6.5, -1.5)$ — *and an open mouth that breathes freely into the left half of the plane."*

---

## ✅ Step 7 — Verify With Test Points

The test point is not just a graphing trick — it is a **proof**. Once you understand why one point speaks for an entire region (as explored in the last lesson), testing becomes a verification ritual rather than a guess.

**Test $(0, 0)$ — expected to be inside the feasible region:**

- Check inequality 1: $0 > 0 - 8 \implies 0 > -8$ ✅
- Check inequality 2: $0 < 5 - 0 \implies 0 < 5$ ✅

$(0, 0)$ satisfies both. It lives inside the feasible region. ✓

**Test $(7, 0)$ — expected to be outside (since $7 > 6.5$):**

- Check inequality 1: $0 > 7 - 8 \implies 0 > -1$ ✅ *(passes the first)*
- Check inequality 2: $0 < 5 - 7 \implies 0 < -2$ ❌ *(fails the second)*

$(7, 0)$ fails inequality 2. It is outside the feasible region. ✓

**Test $(6.5, -1.5)$ — the intersection point, expected to be excluded:**

- Check inequality 1: $-1.5 > 6.5 - 8 \implies -1.5 > -1.5$ ❌ *(not strictly greater)*

The intersection point fails inequality 1. It is not in the solution — as expected. ✓

---

## 🏗️ Why the Feasible Region Matters Beyond This Problem

The work you have just done is not an isolated exercise. The feasible region is one of the central objects in applied mathematics, and its uses run deep.

**In linear programming**, the feasible region is the set of all valid options. If you are a factory deciding how many units of two products to make — subject to labor limits, material limits, and demand limits — every constraint draws a boundary. The feasible region is everything your factory *could* produce without violating any rule. The *optimal* production plan — the one that maximizes profit or minimizes cost — is always found at a **corner point** of the feasible region, not somewhere in the middle.

**In economics**, feasible regions represent budget sets, production possibility frontiers, and constraint systems. The algebra you practiced here is exactly what economists use to model rational choice.

**In machine learning**, the boundary of a feasible region is called a decision boundary. A classifier learning to separate two categories of data is, at its core, drawing inequalities across a coordinate plane and asking: which side does this point fall on?

> *"What you have learned to draw on graph paper, engineers draw in factories, economists draw in models, and algorithms draw in data. The region is always the same idea — the set of everything that is simultaneously possible."*

---

## 📋 The Complete Method — Consolidated

Every system of linear inequalities can be solved with these six moves, in order:

1. **Identify the boundary lines** by replacing each inequality symbol with $=$.
2. **Draw each boundary** as **dashed** for strict inequalities ($<$, $>$) or **solid** for inclusive ones ($\leq$, $\geq$).
3. **Shade each half-plane** individually — above the line for $>$ or $\geq$, below for $<$ or $\leq$.
4. **Locate the feasible region** as the area where all shadings overlap.
5. **Find the intersection point(s)** by solving the boundary equations simultaneously. Check whether these points are included or excluded based on the inequality symbols.
6. **Verify** with a test point inside the overlap and at least one outside.

---

## 🌟 What This Lesson Has Really Taught You

The mechanics of this lesson are clean and followable. But the idea underneath them is worth sitting with.

Two constraints, each drawing a half-plane, together carve out a precise territory — a region that is simultaneously *above one line and below another*. The algebraic description compresses it into a compound inequality. The geometric description makes it visible. The intersection point marks where the two worlds run out of room to coexist. And the test point confirms, with a single calculation, what the entire region does.

You have not just learned to shade a graph. You have learned to think in **constraint space** — to ask, for any system of rules: *what is the complete set of possibilities that satisfies all of them at once?* That is the feasible region. And now, it is yours.

> *"The line divides. The shading includes. The test point decides. And the feasible region — that beautiful, infinite wedge — is where all the rules agree, and all the answers live."*

---

*📘 Next up: Solving Multi-Step and Compound Inequalities — when constraints chain together along a single variable, and the solution narrows to an interval (or splits into two).*
