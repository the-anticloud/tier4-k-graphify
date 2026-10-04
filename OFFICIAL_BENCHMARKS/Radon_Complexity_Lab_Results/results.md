# Radon_Complexity_Lab_Results
**Project:** `K_GRAPHIFY` | **Status:** `PASS` | **Run:** `2026-09-30T17:14:20.030944+00:00`

**Framework:** [Radon — Cyclomatic Complexity & Maintainability Index](https://radon.readthedocs.io/)

## Key Metrics

- **files_analyzed:** `10`
- **average_complexity:** `{'grade': 'B', 'score': 5.5}`
- **complexity_grade:** `B`
- **complexity_score:** `5.5`
- **mi_output:** `E:\fenta\Downloads\The Anticloud\TIER_4_INFERENCE_AGENTS\K_GRAPHIFY\UPSTREAM\doc\conf.py - A (71.55)
E:\fenta\Downloads\`

## Raw Output (first 50 lines)
```
E:\fenta\Downloads\The Anticloud\TIER_4_INFERENCE_AGENTS\K_GRAPHIFY\UPSTREAM\doc\conf.py
    F 289:0 new_setitem - B (6)
    F 314:0 new_str - A (2)
    F 275:0 setup - A (1)
E:\fenta\Downloads\The Anticloud\TIER_4_INFERENCE_AGENTS\K_GRAPHIFY\UPSTREAM\networkx\conftest.py
    F 79:0 pytest_collection_modifyitems - B (7)
    F 44:0 pytest_configure - A (5)
    F 25:0 pytest_addoption - A (1)
    F 105:0 set_warnings - A (1)
    F 137:0 add_nx - A (1)
E:\fenta\Downloads\The Anticloud\TIER_4_INFERENCE_AGENTS\K_GRAPHIFY\UPSTREAM\networkx\convert.py
    F 374:0 from_dict_of_dicts - D (26)
    F 34:0 to_networkx_graph - D (25)
    F 253:0 to_dict_of_dicts - C (14)
    F 213:0 from_dict_of_lists - B (8)
    F 187:0 to_dict_of_lists - A (5)
    F 461:0 to_edgelist - A (2)
    F 479:0 from_edgelist - A (1)
E:\fenta\Downloads\The Anticloud\TIER_4_INFERENCE_AGENTS\K_GRAPHIFY\UPSTREAM\networkx\convert_matrix.py
    F 1132:0 from_numpy_array - E (33)
    F 318:0 from_pandas_edgelist - C (20)
    F 893:0 to_numpy_array - C (20)
    F 496:0 to_scipy_sparse_array - C (14)
    F 226:0 to_pandas_edgelist - C (13)
    F 783:0 from_scipy_sparse_array - C (11)
    F 765:0 _generate_weighted_edges - A (4)
    F 46:0 to_pandas_adjacency - A (2)
    F 154:0 from_pandas_adjacency - A (2)
    F 755:0 _dok_gen_triples - A (2)
    F 721:0 _csr_gen_triples - A (1)
    F 734:0 _csc_gen_triples - A (1)
    F 747:0 _coo_gen_triples - A (1)
E:\fenta\Downloads\The Anticloud\TIER_4_INFERENCE_AGENTS\K_GRAPHIFY\
```

---
_Anticloud Independent Benchmark — 2026-09-30T17:14:20.030944+00:00_