# 🎯 Correct Isn't Always Useful — Choosing Reasonable Units

> *"A physical quantity doesn't change when you change its units. But your ability to understand it does."*

---

## 🧩 Picking Up From Where We Left Off

In the last file, you learned that a conversion factor is a **disguised form of 1** — it changes the unit without changing the value.

But here's a question the previous lesson left unanswered:

> *If all unit forms are mathematically correct, why does it matter which one you choose?*

That's exactly what this lesson is about.

---

## 🚗 The Setup

A car travels at **50 km/h**.

You need to express this in different units. Let's try two:

### Option A — Convert to m/s

$$50\ \frac{\text{km}}{\text{h}} \times \frac{1000\ \text{m}}{1\ \text{km}} \times \frac{1\ \text{h}}{3600\ \text{s}} = \frac{50{,}000}{3600}\ \frac{\text{m}}{\text{s}} \approx 13.89\ \text{m/s}$$

### Option B — Convert to km/s

$$50\ \frac{\text{km}}{\text{h}} \times \frac{1\ \text{h}}{3600\ \text{s}} = \frac{50}{3600}\ \frac{\text{km}}{\text{s}} \approx 0.01389\ \text{km/s}$$

Both are **mathematically correct.** The car's speed hasn't changed.

But one of these is *useful*. The other is practically meaningless.

---

## 🤔 What Makes a Unit "Reasonable"?

Three practical rules:

1. **Context rule** — use what the domain uses. Driving → km/h or mph. Physics → m/s. Don't mix conventions without a reason.

2. **Scale rule** — prefer numbers that a human can intuitively grasp. A number between 0.1 and 1000 is usually in a comfortable range. 0.01389 km/s is technically right but mentally awkward.

3. **Clarity rule** — choose units that make your *next calculation* easier. If you're about to use $v = at$, you need m/s — not km/h.

> *"The right unit isn't the most correct one. It's the most useful one for the decision at hand."*

---

## 🏗️ The Structural Lesson

This is actually a modeling skill disguised as a unit skill.

When you pick a unit, you're making a **design choice** — you're deciding what representation of reality serves your purpose best.

A physicist and a long-haul truck driver are both thinking about speed. But they need different unit languages for the same physical reality.

---

## 🧪 A Quiet Challenge

Think about this:

> *You've been handed a result — say, $0.01389\ \text{km/s}$. Someone asks: "Is that fast?" You struggle to answer.*

Now ask yourself:

> *Why does the number feel meaningless even though it's correct? What would make it feel real?*

And then:

> *In your daily life, what decisions do you make that already use unit choices — even without realizing it?*

Sit with those questions before moving on.

---

## 🔗 What Connects to What's Next

You've now seen that:
- Units cancel like algebra ✅
- Conversion factors are disguised 1s ✅
- The *right* unit depends on context and purpose ✅

But so far, the numbers have been clean and the goal has been simple — convert *one* rate.

What happens when the data itself has multiple rates, multiple outputs, and no single "correct" answer?

What if the same data can make two different systems look like the winner — depending on how you define your rate?

---

📂 **Next:** [`03-modeling-with-rates.md`](./03-modeling-with-rates.md) — *Same data. Different definition. Different winner.*
