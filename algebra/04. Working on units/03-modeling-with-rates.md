# 📊 Same Data, Different Winner — Modeling With Rates

> *"Numbers don't speak. You make them speak. And if you define the wrong rate, you'll defend the wrong conclusion."*

---

## 🔁 Connecting Back

You've learned that units are algebraic. You've learned that a good unit choice depends on context.

Now here's the uncomfortable next step:

**You choose what counts as output. You choose what counts as input. And that choice changes the conclusion.**

Sal Khan demonstrates this with two websites. Forget the surface story — here's the structural lesson.

---

## 🌐 The Setup: Website A vs Website B

| Metric | Website A | Website B |
|---|---|---|
| Writers | 5 | 11 |
| Posts | 110 | 200 |
| Profit | $10,000 | $28,000 |
| Likes/post | 3,500 | 2,000 |

Same dataset. Now let's build rates.

---

## ⚖️ Layer 1 — Single-Level Rates

### Profit per Writer
$$\frac{\text{Profit}}{\text{Writers}}:$$
- A = $10{,}000 ÷ 5 = \$2{,}000$
- B = $28{,}000 ÷ 11 ≈ \$2{,}545$

**Website B wins.** ✅

### Posts per Writer
$$\frac{\text{Posts}}{\text{Writers}}:$$
- A = $110 ÷ 5 = 22$
- B = $200 ÷ 11 ≈ 18.2$

**Website A wins.** ✅

*Same data. Already two different winners.*

---

## 🔢 Layer 2 — Derived Totals (Multiplying Rates)

Here's where it gets deeper.

$$\text{Total Likes} = \text{Posts} \times \frac{\text{Likes}}{\text{Post}}$$

Watch the unit cancellation:

$$\text{posts} \times \frac{\text{likes}}{\text{post}} = \text{likes}$$

- A = $110 \times 3{,}500 = 385{,}000$
- B = $200 \times 2{,}000 = 400{,}000$

**Website B wins in total likes** — even though Website A has *higher likes per post*.

> *A strong average can lose to higher volume. That's real-world math.*

This is exactly the same structure as:
$$\frac{\text{miles}}{\text{hour}} \times \text{hours} = \text{miles}$$

Unit cancellation isn't just for conversions. **It's the foundation of composed metrics.**

---

## 🧱 The Three Layers of Measurement

**Layer 1 — Raw counts:** Writers, posts, profit, likes/post

**Layer 2 — Single rates:** Profit/writer, posts/writer, likes/post

**Layer 3 — Composed metrics:** Total likes, likes/writer, profit/post

As you go deeper into the layers, you can uncover subtler truths — but also create more opportunities to mislead.

---

## 🎯 The Brutal Truth

Here's what most people miss:

> *You can manufacture almost any conclusion if you're careless with definitions.*

Website A wins on posts/writer and likes/post.
Website B wins on profit/writer and total likes.

Neither answer is universally correct. **Each metric answers a different question.**

---

## 🤔 Stop and Think

Before reading further, sit with this:

> *You are the CEO. You want to maximize long-term business growth. Which single metric would you prioritize — and why?*

Your options:
- Profit per writer
- Subscribers per post
- Subscribers per writer
- Revenue per subscriber

Don't pick the one that sounds smartest. **Reason it from the goal.**

Ask yourself: *What decision is this metric actually supporting?*
Ask yourself: *What does this metric hide that another one reveals?*

If you can justify one metric cleanly — you understood the lesson.
If you find yourself saying "it depends" — you're even closer to the truth.

---

## 🔗 What Comes Next

You've now seen that:
- Rates are choices, not facts ✅
- The same data supports different narratives depending on the metric ✅
- Composed metrics (derived units) reveal things simple rates can't ✅

But there's one more level.

What if you didn't need to write an equation at all?
What if the *units themselves* guided every step — from the given data, all the way to the answer?

That's dimensional chaining. And it's the most powerful form of everything you've learned.

---

📂 **Next:** [`04-dimensional-chaining.md`](./04-dimensional-chaining.md) — *Let the units do the thinking.*
