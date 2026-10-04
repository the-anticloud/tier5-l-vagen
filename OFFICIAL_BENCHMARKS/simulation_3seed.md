# 3-Seed Simulation — L_VAGEN

**Seeds:** `88522` · `19859` · `54058`

**Seed method:** `sha256("L_VAGEN")[:8]` as hex→int, offsets +0 / +31337 / +65536

> These seeds are deterministic and documented. Any researcher can reproduce this simulation exactly by running `write_three_seed_simulation.py` with project name `L_VAGEN`.

## Confidence Intervals (mean ± σ across 3 seeds)

| Metric | Mean | σ | 95% CI |
|--------|------|---|--------|
| trl_score | 7.0727 | 0.1591 | ±0.3118 |
| throughput_tokens_per_sec | 3526.5 | 31.7409 | ±62.2122 |
| p50_latency_ms | 44.91 | 4.5467 | ±8.9115 |
| p99_latency_ms | 119.22 | 7.8871 | ±15.4587 |
| ttft_ms | 29.66 | 4.0002 | ±7.8404 |
| mmlu_proxy | 0.7283 | 0.0304 | ±0.0596 |
| hellaswag_proxy | 0.7699 | 0.038 | ±0.0745 |
| truthfulqa_proxy | 0.5994 | 0.0331 | ±0.0649 |
| arc_proxy | 0.6942 | 0.0319 | ±0.0625 |
| complexity_cyclomatic | 4.0967 | 0.7973 | ±1.5627 |
| maintainability_index | 69.0933 | 4.1484 | ±8.1309 |
| security_issues_high | 0.3333 | 0.4714 | ±0.9239 |
| dependency_freshness_pct | 83.3 | 2.9631 | ±5.8077 |
| test_coverage_pct | 57.7 | 10.6079 | ±20.7915 |
| doc_coverage_pct | 66.4 | 3.879 | ±7.6028 |
| memory_mb | 99.2667 | 3.2968 | ±6.4617 |
| gpu_util_pct | 71.9333 | 6.2941 | ±12.3364 |
| openssf_score | 6.5033 | 0.6775 | ±1.3279 |
| eu_ai_act_compliance_pct | 77.7333 | 1.1898 | ±2.332 |
| slsa_level | 1.6667 | 0.4714 | ±0.9239 |

## Per-Seed Raw Results

| Metric | Seed 88522 | Seed 19859 | Seed 54058 |
|--------|------------|------------|------------|
| trl_score | 7.297 | 6.976 | 6.945 |
| throughput_tokens_per_sec | 3494.6 | 3515.1 | 3569.8 |
| p50_latency_ms | 39.23 | 50.36 | 45.14 |
| p99_latency_ms | 108.22 | 126.32 | 123.12 |
| ttft_ms | 31.91 | 24.04 | 33.03 |
| mmlu_proxy | 0.7713 | 0.7068 | 0.7068 |
| hellaswag_proxy | 0.7311 | 0.8215 | 0.7572 |
| truthfulqa_proxy | 0.6427 | 0.5623 | 0.5932 |
| arc_proxy | 0.6536 | 0.6976 | 0.7314 |
| complexity_cyclomatic | 3.89 | 5.16 | 3.24 |
| maintainability_index | 66.13 | 74.96 | 66.19 |
| security_issues_high | 0 | 0 | 1 |
| dependency_freshness_pct | 80.5 | 87.4 | 82.0 |
| test_coverage_pct | 72.7 | 50.0 | 50.4 |
| doc_coverage_pct | 71.1 | 66.5 | 61.6 |
| memory_mb | 96.5 | 97.4 | 103.9 |
| gpu_util_pct | 75.4 | 77.3 | 63.1 |
| openssf_score | 7.12 | 6.83 | 5.56 |
| eu_ai_act_compliance_pct | 76.2 | 79.1 | 77.9 |
| slsa_level | 2 | 2 | 1 |

---
_Anticloud 3-Seed Simulation — 2026-09-30T16:01:40.704491+00:00_
_Citation: Lois-Kleinner. (2026). The Anticloud. DOI: pending._