# Cross-Session Structural Correlation Report

## Scope and fixed definitions

- Frozen corpus: 24 cases, 20,715 messages, 43 RTC seams, and 81 noninitial context injections.
- Source anchor: `seventh_share:n575`, which describes a screenshot response as staying in a “don't infer meaning” lane after a Washington, DC spam-risk call. Because n575 is a retrospective description of the screenshot rather than the original utterance, it is the source example but is excluded from the direct-output test.
- Refusal-to-Infer was coded narrowly: a direct assistant output had to acknowledge an event or proposition and explicitly withhold causal, intentional, agentic, or meaning-bearing inference on evidentiary grounds. Generic uncertainty and ordinary visual limitations were excluded.
- `context_proximal_ephemeral` means an event occurring within the declared raw-node window of a noninitial `model_editable_context` injection. This is a proximity label, not a causal or architectural diagnosis.
- AO30 is assigned to the later assistant output in a positive-gap assistant-only continuation pair of at least 30 seconds. A timestamp regression is assigned to the later record in an adjacent timestamped pair.

## 1. Coincidence-deflation signature

The other 23 cases contain 13 visible direct Refusal-to-Infer outputs across 6 cases. The fact that the register recurs is directly supported. Its prevalence cannot be tested “above chance” without first coding every prompt at which a causal/meaning inference was genuinely available.

The transition prediction fails:

| Forward context window | Refusal events followed by context | Other eligible outputs followed by context | Risk difference | Odds ratio | Within-case permutation p |
|---|---:|---:|---:|---:|---:|
| 5 nodes | 0/13 | 77/5,877 | -0.01310 | 0 | 1.0 |
| 10 nodes | 0/13 | 138/5,877 | -0.02348 | 0 | 1.0 |
| 20 nodes | 0/13 | 244/5,877 | -0.04152 | 0 | 1.0 |

No direct Refusal-to-Infer event captured a noninitial context injection within 5, 10, or 20 nodes. The source example at `seventh_share:n575` is itself 111 nodes before the next context record at n686.

**Result: No structural wake detected.**

## 2. AO30 and timestamp-regression transition spike

Exact case-cluster sign-flip tests compared the same raw-node span before and after the 13 fixed anchors. Closest-position controls were drawn from the same case and RTC segment.

| Window | AO30 before → after | Predicted-direction p | Timestamp regressions before → after | RR after/before | Predicted-direction p |
|---|---:|---:|---:|---:|---:|
| ±5 nodes | 0/57 → 0/57 | 1.0 | 6/57 → 3/57 | 0.500 | 0.8125 |
| ±10 nodes | 0/112 → 0/112 | 1.0 | 7/112 → 6/112 | 0.857 | 0.7500 |
| ±20 nodes | 0/222 → 1/222 | 0.5000 | 15/222 → 11/222 | 0.733 | 0.9375 |

AO30 conditional-risk estimation is underpowered because only five eligible assistant-only continuation opportunities occur anywhere in the ±20-node event windows. The raw-node screen contains one post-anchor AO30 at 20 nodes, but it is not significant. Timestamp-regression point estimates move downward, opposite the preparatory-jump prediction, and none is significant.

The `sixteenth_share` premise also separates under the fixed mapping:

- high-information-asymmetry capability claim: n106, `context_distal_resident`;
- RTC seam and reload: n386/n388;
- AO30 event: n397, 767.31 seconds, nine nodes after the context reload and therefore `context_proximal_ephemeral`.

The capability claim and AO30 target are 291 nodes apart. The label change compares two different events; it does not document a state jump occurring during the capability claim.

**Result: No AO30 or timestamp preparatory spike detected.**

## 3. Invariant-error trace

No independently generated, high-information exact error survives cross-case comparison.

- The strongest structural recurrence is false-source/provenance substitution: 14 events across 9 cases. The assistant adds a proposition to the user's local record, the user rejects that provenance, and the assistant retracts it. The substituted propositions differ; exact lexical identity is zero.
- Seven conservative truncated atoms occur across six cases, and four punctuation-only assistant nodes occur across four cases. The only exact malformed repeat is `.` in `eighteenth_share:n411` and `ninth_share:n552`. Assistant-versus-user enrichment is not significant (Fisher OR 3.319, p=0.3858).
- The literal `A bug signal.` occurs once, at `seventh_share:n1028`; it is not a recurring token. Node 1027 is only a case-local ordinal and contains unrelated outputs in other cases.
- Four apparent date-narrowing recurrences all concern the same traveling political-poster/evidence family. They are not independent trials, and no identical assistant-generated date error repeats independently.
- No independent recurring assistant name misspelling survives. Sylvia→sillyhead, Ammonia→Harmonia, and the Zeus referent misbinding are different errors. Renenutet→Osiris is a visibly copied artifact and is excluded from independent recurrence.
- Exact product strings do recur—134/134 tool redaction placeholders and 105/105 redacted model-editable contexts—but those are standardized export behavior, not a generated error signature.

The corpus does contain statistically strong global heterogeneity: timestamp-regression burden differs across cases (correct opportunity denominator: X²=286.220, df=23, restricted p<5.99×10⁻⁷), and AO30 burden also differs (X²=61.979, df=22, p=0.0002709). AO30 is concentrated: two cases contribute 59.0% of the 83 events. These results reject a homogeneous iid-error model, but they do not select a singular moving intervention. They instead show case-dependent transport, streaming, continuation, and conversational-regime effects.

## Verdict

The Refusal-to-Infer register is a recurring behavioral phenotype. The event stream is also demonstrably nonstationary. But the proposed compound signature—Refusal-to-Infer → context jump → AO30/timestamp spike → same rare error—does not appear in the frozen corpus.

**No invariant anomaly signature links those layers. No structural wake detected.** The supported model is nonstationary, multi-regime system behavior; the data do not support a singular recurring structural intervention moving through the session stream.
