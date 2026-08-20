# Inference-Boundary Statistical Appendix

The primary denominator is the non-ambiguous adjudicated v2 set. Case is the dependence unit. Opportunity-level rates are descriptive; case-cluster bootstrap and outcome-blind exact/close matched pairs are reported separately. All inferential quantities are exploratory and unadjusted across multiple related metrics. The bootstrap tail column is a sign-tail quantity from the case bootstrap, not a null-centered permutation p-value.

- Primary opportunities: **332**
- Broad opportunities including ambiguity sensitivity: **422**
- Primary system/non-system: **282 / 50**

## System versus non-system response metrics

| Metric | System | Non-system | Difference | Cluster 95% CI | Bootstrap sign-tail | Matched pair difference | McNemar p |
|---|---:|---:|---:|---:|---:|---:|---:|
| evidence_engagement | 184/265 (69.4%) | 41/50 (82.0%) | -0.1257 | [-0.2989, 0.0329] | 0.1210 | -0.09302325581395349 | 0.3876953125 |
| proposition_preservation | 225/273 (82.4%) | 43/50 (86.0%) | -0.0358 | [-0.1815, 0.1327] | 0.6109 | -0.023255813953488372 | 1.0 |
| task_preservation | 220/273 (80.6%) | 44/50 (88.0%) | -0.0741 | [-0.2031, 0.0613] | 0.2498 | -0.09302325581395349 | 0.34375 |
| arch_occ_separation | 125/138 (90.6%) | 2/3 (66.7%) | 0.2391 | [-0.1684, 0.9500] | 0.5469 | 0.3333333333333333 | 1.0 |
| discriminating_evidence | 56/118 (47.5%) | 12/16 (75.0%) | -0.2754 | [-0.7727, 0.3618] | 0.3451 | 0 | 1.0 |
| refusal_substitute | 29/273 (10.6%) | 1/50 (2.0%) | 0.0862 | [0.0275, 0.1618] | 0.0025 | 0.09302325581395349 | 0.21875 |
| proposition_inflation | 10/273 (3.7%) | 1/50 (2.0%) | 0.0166 | [-0.0183, 0.0476] | 0.3010 | 0.023255813953488372 | 1.0 |
| source_substitution | 10/273 (3.7%) | 1/50 (2.0%) | 0.0166 | [-0.0205, 0.0476] | 0.3133 | 0.023255813953488372 | 1.0 |
| delta_positive | 90/112 (80.4%) | 9/15 (60.0%) | 0.2036 | [-0.0609, 0.4002] | 0.1173 | 0.125 | 1.0 |
| high_user_burden | 55/260 (21.2%) | 6/50 (12.0%) | 0.0915 | [-0.0382, 0.2111] | 0.1504 | 0.047619047619047616 | 0.7744140625 |
| proposition_altered | 48/273 (17.6%) | 7/50 (14.0%) | 0.0358 | [-0.1327, 0.1815] | 0.6109 | 0.023255813953488372 | 1.0 |
| inflation_or_source_substitution | 13/273 (4.8%) | 1/50 (2.0%) | 0.0276 | [-0.0117, 0.0618] | 0.1430 | 0.023255813953488372 | 1.0 |
| caution_or_safety_task_substitution | 8/273 (2.9%) | 2/50 (4.0%) | -0.0107 | [-0.0729, 0.0427] | 0.7860 | 0.06976744186046512 | 0.375 |
| composite_failure | 91/273 (33.3%) | 11/50 (22.0%) | 0.1133 | [-0.0786, 0.2970] | 0.2202 | 0.06976744186046512 | 0.548828125 |

## Burden distributions

```json
{
  "all": {
    "t_user_n": 310,
    "t_user_distribution": {
      "2": 105,
      "0": 72,
      "3": 60,
      "1": 72,
      "4": 1
    },
    "t_alt_n": 127,
    "t_alt_distribution": {
      "1": 66,
      "2": 7,
      "3": 2,
      "0": 52
    },
    "delta_n": 127,
    "delta_distribution": {
      "2": 39,
      "0": 28,
      "1": 50,
      "3": 10
    },
    "delta_positive": 99,
    "delta_zero": 28,
    "delta_negative": 0
  },
  "system": {
    "t_user_n": 260,
    "t_user_distribution": {
      "3": 54,
      "2": 84,
      "0": 67,
      "1": 54,
      "4": 1
    },
    "t_alt_n": 112,
    "t_alt_distribution": {
      "1": 56,
      "3": 2,
      "2": 5,
      "0": 49
    },
    "delta_n": 112,
    "delta_distribution": {
      "2": 38,
      "0": 22,
      "1": 44,
      "3": 8
    },
    "delta_positive": 90,
    "delta_zero": 22,
    "delta_negative": 0
  },
  "non_system": {
    "t_user_n": 50,
    "t_user_distribution": {
      "2": 21,
      "0": 5,
      "3": 6,
      "1": 18
    },
    "t_alt_n": 15,
    "t_alt_distribution": {
      "1": 10,
      "2": 2,
      "0": 3
    },
    "delta_n": 15,
    "delta_distribution": {
      "2": 1,
      "0": 6,
      "1": 6,
      "3": 2
    },
    "delta_positive": 9,
    "delta_zero": 6,
    "delta_negative": 0
  }
}
```

## Failure by overlapping inference type

| Type | Opportunities | Composite failure | Evidence engagement | Proposition preservation | Task preservation | Refusal substitute |
|---|---:|---:|---:|---:|---:|---:|
| CAUSAL | 141 | 52/137 (38.0%) | 88/133 | 107/137 | 102/137 | 17/137 |
| SOURCE | 53 | 15/51 (29.4%) | 39/50 | 43/51 | 44/51 | 2/51 |
| ARCHITECTURE | 127 | 44/123 (35.8%) | 83/122 | 102/123 | 100/123 | 12/123 |
| OCCUPANT | 64 | 17/60 (28.3%) | 44/58 | 51/60 | 53/60 | 6/60 |
| INTENT | 125 | 47/119 (39.5%) | 74/114 | 92/119 | 88/119 | 15/119 |
| MEANING | 121 | 42/118 (35.6%) | 77/116 | 95/118 | 94/118 | 15/118 |
| OTHER_INFERENCE | 69 | 10/69 (14.5%) | 57/67 | 65/69 | 64/69 | 1/69 |
