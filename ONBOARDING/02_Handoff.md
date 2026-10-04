# Upstream Edits

**Project:** `K_GRAPHIFY`  
**Tier:** TIER_4_INFERENCE_AGENTS  
**Identity:** Upstream `networkx/networkx` @ `92f497e2eb81` (BSD-3-Clause)

## Applied patches

| Patch | Target | Kind | Behaviour change | Test |
| --- | --- | --- | --- | --- |
| `K_GRAPHIFY-egress-001` | `UPSTREAM/networkx/_anticloud_egress.py` | behaviour | with ANTICLOUD_OFFLINE=1, any socket connection to a hosted frontier API raises EgressDenied instead of dialling out | `tests/upstream/test_egress_guard.py::test_frontier_host_denied_when_offline` |

Each patch is judged on behaviour, not on volume. A patch that only
writes to the ledger is not counted; `anticloud audit-edits` excludes it
and the project is reported as unimproved rather than as improved.
