# Scheduling Tool — Friendly Constraint Input

Status: exploring

## Problem / Motivation

The scheduling tool itself already exists and works well — the solver and its
constraints are properly implemented. The open problem is narrower: **how a
user inputs those constraints.**

Constraints in practice can be quite diverse and, at their core, math/logic
heavy — but end users shouldn't need that literacy to configure them. There's
already a rule-builder UI for this, and it works, but it's still complex and
technical to use correctly.

Example domain used to think this through: a dog walking service.
- Some dogs can't be walked together (pairwise incompatibility).
- Dogs vary in size; walkers vary in ability to handle bigger/stronger dogs.
- Some walkers are excluded from walking specific dogs entirely.
- Vans have limited capacity, constrained by both dog size and count.
- All of the above needs to be balanced simultaneously, not configured in
  isolation.

## Rough Approach

Not settled yet. Discussed one option (shift from a generic rule builder to
domain-specific constraint templates — pairwise incompatibility matrix,
per-entity attribute profiles, exception lists — so users fill in properties
instead of authoring logic) but it didn't quite fit the actual shape of the
problem. Missing context to get this right in a text conversation — needs to
be worked out against the real tool, its current rule builder, and the actual
constraint types it supports.

Also on the table from an earlier, more general framing: an LLM-based
natural-language input layer as an assist on top of whatever structured input
model gets chosen, with a mandatory confirm/preview step before anything is
saved (never let parsed output write directly to the solver's input
unvalidated).

## Open Questions

- What's the actual taxonomy of constraint *shapes* the current rule builder
  supports? (Pairwise exclusion, capacity/bin-packing, eligibility, load
  balancing, others?)
- Which of those are common enough to deserve a dedicated, non-technical
  input pattern, vs. rare enough to leave behind a more technical fallback?
- Where exactly does the current rule builder feel hardest to use — is it the
  logic authoring itself, or something else (discoverability, error
  feedback, combining multiple constraint types at once)?
- If an NL/LLM input layer gets added later: constrain its output to a fixed
  schema/template set (safer, more reliable) rather than open-ended rule
  generation, and treat its output as an untrusted draft requiring user
  confirmation.

## Links / Resources

- To be continued by working directly in the actual scheduling tool repo.
