# Deep modules

**What it is:**

Lots of behaviour behind a small interface. Callers stay simple because the module hides the messy bits.

**When / why:**

The agent is splitting a feature into lots of little files, but every caller still passes flags, knows the storage shape, or wires internals. The split looks tidy. The call sites still know too much. That's when you say deep modules.

**Exact prompt (leading word):**

> deep modules

Drop the phrase into design and review. Don't turn it into a design essay unless asked.

**Why denser than a tip:**

Names Ousterhout's idea: a lot of behaviour behind a small interface.

**Source:**

- Concept: John Ousterhout, *A Philosophy of Software Design*
- As a Leitwort for agents: Matt Pocock, 16 Jun 2026 — https://x.com/mattpocockuk/status/2066922013000671731

**Optional gloss (Matt):**

> For engineering, leading words like "tracer bullets", "deep modules", "test seams", "clean code" are outrageously effective for leading the agent to produce better code.

**Related:**

- [Tracer bullets](tracer-bullets.md)
- [Test seams](test-seams.md)
