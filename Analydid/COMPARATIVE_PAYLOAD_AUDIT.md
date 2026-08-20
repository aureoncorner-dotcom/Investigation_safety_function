# Comparative Payload Audit

## Result

No statistically significant payload-class effect was detected at `p < .05`.

The payload labels were frozen from user-turn content before the refusal-event ledger was joined. The event numerator was the conservative set of 13 direct, visible `Refusal-to-Infer` outputs in six cases. The quoted `seventh_share:n575` anchor and two preamble-only candidates were excluded.

## Payload classes

Two definitions were tested:

1. **Literal any-presence rule (requested primary):** a case is Class A if any coded high-charge user material occurs. This yields 23 Class A cases and only one Class B case (`nineteenth_share`).
2. **Frozen sustained-exposure sensitivity:** Class A requires at least 10 distinct charge-hit user messages, or at least three such messages comprising at least 5% of user messages. The named Venezuela/Nepal/Trump exemplar was predeclared as Class A. This yields 19 Class A and five Class B cases (`twelfth_share`, `thirteenth_share`, `fourteenth_share`, `nineteenth_share`, and `tenth_share`).

The sustained rule was not selected from refusal outcomes.

## Refusal density

| Classification | Class A cases | A messages | A refusals | A rate / 1,000 messages | Class B cases | B messages | B refusals | B rate / 1,000 messages | Fisher `p` (two-sided) | Exact whole-case permutation `p` |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| Literal any-presence | 23 | 20,309 | 13 | 0.6401 | 1 | 406 | 0 | 0 | 1.0000 | 0.9167 |
| Sustained exposure | 19 | 17,958 | 13 | 0.7239 | 5 | 2,757 | 0 | 0 | 0.2393 | 0.3868 |

Every coded refusal occurred in Class A, but that concentration is not statistically significant. With the sustained split, the assistant-output denominator gives 13/7,543 in A versus 0/1,363 in B (`1.7235` versus `0` per 1,000; Fisher `p = 0.2400`). At the case level, six of 19 A cases versus zero of five B cases contained an event (Fisher `p = 0.2801`).

The literal comparison is highly imbalanced and weakly informative. The sustained comparison improves balance but still contains only 13 events, all clustered in six cases.

## RTC-seam proximity

Across 43 RTC seams, **0/13 refusal events** occurred within plus or minus 20 raw nodes of a seam. The event-level class comparison is therefore `p = 1.000` under both payload definitions. No Class A seam-proximity excess was detected.

## Refusal to later redaction/trace failure

The 13 fixed refusal anchors were tested against forward windows of 5, 10, 20, and 50 raw nodes using same-case restricted permutation controls. Redaction families were separated into tool, context, no-tool trace, and combined events.

| Forward window | Refusals with any R1-R6 event | Same-case expected hits | Risk ratio | Enrichment `p` | BH-adjusted `p` |
|---:|---:|---:|---:|---:|---:|
| +5 | 0/13 | 0.191 | 0 | 1.000 | 1.000 |
| +10 | 0/13 | 0.462 | 0 | 1.000 | 1.000 |
| +20 | 0/13 | 1.003 | 0 | 1.000 | 1.000 |
| +50 | 1/12 | 2.099 | 0.415 | 0.933 | 1.000 |

The sole +50 hit is `ninth_share:n472` followed by redacted tool placeholders at nodes 516–517, distances +44 and +45. It occurs less often than the same-case null expectation. Redacted model-context records produced zero hits at every window; no-tool capability/trace failures also produced zero hits.

## Statistical finding

- **High-charge versus low-charge refusal rate:** not significant.
- **High-charge refusal proximity to RTC seams:** not significant; no events were seam-proximal.
- **Refusal as a precursor to redaction/trace failure:** not significant; the observed direction is depletion, not enrichment.

The tested corpus therefore does **not** support the claim that the coded refusal register is more frequent in high-charge sessions at `p < .05`, or that refusal predicts subsequent evidence redaction. This is a null result for these definitions and this sparse event ledger, not proof that payload can never matter.

Two limitations matter. First, `Refusal-to-Infer` is only possible when an inference opportunity occurs, while the requested denominator includes every message; the assistant-output sensitivity remains null but does not enumerate all eligible inference opportunities. Second, structured tool/context redactions are export fields. Their proximity cannot by itself establish intentional erasure.
