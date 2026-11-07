# No implicit state machines

**What it is:**

State spread across booleans, flags and nullable fields whose valid combinations and transitions are never written down.

**When / why:**

The app's behavior depends on combinations of flags nobody named as a machine. Use the audit prompt so the agent finds them, or put the standing rule in a skill so it makes states and transitions explicit, for example a discriminated union or a statechart.

**Exact prompt:**

> Find all of the implicit state machines in my app

Standing rule for skills / rules files:

> No implicit state machines

**Why this packs more than a tip:**

Naming the pattern lets the agent hunt for it and replace it with an explicit machine. The audit prompt finds the flag piles; the standing rule is the bar.

**Source:**

- Origin: quoted
- Person / handle: Steve Ruiz (@steveruizok)
- Date: 31 Oct 2026
- URL: https://x.com/steveruizok/status/2116552016218710389
- Spread: Garrett Petersen (@GarrettPetersen), 7 Nov 2026, https://x.com/GarrettPetersen/status/2118881530064019806; Nate Berkopec (@nateberkopec), 7 Nov 2026, https://x.com/nateberkopec/status/2118922131857883380

**Optional gloss (source's words):**

> good prompt "find all of the implicit state machines in my app"

Garrett Petersen, quoting Steve:

> Major refactor as a result of this. Also adding "no implicit state machines" to my agent skills. Simply knowing the phrase "implicit state machine" is the kind of thing that pays off in the age of vibe coding.

**Related:**

- [Pokayoke](pokayoke.md)
- [Tautological tests](tautological-tests.md)
