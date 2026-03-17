# 📐 Units Are Not Labels — They Are Algebra

> *"The moment you start treating units like variables, math stops being guesswork and starts being logic."*

---

## 🧠 What Is This Really About?

On the surface, this looks like a lesson about speed and distance.

But underneath, Sal Khan is teaching something far more important:

**Units behave exactly like algebraic symbols.**

You can multiply them. Divide them. Cancel them. Group them.
The same rules that govern variables like *x* and *y* govern meters, seconds, and kilograms.

Once you see that — you never have to *guess* whether to multiply or divide again.

---

## 🔩 The Core Idea

Start with the simple formula:

$$d = r \times t$$

If **r = 5 m/s** and **t = 10 s**, don't just multiply the numbers.
Write the *full* expression — numbers *and* units together:

$$d = (5 \times 10) \times \left(\frac{\text{m}}{\text{s}} \times \text{s}\right)$$

Now look at the unit part:

$$\frac{\text{m}}{\text{s}} \times \text{s} = \frac{\text{m} \times \text{s}}{\text{s}} = \text{m}$$

The seconds **cancel** — just like $\frac{x}{x} = 1$.
What remains is meters. The answer is **50 m**.

The unit didn't just tag along. It *told you the answer was right.*

---

## 🔄 When Units Don't Match — Enter the Conversion Factor

Now suppose **r = 5 m/s** but **t = 2 hours**.

If you multiply naively:

$$5 \frac{\text{m}}{\text{s}} \times 2\ \text{hour} = 10\ \frac{\text{m} \cdot \text{hour}}{\text{s}}$$

That unit — *meter·hour/second* — means nothing physically. It's a warning sign.
Your setup is wrong.

**The fix:** multiply by a conversion factor that equals exactly 1.

Since $1\ \text{hour} = 3600\ \text{s}$, the fraction $\dfrac{3600\ \text{s}}{1\ \text{hour}} = 1$.

Multiplying by 1 never changes the *value* of an expression. But it changes its *form*.

$$d = 5\ \frac{\text{m}}{\text{s}} \times 2\ \text{hour} \times \frac{3600\ \text{s}}{1\ \text{hour}}$$

Now watch:
- **hour** in the numerator cancels with **hour** in the denominator ✅
- **s** in the denominator cancels with **s** in the numerator ✅
- What remains: **meters** ✅

Arithmetic: $5 \times 2 \times 3600 = 36{,}000\ \text{m}$

---

## 💡 The Insight That Changes Everything

You're not *replacing* the hour with 3600 seconds.
You're **multiplying by a disguised form of 1** — a ratio where the numerator and denominator are equal in value but different in unit form.

It's the same as multiplying by $\dfrac{x}{x}$.
The equation stays balanced. The units shift into the form you need.

> *"You're not changing the quantity. You're changing the language it's written in."*

---

## ⚠️ Common Mistakes to Watch For

1. **Wrong direction of conversion factor** — if the unit you want to remove ends up *multiplying* instead of *cancelling*, flip the fraction.
2. **Square and cubic units** — converting area needs the conversion factor *squared*. $1\ \text{m}^2 = (100\ \text{cm})^2 = 10{,}000\ \text{cm}^2$.
3. **Arithmetic last** — cancel units first, compute numbers after. Doing it the other way leads to confusion.

---

## 🧪 Try This Yourself

You've just converted **km/h → m/s** by multiplying by $\dfrac{3600\ s}{1\ hr}$ and $\dfrac{1000\ m}{1\ km}$.

Now ask yourself:

> *If I wanted to go the other direction — convert **m/s → km/h** — how would those same conversion factors need to flip?*

Don't look it up. Reason it from the units.
If your conversion factors cancel correctly and leave km/h, your logic is sound.

When you're confident — move to the next file.

---

📂 **Next:** [`02-reasonable-units.md`](./02-reasonable-units.md) — *When your answer is correct but still wrong.*
