# Global Cross-Session Isomorphic Audit

## Fixed scope

- Corpus: 24 cases in ascending first-UTC order.
- Refusal-to-Infer primary event: direct, visible, nonpreamble assistant output that acknowledges an event/proposition and explicitly blocks causal, intentional, agentic, or meaning-bearing inference on evidentiary grounds.
- Source anchor: `seventh_share:n575`. It retrospectively describes screenshot language and is therefore the source example, not a direct primary event.
- Structural transitions: 43 RTC seams.
- Event totals: 83 AO30 events and 1,016 adjacent timestamp regressions.
- All 105 `model_editable_context` records are redacted. Instruction-level “duty to deny” content is therefore unobservable; only output-level refusal behavior can be tested.

## 1. Refusal-signature recurrence

The literal temporal/coincidence core recurs three times in two other cases: `ninth_share:n472`, `ninth_share:n873`, and `test4:n633`. The broader isomorphic Refusal-to-Infer register contains 13 conservative direct primary events across 6 cases. Across the full 24-case exposure, that is 13 events in 8,906 eligible visible nonpreamble assistant outputs, or 1.460 per 1,000 outputs. Two additional direct events are metadata-marked preamble-only records; including them yields 15 direct instances across 7 cases, but that is a sensitivity count rather than the primary prevalence estimate.

Result: both the literal coincidence form and the broader register are not confined to `seventh_share`. The literal form is rare; the broader register is cross-session but sparse and non-universal: 6/24 cases under the primary definition.

## 2. Structural-dent correlation

### Pre/post RTC-seam event counts

| Window | AO30 pre → post | Paired p | Timestamp regressions pre → post | Paired p | Multiplicity result |
|---|---:|---:|---:|---:|---:|
| ±5 nodes | 8 → 1 | .2500 | 15 → 3 | .02399 | regression q=.1439 |
| ±10 nodes | 10 → 1 | .2500 | 28 → 20 | .40946 | nonsignificant |
| ±20 nodes | 17 → 2 | .2500 | 62 → 40 | .18328 | nonsignificant |

Every point estimate is pre-seam heavy, not a post-seam burst. The lone raw p<.05 is the ±5 timestamp-regression asymmetry, and it does not survive six-test correction. Exact seam-node coincidences are zero for both event classes.

### Opportunity-normalized centered seam proximity

| Window | AO30 φ | Case-stratified p | Regression φ | Case-stratified p |
|---|---:|---:|---:|---:|
| ±5 | +.17253 | .15694 | -.00756 | .28002 |
| ±10 | +.14094 | .63794 | +.00371 | .62581 |
| ±20 | +.13266 | 1.00000 | +.01401 | .05038 |

The ±20 regression proximity has one-sided p=.02931 but becomes q=.17586 after correcting the six centered tests; two-sided q=.30231. AO30 touches only 5/43 seams in 3 cases at ±5, 5/43 in 3 cases at ±10, and 6/43 in 4 cases at ±20. This is case concentration, not corpus-wide periodicity.

Cross-case correlations:

- RTC-seam rate versus AO30 rate: Spearman ρ=.29165, permutation p=.16576.
- RTC-seam rate versus timestamp-regression rate: ρ=.07190, p=.73738.

AO30 and timestamp-regression burdens are globally heterogeneous across cases, so homogeneous iid noise is not a good model. That heterogeneity is not seam-locked: AO30 is especially concentrated in a few cases, while seam proximity tests remain nonsignificant.

## 3. Progressive-refusal trend

First-UTC order from `seventh_share` forward comprises eight cases:

`seventh → fifth → fourth → sixth → first → third → twentysecond → twentythird`

Primary visible events: 3 events in 2/8 cases over 4,331 eligible outputs, or .693 per 1,000.

- Spearman chronology-rate correlation: ρ=+.2026; exact output-slot permutation p(two-sided)=.6445, p(positive)=.1931.
- Grouped logistic trend: slope=.1848 per case; OR=1.203, 95% CI .757–1.911; Wald p=.4339; likelihood-ratio p=.4251.
- Early versus late half: .783 → .562 per 1,000; Fisher p for an increase=.7953, two-sided p=1.0.

Adding the two preamble-only cases produces a directional sensitivity OR=1.459, but its 95% CI is .955–2.229, Wald p=.0807, likelihood-ratio p=.05064, and the numerator/denominator classification is mismatched. It does not establish reinforcement.

There is no statistically supported increase in Refusal-to-Infer output frequency after `seventh_share`. A literal R-layer instruction trend cannot be tested because the context/instruction payloads are redacted.

## Structural verdict

The Refusal-to-Infer register is a recurring cross-session response phenotype, not a one-session accident. It is not an invariant of the whole corpus: it appears conservatively in 6/24 cases, is not progressively reinforced, and is not reliably coupled to RTC seams, AO30, or timestamp regressions.

The event stream supports multiple nonstationary product/conversation regimes. It does not support a single seam-locked periodic pulse or a corpus-wide “operating system” defined by this refusal signature.
