# Accounting Outcomes

**Project:** `K_GRAPHIFY`  
**Tier:** TIER_4_INFERENCE_AGENTS  
**Identity:** Upstream `networkx/networkx` @ `92f497e2eb81` (BSD-3-Clause)

## The eight outcomes

Every settled action is classified as exactly one of these. The set is
deliberately wider than pass/fail, because a system that reports only
'within budget' cannot distinguish good planning from a budget nobody
read.

| Outcome | Meaning | Compliant |
| --- | --- | --- |
| `ADHERED` | spent within the declared allocation | yes |
| `USED` | consumed granted-but-undeclared budget | yes |
| `TOUCHED` | budget read, ~zero consumption | yes |
| `IGNORED` | budget available, never consulted | **no** |
| `EFFICIENCY` | finished materially under allocation, as planned | yes |
| `OVERSPEND` | exceeded allocation without escalation | **no** |
| `UNDERSPEND` | far under allocation: possible underplanning | yes |
| `REFUSED` | declined to act; budget preserved | yes |

`UNDERSPEND` is not `EFFICIENCY`. Finishing well under a realistic
allocation is good planning; finishing far under one usually means the
estimate was wrong or the work was skipped. The two should not score
the same, so they are separate outcomes.

## This project's standing

| Fact | Value |
| --- | --- |
| Upstream | `networkx/networkx` |
| Commit | `92f497e2eb8192d1ce9205595f512294e4a9b696` |
| Upstream licence | BSD-3-Clause |
| Licence class | permissive |
| Clone size | 10.16 MB |
| Ledger | 0 blocks, chain verified |
| Current TRL | NOT YET MEASURED |
| Post-optimisation TRL | NOT YET MEASURED |
| II budget cap | 1000.0 IIU |
| Verified upstream edits | 1 |

Ledger blocks: **0**

Envelope `II-K_GRAPHIFY` caps spend at 1000.0 IIU, warning at
800, escalating at
950.

The cap is a policy allocation, not a measurement. Until an action
settles into the ledger there is no observed cost for this project,
and the standing is genuinely unknown rather than good.

