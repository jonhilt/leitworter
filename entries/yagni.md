# YAGNI

**What it is:**

You Aren't Gonna Need It: an XP rule to write only what the current ask needs, not extras that might be useful later.

**When / why:**

The agent is padding a small change with validation, configuration, error handling or comments you did not ask for. Name YAGNI so it writes the smallest code that does the task.

**Exact prompt:**

> Follow YAGNI principles. Write the smallest code that does what was asked.

**Why this packs more than a tip:**

YAGNI is an established XP principle, so the word pulls in a known bar against speculative code. Nate's variant also names the usual extras to skip: input validation, configuration options, error handling the prompt did not ask for, and comments.

**Source:**

- Origin: quoted
- Person / handle: Nate Berkopec (@nateberkopec)
- Date: 25 Nov 2026
- URL: https://x.com/nateberkopec/status/2125418152758751573
- Variant: https://github.com/nateberkopec/stylebench/blob/main/variants/yagni.md
- Results: https://nateberkopec.github.io/stylebench/

The post announces stylebench for Ruby: a vibes-based, no pass/fail comparison of how models, thinking levels and simple prompt modifications change solutions to small Ruby problems. YAGNI is one of those prompt modifications. Side-by-side results: https://nateberkopec.github.io/stylebench/

**Optional gloss (source's words):**

Full text of `variants/yagni.md`:

> Follow YAGNI principles. Write the smallest code that does what was asked.
>
> Do not add input validation, configuration options, or error handling the prompt did not ask for.
>
> Never add code comments.
