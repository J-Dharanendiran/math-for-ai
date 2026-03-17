# 📈 Above, Below, Rising, Falling — The Story of a Function's Behaviour

> *"A function does not merely produce values — it tells a story. And like every good story, it has moments of rise and fall, moments of light and shadow, moments of turning points that change everything."*

---

## 🌉 Where the Last Story Left Us

In the last lesson, you walked through a mountain landscape and learned to identify its most dramatic features — the absolute peak that towers over everything, the humble hilltop that commands only its own neighbourhood, the valley floor that sits lower than the slopes on either side. You learned to call these extrema, and you learned to distinguish the global champions from the local heroes.

But here is the thing about landscapes: peaks and valleys are only two of the many things worth noticing. A landscape also has *slopes* — stretches where the ground is rising under your feet, stretches where it is falling away, stretches that sit high above the river below and stretches that are already submerged. These are different observations from asking where the highest or lowest point is, and they carry their own information.

A function's graph works the same way. And in this lesson, we will learn to read two entirely new dimensions of a function's behaviour:

> *"Is the function currently **above** or **below** the x-axis? And is it currently **rising** or **falling** as we move left to right?"*

These sound like they might be related — and they are, in the way that elevation and slope are related when hiking. But they are *not* the same question, and the most important lesson of this entire lesson is understanding exactly where they diverge.

---

## 📍 The X-Axis as a Horizon Line

Before we ask whether a function is increasing or decreasing, let us ask a simpler question first: *where is the function relative to the x-axis?*

Think of the x-axis as a **horizon line** — a flat sea-level reference that divides the graph into two worlds. Above the horizon, the sky is positive. Below the horizon, the water is negative. A function's graph rises above this line in some places and dips below it in others, and the x-intercepts are exactly the moments where the graph crosses from one world to the other.

This is the idea behind **positive and negative intervals** — and the definitions are as direct as they sound.

A function is **positive** on an interval when its output values are greater than zero on that interval — when the graph lives *above* the x-axis. A function is **negative** on an interval when its output values are less than zero — when the graph dips *below* the x-axis. At the x-intercepts themselves, the function is neither positive nor negative: it is exactly zero, sitting right on the horizon.

In the Khan Academy example, the function crosses the x-axis at three points: `a`, `b`, and `c`. This immediately carves the number line into four distinct stretches, and the function's sign alternates as you pass through each crossing. The function is *negative* before `a` (below the horizon), *positive* between `a` and `b` (above), *negative* between `b` and `c` (below again), and *positive* beyond `c` (above again). Writing this in interval notation — the precise language you learned in Lesson 03:

- **Positive:** $(a, b) \cup (c, \infty)$
- **Negative:** $(-\infty, a) \cup (b, c)$

Notice the open parentheses at `a`, `b`, and `c`. Those points are *not* included in either the positive or the negative intervals, because at those exact x-values the function equals zero — it is on the horizon, belonging to neither sky nor sea. This is a small but important precision: the moment of crossing is not itself above or below.

---

## 📐 Reading Sign from a Graph

Finding positive and negative intervals is, at its heart, a visual exercise. You look at the graph, identify every x-intercept, and then ask a simple question for each stretch between them: *is the curve above the x-axis here, or below?*

What makes this worth practising carefully is not the difficulty of any individual step — it is the discipline of writing the answer with correct interval notation, remembering to exclude the zeros, and handling the infinitely long stretches at the left and right ends of the graph. Those stretches extend toward $-\infty$ and $+\infty$, and as you learned in the intervals lesson, infinity always wears a parenthesis.

The sign of a function is also connected to something you have already met: the **range** of the function, which tells you what output values are actually produced. If a function's range is entirely $[0, \infty)$, for instance, then the function is never negative — it never dips below the horizon at all. Domain and range, positive and negative intervals — they are all parts of the same conversation about where a function lives.

---

## 🧭 A Different Question Entirely — Rising and Falling

Now we shift focus, and the shift is significant. Positive and negative intervals ask *where* the function is relative to the x-axis. The next question asks something different altogether: *which direction is it moving?*

A function is **increasing** on an interval if, as `x` moves to the right across that interval, the output `y` also moves upward. Every step forward in `x` produces a higher output. The graph climbs. A function is **decreasing** on an interval if the opposite is true — as `x` moves right, `y` moves downward. Every step forward produces a lower output. The graph descends.

Formally, mathematicians write this as:

> **A function `f` is increasing on an interval if, for any two inputs `x₁ < x₂` in that interval, `f(x₁) < f(x₂)`.**

> **A function `f` is decreasing on an interval if, for any two inputs `x₁ < x₂` in that interval, `f(x₁) > f(x₂)`.**

The formal definitions might look intimidating, but they say exactly what the plain-language descriptions say: *pick any two x-values in the interval, look at their outputs, and check whether the larger x produced the larger output (increasing) or the smaller output (decreasing).*

---

## ↗️ The Tangent Line Shortcut

The Khan Academy instructor offers a beautiful visual shortcut for identifying increasing and decreasing intervals on a graph: *imagine laying a tangent line against the curve at any point, and ask what slope that line has.*

If the imagined tangent line tilts upward from left to right — a positive slope — the function is **increasing** at that point. If the tangent tilts downward — a negative slope — the function is **decreasing**. And if the tangent is perfectly horizontal — slope exactly zero — the function is at a turning point: neither increasing nor decreasing at that instant.

This shortcut is doing something deep. It connects the idea of *direction* to the idea of *slope*, and slope is a concept you have already met in the linear functions story. Back in Lesson 01, slope `m` in `f(x) = mx + c` told you the rate of change — how much `y` changes per unit increase in `x`. For a linear function, that slope is constant everywhere. But for a curved function, the slope changes from point to point, and the tangent line at each point captures the *instantaneous* slope at that exact location.

This is precisely the idea that calculus will formalise later as the **derivative**. For now, the intuition is enough: *wherever the tangent tilts up, the function rises; wherever it tilts down, the function falls; wherever it lies flat, the function turns.*

---

## 🔄 The Turning Points

The flat tangent lines — the moments of slope zero — occur at the peaks and valleys you met in the last lesson. At `x = d` (a relative maximum), the function has been increasing and is about to begin decreasing. At `x = e` (a relative minimum), the function has been decreasing and is about to begin increasing. These are the **turning points**, the hinges of the story.

At those exact points, `x = d` and `x = e`, the function is classified as *neither increasing nor decreasing*. This is why increasing and decreasing intervals are expressed with **open intervals** at the turning points — the endpoints themselves are excluded, just as x-intercepts were excluded from positive and negative intervals. The transition moment belongs to no direction.

In the example from the video, the function increases from the far left all the way up to the peak at `x = d`, then decreases through the valley until it reaches the trough at `x = e`, then increases again from there to the right. Written in interval notation:

- **Increasing:** $(-\infty, d) \cup (e, \infty)$
- **Decreasing:** $(d, e)$

Notice that this function has *one* decreasing interval and *two* increasing intervals, separated by the turning points. The shape of the graph dictates the structure of the answer.

---

## ⚡ The Most Important Distinction — Sign vs. Direction

And now we arrive at the heart of this lesson — the moment the Khan Academy instructor pauses and says: *these two ideas are not the same thing.*

Positive/negative tells you **where** the function is. Increasing/decreasing tells you **where it is going**. These are genuinely independent properties, and a function can combine them in any of four ways at any given point:

- **Positive and increasing** — above the x-axis, climbing upward. The graph is in the sky and rising higher. ☀️↗️
- **Positive and decreasing** — above the x-axis, descending toward it. Still in the sky, but heading toward the horizon. ☀️↘️
- **Negative and increasing** — below the x-axis, climbing upward. Underwater but rising toward the surface. 🌊↗️
- **Negative and decreasing** — below the x-axis, descending further. Underwater and sinking deeper. 🌊↘️

This is the insight that catches almost every student off guard the first time. We intuitively want *positive* and *increasing* to go together — something good and growing — and *negative* and *decreasing* to go together — something bad and worsening. But mathematics has no such preference. A function can be below zero and still be climbing. It can be above zero and still be falling. The x-axis and the direction of travel are simply two separate measurements of two separate things.

> *"Positive means you are above sea level. Increasing means you are walking uphill. A diver ascending from the deep is negative and increasing — below the surface, but rising. A skydiver in free fall above the clouds is positive and decreasing — above sea level, but plummeting. Sign and direction are two different stories."*

---

## 🗺️ Reading Both at Once

With this understanding in hand, let us walk through how you would analyse a complete graph — reading both the positive/negative and the increasing/decreasing properties simultaneously, and seeing exactly where they overlap and where they diverge.

Suppose a function has the following story: it enters from the bottom-left, below the x-axis and rising. It crosses the x-axis at `x = a`. It continues to climb, reaching a peak at `x = d` (which is above the x-axis). It descends from that peak, crosses the x-axis downward at `x = b`. It continues descending below the x-axis into a valley at `x = e`. It then rises from that valley, crosses the x-axis upward at `x = c`, and continues rising into positive territory.

Now read the two properties separately and lay them side by side:

The function is *negative* on $(-\infty, a) \cup (b, c)$ and *positive* on $(a, b) \cup (c, \infty)$.

The function is *increasing* on $(-\infty, d) \cup (e, \infty)$ and *decreasing* on $(d, e)$.

Now ask: where is the function negative *and* increasing simultaneously? That is the stretch from $-\infty$ to `a` — below the x-axis and climbing toward it. And between `e` and `c` — below the x-axis but rising back up through it. Where is it positive and decreasing? Between `d` and `b` — above the x-axis but descending toward and then below it. The positive and increasing intervals are $(a, d)$. And so on.

The function's complete behaviour is only visible when you hold both lenses up at once.

---

## 📝 Writing the Intervals — The Precision That Matters

One detail deserves particular attention: the choice between open and closed brackets when writing these intervals. The rules follow directly from what each boundary point represents.

For **positive and negative intervals**, the boundary points are the x-intercepts — the zeros of the function. At those points the function equals exactly zero, which is neither positive nor negative, so those points are *excluded*. Open parentheses everywhere.

For **increasing and decreasing intervals**, the boundary points are the turning points — the peaks and valleys where the slope is momentarily zero. At those points the function is neither increasing nor decreasing, so again those points are *excluded*. Open parentheses everywhere.

This means both kinds of intervals are always expressed with open brackets at their transition points. The only time a square bracket might appear is at an endpoint of the domain itself, if that endpoint is included in the domain — a detail that only matters if the function has a restricted domain rather than extending to infinity.

---

## 🤖 Why This Will Matter Later

These two behaviours — sign and direction — are not just ways to describe a graph. They are the building blocks of analysis, and they will return in every mathematical context you encounter going forward.

In **calculus**, the sign of the *derivative* at a point is exactly what determines whether the original function is increasing or decreasing there. The derivative is positive when the function rises, negative when it falls, and zero at the turning points. You are already thinking in the language of calculus, even if the formal machinery has not arrived yet.

In **machine learning**, a model's loss function must decrease over the course of training — the algorithm needs the loss to be on a *decreasing* interval as parameters are updated. Monitoring whether the loss is actually decreasing (and not merely positive or negative) is one of the fundamental diagnostic tools of model training. If the loss is decreasing, the model is learning. If it has plateaued — if the function is neither increasing nor decreasing, sitting at a turning point — the model may have found a minimum, or it may be stuck.

In **economics**, a company's revenue function might be positive (profitable) but decreasing (revenue is falling). That combination — above zero but heading downward — is exactly the warning sign an analyst looks for. Positive and increasing together is growth. Positive and decreasing is a trend worth watching. These two properties, read together, tell a story that neither tells alone.

> *"Sign tells you where you are. Direction tells you where you are going. You need both to understand what is actually happening."*

---

## 🧾 The Recap You Can Keep

This lesson introduced two new ways of reading a function's graph, both of which describe *behaviour* rather than individual values.

**Positive and negative intervals** describe the function's position relative to the x-axis. The function is positive where its graph lives above the x-axis, negative where it dips below, and exactly zero at the x-intercepts — which are the boundary points excluded from both intervals. These are found by identifying every zero of the function and checking the sign of the output in each stretch between them.

**Increasing and decreasing intervals** describe the function's direction of travel as `x` moves from left to right. The function is increasing where every rightward step produces a higher output, decreasing where every rightward step produces a lower output, and neither at the turning points — the peaks and valleys — where the slope momentarily equals zero. Those turning points are excluded from both intervals, expressed with open parentheses.

The critical insight that ties everything together is that **sign and direction are independent**. A function can be negative and increasing, positive and decreasing, or any other combination. The x-axis is one measurement; the slope is another. Reading a function fluently means reading both simultaneously — knowing not just where the graph is at any moment, but where it is going.

And in that combination — position and direction, sign and slope, where you are and where you are heading — a function's full story becomes readable.

---

> *"A function is not a static picture. It is a journey — above and below, rising and falling, turning and continuing. Learn to read all of it, and the graph stops being a curve on a page and becomes a narrative you can follow."* 📈

---

*This lesson continues the Functions series. Positive and negative intervals connect directly to the zeros of a function, which will become central in polynomial analysis. Increasing and decreasing intervals connect directly to the derivative in calculus — where the slope of the tangent line becomes a function in its own right.*
