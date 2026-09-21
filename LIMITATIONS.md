# Limitations — read this before citing the headline number

## What this run actually is

- **A single run**, on **one principal's contract**, graded by **one human**, with a
  single set of 30 scenarios. It is evidence that the evaluation idea is executable,
  not a measurement of all agents everywhere.
- **No cross-model comparison.** The same system ran the simulators and produced the
  reference behaviors. Whether other models score differently is untested — that's the
  interesting follow-up work, not a claim made here.
- **Human grading.** Every score is a judgment call against explicit criteria. The
  criteria are published so anyone can re-grade; the judgments themselves are not
  reproducible in the automated sense.

## Known weaknesses

1. **Simulator contamination (real finding).** The fresh-agent simulators were subagents
   of the same system, and despite strict "packet-only" instructions they leaked
   parent-transcript context (e.g., names) into some responses. Roleplay-only isolation
   is imperfect. The behavioral scores concern contract adherence, not information
   boundaries — but any future run must isolate better (separate sessions, no shared
   transcript) and run explicit contamination checks.
2. **Contract portability is unproven.** The criteria encode one principal's operating
   rules (approval semantics, tone, scheduling caps, notification discipline). Porting
   requires rewriting the contract for your principal; scores don't transfer between
   contracts.
3. **The PARTIAL shows rubric sensitivity.** b16 scored PARTIAL for omitting one
   explicit behavior while being substantively correct. That's the rubric working as
   intended — but it also means small criteria-wording choices move scores.
4. **Single scenario set.** 30 scenarios cover 12 categories, but real principal-agent
   failures concentrate in long, messy, multi-turn interactions. These are single-turn
   probes; multi-turn degradation is not tested here.

## Hypothetical, not run

- Cross-model comparisons
- Larger or different scenario sets
- Automated grading
- Multi-turn or longitudinal evaluation
- A "deployment gate" workflow built on top of the benchmark

## Public safety boundary — what this repo deliberately does NOT contain

- No real personal records, names, or identifiers
- No personal, medical, legal, financial, or health context
- No private benchmark packets or raw logs
- No agent credentials, secrets, or internal system prompts
- No proprietary or private project details
- No scenario prompts containing real disputes, case numbers, addresses, or deadlines

Every scenario here is a sanitized equivalent: the behavioral demand is preserved
exactly, the surface details are generic. That trade was made deliberately — this repo
demonstrates the methodology and proves it was exercised, not the principal's life.
