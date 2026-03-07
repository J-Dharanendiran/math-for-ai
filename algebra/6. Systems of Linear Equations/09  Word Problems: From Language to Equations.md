# 📝 Lesson 9 — Word Problems: From Language to Equations

> *"An equation is just a sentence in disguise. The skill is not solving it — the skill is **hearing** it."*

---

## 🧭 Why Word Problems Feel Like a Different Subject

Here is the truth that most algebra courses never say out loud:

> *"Word problems are not harder than equations. They just have extra packaging."*

The moment a problem arrives wrapped in words, something in our brain registers it as a different, more threatening kind of mathematics. But the underlying algebra is identical to problems we have already solved. What is new — and what this entire lesson is about — is the **translation step**: converting natural language into precise mathematical structure.

Once you master translation, a word problem is simply an equation that has not been written down yet. Your job is to find it.

---

## 🏛️ The Universal Framework

Before diving into the problems, here is the skeleton that every word problem shares:

1. 🎯 **Identify the unknowns** — What is the story actually asking you to find? Name it with a variable.
2. 🔍 **Extract the relationships** — Every sentence either states a value or describes how values relate. Those relationships become your equations.
3. ⚖️ **Recognise when two expressions describe the same thing** — This is the pivotal move. When two phrases both describe the same quantity, set them equal.
4. 🔧 **Solve the algebra** — Once the equation is built correctly, this is usually the easy part.
5. ✅ **Verify against the original story** — Not just the equations. The *story*.

Keep this framework in your mind as we work through all four problems.

---

---

# 🧒 Problem 1 — Imran's Age

## The Problem

> *"In 40 years, Imran will be 11 times as old as he is right now. How old is he right now?"*

---

## 🔑 Step 1 — Name the Unknown

The story asks for Imran's **current** age. So we write:

> **Let x = Imran's current age (in years)**

- This seems obvious, but notice the precision: not "Imran's age in general," but specifically his **current** age.
- This matters because the problem involves **two different points in time** — now, and 40 years from now.
- Getting the definition exactly right is what stops confusion later.

> *"Before any algebra can happen, the unknown must have a name. A variable without a clear definition is a door without a label — you don't know what's behind it."*

---

## 🔍 Step 2 — Find the Two Descriptions

This is the most important step in the entire problem. Read the sentence slowly:

> *"In 40 years, Imran will be 11 times as old as he is **right now**."*

This one sentence secretly contains **two separate ways of describing the same future age**. Let us pull them apart.

**Description 1 — The time-travel description 🕐**

If Imran is `x` years old today, then aging forward 40 years is simply addition:

> **Future age = x + 40**

- This is completely literal. Age increases at one year per year.
- Nothing fancy. If he is 10 now, he will be 50 in 40 years. If he is `x` now, he will be `x + 40`.

**Description 2 — The multiplier description ✖️**

The problem also says that future age equals **11 times his current age**:

> **Future age = 11x**

- ⚠️ Read this carefully: it says 11 times his **current** age `x`, not 11 times his future age.
- The comparison is **anchored to the present**.
- This is the detail most students miss on their first read.

---

## ⚖️ Step 3 — Form the Equation

> *"Two roads lead to the same destination. If they are both correct, they must end at the same place."*

Both expressions describe the **same future age**. There is only one value of "Imran's age in 40 years" — we simply have two ways to express it. So:

> **11x = x + 40**

- This equation did **not** appear in the problem statement.
- You had to **construct** it by recognising that two phrases described the same thing.
- This act of construction — not the arithmetic — is the real skill.

---

## 🔧 Step 4 — Solve

**Subtract `x` from both sides** to gather all variable terms on the left:

> 11x − x = x + 40 − x

> **10x = 40**

*Why both sides?* Because an equation is a **balance**. Any operation on only one side tips the scale and destroys the equality.

**Divide both sides by 10:**

> **x = 4**

✅ **Imran is currently 4 years old.**

---

## ✅ Step 5 — Verify Against the Story

> *"The algebra guarantees you solved the equation correctly. Only verification guarantees the equation matched the story."*

- Imran's current age → **4**
- Imran's age in 40 years → **4 + 40 = 44**
- Is 44 equal to 11 times his current age? → **11 × 4 = 44** ✅

The answer holds.

---

## 💡 The Deeper Takeaway

The equation `11x = x + 40` looks simple, but it rests on a subtle assumption: that **"11 times as old"** refers to his *present* age, not his future one. If the problem said "11 times as old as he will be," the equation would be completely different. Always pause and ask yourself: *"This multiple — of **what**, at **what moment** in time?"*

---
---

# 👴👶 Problem 2 — Ben and William

## The Problem

> *"William is currently four times as old as Ben. Twelve years ago, William was seven times as old as Ben. How old is Ben now?"*

---

## 🔑 Step 1 — Name the Unknown (and Decide How Many Variables You Need)

The problem asks for Ben's current age:

> **Let b = Ben's current age (in years)**

Now here is a critical question: *do we also need a variable for William?*

The answer is **no** — and understanding why is one of the most important reasoning moves in this problem.

- The very first sentence says: *"William is currently **four times** as old as Ben."*
- This means William's age is completely determined the moment we know Ben's age.
- William's current age = **4b**

> *"When one person's age is given as a multiple of another's, you do not need a second variable. The relationship already expresses one in terms of the other."*

Two people. One variable. The present relationship collapses them together.

---

## 📊 Step 2 — Build the Age Table

With two people and two points in time, the most powerful move is to lay everything out in a table. It forces you to be systematic and exposes the structure of the problem at a glance.

| Person | Age **Now** | Age **12 Years Ago** |
|--------|:-----------:|:--------------------:|
| Ben | `b` | `b − 12` |
| William | `4b` | `4b − 12` |

> ⚠️ **The Most Common Mistake in Age Problems:**
>
> Students sometimes write William's past age as `4(b − 12)` instead of `4b − 12`. These are **very different numbers**. Here is why the second one is correct and the first is not:
>
> - The statement *"William is four times Ben's age"* applies **only right now**, at the present moment.
> - In the past, the ratio between their ages was different — that is, in fact, what the second sentence of the problem is telling us.
> - Time passes **equally for everyone**: everyone's past age = their current age minus the elapsed years.
> - So William, who is `4b` now, was `4b − 12` twelve years ago. We subtract 12 from his **current** age, not from his ratio.

Think of it this way: if you earn £4 for every £1 Ben earns today, that does not mean you earned £4 for every £1 he earned last year. The ratio is a snapshot of **now**.

---

## 🔍 Step 3 — Translate the Key Sentence

We now have expressions for everyone's age at every relevant time. There is one sentence we have not yet used:

> *"Twelve years ago, William was **seven times** as old as Ben."*

This sentence is looking at the **past column** of our table. It says:

> *William's age 12 years ago = 7 × Ben's age 12 years ago*

Substituting from the table:

> **7(b − 12) = 4b − 12**

- The parentheses around `b − 12` are **essential** — the 7 multiplies the entire expression, not just `b`.
- This equation now encodes the complete story.

---

## 🔧 Step 4 — Solve

**Distribute the 7:**

> 7b − 84 = 4b − 12

**Subtract `4b` from both sides:**

> 3b − 84 = −12

**Add 84 to both sides:**

> 3b = 72

**Divide by 3:**

> **b = 24**

✅ **Ben is 24 years old.** And William, being four times Ben's age, is **96 years old.**

---

## ✅ Step 5 — Verify Against Both Conditions

**Present condition** — Is William four times Ben?
> 4 × 24 = **96** ✅

**Past condition** — Twelve years ago:
- Ben was 24 − 12 = **12**
- William was 96 − 12 = **84**
- Is 84 seven times 12? → **7 × 12 = 84** ✅

Both sentences of the original problem are fully satisfied.

---

## 💡 The Deeper Takeaway

This problem teaches two things that go beyond the arithmetic:

1. **Multiplicative relationships are time-specific.** A ratio holds at the moment it is stated. Do not carry it backwards or forwards through time.
2. **Universal time shift.** Everyone ages at the same rate. Past age = current age − elapsed years. This applies to every person in the problem, independently and equally.

> *"The ratio tells you about now. The subtraction tells you about then. Keep them separate and the problem almost solves itself."*

---
---

# 🏭 Problem 3 — The Factory (A System with No Solution)

## The Problem

> *"In a factory, each machine produces 14 toys and each worker packs 2 toys. At the end of the day, 40 toys remained unpacked. The number of workers was eight less than seven times the number of machines. How many machines and workers are there?"*

This problem looks like a routine two-variable system. It is not. The algebra will expose something remarkable — the problem's own data **contradicts itself**.

---

## 🔑 Step 1 — Name the Unknowns

> **Let M = number of machines**
> **Let W = number of workers**

Unlike the age problems, these two quantities do not have an obvious direct relationship upfront — the relationship is given as a separate piece of information. So we genuinely need both variables here.

---

## 🔍 Step 2 — Translate Constraint 1: The Production Equation

The first block of information is about what machines and workers actually do:

- Each machine produces **14 toys** → total produced = `14M`
- Each worker packs **2 toys** → total packed = `2W`
- **40 toys remained unpacked** at the end of the day

Build this up from first principles:

> *Produced − Packed = Unpacked*

> **14M − 2W = 40** ← Equation 1

---

## 🔍 Step 3 — Translate Constraint 2: The Worker-Machine Relationship

Read the sentence phrase by phrase:

- *"Seven times the number of machines"* → `7M`
- *"Eight less than that"* → `7M − 8`
- *"The number of workers was..."* → this equals `W`

> **W = 7M − 8** ← Equation 2

---

## 🔧 Step 4 — Substitute and Solve

Equation 2 already expresses `W` directly — this is an open invitation to substitute. Replace `W` in Equation 1 with `7M − 8`:

> 14M − 2(7M − 8) = 40

> ⚠️ **The parentheses are critical.** The `−2` multiplies **both** terms inside. Do not drop them.

Distribute the `−2`:

> 14M − 14M + 16 = 40

Combine the `M` terms:

> **16 = 40**

---

## 🚨 Step 5 — Read the Contradiction

> *"Zero equals six? The calculator must be broken."*
>
> *"The calculator is fine. The factory is broken."*

The statement `16 = 40` is not a miscalculation. It is the algebra delivering a verdict:

> **No values of M and W can satisfy both equations simultaneously. The system has no solution.**

---

## 🗺️ Step 6 — Understand Why (The Geometry)

Let us rewrite Equation 1 in the same form as Equation 2 by solving for `W`:

> 14M − 2W = 40 → 2W = 14M − 40 → **W = 7M − 20**

Now compare the two equations side by side:

| | Equation |
|---|----------|
| From constraint 1 | W = **7M − 20** |
| From constraint 2 | W = **7M − 8** |

- Both lines have **the same slope: 7**.
- But they have **different intercepts**: −20 versus −8.
- On a graph, these are **parallel lines** — running side by side forever, never intersecting.

> *"The solution to a system lives where two lines cross. Parallel lines never cross. Therefore, no solution exists."*

In the story, this means: the production data implies workers should equal `7M − 20`, but the given relationship says they equal `7M − 8`. Both cannot be true at the same time. The factory as described **cannot logically exist**.

---

## 💡 The Deeper Takeaway

> *"Algebra is not just a calculation machine. It is a consistency checker."*

When the constraints you are given contradict each other, algebra exposes it — clearly, precisely, and without ambiguity. The false statement `16 = 40` is not a failure. It is the mathematics working perfectly, telling you: *"The world you described cannot exist."*

In engineering, economics, and data science, this kind of contradiction appears constantly. The algebra does not panic — it simply reports the truth.

---
---

# 🍎 Problem 4 — The Fruit Market (Another Impossible System)

## The Problem

> *"On the first market visit, 2 pounds of apples and 1 pound of bananas cost \$3. On the second visit, 6 pounds of apples and 3 pounds of bananas cost \$15. Find the price per pound of apples and bananas."*

---

## 🔑 Step 1 — Name the Unknowns

> **Let a = price per pound of apples (in dollars)**
> **Let b = price per pound of bananas (in dollars)**

No upfront relationship connects these two quantities. We need both variables.

---

## 🔍 Step 2 — Translate Visit 1

> *"2 pounds of apples and 1 pound of bananas cost \$3."*

- 2 pounds of apples at `a` dollars/pound → costs `2a`
- 1 pound of bananas at `b` dollars/pound → costs `b`
- Total: \$3

> **2a + b = 3** ← Equation 1

---

## 🔍 Step 3 — Translate Visit 2

> *"6 pounds of apples and 3 pounds of bananas cost \$15."*

> **6a + 3b = 15** ← Equation 2

---

## ⚡ Step 4 — The Ratio Test (30-Second Early Warning)

Before doing any algebra, check the ratios of coefficients across both equations:

| | Equation 1 | Equation 2 | Ratio |
|---|:-----------:|:----------:|:-----:|
| Apples coefficient | 2 | 6 | **3** |
| Bananas coefficient | 1 | 3 | **3** |
| Constant (cost) | 3 | 15 | **5** |

- The left-side ratios are both **3** — equal. ✅
- The right-side ratio is **5** — different. ❌

> *"When the left sides are proportional but the right sides are not — stop. The system is already broken. No solution exists before a single algebraic step is taken."*

This test takes 20 seconds and saves minutes of algebra. Learn it.

---

## 🔧 Step 5 — Confirm via Elimination

We proceed through the algebra to see the contradiction emerge.

**Multiply Equation 1 by −3:**

> −3 × (2a + b = 3) → **−6a − 3b = −9**

**Add to Equation 2:**

> (6a + 3b) + (−6a − 3b) = 15 + (−9)

> **0 = 6**

Zero does not equal six. Contradiction confirmed.

---

## 🗺️ Step 6 — Understand the Geometry

Rewrite both equations in slope-intercept form:

- Equation 1: **b = −2a + 3**
- Equation 2: **b = −2a + 5**

- Same slope: **−2** on both. They are parallel.
- Different intercepts: **3** vs **5**. They never meet.

And in the story? The reasoning is beautifully simple:

- Visit 1 bought one "basket" (2 apples, 1 banana) for \$3.
- Visit 2 bought **three of that same basket** (6 apples, 3 bananas).
- If prices were consistent, Visit 2 should cost exactly **3 × \$3 = \$9**.
- But it cost **\$15**. That is impossible under fixed prices.

> *"The market visits are not describing the same price reality. Either prices changed between visits, the data was recorded incorrectly, or the problem is intentionally constructed as a trap."*

The algebra proves it, cleanly and irrefutably.

---

## 💡 The Deeper Takeaway

This problem reveals the **deepest use** of a system of equations — one that most algebra courses never explicitly name:

> *"A system of equations does not just find unknowns. It tests whether a set of facts is **internally consistent**."*

When you set up the equations and the algebra produces a contradiction, you have answered something more important than the original question: you have proven that **no world exists where all the given facts are simultaneously true**. The solution set is empty — written mathematically as ∅.

This reasoning is the bedrock of hypothesis testing in statistics and machine learning. Assume the data is consistent, derive what it implies, check whether the implication holds — and if it does not, reject the assumption.

---
---

# 🔄 The Big Picture — Four Problems, One Framework

Now that all four problems are complete, let us step back and see what they collectively reveal.

---

## The Three Fates of a System

All four problems fall into one of three possible outcomes, which together form the complete taxonomy of linear systems:

| Algebraic Result | Geometric Picture | Meaning | Problems |
|---|---|---|---|
| `x = a specific number` | Two lines **crossing** at one point | Consistent, independent — **one solution** | Problems 1 & 2 |
| `0 = 0` | Two **identical** lines | Consistent, dependent — **infinite solutions** | *(Lesson 8)* |
| `0 = nonzero` | Two **parallel** lines | Inconsistent — **no solution** | Problems 3 & 4 |

---

## The One Skill That Unites Everything

Every problem in this lesson — regardless of whether it had one solution, no solution, or infinite solutions — required exactly the same core act:

> **Reading a sentence and recognising the mathematical relationship hiding inside it.**

- When the sentence says *"in 40 years he will be 11 times his current age"* → you hear **two descriptions of the same quantity** and write `11x = x + 40`.
- When the sentence says *"twelve years ago, William was seven times Ben"* → you look at the **past column** and write `7(b − 12) = 4b − 12`.
- When the data produces `16 = 40` or `0 = 6` → you hear the algebra saying **"this story cannot exist"** and report no solution.

The numbers change. The names change. The costume changes. But the skeleton is always the same.

---

## ⚠️ The Five Most Common Mistakes (Summary)

1. **Misidentifying the anchor of a ratio** — *"11 times his current age"* is not the same as *"11 times his future age."* Always ask: this multiple, of *what*, at *what moment*?
2. **Reapplying a present ratio to the past** — William's age 12 years ago is `4b − 12`, not `4(b − 12)`. Time shifts are additive and universal; ratios are snapshots of a single moment.
3. **Dropping parentheses during substitution** — When substituting `7M − 8` into an equation, it must be wrapped in parentheses so every term gets multiplied.
4. **Panicking at a contradiction** — `0 = 6` is not an arithmetic error. It is the correct answer to the question: *"Is this data consistent?"* Answer: no.
5. **Verifying in only one equation** — Always check the final answer against **all** original sentences in the problem, not just the equation you happened to solve last.

---

## 🌟 One-Line Takeaway

> *"A word problem is an equation waiting to be written. Your job — the only job — is the translation. Get that right, and the algebra takes care of itself."*

---

*— Lesson 9 of the Systems of Linear Equations series.*
*Connects to: Lesson 1 (The Troll's Riddle), Lesson 2 (Lauren's Café), Lesson 3 (The Art of the Setup), Lesson 4 (Solving by Substitution), Lesson 5 (A Conceptual Journey), Lesson 6 (Worked Examples & Exercises), Lesson 7 (When Systems Have No Solution), Lesson 8 (When Systems Have Infinite Solutions).*
