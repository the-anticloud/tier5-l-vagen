# HF_Leaderboard_Lab_Results

**Project:** `L_VAGEN`  
**Tier:** `TIER_5_WORLD_NEURO_EMBODIED`  
**Slug:** `volcengine/verl`  
**Commit:** `fbb4b3a8bf63`  
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
| Avg latency | **57.31 ms** |
| Min latency | 50.52 ms |
| Max latency | 67.03 ms |
| Samples | 5 |

### Real Tokenization Results

| Field | Value |
| ----- | ----- |
| Token count | **40** |
| Tokenization latency | 1.0 ms |
| Classification label | `LABEL_0` |
| Classification score | 0.5865 |
| Classification latency | 69.32 ms |
| Status | **PASS** |

**Input text tokenized:**
```
L_VAGEN (volcengine/verl) — 1240 files, 206940 source lines, licence Apache-2.0, primary language ['Python']
```

**First 20 tokens:**
```
['[CLS]', 'l', '_', 'va', '##gen', '(', 'vol', '##cen', '##gin', '##e', '/', 've', '##rl', ')', '—', '124', '##0', 'files', ',', '206']
```

> Full MMLU/HellaSwag/TruthfulQA/ARC/Winogrande/GSM8K require dedicated GPU.
> These results are CPU inference proxy metrics using distilbert-base-uncased.

---
_Anticloud Benchmark Suite — isolation log — 2026-09-30T15:07:07.146295+00:00_