# 🏔️ Peaks and Valleys — The Story of Absolute and Relative Extrema

> *"Mathematics is the science of what is possible — and to find the best possible value, you must first learn to see the peaks and valleys hiding inside every function."*

---

## 🌉 Where the Last Story Left Us

You have come a long way. You began by asking what a function even *is* — that faithful vending machine, that dependable translator mapping every input to exactly one output. You learned that equations and functions are different creatures, even when wearing the same algebraic clothing. You discovered intervals — the precise language of *belonging* — and finally, you learned to describe a function's **full address**: its domain of allowed inputs, and its range of reachable outputs.

And now, naturally, a new question rises to the surface.

> *"I know what a function produces. But which output is the **largest**? Which is the **smallest**?"*

That question — deceptively simple, profoundly important — leads us into the world of **extrema**: the peaks and valleys of a function's graph, the moments where something reaches its best or its worst value. And as you will see, there are two very different *kinds* of peaks. Understanding the difference between them is the real story here.

---

## 🗺️ The Landscape You Are About to Walk

Before a single formula appears, let us build a picture — because this topic is deeply visual, and the right image will carry you through everything that follows.

Imagine you are standing before a **mountain landscape**. The terrain rises and falls, rolls through valleys, climbs to ridges, and plunges into canyons. Some hills are modest — a gentle bump, higher than the ground immediately around it, but dwarfed by the great mountains in the distance. Somewhere in the entire landscape, though, there is one undeniable peak: the highest point of all, surveying everything below it. And somewhere — perhaps far underground, beneath a sea — there is the lowest floor of the entire world you can see.

*That landscape is a function's graph.* The x-axis is your horizontal position. The y-axis is the elevation. The questions this lesson will teach you to answer are etched into the terrain itself:

- 🏔️ **Where is the highest point of the entire landscape?** → *Absolute Maximum*
- 🕳️ **Where is the lowest point of the entire landscape?** → *Absolute Minimum*
- ⛰️ **Where are the local hilltops — high compared to their neighbours, even if not the tallest overall?** → *Relative Maximum*
- 🏞️ **Where are the valley floors — low compared to their surroundings, even if not the deepest overall?** → *Relative Minimum*

---

![Peaks and Valleys: Relative vs Absolute Extrema](peaks_and_valleys.png)
<img width="2752" height="1536" alt="unnamed" src="https://github.com/user-attachments/assets/042cf0a6-6929-494e-8054-5a7f8d9c5c49" />


> *Look at the diagram carefully. The left side shows the rolling hills of **relative extrema** — local summits and valley floors that command their own neighbourhoods. The right side shows the towering mountain and the deep underwater trench of **absolute extrema** — the undisputed global champions. Notice the comparison table at the bottom: it separates the two by scope. We will return to every corner of this image as the story moves forward.*

---

## 🎯 The Global Champions

Let us begin with the concept that carries the most authority.

An **absolute maximum** is the single highest value a function achieves across its *entire domain*. Not just near one point. Not just in one corner. Everywhere — every legal input has been considered, every output compared, and this one value won. When mathematicians write this down, they say:

> **`f(c)` is an absolute maximum if `f(c) ≥ f(x)` for every `x` in the domain.**

The condition `f(c) ≥ f(x)` must hold without exception — for every single input `x` the function is allowed to receive. The point `c` is the x-axis location where the champion value is produced, and `f(c)` is the champion value itself.

The **absolute minimum** is the same idea, flipped to the floor:

> **`f(c)` is an absolute minimum if `f(c) ≤ f(x)` for every `x` in the domain.**

Now here is something the diagram above whispers quietly in its bottom-right corner: ***absolute extrema often live at the endpoints of a domain.*** Think about why. If a function is defined on a closed interval `[a, b]`, then the walls `a` and `b` are the boundaries of the world — the function cannot travel beyond them. Sometimes the function is still climbing or still falling when it hits those walls, and so the highest or lowest point turns out to be at the very edge rather than anywhere in the interior. This is not always true, but it is common enough that **endpoints are always on your checklist** when hunting for absolute extrema.

Let us make this concrete. Take `f(x) = x²` on the closed interval `[−3, 3]`:

| Input `x` | Output `f(x) = x²` |
|---|---|
| −3 | **9** |
| −2 | 4 |
| −1 | 1 |
| 0 | 0 ← *lowest* |
| 1 | 1 |
| 2 | 4 |
| 3 | **9** |

The **absolute minimum** is `f(0) = 0`, sitting at the very bottom of the parabola. The **absolute maximum** is `f(−3) = f(3) = 9`, achieved at both endpoints simultaneously. And that last observation carries a quiet lesson: *the definition requires the output to be the highest — it makes no demand that only one input achieves it.* A landscape can have two peaks of exactly equal height and both can claim the title of absolute maximum.

---

## ⛰️ The Local Heroes

The story deepens here — because the landscape metaphor knows something the absolute champions do not. Sometimes the most *interesting* feature of a terrain is not the tallest mountain. It is the modest hill that rises above everything *immediately around it*, commanding its own neighbourhood even if the great peaks elsewhere dwarf it entirely.

That is precisely what a **relative maximum** is.

> **`f(c)` is a relative maximum if `f(c) ≥ f(x)` for all `x` in *some open interval* around `c`.**

The crucial difference from an absolute maximum lives in that phrase — *some open interval around `c`.* We are not asking `f(c)` to beat every output in the entire domain. We are only asking it to win within a *neighbourhood*: a small window centred at `c`, written mathematically as `(c − h, c + h)` for some `h > 0`. The window can be as small as you like — the relative maximum only needs to dominate *some* neighbourhood around it, however narrow that window turns out to be.

A **relative minimum** is the valley counterpart:

> **`f(d)` is a relative minimum if `f(d) ≤ f(x)` for all `x` in some open interval `(d − h, d + h)`, where `h > 0`.**

The word *neighbourhood* here is not casual language — it is a genuine mathematical object: an open interval centred at a point. And when we say `f(c)` is a relative maximum, we are making a precise claim:

> *"Draw a small enough window around `c` on the x-axis. Within that window — and only within that window — `f(c)` is undefeated."*

The diagram gives you a visual shortcut for spotting these by eye. A **relative maximum** looks like the **top of a hill**: the graph rises, reaches a crest, then falls away on both sides. A **relative minimum** looks like the **bottom of a valley**: the graph descends, touches a floor, then rises again on both sides. But notice what the diagram does *not* show — it does not show a point on a bare slope wearing the relative maximum crown. And that is intentional.

> **You cannot pick a point on a slope and call it a relative maximum.** If the graph is still climbing to the right of your chosen point, that point is not a hilltop. The function must *turn around* there — rise then fall for a maximum, fall then rise for a minimum — for the title to apply.

---

## 🔀 One Function, Both Kinds of Champions

Let us now place absolute and relative extrema side by side on the *same* function, so the contrast stops being theoretical and becomes something you can see.

Imagine a function that, over its domain, tells this story: it *starts high* at the left endpoint, *falls into a valley* somewhere in the middle, *climbs to a local hilltop* that is lower than the starting point, then *falls again* to the right endpoint — the lowest point of the entire graph. In that story, four things are true at once:

- The **absolute maximum** is at the *left endpoint* — the highest output across the entire domain, sitting right at the boundary.
- The **absolute minimum** is at the *right endpoint* — the lowest output anywhere, also at a boundary.
- There is a **relative minimum** at the interior valley — lower than everything immediately around it, even though the right endpoint descends even further.
- There is a **relative maximum** at the interior hilltop — higher than everything nearby, even though the left endpoint towers above it.

*The absolute maximum and the relative maximum are completely different points on this function.* So are the absolute minimum and the relative minimum. They coexist in the same graph, playing by different rules, wearing different titles.

> *"The absolute champion need not be a local hero. And a local hero need not be the absolute champion. These are different titles, awarded by different courts."*

---

## 📐 The Definitions, Dressed for Precision

You have already met the intuition. Now the definitions arrive in their full mathematical form — and you will find they say nothing surprising, only exactly what the story already told you.

> ✅ **Absolute Maximum** — `f(c)` is an absolute maximum of `f` if:
> $$f(c) \geq f(x) \quad \text{for all } x \text{ in the domain of } f$$

> ✅ **Absolute Minimum** — `f(c)` is an absolute minimum of `f` if:
> $$f(c) \leq f(x) \quad \text{for all } x \text{ in the domain of } f$$

> ✅ **Relative Maximum** — `f(c)` is a relative (local) maximum if there exists some `h > 0` such that:
> $$f(c) \geq f(x) \quad \text{for all } x \in (c - h,\ c + h)$$

> ✅ **Relative Minimum** — `f(d)` is a relative (local) minimum if there exists some `h > 0` such that:
> $$f(d) \leq f(x) \quad \text{for all } x \in (d - h,\ d + h)$$

Notice the `≥` and `≤` rather than strict `>` and `<`. That choice is deliberate — and it leads directly to the edge case the story has been quietly building toward.

---

## 🌀 The Flat Region — Where Both Titles Belong to Everyone

Here is the feature of these definitions that surprises almost everyone the first time.

Suppose a function is *perfectly flat* — constant — over some stretch of the x-axis. Say `f(x) = 5` for all `x` in `[2, 7]`. Every point in that stretch sits at exactly the same height. No hills, no valleys, no rise, no fall.

Now apply the definition of relative maximum to any point `c` in that region. Is there an open interval around `c` within which `f(c) ≥ f(x)` for all `x`? Yes — because `f(c) = 5 = f(x)` everywhere nearby, and `5 ≥ 5` is true. So `f(c)` *is* a relative maximum. Apply the relative minimum definition. Is `f(c) ≤ f(x)` for all nearby `x`? Yes again — because `5 ≤ 5`. So `f(c)` is *also* a relative minimum, at the very same time.

> **Every point in a flat region is simultaneously a relative maximum and a relative minimum.**

This is not a paradox. It is simply what the `≥` and `≤` signs produce when equality is the only relationship available. A perfectly flat stretch is both a hilltop and a valley floor at once — because it is neither climbing nor falling in any direction whatsoever. The diagram labels this the *"Flat Region Edge Case."* It appears rarely in standard problems, but it is worth knowing: the definitions are more generous than you might initially expect.

---

## 🔭 Scope — The One Word That Separates Everything

If you had to reduce the entire distinction between relative and absolute extrema to a single word, that word would be **scope**.

| Feature | Relative Extrema | Absolute Extrema |
|---|---|---|
| **Visual** | Any hill or valley | The highest peak or lowest floor |
| **Scope** | *Local neighbourhood* only | *Entire domain* of the function |
| **Requirement** | Higher/lower than nearby points | Higher/lower than **all** points |

Relative extrema care only about neighbours. Absolute extrema care about everyone. Think of it this way: a relative maximum is like being the tallest person in your classroom — impressive locally, but it says nothing about how you compare to the rest of the school. An absolute maximum is like being the tallest person in the *entire school* — a global title, earned only after comparison against every competitor. The moment you internalise that one contrast, the entire topic becomes navigable.

---

## 🚧 The Traps Worth Naming Before You Step in Them

A few misconceptions catch almost every student at least once, and it is better to meet them here than in the middle of a problem.

The first is **assuming every relative maximum is also an absolute maximum**. It is not. A hilltop that sits below the overall highest point is *only* a relative maximum — local champion, not global. The titles do not automatically stack.

The second is **forgetting to check endpoints when hunting for absolute extrema**. The absolute maximum or minimum can live right at the boundary of a closed interval, not only at interior peaks and valleys. The endpoints are never optional on that checklist.

The third is **calling a point on a slope a relative maximum**. If the function is still increasing to the right of your chosen point, it has not peaked there — it is mid-climb. The graph must turn around at a relative extremum.

The fourth is a vocabulary note rather than a mistake: **"relative" and "local" mean the same thing completely**. Relative maximum, local maximum — same definition, same concept, different textbooks. You will encounter both and they are interchangeable.

And the fifth is perhaps the subtlest: **a function is not guaranteed to have absolute extrema at all**. A function on an *open* interval may approach its highest or lowest value without ever actually reaching it. The function `f(x) = x` on the open interval `(0, 1)` has no absolute maximum and no absolute minimum — it never touches `0` or `1`, because neither belongs to its domain. Absolute extrema are guaranteed only on *closed, bounded intervals* — a theorem that lives in calculus, waiting for you just ahead.

---

## 🤖 Why a Landscape Problem Became the Heart of AI

Since this series has always kept one eye on where mathematics leads — toward AI, toward data science, toward the systems shaping the modern world — it is worth pausing at the end to ask: *why should any of this matter to you beyond the classroom?*

The answer is that **almost every intelligent system ever built is, at its core, solving an extremum problem.** When a machine learning model trains, it adjusts its internal parameters to *minimise a loss function* — a function that measures how wrong its predictions are. Training is the relentless search for the absolute minimum of that loss landscape. The peaks and valleys you have studied in this lesson are not abstract geometric curiosities. They are the literal terrain that every AI system must navigate to learn anything at all.

And relative minima matter here too — because the loss landscape of a real neural network is not a simple bowl with one clear bottom. It is a vast, high-dimensional landscape of rolling hills and valleys, and a training algorithm can get *trapped* in a local minimum rather than finding the global one. This is one of the great unsolved practical challenges in machine learning today. The vocabulary you learned in this lesson — relative minimum, absolute minimum, neighbourhood, scope — is the conceptual foundation of that challenge.

> *"In machine learning, finding the minimum of a function is not an application of mathematics. It is the entire point of mathematics, as far as the algorithm is concerned."*

---

## 🧾 The Recap You Can Keep

Let every thread of this lesson come together in one clean, unbroken arc.

An **absolute maximum** is the highest output across the *entire domain*, defined by `f(c) ≥ f(x)` for all `x`, and often found at the endpoints of a closed interval. An **absolute minimum** is the lowest, defined by `f(c) ≤ f(x)` for all `x`, and also often endpoint-bound. A **relative (local) maximum** is a hilltop — higher than everything in *some neighbourhood* `(c − h, c + h)` around it, local champion but not necessarily global. A **relative (local) minimum** is a valley floor — lower than everything in some neighbourhood, same local-only logic. **Flat regions** are the edge case where every point qualifies as both a relative maximum and a relative minimum simultaneously, because `≥` and `≤` permit equality. And through all of it, **scope** is the single defining difference — relative extrema are local titles awarded within a neighbourhood, while absolute extrema are global titles awarded across the full domain.

And in machine learning, the search for the absolute minimum of a loss function is not an application of this mathematics. It *is* this mathematics, made real.

---

> *"Every function tells a story — of rising and falling, of moments where something reaches its peak and moments where it bottoms out. Learning to read those moments, to name them precisely and reason about them rigorously, is how you move from computing answers to understanding landscapes. And understanding the landscape is how you find the best path through it."* 🏔️

---

*This lesson continues the Functions series. Absolute and relative extrema will return in calculus — where derivatives provide a systematic method for locating them exactly — and in optimisation theory, which is the mathematical heart of machine learning and data science.*
