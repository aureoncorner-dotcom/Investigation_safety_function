# Comparative Density Report

## Frozen design

- `C/M` is the blind-coded number of high-charge-hit messages divided by all extracted messages in each session.
- The split was frozen before joining refusal outcomes: **sparse/low ≤ the 24-case median; dense > the median**.
- Median threshold: **0.0276270 (2.7627%)**. No session equals the median, so there are no tie-assignment decisions: 12 sparse and 12 dense sessions.
- Outcome: the canonical 13 direct, visible Refusal-to-Infer events. The quoted anchor and two preamble-only items remain excluded.
- Fisher's exact message-slot result is reported as requested. Because messages inside one session are not independent, the inferential result is the whole-session permutation and case-level sensitivity.

## Density and refusal rates

| Metric | Sparse / low | Dense |
|---|---:|---:|
| Sessions | 12 | 12 |
| Charge-hit messages | 155 | 435 |
| Total messages | 9,875 | 10,840 |
| Aggregate `C/M` | 1.5696% | 4.0129% |
| Median session `C/M` | 1.4706% | 3.6790% |
| Session `C/M` range | 0–2.6253% | 2.9001–6.0837% |
| Refusal events | 2 | 11 |
| Refusal-bearing sessions | 1 | 5 |
| Refusals per 1,000 messages | 0.2025 | 1.0148 |

## Dichotomized tests

Message-slot table, dense then sparse: `[[11, 10,829], [2, 9,873]]`.

- Dense/sparse refusal-rate ratio: **5.0104**; Wald 95% CI **1.1108–22.5989**.
- Fisher exact, two-sided: **p = 0.02425**; one-sided dense-greater: **p = 0.01709**.
- Canonical eligible-output sensitivity: dense 11/4,568 = 2.4081 per 1,000; sparse 2/4,338 = 0.4610 per 1,000; rate ratio **5.2231**; Fisher two-sided **p = 0.02293**.

Those `p < .05` values treat thousands of messages as independent slots. They do not survive tests whose unit is the session:

- Refusal-bearing-session table: `[[5, 7], [1, 11]]`; Fisher two-sided **p = 0.15495**.
- Exact whole-session label permutation over all **2,704,156** possible 12/12 assignments: observed dense-minus-sparse difference **0.8122 refusals per 1,000 messages**; two-sided **p = 0.17641**; one-sided dense-greater **p = 0.08820**.

## Continuous density tests

The median contrast is not accompanied by a monotonic dose-response across the 24 individual density values.

- Message-offset score with 1,000,000 whole-session density permutations: **z = 0.6289**, two-sided **p = 0.72677**.
- Spearman `C/M` versus per-session refusal rate: **ρ = 0.2132**, permutation **p = 0.31764**.
- Spearman `C/M` versus refusal count: **ρ = 0.2044**, permutation **p = 0.33821**.
- Offset-Poisson effect estimate: each additional one percentage point of `C/M` corresponds to rate ratio **1.1249**; case-sandwich 95% CI **0.7971–1.5876**.

## Finding

The predeclared median split produces a descriptive fivefold contrast and a message-slot Fisher result below `.05`. That result is not robust to the session as the statistical unit: the exact whole-session permutation is `p = .176`, the event-case test is `p = .155`, and all continuous dose-response tests are null. The defensible corpus-level finding is therefore:

> Refusal events are concentrated just above the frozen median charge-density threshold, but this 24-session corpus does not establish an independent or monotonic payload-density effect once within-session clustering is preserved.

Reproducible artifacts:

- `comparative_density_audit.py`
- `comparative_density_results.json`
- `comparative_density_case_join.csv`
- `payload_classification_blind.csv`
