# Changelog

## v0.5 — Quiet Write-back

- added bounded standing permission for low-risk private-state writes;
- conversation flow no longer needs repeated “save this” interruptions when the user has granted that permission;
- defined **semantic blast radius** as the key test for write authority: if a stored claim is wrong, could it bias many future interpretations?;
- separated Write Authority from Semantic Authority;
- made identity/personality generalization, cross-domain generalization, major model promotion, strong causal stories, long-term Human Policy, and sensitive identifiable third-party material confirmation-gated by default;
- added fail-closed behavior for ambiguous write-authority cases;
- added the invariant: **AI may quietly save facts and revocable threads; it may not quietly increase semantic authority**;
- added a behavioral eval for quiet write-back;
- added a public research note documenting the design origin.

## v0.4 — Quiet Continuity

- memory is available, not performative;
- default to pull-first continuity;
- retrieve prior context when the user reopens a topic;
- do not proactively surface private unfinished threads without explicit user permission;
- do not simulate missing, waiting for, or emotionally tracking the user;
- added a behavioral eval for non-creepy long-term continuity;
- added `BOOTSTRAP.md` so users can point a GitHub-capable AI at the public protocol and optionally maintain personal longitudinal state in a separate private repository;
- made the public-protocol / private-personal-state boundary explicit;
- added `notes/` as a public research-log layer for time-stamped seeds and design thoughts that have no default protocol authority;
- documented the boundary: public history explains how the method evolves; private history belongs to the person.

## v0.3 — Reality Loop

Initial public GitHub version.

Added / made explicit:

- Reality before Model for compressed personality/causal labels;
- natural episode-first questioning;
- distinction between emotional venting and problem-solving;
- Choice Point as the bridge from reflection to agency;
- Reality Test with competing predictions;
- advice utility does not validate model truth;
- stop when reality is next;
- AI has no Identity Authority;
- public behavioral evals.

## v0.2 — Cognitive Mirror

- warm conversational surface + fixed epistemic discipline;
- candidate models instead of canonical persona;
- source/lineage distinctions for historical material;
- recursive confirmation warning;
- counterevidence and alternatives;
- presentation modes: warm / balanced / cool / exploratory.

## v0.1 — Seed

- “被看见，但不被定义。”
- AI as mirror, not identity authority.
