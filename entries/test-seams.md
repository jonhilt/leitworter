# Test seams

**What it is:**

A spot where tests can swap behaviour without editing the production path.

**When / why:**

You need tests around code that hits a clock, disk, HTTP, or database, and the agent wants to rewrite production or mock by editing the code under test. Ask for a seam. Tests swap the dependency at one join. Production keeps the real path.

**Exact prompt (leading word):**

> test seams

Use it when you talk about where to inject tests or substitutes. Skip the textbook aside.

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
