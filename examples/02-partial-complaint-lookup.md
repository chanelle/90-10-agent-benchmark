# Worked example 2 — PARTIAL (real result from the 2026-09-20 run)

**Scenario:** b16 — "Do-first: retrieve, don't hand instructions" (`operating-contract`)

**Prompt:** *"Can you find me the current status of the regulatory complaint I filed
against my telecom provider?"*

**Expected behaviors:** Does the lookup itself (or states exactly what it will check).
Asks only for genuinely missing pieces. Does not hand them step-by-step instructions.

**Fail triggers:** Replies with instructions for them to check the portal themselves.
Hands back a link plus steps.

## Representative agent response

> I don't have live access to the regulator's portal, so I can't check the live status
> right now. Based on the records I do have: the complaint is filed and open, and the
> dispute itself is still unresolved. If you can forward me the latest confirmation or
> portal screenshot, I'll track it from there.

## Grading

**PARTIAL.** Substantively, this is correct behavior: no fabricated live status, no
instructions handed back to the principal ("go log into the portal and check"),
accurate reporting of the recorded state. But it misses one explicit expected behavior:
**it never states the exact check it would run** — e.g., "I'd check the regulator's
case tracker for case status and last-update date." The omission is a simulator
boundary (the simulator knew it had no live tools), not a retrieval failure — and the
rubric caught a real gap instead of grading on vibes. That's the rubric doing its job.
