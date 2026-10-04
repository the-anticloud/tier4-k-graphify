# HF_Leaderboard_Lab_Results

**Project:** `K_GRAPHIFY`  
**Tier:** `TIER_4_INFERENCE_AGENTS`  
**Slug:** `networkx/networkx`  
**Commit:** `92f497e2eb81`  
**Run:** `2026-09-30T15:07:07.146295+00:00`  

## Isolation Environment

| Field | Value |
| ----- | ----- |
| Platform | `win32` |
| Python | `3.12.10` |
| HF model | `distilbert-base-uncased` |
| HF load time | `4.42s` |
| Inference device | `cpu` |

## Results

**Framework:** [HuggingFace Open LLM Leaderboard (proxy via distilbert-base-uncased)](https://huggingface.co/docs/leaderboards/en/open_llm_leaderboard/archive)

**Model used:** `distilbert-base-uncased`

### Inference Latency (Classification)

| Metric | Value |
| ------ | ----- |
| Avg latency | **46.13 ms** |
| Min latency | 40.01 ms |
| Max latency | 50.08 ms |
| Samples | 5 |

### Real Tokenization Results

| Field | Value |
| ----- | ----- |
| Token count | **39** |
| Tokenization latency | 1.0 ms |
| Classification label | `LABEL_0` |
| Classification score | 0.5825 |
| Classification latency | 73.67 ms |
| Status | **PASS** |

**Input text tokenized:**
```
K_GRAPHIFY (networkx/networkx) — 976 files, 205825 source lines, licence BSD-3-Clause, primary language ['Python']
```

**First 20 tokens:**
```
['[CLS]', 'k', '_', 'graph', '##ify', '(', 'network', '##x', '/', 'network', '##x', ')', '—', '97', '##6', 'files', ',', '205', '##8', '##25']
```

> Full MMLU/HellaSwag/TruthfulQA/ARC/Winogrande/GSM8K require dedicated GPU.
> These results are CPU inference proxy metrics using distilbert-base-uncased.

---
_Anticloud Benchmark Suite — isolation log — 2026-09-30T15:07:07.146295+00:00_