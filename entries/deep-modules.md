# Deep modules

**What it is:**

A lot of behaviour behind a small interface. Callers stay simple because the module hides the work.

**When / why:**

Use deep modules when an agent is carving a feature into many small files whose callers still pass flags, know the storage shape, or wire internals. Reach for this when the split looks tidy but every call site has to know too much.

**Exact prompt (leading word):**

> deep modules

Use the phrase in design and review. Do not expand it into a design essay unless asked.

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
