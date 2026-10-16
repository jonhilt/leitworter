# Holdout

**What it is:**

Holdout-set evaluation from machine learning. The work gets scored on checks the agent has not seen, not only on the ones you gave it.

**When / why:**

You hand the agent a task with tests or acceptance criteria and it bends the code to pass exactly those. Tell it you will judge against a holdout, so it builds for the real goal and leaves room for cases you have not shown it.

**Exact prompt:**

> you will be judged against a holdout

**Why this packs more than a tip:**

It names a known evaluation setup, so the agent treats the stated tests as a sample, not the whole exam. That pushes against overfitting to the checks already on the page.

**Source:**

- Origin: quoted
- Person / handle: Nate Berkopec (@nateberkopec), crediting the idea to Dan Luu
- Date: 15 Oct 2026
- URL: https://x.com/nateberkopec/status/2110627578633691308

**Related:**

- [Tautological tests](tautological-tests.md)
- [What would make this wrong](what-would-make-this-wrong.md)
