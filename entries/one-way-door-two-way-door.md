# One-way door / two-way door

**What it is:**

A forced split of a risky change: first a reversible (two-way door) PR, then a stacked follow-up that actually takes the irreversible (one-way door) step.

**When / why:**

A huge PR is about to mix a reversible rollout with an irreversible cut: dropping a column, deleting the old path, a hard cutover. Ask the agent to split it, so you can ship and test the reversible part in production before the door closes.

**Exact prompt:**

> Split this "one-way door" PR into two:
>
> 1. A PR that implements everything, except it can be easily reverted (a two-way door)
> 2. A followup PR (stacked on top) that actually goes through the one-way door
>
> AKA expand/contract. Use feature flags as needed.

**Why this packs more than a tip:**

It names two things the model already has: one-way vs two-way doors, and expand/contract. The agent sorts the work into a reversible part and an irreversible part, so most of the change can be tested in production before the door closes.

**Source:**

- Origin: quoted
- Person / handle: Matt Pocock (@mattpocockuk)
- Date: 26 Oct 2026
- URL: https://x.com/mattpocockuk/status/2114749427889979405

**Optional gloss (source's words):**

> Lets you de-risk a huge PR by testing large chunks of it in production first.

**Related:**

- [Tracer bullets](tracer-bullets.md)
- [Vertical slices](vertical-slices.md)
- [Brittle / durable](brittle-durable.md)
