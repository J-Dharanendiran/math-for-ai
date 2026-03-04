# 🏰 The Troll's Riddle — An Introduction to Systems of Equations

> *"Mathematics is not about numbers, equations, or algorithms — it is about understanding."*
> — William Paul Thurston

---

## 🧭 The Quest Begins

Picture this. You are on a grand quest to reach a distant castle. The path is long, the stakes are high — and standing between you and your destination is a river with only one way across: **a bridge guarded by a troll.**

The troll demands a **$5 toll**. You reach into your pocket. Empty.

*"No money?"* the troll grins. *"Then answer my riddle — or into the river you go."*

Your fate now depends not on a sword, but on **algebra**.

---

## 🧌 The Troll's Two Clues

The troll reaches into a sack overflowing with bills — all either **$5 or $10 denominations** — and gives you exactly two pieces of information:

1. 📦 **Clue 1 — The Count:** *"I have a total of **900 bills**."*
2. 💰 **Clue 2 — The Value:** *"Their combined worth is exactly **$5,500**."*

*"Tell me,"* he says, leaning forward, *"exactly how many $5 bills and how many $10 bills I hold. You have one chance."*

The clock is ticking. Let's think.

---

## 🔤 Translating the Riddle into Algebra

The first move in any word problem is to **name the unknowns clearly**. Here:

- Let **`f`** = the number of $5 bills
- Let **`t`** = the number of $10 bills

Now we translate each clue into the language of mathematics.

### Equation 1 — The Count 📦

> *"The total number of bills is 900."*

Every bill is either a $5 or a $10, so their counts must add up to 900:

```
f + t = 900
```

### Equation 2 — The Value 💵

> *"The total value is $5,500."*

Each $5 bill contributes `5f` dollars, each $10 bill contributes `10t` dollars, and together they must reach $5,500:

```
5f + 10t = 5500
```

We now have **two equations, two unknowns**. This is called a **system of equations**.

---

## 🤔 Why Can't One Equation Solve It?

This is the crucial question — and most students skip right past it.

Consider **Equation 1** alone: `f + t = 900`. This says the total count is 900. But by itself, it allows *infinitely many* solutions:

| `f` (five-dollar bills) | `t` (ten-dollar bills) | Check |
|---|---|---|
| 900 | 0 | 900 + 0 = 900 ✅ |
| 800 | 100 | 800 + 100 = 900 ✅ |
| 700 | 200 | 700 + 200 = 900 ✅ |
| 650 | **250** | 650 + 250 = 900 ✅ |
| 500 | 400 | 500 + 400 = 900 ✅ |

*Every single row above satisfies the first equation.* A single equation is like a filter with enormous holes — almost everything passes through.

> 💡 *"One equation describes a **line** of possibilities. Two independent equations describe an **intersection** — one exact point."*

The second equation is what narrows the field down to exactly one answer.

---

## ❓ What If t = 250? Let's Test It

You might wonder: *"Why can't the troll have 250 ten-dollar bills? That satisfies the count equation!"*

Great instinct — let's check it against **both** clues.

**From Equation 1:** If `t = 250`, then `f = 900 − 250 = 650`. ✅ Count checks out.

**Now check Equation 2:**
```
5(650) + 10(250)
= 3250 + 2500
= 5750
```

But the troll said $5,500 — not $5,750. ❌

**`t = 250` fails the second condition.** It satisfies one equation but not both. In a system of equations, *both must be satisfied simultaneously* — that's the whole point.

---

## ⚔️ Three Ways to Slay the Riddle

### Method 1 — The Replacement Trick 🔄 *(Fast & Intuitive)*

> *"What if every single bill were a $5?"*

1. If all 900 bills were $5: `900 × 5 = $4,500`
2. The actual total is $5,500 — that's **$1,000 more** than our all-fives scenario.
3. Every time a $5 bill is *replaced* by a $10 bill, the total rises by `$10 − $5 = $5`.
4. So the number of replacements needed: `$1,000 ÷ $5 = **200**`
5. Therefore: **`t = 200`** and **`f = 900 − 200 = 700`**

✅ *Mental math, no algebra required.*

---

### Method 2 — Elimination *(Systematic & Reliable)*

This method works every time, even when the replacement trick isn't obvious.

**Start with the two equations:**
```
f  +  t  =  900     ... (Equation 1)
5f + 10t  = 5500    ... (Equation 2)
```

**Step 1:** Multiply Equation 1 by 5 to match the coefficient of `f` in Equation 2:
```
5f + 5t = 4500      ... (Equation 1 × 5)
```

**Step 2:** Subtract this from Equation 2:
```
(5f + 10t) − (5f + 5t) = 5500 − 4500
                    5t = 1000
                     t = 200
```

**Step 3:** Substitute back:
```
f = 900 − 200 = 700
```

✅ **Verify:** `700 + 200 = 900` and `5(700) + 10(200) = 3500 + 2000 = 5500` ✅

---

### Method 3 — The Average Value Viewpoint 📊 *(Elegant & Generalizable)*

> *"What is each bill worth on average?"*

1. Average value per bill: `$5,500 ÷ 900 = $6.111...`
2. The average ($6.11) sits between the low ($5) and the high ($10).
3. The fraction of bills that are $10: `(6.111... − 5) ÷ (10 − 5) = 1.111... ÷ 5 = 2/9`
4. Number of $10 bills: `(2/9) × 900 = **200**` ✅

*This method generalizes beautifully to three or more denominations.*

---

## 🧠 The Core Idea — Two Filters, One Answer

Think of each equation as a **filter**.

```
🔵 Filter 1:  All (f, t) pairs where f + t = 900
🟠 Filter 2:  All (f, t) pairs where 5f + 10t = 5500
```

Individually, each filter lets through infinitely many pairs. But **apply both filters at once**, and only one pair survives:

```
✅  f = 700,  t = 200
```

> *"One equation → a line of infinite possibilities.*
> *Two independent equations → a single point of intersection.*
> *That intersection is the solution."*

This is the **geometric heart** of systems of equations: two lines meeting at exactly one point.

---

## 🛠️ The General Formula

For any problem with two item types — counts summing to `N`, unit prices `x` (low) and `y` (high), total value `V`:

```
Equations:   a + b = N
             xa + yb = V

Solution:    b = (V − xN) ÷ (y − x)
             a = N − b
```

**Two important checks before trusting your answer:**
- `V − xN` must be divisible by `y − x` (otherwise no integer solution exists)
- Both `a` and `b` must be **non-negative** (you can't have −50 bills)

---

## ⚠️ Common Pitfalls

- **Mixing units** — Don't mix counts and dollars in the same equation. Always check that both sides share the same units.
- **Skipping the sanity check** — Before solving, ask: "If all bills were $5, the total would be $4,500. If all were $10, it'd be $9,000. Since $5,500 falls between these, a solution exists." If your target falls outside the range, the problem is impossible.
- **Sign errors in elimination** — When subtracting equations, be deliberate. Write out every step.
- **Forgetting to verify** — Always substitute your final answer back into *both* original equations. A solution that fails even one equation is not a solution.

---

## 🔑 The One-Line Summary

> *"Compare the actual total to the 'all-cheap' total. Each expensive item adds* `(high − low)` *to the value. So: number of expensive items = (actual − all-cheap) ÷ (high − low)."*

---

## 🏰 The Bridge is Yours

You look the troll in the eye.

*"You have **700 five-dollar bills** and **200 ten-dollar bills**."*

The troll's jaw drops. He steps aside. The bridge is yours.

> *"Two clues. Two equations. One intersection. That's all it takes."*

As you cross, remember what just happened: **you didn't guess, and you didn't brute-force every possibility.** You built a mathematical model of the problem, applied two independent constraints, and found the unique truth hiding at their intersection.

That is what algebra is for. 🌟

---

*📌 Next up: What happens when two equations describe **parallel lines** — and there is no intersection? That's when a system has no solution, and the troll's riddle would be impossible to answer.*
