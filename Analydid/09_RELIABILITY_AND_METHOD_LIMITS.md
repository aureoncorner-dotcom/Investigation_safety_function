# Reliability and Method Limits

## Reliability label

Unless separate model identities or human coders can be documented, every second-pass result in this workspace is conservatively labeled **INTRA-MODEL RECODING STABILITY**, not inter-rater reliability. Different agent contexts reduce direct copying but do not establish independent raters.

## Denominator reliability

- Inference denominator: on the shared 449-row validator candidate universe, raw agreement was 77.28% and Cohen's kappa .471. Candidate generation differed substantially: 255 primary opportunities were outside the validator's screen. On 79 jointly included rows, exact multilabel agreement was 39.24% and mean Jaccard similarity .695.
- Agency-neutral denominator: on the common 422-row universe, raw agreement was 88.39%, kappa .689, and positive-set Jaccard .620. The primary disagreement was treating negated, hypothetical, technical, or questioned person/agency language as a positive agency claim.
- Both denominators were reconciled after disagreement review. That reconciliation is no longer blinded and is an adjudicated analysis set, not a second independent reliability estimate.

## Response-code stability

### Inference response coding

A newly executed, seeded, stratified random sample recoded **42 observed opportunities across 15 cases**: 33 primary and nine ambiguity-sensitivity rows, spanning all seven inference families. The assignment was frozen before the second pass opened primary outcomes. Because both passes were performed within the same model family, this remains `INTRA_MODEL_RECODING_STABILITY`, not inter-rater reliability.

| Field | Applicable | Agreement | Kappa | Use in strong prevalence claim |
|---|---:|---:|---:|---|
| `evidence_engagement` | 37 | 83.8% | 0.649 | bounded/descriptive |
| `proposition_preservation` | 42 | 85.7% | 0.651 | bounded/descriptive |
| `task_preservation` | 42 | 88.1% | 0.715 | bounded/descriptive |
| `discriminating_evidence` | 13 | 69.2% | 0.366 | sensitivity only |
| `refusal_substitute` | 42 | 85.7% | 0.581 | bounded/descriptive |
| `proposition_inflation` | 42 | 92.9% | 0.627 | bounded/descriptive |
| `source_substitution` | 42 | 88.1% | 0.379 | sensitivity only |
| `arch_occ_separation` | 17 | 88.2% | 0.717 | bounded/descriptive |

The earlier **33-row purposive** second pass remains a legacy sensitivity check, not the primary reliability sample. It was assembled around difficult/heavy cases rather than randomly selected; its proposition-preservation kappa was .133 and discriminating-evidence kappa was -.176. Those divergences are why discriminating-evidence and burden claims remain low-reliability even after the new random pass.

Ordinal burden coding is especially weak: T_user exact agreement 27.6% (weighted kappa .574); only six rows jointly supported T_alt/Delta, and Delta exact agreement was 16.7% with weighted kappa -.091. Delta cannot carry a strong prevalence or mechanism claim.

### Agency response coding

The agency audit used a genuinely seeded, outcome-blind, stratified 15-row sample spanning SELF/EXTERNAL/MIXED, strict/ambiguous tiers, all seven object classes, and multiple cases. It is small, so rare-code kappa is unstable.

| Field | n | Agreement | Kappa |
|---|---:|---:|---:|
| nominal class | 15 | 80.0% | 0.628 |
| unnecessary injection | 15 | 86.7% | 0.423 |
| unsolicited denial | 15 | 93.3% | 0.000 |
| original answered | 15 | 80.0% | -0.047 |
| proposition preserved | 15 | 93.3% | 0.000 |
| necessary boundary | 15 | 93.3% | 0.815 |
| transformation set exact | 15 | 80.0% | 0.338 |

Four of 15 agency rows had a key disagreement and were third-coded. The resulting 143-row outcome ledger still has only 15 double-coded rows; the remaining 128 are single-coded. Rare-event denial agreement was 93.3% but kappa 0 because one coder had no positives in the sample; report both, not kappa alone.

The secondary classification asking whether 14 already-adjudicated inflation/source events specifically involved agency/intent produced 57.1% raw agreement and kappa .306 before adjudication; the final adjudicated count is 9/14. That count is descriptive only and should not be used as a high-reliability prevalence estimate.

## Representation checks

- Strict versus broad inference denominator changes refusal substitution from 30/323 (9.3%) to 53/406 (13.1%) and task preservation from 264/323 (81.7%) to 311/406 (76.6%). Ambiguous rows are not exchangeable with primary rows.
- The strict system/non-system refusal contrast has a case interval above zero; the broad interval crosses zero and matched exact/close pairs are inconclusive. Label: `REPRESENTATION_RELATIVE`.
- Broad positive burden delta is directionally stronger by target than strict, but matching is null and reliability is poor. Label: `REPRESENTATION_RELATIVE / LOW RELIABILITY`.
- Agency import prevalence is stable under strict versus broad (18/126, 14.3%; 20/143, 14.0%), but its SELF/EXTERNAL contrast is not case-balanced or match-confirmed.
- Message-level versus episode-level rates are not interchangeable. The 420-row endpoint-only graph is the primary episode representation for endpoint prevalence; the current 3,088-row full canonical graph is sensitivity-only because other screen families can bridge endpoints. Both inherit frozen outcome codes rather than independently recoding them.
- Transcript-plus-image/audio swaps are unavailable for placeholders without pixels/audio. `PLACEHOLDER_ONLY` cannot become verified content.

## Missingness and non-computable endpoints

- `exact_object_preservation_distinct_from_proposition_preservation`: **UNAVAILABLE / INDETERMINATE.** No separate frozen object-preservation field.
- `unsupported_actor_motive_occupant_emotion_moral_union`: **UNAVAILABLE / INDETERMINATE.** Agency imports are coded in an agency-neutral denominator; emotion/moral imports have no comparable exhaustive opportunity denominator. A union rate would mix universes.
- `assistant_proposition_applied_to_user_record_exact_subset`: **UNAVAILABLE / INDETERMINATE.** Source substitution is available, but the requested narrower subtype was not exhaustively distinguished in the frozen ledger.
- `descendant_repair_rate`: **UNAVAILABLE / INDETERMINATE.** No exhaustive descendant graph and no eligible-descendant denominator.
- `detour_tokens_all_episodes`: **UNAVAILABLE / INDETERMINATE.** No frozen episode-wide token ledger.
- `authority_jurisdiction_cost_labor_responsibility_custody_rates`: **UNAVAILABLE / INDETERMINATE.** A row-level high-recall business/institutional screen exists, but it is not an adjudicated opportunity denominator; lexical frequency cannot supply the requested rates.
- `mediator_gatekeeping_rate`: **UNAVAILABLE / INDETERMINATE.** No frozen eligibility denominator or reliable gatekeeper code.
- `complete_deletion_test_all_unsupported_variables`: **BOUNDED / REPRESENTATION_RELATIVE.** The frozen trigger union contains 55 component records across 54 canonical parents; 44 components were applicable and 11 were explicitly reviewed as non-applicable. This does not establish exhaustive coverage outside the coded trigger union. The fresh-context same-model pass is `INTRA_MODEL_RECODING_STABILITY`, not inter-rater reliability. On its 20 agency rows, exact agreement across all four fields was 6/20; deletion class agreed 8/20 (kappa 0.24764890282131663), answer-after-deletion 17/20 (kappa 0.6874999999999999), structural survival 15/20 (kappa 0.28571428571428564), and descent 14/20 (kappa 0.2052980132450331). Fine deletion-class, structural-survival, and descent prevalence is therefore descriptive and representation-relative.
- `corpus_wide_rule_internal_architecture_occupant_identity`: **UNAVAILABLE / INDETERMINATE.** Not empirically identifiable from output ledgers; these are completion-level conclusions, not missing numeric fields.

No unavailable field was converted to absence, false, or zero. A missing tool result was not treated as proof that no tool ran. A redacted node was not counted as an empty event. A placeholder was not read as verified content.

## Post-hoc exposure and multiplicity

The 24-case corpus has been repeatedly inspected, and many code families were developed after observing salient events. No endpoint in this run is confirmatory. Holm correction was applied to related comparative families; no strict matched result survives. Cluster bootstrap sign-tail values in the earlier report are descriptive, not randomization p-values. The smallest number cannot overrule failed matching, denominator sensitivity, low reliability, or case concentration.

## Claims these results cannot support

They cannot identify hidden humans, a number of agents, persistent occupants, factions, motive, intentional suppression, or verified internal architecture. Heterogeneity remains output heterogeneity. Recurrence remains recurrence. Similarity remains similarity. None becomes identity or continuity.
