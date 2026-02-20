# When "OR" Creates Full Coverage — The Structure Behind Compound Inequalities

In the previous file, you learned that every linear equation collapses to a structural skeleton — and that skeleton forces exactly one of three outcomes: one solution, no solution, or infinite solutions. That was about **equality**. This file asks a broader question: what happens when we stop demanding equality and instead ask where a condition is *at least partially* satisfied? That shift from equality to inequality, and from a single condition to two connected conditions, opens up an entirely new kind of structural thinking — one based not on intersection points, but on **regions and coverage**.

---

## 🔗 Where This Connects

In the previous document, we studied what happens when two linear expressions are set equal. We discovered that the outcome depends entirely on the structure of the coefficients — whether slopes match, whether constants match — and from that structure, only three outcomes are possible.

But equality asks a very strict question: *"Where are these two expressions exactly the same?"* The answer is either one point, no point, or every point.

Inequalities ask something broader: *"Where is at least one condition satisfied?"* And when you connect two inequality conditions with the word **OR**, you are building a solution set from the union of two regions — which sometimes covers the entire number line, and sometimes leaves a gap. Understanding which outcome occurs, and why, is the structural insight this file is building toward.

---

## 🎬 The Given Compound Inequality

$$5z + 7 < 27 \quad \textbf{or} \quad -3z \leq 18$$

At first glance, this looks like a straightforward two-part problem — solve each side, write the answer. But something structurally interesting happens here. The final solution turns out to be **all real numbers**. Not because of a coincidence in the arithmetic, but because of a precise geometric relationship between the two solution regions. That is what we are about to unpack.

---

## Step 1 — Solve Each Inequality Separately

With compound inequalities, the first move is always to treat each part as its own independent problem. The word OR connecting them does not affect how you solve either side — it only affects how you *combine* the results afterward.

### First Inequality

$$5z + 7 < 27$$

Subtract 7 from both sides:

$$5z < 20$$

Divide by 5 — positive divisor, so no sign flip:

$$z < 4$$

This inequality is satisfied by every real number to the left of 4, not including 4 itself. In interval notation: $(-\infty, 4)$.

### Second Inequality

$$-3z \leq 18$$

Divide both sides by $-3$. This is the step students most commonly get wrong. Because you are dividing by a **negative number**, the inequality sign must flip — $\leq$ becomes $\geq$:

$$z \geq -6$$

This inequality is satisfied by every real number to the right of $-6$, including $-6$ itself. In interval notation: $[-6, +\infty)$.

---

## 🧠 The Structural Question

After solving both sides, most students immediately write the union and move on. But the more important question to ask at this stage is not *"did I solve correctly?"* — it is:

> *"Do these two regions leave any gap uncovered on the number line?"*

That is the structural lens. You are not just combining two answers. You are asking whether two regions, taken together, account for every possible real number — or whether there is some stretch of the number line that neither region claims.

We now have:

$$z < 4 \quad \textbf{or} \quad z \geq -6$$

Which in interval notation is:

$$(-\infty,\ 4) \quad \cup \quad [-6,\ +\infty)$$

The union symbol $\cup$ is the mathematical expression of OR. A number belongs to the solution set if it belongs to **either** interval — it does not need to satisfy both.

---

## 📉 Visualizing the Regions

The number line makes the structure immediately visible:

```
First inequality  (z < 4):
←══════════════════════o————————————
                       4

Second inequality (z ≥ -6):
————————————●══════════════════════→
           -6

Combined (union):
←══════════════════════════════════→
           -6          4
```

The first inequality shades everything to the **left** of 4. The second shades everything to the **right** of $-6$. The critical observation is that these two regions **overlap** between $-6$ and $4$ — and because they overlap, there is no gap anywhere on the number line. Every point is claimed by at least one of the two regions.

---

## 🚀 Why the Entire Number Line Is Covered

To be fully convinced, it helps to test the logically extreme cases — not just a value in the middle, but values at the edges of where you might expect the coverage to break down.

Take a very large number, say $z = 10{,}000$. Does it satisfy the first inequality? No — $10{,}000$ is not less than 4. Does it satisfy the second? Yes — $10{,}000 \geq -6$. So it is in the solution set.

Take a very negative number, say $z = -1{,}000$. Does it satisfy the first inequality? Yes — $-1{,}000 < 4$. It does not even need to pass the second check. It is already in.

Take a number right in the overlap zone, say $z = 0$. It satisfies both inequalities simultaneously — $0 < 4$ and $0 \geq -6$. Both are true.

There is literally no real number that fails **both** conditions. Since OR only requires one condition to be true, every real number qualifies. The union is:

$$(-\infty, 4) \cup [-6, +\infty) = (-\infty, +\infty)$$

Which is simply: **all real numbers**.

---

## 🔁 Structural Parallel to Linear Equations

This outcome has a deep parallel to something you already understand. In the linear equations file, when slopes matched **and** constants matched, the two expressions were identical — they agreed at every point on the number line, producing infinite solutions. The algebra collapsed to $0 = 0$, a statement that is always true.

Here, something structurally analogous happens. The two inequality regions are not identical, but together they **cover** every point on the number line. No real number escapes both conditions. Just as $0 = 0$ signaled total agreement between two expressions, the complete union here signals total coverage by two regions.

Different mechanism, same structural outcome: the answer expands to encompass everything.

Now consider what would have changed if the second inequality had been $z \geq 10$ instead of $z \geq -6$. Then the two regions would be $(-\infty, 4)$ and $[10, +\infty)$ — and the stretch between 4 and 10 would be claimed by neither. A gap would exist, the union would not cover everything, and the answer would be written as $(-\infty, 4) \cup [10, +\infty)$. The outcome depends entirely on whether the boundary points create overlap or separation — which is a structural question about position, not an arithmetic question about steps.

---

## 🧪 Test Yourself — Create a Gap Example

Now that you understand what makes coverage complete, try to construct the opposite. Design a compound inequality with OR whose solution is **not** all real numbers — one where a gap exists between the two regions.

To do this, think backwards. You need two boundary points where the first region ends **before** the second region begins, with no overlap between them. What would the two original inequalities need to look like to produce that structure?

Once you have your example, solve both sides, draw the number line, identify the gap, and write the union in interval notation. If you can construct and explain a gap example from scratch, you have fully internalized the structural logic — not just the procedure.

---

> *"The goal was never to find a number. The goal was to map where the truth lives."*

---

*Next: Compound Inequalities with AND — where both conditions must be satisfied simultaneously, the solution becomes an intersection rather than a union, and the outcome can shrink to a bounded region, a single point, or nothing at all.*
