# Test seams

**What it is:**

A place you can change behaviour in tests without editing the production path.

**When / why:**

Use test seams when you need tests around code that hits a clock, filesystem, HTTP, or database, and the agent wants to rewrite the production path or mock by editing the code under test. Ask for a seam so tests can substitute a dependency at one join, and production stays on the real path.

**Exact prompt (leading word):**

> test seams

Use the phrase when talking about where to inject tests or substitutes. Skip the textbook digression.

**Why denser than a tip:**

Names Feathers' idea: a place you can alter behaviour in tests without editing production paths.

**Source:**

- Concept: Michael Feathers, *Working Effectively with Legacy Code*
- As a Leitwort for agents: Matt Pocock, 16 Jun 2026 — https://x.com/mattpocockuk/status/2066922013000671731

**Optional gloss (Matt):**

> For engineering, leading words like "tracer bullets", "deep modules", "test seams", "clean code" are outrageously effective for leading the agent to produce better code.

**Related:**

- [Tracer bullets](tracer-bullets.md)
- [Deep modules](deep-modules.md)
