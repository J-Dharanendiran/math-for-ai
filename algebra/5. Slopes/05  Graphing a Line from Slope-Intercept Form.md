# 📊 Graphing a Line from Slope-Intercept Form

> *"The equation already contains the full graph. Your job is just to read it."*

Slope-intercept form allows you to graph a line immediately because it directly gives you two things: the **starting point** and the **direction of movement** — no tables, no guessing.

Example equation used throughout:

```
y = (1/3)x - 2
```

---

## 1. 🔍 Identify Slope and Intercept

```
m = 1/3   →   slope
b = -2    →   y-intercept
```

**Slope `m = 1/3`** — for every +3 in x, y increases by +1. A gentle, slow rise.

**Intercept `b = -2`** — the line crosses the y-axis at `(0, -2)`, below the origin.

---

## 2. 📍 Plot the Intercept

The y-intercept is always your **first point** and your anchor.

```
Point: (0, -2)
```

Confirm by substituting x = 0:

```
y = (1/3)(0) - 2 = -2  ✅
```

---

## 3. ↗️ Apply the Slope

Slope is always **rise over run**.

```
Slope = 1/3

rise = +1   (move up 1)
run  = +3   (move right 3)
```

From `(0, -2)`:

- Right 3 → x = 3 | Up 1 → y = -1 | **New point: `(3, -1)`** ✅

Slope also works in reverse — go left 3, down 1:

- Left 3 → x = -3 | Down 1 → y = -3 | **New point: `(-3, -3)`** ✅

> ⚠️ *Common mistake: reading `1/3` as run 1, rise 3. The fraction is always rise ÷ run. Rise = 1, Run = 3.*

---

## 4. 📋 Generate Points

Apply the slope pattern repeatedly in both directions:

| x  | y  | Point    |
|----|----|----------|
| -6 | -4 | (-6, -4) |
| -3 | -3 | (-3, -3) |
|  0 | -2 | (0, -2)  |
|  3 | -1 | (3, -1)  |
|  6 |  0 | (6, 0)   |

Notice: every time x increases by **3**, y increases by **1**. That's `m = 1/3` confirmed in the numbers.

> *Two points are enough to draw the line. More points confirm you haven't drifted.*

---

## 5. ✏️ Draw the Line

Connect at least two points with a straight line extending in both directions.

This line will visibly:
- **Rise slowly** left to right — slope `1/3` is small and positive.
- **Cross the y-axis at -2** — below the origin.

> 🎯 *If the line passes through every point in your table, you've graphed it correctly.*

---

## 6. 🧠 Conceptual Meaning of the Slope

The slope `1/3` is a **rate of change** — not just a graphing instruction. It says: for every +3 in x, y increases by exactly +1, everywhere on the line.

**Why this matters beyond algebra:**

```
Algebra:          y  = mx  + b
Machine Learning: ŷ  = wx  + b
```

- `m` (slope) becomes `w` — the **model weight**
- `b` (intercept) becomes `b` — the **bias**

These algebra notes are literally the foundation of **linear regression**.

Verify numerically using `(0, -2)` and `(3, -1)`:

```
m = (-1 - (-2)) / (3 - 0) = 1/3  ✅
```

---

## 7. ✅ Key Takeaways

1. **Identify** `m` and `b` directly from the equation.
2. **Plot** `(0, b)` as the anchor point.
3. **Apply** rise/run — right by denominator, up by numerator.
4. **Repeat** the pattern to generate more points.
5. **Connect** with a straight line in both directions.

- 📌 Slope works in both directions — right/up and left/down give the same line.
- 📌 Rise = numerator, Run = denominator — never flip them.
- 📌 Sign of `b` matters — `b = -2` starts *below* zero.
- 📌 Two points define the line. More points verify it.

---

---

# 📘 Follow-Up Topics: Four More Ways to Work with `y = mx + b`

> *"Graphing from an equation is one skill. Real fluency means moving in every direction — from graph to equation, from a point to a full line, from two coordinates to a formula, from a story to a model."*

---

## 📐 Follow-Up 1: Reading the Equation from a Graph

**The reverse skill** — given a graph, write the equation.

### Steps

1. Pick **two clean grid-intersection points** on the line.
2. Compute slope: `m = (y₂ - y₁) / (x₂ - x₁)`
3. **Read the y-intercept** — where the line crosses the y-axis. Below origin = negative `b`.
4. **Substitute** into `y = mx + b`.

### ✏️ Worked Example

Line passes through `(0, -3)` and `(2, 1)`:

```
m = (1 - (-3)) / (2 - 0) = 4/2 = 2

b = -3   (crosses y-axis at -3)

Equation:  y = 2x - 3
```

### ⚠️ Watch For

- **Fractional slopes** — rise 3, run 2 → keep it as `3/2`. Don't round or convert to decimal.
- **Negative slopes** — a falling line gives negative rise. Let the subtraction handle the sign automatically.
- **Sign of b** — a line crossing below the origin means `b` is negative.

---

## 🎯 Follow-Up 2: Finding the Equation from Slope and One Point

**When slope is known and one point is given** — that's all you need.

### Steps

1. Write `y = mx + b` and plug in the slope.
2. Substitute the known point's coordinates for x and y.
3. Solve for `b`. Write the final equation.

### ✏️ Worked Example

*Slope = `-3/4`, passes through `(0, 8)`:*

```
y = (-3/4)x + b

Substitute (0, 8):
  8 = (-3/4)(0) + b
  8 = b

Equation:  y = -3/4 x + 8
```

> 💡 *When the given point sits on the y-axis (x = 0), the slope term disappears and `b` reveals itself instantly — the easiest possible case.*

**Key concept:** Slope tells the line how to *move*. The point tells it *where to be*. Together they define exactly one unique line — no ambiguity.

---
