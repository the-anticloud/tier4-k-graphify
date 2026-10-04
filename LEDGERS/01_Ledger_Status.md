# Ledger Status

**Project:** `K_GRAPHIFY`  
**Tier:** TIER_4_INFERENCE_AGENTS  
**Identity:** Upstream `networkx/networkx` @ `92f497e2eb81` (BSD-3-Clause)

## Chain state

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

- Blocks: **0**
- Head digest: `None`
- Chain verification: **verified**

## Independent verification

The chain is verifiable without trusting this project's tooling:

```
anticloud ledger verify
anticloud ledger export > ledger.jsonl
```

Each block carries the previous block's digest, so removing or reordering an
entry invalidates every block after it. That property is the reason the
ledger can stand in for a claim of what happened.
