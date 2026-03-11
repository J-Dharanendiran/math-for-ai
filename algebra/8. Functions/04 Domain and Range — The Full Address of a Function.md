# 🎯 Domain and Range — The Full Address of a Function

> *"A function without a domain is like a sentence without a subject — grammatically present, but fundamentally incomplete."*

---

## 🌉 Where the Last Story Left Us

In the last lesson, you learned to write intervals — to say precisely which real numbers belong to a set and which do not. You saw filled dots and hollow circles, square brackets and round ones, the union symbol stitching together sets with gaps. It felt like learning punctuation: small marks carrying enormous meaning.

But punctuation exists to serve language. And the language it serves here is the language of functions.

Every time you restricted a domain — `x ≥ 0` for the square root branch, `[−5, 5]` for the semicircle — you were already doing domain work without calling it that. Now we name it properly, build it carefully, and see the second side of the coin it lives on: the **range**.

> *"The domain tells a function what it is allowed to receive. The range tells the world what it is capable of producing."*

These two sets — one for inputs, one for outputs — are the **full address** of a function. A formula alone is not enough. Where it lives and what it can reach are just as essential.

---

## 🚪 The Domain — Legal Inputs Only

The **domain** of a function is the set of all inputs for which the function produces a valid, defined output. Think of it as the function's front door policy: some values are welcome, and some are turned away — not out of preference, but because the mathematics simply breaks down for them.

Most functions you will encounter have domains that are restricted by one of three culprits.

**The first culprit is division by zero.** Consider `f(x) = 2/x`. Feed in `x = 3` and you get `2/3` — perfectly fine. Feed in `x = π` and you get `2/π` — still fine. But feed in `x = 0` and the universe objects: `2/0` is undefined. There is no real number that `2/0` equals. So `x = 0` is evicted from the domain, and the domain becomes:

$$\{x \in \mathbb{R} \mid x \neq 0\} \quad = \quad (-\infty, 0) \cup (0, \infty)$$

Notice that the formula `2/x` looks perfectly innocent — there is no visual alarm. The restriction only reveals itself when you ask: *where does this break?*

**The second culprit is the square root of a negative number.** The principal square root is only defined for non-negative inputs — you cannot take the square root of a negative number and stay in the real numbers. So for `g(y) = √(y − 6)`, the expression inside the radical must satisfy `y − 6 ≥ 0`, which gives `y ≥ 6`. The domain is `[6, ∞)` — and the function does not exist at all to the left of `y = 6`.

**The third culprit is explicit restriction** — functions that are simply *declared* to exist only at certain points. The function `h(x)` defined as `h(π) = 1` and `h(3) = 0`, with nothing else specified, has domain `{3, π}`. Not an interval, not a connected stretch of the number line — just two isolated points. This might look exotic, but it is a perfectly valid function: every input in its domain has exactly one output. That is all a function requires.

---

## 🧭 Finding the Domain — A Reliable Path

Whenever you encounter a new function and need its domain, the process is the same: look for every place the formula might break, exclude those inputs, and express what remains in interval notation.

1. **Find every denominator** and solve for when it equals zero. Those values are excluded.
2. **Find every even root** (square root, fourth root, etc.) and require the radicand to be `≥ 0`. Solve the resulting inequality.
3. **Find every logarithm** and require its argument to be strictly greater than zero. Solve `argument > 0`.
4. **If the function is piecewise or explicitly defined**, the domain is the union of the specified input sets.
5. **For compositions `f(g(x))`**, first find the domain of `g`, then require that `g(x)` lands inside the domain of `f`. The final domain satisfies both conditions simultaneously.

Let's walk a slightly harder example through all of this. Take `p(x) = √(x − 1) / (x − 3)`. Two restrictions apply here at once: the square root requires `x − 1 ≥ 0`, giving `x ≥ 1`; and the denominator requires `x ≠ 3`. Combining these, the domain is all `x ≥ 1` with `x = 3` removed:

$$[1, 3) \cup (3, \infty)$$

The lesson of interval notation is paying off immediately — without it, you could not write this answer cleanly.

> *"Finding a domain is an act of mathematical honesty: you are admitting every place the function might mislead you and removing it from consideration before any damage is done."*

---

## 🌅 The Range — What the Function Can Actually Produce

The domain answers the question: *what can go in?* The range answers the other half: *what can come out?*

The **range** of a function is the set of all output values the function actually produces when you feed it every element of its domain. It is not the set of outputs you *imagine* it might produce, or the set you *wish* it produced — it is the set it *actually does* produce.

This distinction becomes vivid immediately with `f(x) = x²`.

The domain is all real numbers — you can square any real number without issue. But now ask: what values can `x²` actually reach? Squaring a positive number gives a positive result. Squaring a negative number *also* gives a positive result (because `(−3)² = 9`). Squaring zero gives zero. No matter what you put in, the output is never negative.

*The range is `[0, ∞)` — non-negative reals only.* The number `−1` will never appear as an output of `f(x) = x²`, no matter which `x` you choose. If someone asks you to solve `x² = −1` in the real numbers, you can answer immediately: *impossible, because `−1` is not in the range*.

---

## 🕳️ The Hole That Changes Everything

The second example from the video is more subtle, and it is worth dwelling on.

Consider `g(x) = x²/x`. Your algebra instinct says: *simplify — cancel the `x` from top and bottom and you get `g(x) = x`.* And algebraically, that simplification is correct. For any `x ≠ 0`, the function behaves exactly like the identity function.

But the original function `x²/x` is **undefined at `x = 0`**, because you cannot divide by zero. The domain is `ℝ \ {0}` — all reals except zero. And because `x = 0` is not in the domain, the output `g(0) = 0` is never produced. The range is also `ℝ \ {0}` — all reals except zero.

On a graph, this appears as the line `y = x` with a single hollow circle punched out at the origin. The function traces the entire line *except for that one point*. It looks almost complete — but "almost" is not "entirely", and in mathematics that gap is real.

> *"Cancelling a factor in algebra removes it from the formula — but it does not restore it to the domain. The original function will never produce the value that the simplification forgot."*

This is one of the most common mistakes in all of calculus: simplifying an expression, forgetting the domain restriction that created the simplification, and then claiming an output value that the original function could never actually reach. Always refer back to the original expression when determining domain and range.

---

## 🔭 How Range and Domain Speak to Each Other

The domain and range do not live in isolation — they are in constant conversation with each other, and changes to one ripple through to the other.

**The range depends entirely on the domain.** The same formula can have completely different ranges depending on which domain you declare. The function `f(x) = x²` with domain `ℝ` has range `[0, ∞)`. But `f(x) = x²` with domain `[1, 3]` has range `[1, 9]` — because the smallest square on `[1, 3]` is `1² = 1` and the largest is `3² = 9`. Restrict the inputs, and you automatically restrict the outputs.

**Invertibility lives at the intersection.** A function can only have an inverse on a set where it is *one-to-one* — where different inputs produce different outputs — and where its range covers the intended codomain. This is exactly why `f(x) = x²` needs a domain restriction to have an inverse: on all of `ℝ`, both `3` and `−3` produce `9`, so the function is not one-to-one. Restrict the domain to `[0, ∞)`, and the function becomes one-to-one, its range is `[0, ∞)`, and its inverse is `f⁻¹(x) = √x`. *You cannot have a square root without first making a decision about the domain of the square.*

**Solvability of equations lives in the range.** When someone asks you to solve `f(x) = c`, the very first question should be: *is `c` in the range of `f`?* If it is not, the equation has no solution and no further work is needed. If `f(x) = x²`, then `f(x) = −1` has no real solution — not because the algebra fails, but because `−1` is simply not in the range. Checking the range before solving is not laziness; it is mathematical efficiency.

---

## 🧪 Quick Examples to Cement the Picture

A handful of worked examples, read carefully, do more for understanding than a page of theory:

- `f(x) = 1/(x − 2)`: domain is `(−∞, 2) ∪ (2, ∞)`, range is also `(−∞, 0) ∪ (0, ∞)` — the output can never be zero because no finite `x` makes `1/(x−2) = 0`.
- `g(x) = √(x + 3)`: domain is `[−3, ∞)`, range is `[0, ∞)` — square roots are always non-negative.
- `h(x) = 1/(x² + 1)`: domain is all of `ℝ` (the denominator `x² + 1` is always at least `1`, never zero); range is `(0, 1]` — the output approaches zero but never reaches it, and reaches its maximum of `1` at `x = 0`.
- `f(x) = eˣ`: domain is `(−∞, ∞)`, range is `(0, ∞)` — the exponential is always positive, no matter how negative the input becomes.

Each example is a small story: the domain tells you where the function is alive, and the range tells you what territory it covers while it lives.

---

## 🚧 The Mistakes Worth Warning You About

A few traps catch almost every student at least once, so it is better to name them now:

- **Cancelling a factor and forgetting the hole.** Simplifying `x²/x` to `x` is algebraically correct, but the point `x = 0` remains excluded from the domain — and therefore from the range — regardless of the simplification.
- **Confusing codomain with range.** The *codomain* is the set you *declare* outputs to live in (often `ℝ`). The *range* is the set outputs *actually* occupy. Declaring `ℝ` as codomain does not make the range all of `ℝ` — `f(x) = x²` has codomain `ℝ` but range `[0, ∞)`.
- **Forgetting endpoint inclusion when the maximum or minimum occurs at an excluded boundary.** If the domain is `(0, 1)` (open) and the function achieves its maximum value only at `x = 1`, then that maximum is *not in the range*, because `x = 1` is not in the domain.
- **Assuming a continuous function has all of `ℝ` as its range.** Continuity on all of `ℝ` does not mean the function reaches every real value. `eˣ` is continuous everywhere but never outputs a negative number.

---

## 🧾 Everything Tied Together

The journey of this lesson has two equal halves that complete each other.

The **domain** is the set of legal inputs — every value of `x` for which the function is defined and produces a real, valid result. It is determined by hunting for division by zero, negative radicands, non-positive logarithm arguments, and explicit restrictions. It is expressed in interval notation and set-builder form, using exactly the grammar the last lesson taught you.

The **range** is the set of actual outputs — everything the function can produce when fed every element of its domain. It is not declared but *derived*, either by algebraic inversion, by examining the graph, by checking limits at boundaries, or by reasoning about the behaviour of the formula. It changes when the domain changes. It governs whether equations are solvable, whether inverses exist, and how functions can be composed.

Together, domain and range give a function its complete identity. The formula is the rule. The domain is where the rule applies. The range is what the rule achieves. A function described by all three is fully specified — and a function missing any one of them is only partially known.

> *"Domain and range are not administrative details appended to a function after the real work is done. They are the real work. Know them, and you know the function. Ignore them, and the formula is just a beautiful lie."* 🎯

---

*This lesson continues the Functions series. Domain and range will reappear in every topic ahead — in piecewise functions, in inverse functions, in limits and continuity, and throughout calculus. The language built here is the foundation for all of it.*
