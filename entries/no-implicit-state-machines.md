# No implicit state machines

**What it is:**

State spread across booleans, flags and nullable fields whose valid combinations and transitions are never written down.

**When / why:**

The app's behavior depends on combinations of flags nobody named as a machine. Use the audit prompt so the agent finds them, or put the standing rule in a skill so it makes states and transitions explicit, for example a discriminated union or a statechart. For a deeper pass, use Trevin Chow's bug-hunt prompt: document the machines, prove which invalid states the code can actually reach, then fix them with tests.

**Exact prompt:**

> Find all of the implicit state machines in my app

Standing rule for skills / rules files:

> No implicit state machines

Bug hunt (Trevin Chow):

> Find the app’s explicit and implicit state machines and document their states, invariants, and transition tables in one file. Identify invalid states or transitions the code can actually reach, with evidence, including through retries and concurrency. Prioritize confirmed bugs by impact, group related fixes into issues, then fix them with regression tests and keep the document updated.

**Why this packs more than a tip:**

Naming the pattern lets the agent hunt for it and replace it with an explicit machine. The audit prompt finds the flag piles; the standing rule is the bar; the bug-hunt prompt turns the name into a documented machine plus confirmed bugs.

**Source:**

- Origin: quoted
- Person / handle: Steve Ruiz (@steveruizok)
- Date: 31 Oct 2026
- URL: https://x.com/steveruizok/status/2116552016218710389
- Spread: Garrett Petersen (@GarrettPetersen), 7 Nov 2026, https://x.com/GarrettPetersen/status/2118881530064019806; Nate Berkopec (@nateberkopec), 7 Nov 2026, https://x.com/nateberkopec/status/2118922131857883380
- Extension: Trevin Chow (@trevin), 6 Nov 2026, https://x.com/trevin/status/2118690987153186845

**Optional gloss (source's words):**

> good prompt "find all of the implicit state machines in my app"

Garrett Petersen, quoting Steve:

> Major refactor as a result of this. Also adding "no implicit state machines" to my agent skills. Simply knowing the phrase "implicit state machine" is the kind of thing that pays off in the age of vibe coding.

Trevin Chow, quoting Steve:

> This is an amazing prompt that helps find a ton of bugs for me.

**Related:**

- [Pokayoke](pokayoke.md)
- [Tautological tests](tautological-tests.md)
