# 🗺️ The Half-Plane — When Algebra Stops Pointing and Starts Painting
> *"You already know how to find where a line lives. Now it's time to learn which side of it is home."*

---

In the last lesson, you learned that a linear inequality doesn't describe a single line — it describes an entire **region**. You learned that the boundary line is drawn solid or dashed depending on whether the inequality is inclusive or strict, and that shading one half of the plane communicates infinitely many solutions all at once.

But there is one moment from that lesson worth slowing down on: the **test point**.

It seemed almost too simple, didn't it? You pick one point, plug it in, and suddenly — the whole region is decided. How does one point speak for an entire half-plane? Why does it work so consistently, every single time? And what does it feel like, mathematically, when you're *inside* the solution region versus *outside* it?

That is what this lesson is about. Not just the technique — but the **understanding underneath it.**

---

## 🌍 From Equations to Regions — The Shift in Thinking

Before we dive into the mechanics, let's anchor ourselves in the conceptual shift that inequalities demand.

When you work with an **equation** like $y = 3x + 5$, you're dealing with *one specific output* for every input. Choose $x = 1$ and you get exactly $y = 8$. Choose $x = 0$ and you get exactly $y = 5$. The equation is precise, narrow, unambiguous — a single thread stretched across the plane.

An **inequality** like $y < 3x + 5$ does something fundamentally different.

> *"The equation says: here is the answer. The inequality says: here is the boundary — now pick a side."*

Choose $x = 0$ and the boundary gives you $y = 5$. But the inequality doesn't say $y$ must equal $5$. It says $y$ must be **less than 5**. So for that single $x$-value, every $y$ in the infinite interval $(-\infty, 5)$ is a valid answer:

- $y = 4$ ✅
- $y = 0$ ✅
- $y = -1{,}000$ ✅
- $y = 5$ ❌ *(not strictly less than)*
- $y = 6$ ❌

You are no longer searching for a point. You are **defining a territory**.

---

## 🗺️ What "Below the Line" Really Means

Here's a question worth pausing over: when we say *"shade below the line,"* what does **below** actually mean in a mathematical sense?

It means this — for any given $x$, the $y$-values that satisfy the inequality are those that fall short of the boundary value. The boundary line, $y = 3x + 5$, gives you the **threshold** at every $x$. Everything beneath that threshold satisfies $y < 3x + 5$. Everything above it does not.

Visually, this creates a **half-plane** — one of the two infinite regions that any line divides the coordinate plane into. The line is the divider. The inequality tells you which side of the divider is valid.

| Region | Relationship to line | Satisfies $y < 3x + 5$? |
|--------|---------------------|------------------------|
| Below the line | $y < 3x + 5$ | ✅ Yes |
| On the line | $y = 3x + 5$ | ❌ No (strict inequality) |
| Above the line | $y > 3x + 5$ | ❌ No |

This isn't just a graphing trick. This is the geometry of constraints — and it's the same geometry that powers optimization problems, machine learning decision boundaries, and engineering feasibility analysis. The half-plane is a fundamental mathematical object.

---

## 🔬 The Test Point — Not a Guess, But a Proof

Let's talk about why the test point works. Because it shouldn't feel like magic — and once you understand it, it won't.

When you draw the boundary line for $y < 3x + 5$, you split the coordinate plane into two halves. Think of the plane as two countries, with the boundary line as their shared border. Every point in **Country A** (below the line) makes $y - 3x - 5 < 0$. Every point in **Country B** (above the line) makes $y - 3x - 5 > 0$. On the border itself, $y - 3x - 5 = 0$ exactly.

Here is the crucial mathematical fact:

> *"A continuous linear function cannot change sign without crossing zero. And crossing zero means crossing the boundary line."*

Because $f(x, y) = y - 3x - 5$ is a **continuous, linear function**, it changes smoothly — no jumps, no gaps, no sudden reversals. If you start in a region where $f < 0$, you **cannot** reach a point where $f > 0$ without passing through the line where $f = 0$ first.

This means: within a single half-plane, the sign of $f$ never changes. If one point in the lower half-plane satisfies the inequality, **every** point in that half-plane satisfies it.

So the test point doesn't guess what the whole region does. It *confirms* what the mathematics already guarantees.

---

## 🧪 Step-by-Step: Graphing $y < 3x + 5$

Let's walk through a complete example together, narrating each decision as we make it.

**Step 1 — Identify the boundary line.**

Replace the inequality with equality: $y = 3x + 5$. This is in slope-intercept form, so we can read off everything we need.

- **y-intercept:** $5$, so the line crosses the $y$-axis at $(0, 5)$.
- **Slope:** $3$, meaning for every 1 unit right, the line rises 3 units up.

From $(0, 5)$, step right 1 and up 3 to land at $(1, 8)$. Step left 1 and down 3 to land at $(-1, 2)$. Connect these and extend in both directions.

**Step 2 — Decide: solid or dashed?**

The symbol is strictly $<$, with no "equal to" component. So the boundary is **not** part of the solution. Draw a **dashed line**. This is a promise to the reader: *"The line marks the edge, but it belongs to neither side."*

**Step 3 — Pick a test point.**

Choose $(0, 0)$ — it's off the line, and substituting zeros is arithmetic-free.

$$0 < 3(0) + 5 \implies 0 < 5 \quad ✅$$

The origin satisfies the inequality. So the origin is inside the solution region.

**Step 4 — Shade the correct half-plane.**

Since $(0, 0)$ satisfies the inequality and $(0, 0)$ is **below** the boundary line, shade the **lower half-plane** — everything below the dashed line, extending infinitely in every direction downward.

> *"The test point named the country. The shading filled it in."*

---

## 🎯 Practising the Decision: Which Side to Shade?

The test point is reliable, but it's worth building intuition about **why** certain inequalities shade above and others shade below. Here's the pattern:

- **$y < \text{something}$** → shade **below** (you want $y$ to be smaller than the boundary)
- **$y > \text{something}$** → shade **above** (you want $y$ to be larger than the boundary)
- **$y \leq \text{something}$** → shade **below**, with a **solid** boundary
- **$y \geq \text{something}$** → shade **above**, with a **solid** boundary

This holds whenever the inequality is already solved for $y$. If it isn't — say, the inequality is $2x + 3y < 9$ — always run the test point rather than relying on this pattern, because rearranging can flip the sign and change which side you shade.

---

## ⚠️ The One Situation Where $(0, 0)$ Fails You

The origin is almost always the best test point. Almost.

The single exception: **when the boundary line passes through the origin itself.**

If the equation of your boundary line is something like $y = 2x$ or $3x - y = 0$, then $(0, 0)$ lies exactly on the line — and a test point must always be *off* the boundary. In these cases, simply choose a nearby point like $(0, 1)$, $(1, 0)$, or $(1, 1)$ instead.

> *"The origin is the most convenient test point in the world — right up until it's standing on the fence you're trying to judge."*

---

## 🔗 Connecting Back: Why This Extends Infinitely

Recall from the last lesson: when we shade a half-plane, that shading does not stop at the edges of the graph paper. The region extends **without bound** in all directions below (or above, or to the left, or to the right of) the boundary.

To feel this concretely, consider $y < 3x + 5$ at a few very different $x$-values:

1. At $x = 0$: boundary is $y = 5$. Allowed: all $y < 5$, stretching down to $-\infty$.
2. At $x = 10$: boundary is $y = 35$. Allowed: all $y < 35$, stretching down to $-\infty$.
3. At $x = -100$: boundary is $y = -295$. Allowed: all $y < -295$, stretching down to $-\infty$.

At every single $x$-value, the allowed $y$-values form an infinite downward interval. The solution set is not a bounded shape — it is a **half-plane**, genuinely infinite in extent.

This is exactly what the shading represents, even when the paper runs out.

---

## 🏗️ Building Toward Systems: What Happens With Two Inequalities?

Now here is where the real power begins to emerge.

You have been graphing one inequality — one half-plane. But what happens when two constraints must hold **simultaneously**? What if you need:

$$y < 3x + 5 \quad \text{AND} \quad y \geq -x + 1$$

Each inequality shades its own half-plane. The solution to **both** is the region where those two shadings **overlap** — every point that lives inside both half-planes at once.

That overlapping region is called the **feasible region**, and it is the geometric heart of systems of inequalities. Depending on the two lines, the overlap might be:

- A **wedge-shaped region** that opens in one direction and extends infinitely
- A **bounded polygon** if more constraints are added
- An **empty set** if the constraints contradict each other entirely

> *"One inequality fills half the plane. Two inequalities narrow it further. Three or more can carve out a precise, bounded territory — or prove that no territory exists at all."*

This is the bridge to the next topic: **systems of linear inequalities**, where multiple constraints share one graph and their intersection becomes the answer. Every point you'll find there, every corner of that feasible region — it all starts with the single skill you've just practiced: drawing the boundary, picking the test point, and shading the right half.

---

## 📋 The Complete Method — Consolidated

Here is the full graphing procedure, as a permanent reference:

1. **Rewrite** the inequality in slope-intercept form if it isn't already.
2. **Identify** the boundary line by replacing the inequality symbol with $=$.
3. **Plot** the boundary using the $y$-intercept and slope.
4. **Draw** the boundary as a **dashed line** for $<$ or $>$, and a **solid line** for $\leq$ or $\geq$.
5. **Choose** a test point not on the boundary — $(0, 0)$ unless the line passes through the origin.
6. **Substitute** the test point into the original inequality.
7. **Shade** the half-plane that contains the test point if it satisfies the inequality; shade the opposite half if it doesn't.

---

## ✨ What You've Actually Learned

The mechanics above are straightforward. But the deeper understanding is worth naming clearly.

You've learned that a linear inequality doesn't describe a relationship between specific numbers — it describes a **constraint on a region of the plane**. You've learned that the boundary line is not the answer, but the **edge of the answer**. You've learned that testing one point is not a shortcut or an approximation — it is a **logically complete proof**, backed by the continuity of linear functions.

And perhaps most importantly, you've begun to see that the coordinate plane is not just a place where lines live.

It is a place where **choices are made**, **constraints are drawn**, and **solutions take up space**.

> *"The equation drew a line. The inequality drew a world. And now you know how to read both."*

---

*📘 Next up: Systems of Linear Inequalities — where multiple boundaries share the same plane, and the solution is wherever all the rules agree.*
