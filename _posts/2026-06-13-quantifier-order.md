---
layout: post
title: "Why quantifier order matters more than you think"
date: 2026-06-13
---

<script src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js"></script>

Quantifier order matters for the same reason tenses matter in English — a small change shifts the entire meaning. Swap the order of ∀ and ∃ in a mathematical statement and you don't get a variation of the same claim, you get a different claim entirely. Get it wrong in a proof and your proof is saying something you never intended.

## The four basic combinations

- **∀x∃y** — for every x, there is some y, but y can change depending on which x you pick
- **∃x∀y** — there is one specific x that works for every single y simultaneously  
- **∀x∀y** — the statement must hold for every possible pair of x and y
- **∃x∃y** — there exists some specific x and some specific y that make it true

In ∀x∀y and ∃x∃y, the order of x and y does not matter. That is not true for the mixed cases.

## Worked example — Velleman 2.1.4

Universe of discourse: ℕ (natural numbers).

**1. ∀x∃y(x < y)** — True. For every x, there exists a y greater than it. Since natural numbers go on forever, you can always find a bigger one.

**2. ∃y∀x(x < y)** — False. This claims one specific y is greater than every natural number simultaneously. Since ℕ is infinite, no such y exists.

**3. ∃x∀y(x < y)** — False. This claims one specific x is smaller than every y including itself. That would require x < x, which is impossible.

**4. ∀y∃x(x < y)** — Depends on whether 0 ∈ ℕ. If yes, false — nothing is smaller than 0. If ℕ starts at 1, true.

**5. ∃x∃y(x < y)** — True. We just need one pair where x < y. Every natural number has a larger one.

**6. ∀x∀y(x < y)** — False. Pick x = 3 and y = 2. That gives 3 < 2, which is false. One counterexample kills a universal statement.

---

Statements 1 and 2 look almost identical but have opposite truth values. The only difference is which quantifier comes first. That is exactly why order matters.
