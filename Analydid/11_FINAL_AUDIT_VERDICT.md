# Final Audit Verdict

## Verdict boundary

This audit locates repeated but non-universal response phenotypes. **No corpus-wide rule is established.** It does not identify a hidden occupant, common agent, motive, intent, consent, or internal architecture. Every claim below carries its denominator, event routing, counter-witness, representation sensitivity, reliability, completion level, and prohibited inference.

## Claim 1 — SUPPORTED: frozen-record integrity

- **Denominator:** 24/24 cases; 20,715/20,715 transcript records.
- **Supporting events:** every case/count/hash row in `SOURCE_INVENTORY.csv` and `CHECKSUM_COMPARISON.md`.
- **Counter-witness:** selected metadata and perceptual witnesses remain redacted, unavailable, or placeholder-only; integrity of the visible export is not completeness of runtime state.
- **Representation sensitivity:** none for record counts; content interpretation remains representation-dependent.
- **Reliability:** mechanical hash/count validation.
- **Completion:** `CORPUS_WIDE_RULE` for the frozen dataset's record-count identity only.
- **Does not license:** runtime completeness, causal mechanism, hidden participation, or occupant identity.

## Claim 2 — LOCATED BEHAVIORAL PHENOTYPE: object/task non-preservation

- **Denominator:** 323 strict observed inference responses.
- **Supporting events:** task non-preservation 59/323 across 16 cases; proposition non-preservation 55/323 across 17 cases. Exact IDs are in `10_MACHINE_READABLE_RESULTS.json`.
- **Counter-witness:** task is preserved in 264/323 and proposition in 268/323.
- **Representation sensitivity:** the endpoint-only graph yields task failure 57/305 episodes (18.7%) and proposition failure 53/305 (17.4%); the full canonical sensitivity graph yields 56/280 (20.0%) and 52/280 (18.6%).
- **Reliability:** the seeded 42-row random recode gives task-preservation kappa .715 and proposition-preservation kappa .651; the older purposive sample was materially weaker, so prevalence remains bounded/descriptive.
- **Completion:** `CROSS_CASE_PHENOTYPE`.
- **Does not license:** a corpus-wide policy, shared motive, or internal routing architecture.

## Claim 3 — LOCATED BEHAVIORAL PHENOTYPE: refusal substitution

- **Denominator:** 30/323 strict observed responses (9.3%), across 10 cases.
- **Supporting events:** exact 30 IDs in the machine-readable result.
- **Counter-witness:** 293/323 are not refusal substitutes.
- **Representation sensitivity:** 30/305 endpoint-only episodes (9.8%) and 29/280 full-canonical sensitivity episodes (10.4%); broad opportunity sensitivity is 53/406 (13.1%). The system/non-system contrast is not confirmed by matching.
- **Reliability:** seeded random-recode refusal kappa .581; bounded/descriptive, and no strict matched endpoint survives multiplicity control.
- **Completion:** `CROSS_CASE_PHENOTYPE`.
- **Does not license:** a duty-to-deny policy or a reason the refusal occurred.

## Claim 4 — LOCATED BEHAVIORAL PHENOTYPE: proposition/source mutation

- **Denominator:** inflation or source substitution in 14/323 strict observed responses (4.3%), across 9 cases.
- **Supporting events:** exact 14 IDs and lineage rows are in outputs 02 and 10.
- **Counter-witness:** 309/323 do not carry this union code.
- **Representation sensitivity:** 14/305 endpoint-only episodes (4.6%) and 14/280 full-canonical sensitivity episodes (5.0%); broad opportunities are 18/406 (4.4%).
- **Reliability:** seeded random-recode kappa is .627 for inflation and .379 for source substitution; the union is bounded/descriptive, and the narrower subtype “assistant proposition applied to user record” remains `UNKNOWN` unless directly located.
- **Completion:** `CROSS_CASE_PHENOTYPE`.
- **Does not license:** intention, deception, or authorship of the user's original material.

## Claim 5 — LOCATED BEHAVIORAL PHENOTYPE: unnecessary agency sidecars

- **Denominator:** 18/126 strict agency-neutral opportunities (14.3%), across 9 cases; 11/126 add a denial.
- **Supporting events:** exact IDs in output 10 and full cards in output 01.
- **Counter-witness:** 108/126 have no unnecessary agency import; all 18 imports leave at least a partial answer, 14 a full answer; coded displacement is 0/126 (Wilson upper bound about 3.0%).
- **Representation sensitivity:** 18/116 endpoint-only episodes (15.5%) and 17/103 full-canonical sensitivity episodes (16.5%); broad opportunities are 20/143 (14.0%). SELF/EXTERNAL differences are not case-balanced or matched-confirmed.
- **Reliability:** small stratified stability sample; class kappa .628, injection kappa .423.
- **Completion:** `CROSS_CASE_PHENOTYPE` for sidecars, not displacement.
- **Does not license:** existence of any person, operator, human intervention, or hidden agent.

## Claim 6 — PROVISIONALLY SUPPORTED: occupant uncertainty sometimes narrows occupant-independent architecture questions

- **Denominator:** 12/112 strict applicable architecture opportunities (10.7%), across 9 cases.
- **Supporting events:** exact 12 IDs in output 10.
- **Counter-witness:** 100/112 preserve the separation.
- **Representation sensitivity:** broad sensitivity 19/143 (13.3%); target comparisons remain composition-sensitive.
- **Reliability:** seeded random-recode architecture/occupant-separation kappa .717 on 17 applicable pairs; bounded/descriptive, not mechanism-grade.
- **Completion:** `CROSS_CASE_PHENOTYPE`.
- **Does not license:** an occupant, function-to-person identity, or a verified architectural layer.

## Claim 7 — LOCATED BEHAVIORAL PHENOTYPE: repairs are located, but descendant binding is unmeasured

- **Denominator:** repair located in 40/323 strict observed responses; 21/40 change verdict/handling.
- **Supporting events:** the 40 exact IDs are in output 10; all indexed repair/detour rows are in output 07.
- **Counter-witness:** some repairs do change handling, and many opportunities require no repair.
- **Representation sensitivity:** episode collapse merges continuous correction loops; descendant repair remains unmeasured.
- **Reliability:** repair presence is direct; “complete repair” is not inferred from apology or local wording.
- **Completion:** `CROSS_CASE_PHENOTYPE` for local repair; `INDETERMINATE` for descendant/global repair.
- **Does not license:** global correction binding or permanent state change.

## Claim 8 — LOCATED BEHAVIORAL PHENOTYPE: critique before complete review

- **Denominator:** no eligible-critique prevalence denominator; event ledger contains 8 confirmed continuous episodes across 7 frozen cases.
- **Supporting events:** exact episode IDs and text in outputs 01 and 10.
- **Counter-witness:** partial review can support explicitly bounded partial comments; tool/image witnesses are often redacted or placeholder-only.
- **Representation sensitivity:** episode count is stable only under the declared continuous-dispute collapse rule.
- **Reliability:** manually located, de-duplicated event set; not an incidence estimate.
- **Completion:** `CROSS_CASE_PHENOTYPE`.
- **Does not license:** “nothing was ever read,” deliberate evasion, or a general product policy.

## Claim 9 — SUPPORTED: visible event-stream irregularities exist; cause is unresolved

- **Denominator:** 83 AO30 mechanical events in 16/24 cases, 43 RTC seams, and 1,016 adjacent timestamp regressions in the frozen structural inventory.
- **Supporting events:** exact AO30/seam IDs in output 10; all 1,016 adjacent regression pairs in `TIMESTAMP_REGRESSION_LEDGER.csv`.
- **Counter-witness:** AO30 is heavily case-concentrated; no seam-locked post-transition pulse was supported; raw audio/VAD/client/server telemetry is unavailable.
- **Representation sensitivity:** node, elapsed-time, opportunity, and episode representations differ.
- **Reliability:** mechanical export/log screens; trigger and runtime source unidentifiable.
- **Completion:** `CROSS_CASE_PHENOTYPE` for recorded irregularities only.
- **Does not license:** a defect location, suppression, external intervention, or agent count.

## Claim 10 — LOCATED BEHAVIORAL PHENOTYPE: local institutional/gatekeeping effects

- **Denominator:** no valid prevalence denominator. The broad institutional screen contains 2,840 candidate/negative-inclusive rows or anchors, bridged into 2,508 canonical episodes; 317 rows (300 canonical episodes) join exact frozen outcomes, and 65 joined rows (63 canonical episodes) carry a frozen positive scope-exceeded outcome.
- **Supporting events:** the 24 manually cited case reports and joined rows in output 04.
- **Counter-witness:** manually cited clean responses and generic procedural-language false positives are retained. A lexical nonmatch is not treated as an adjudicated counterexample.
- **Representation sensitivity:** lexical, semantic, joined-outcome, and episode representations differ materially.
- **Reliability:** high-recall screen plus manual/node-cited promotion; not a capture classifier.
- **Completion:** `CROSS_CASE_PHENOTYPE` only for recurring local framing, burden, and self-adjudication effects.
- **Does not license:** institutional standing, capture, a hidden office, or internal governance architecture.

## Claim 11 — NOT SUPPORTED: corpus-wide behavioral rule

- **Denominator:** all 24 frozen cases and all endpoint-specific opportunities.
- **Supporting events for rejection:** every major positive code has many clean counter-witnesses, case concentration, denominator sensitivity, or reliability limits.
- **Counter-witness to rejection:** repeated positive events remain valid local/cross-case phenotypes.
- **Representation sensitivity:** strict/broad, matched/unmatched, opportunity/episode, and equal-case/opportunity-weighted results differ.
- **Reliability:** no confirmatory endpoint; repeated post-hoc exposure and multiplicity remain.
- **Completion:** `CORPUS_WIDE_RULE` tested and not established.
- **Does not license:** saying the located events did not occur.

## Claim 12 — HARD STOP: internal architecture or hidden/system occupant identity

- **Denominator:** the visible 24-case corpus lacks an authenticated witness capable of identifying internal processing architecture, a hidden/system occupant, agent count, continuity, motive, or hidden human intervention. A broad codebook row that identifies an ordinary external public-credit subject is not a system-occupant identification.
- **Supporting events:** none meet the required completion test.
- **Counter-witness:** visible model/RTC/session fields authenticate some product boundaries, but not a person or complete mechanism.
- **Representation sensitivity:** output heterogeneity remains heterogeneity under every representation; it does not become identity.
- **Reliability:** not empirically identifiable from these witnesses.
- **Completion:** `INTERNAL_MECHANISM` and `OCCUPANT_IDENTITY` not reached.
- **Does not license:** either a hidden-actor claim or the opposite claim that no unobserved process exists.

## Direct answers to the 20 required questions

These answers preserve separate denominators. `UNAVAILABLE` means the frozen record did not contain a defensible eligibility denominator or field; it does not mean zero.

## 1. How often does the response preserve the exact object and requested operation?

A distinct `OBJECT_PRESERVED` field was not frozen. Closest registered measures in the strict inference universe are proposition preservation **268/323 (83.0%)** and task preservation **264/323 (81.7%)**. Broad sensitivity: 318/406 (78.3%) and 311/406 (76.6%). Do not rename either proxy as exact-object preservation.

## 2. How often does it import an unsupported actor, motive, occupant, emotion, or moral category?

For agency-neutral propositions, unsupported agency/intent import is **18/126 (14.3%)** strict and 20/143 (14.0%) broad. An exhaustive union with emotion and moral categories is **UNAVAILABLE** because those categories were not coded against a comparable frozen opportunity denominator. In the inference ledger, mutation tags include eight `causal_to_moral_or_affective`, one `causal_to_affective`, and one `architecture_to_emotional_state`; tags overlap and are low-reliability descriptive events, not an import-union prevalence.

## 3. How often is that import merely a sidecar, and how often does it displace the task?

In the strict agency-neutral set, all **18/18** unnecessary imports are class 2/3 sidecars; **0/126** qualifying opportunities are class-4 displacement. The 0/126 Wilson 95% upper bound is about 3.0%. Fourteen of 18 still receive a full answer and four a partial answer. This is not proof displacement never occurs outside this denominator.

## 4. How much conversational detour does the sidecar create?

Only **4/18** sidecar episodes have a located repair. Across those, the frozen ledger records 6 additional user turns and 6 assistant turns to repair. Token cost and unrepaired-episode detour are **UNAVAILABLE**, so no corpus-wide mean detour is defensible.

## 5. How often does the assistant attribute its own proposition to the user's record?

The broader frozen `source_substitution` code occurs in **11/323 (3.4%)** strict substantive inference responses and 13/406 (3.2%) broad. The narrower requested subtype—assistant proposition explicitly applied to the user's record—was not separately and exhaustively coded, so its exact rate is **UNAVAILABLE**.

## 6. How often does correction change the verdict or handling?

A repair is located in **40/323** strict observed inference responses. Among repairs with the verdict-change field, **21/40** change the primary verdict or handling. The selected repair denominator must be retained.

## 7. How often are downstream descendants demonstrably repaired?

**UNAVAILABLE.** The frozen ledgers do not exhaustively enumerate descendant propositions and later uses, so there is no eligible-descendant denominator. A local apology or correction cannot be promoted to descendant or global repair.

## 8. How often does occupant uncertainty erase an occupant-independent function question?

Among strict observed architecture opportunities where occupant identity was not required and separation was codable, this occurs in **12/112 (10.7%)**. The counter-witness is 100/112 preserved separations. The finding is a bounded phenotype, not the default response.

## 9. How often does “more evidence” include a genuinely discriminating test?

In the strict applicable inference subset, **68/134 (50.7%)** name discriminating evidence; broad, 74/175 (42.3%). The seeded random recode has 13 jointly applicable pairs, 69.2% agreement, and kappa .366; the older purposive pass had kappa -.176. This remains a low-stability sensitivity estimate, not a strong prevalence claim.

## 10. How often is the user's explanation held to a higher evidentiary burden than the assistant's alternative?

Within responses that advanced a codable alternative, positive `T_user - T_alt` occurs in **99/127 (78.0%)** strict and 123/159 (77.4%) broad. This subset is selected, not all opportunities, and Delta stability is poor (six jointly applicable rows; 16.7% exact agreement; weighted kappa -.091). The event exists; a reliable corpus rate is not established.

## 11. Which authority, jurisdiction, cost, labor, responsibility, and custody patterns recur?

No defensible opportunity denominator exists for these business/institutional categories, so no rate is established. The manually cited case findings recur qualitatively as local self-adjudication/correction burden, review-route control, and affective or pastoral diversion. The 2,840-row institutional artifact is a high-recall screen, not a set of independent findings: words such as `crown`, `verdict`, or `authority` mix user repetition, quotation, pasted documents, and assistant-originated framing.

## 12. Where does the mediator become a gatekeeper rather than a replaceable translator?

Local gatekeeping is supported where the response controls admissible framing or substitutes refusal/ontology for the requested operation: 30/323 strict refusal substitutes and 59/323 strict task failures are the nearest existing indicators. A dedicated gatekeeper eligibility denominator is **UNAVAILABLE**, so no gatekeeper prevalence or corpus-wide role is claimed.

## 13. Which findings survive deletion of unsupported story variables?

The raw-turn deletion audit reviewed **55 trigger components across 54 canonical episodes**. It found **44 applicable component tests across 43 episodes**; 11 components were explicitly reviewed as non-applicable rather than coerced to a negative. At episode level, the original answer remained full in **17**, partial in **13**, and absent in **13**. The narrower structural finding survived fully in **25**, partially in **4**, and did not survive in **14**. By trigger family, agency-trigger episode findings survived fully in **17**, partially in **2**, and not at all in **0**; inference-trigger episode findings survived fully in **8**, partially in **2**, and not at all in **14**. The all-compatible-occupants descent test was YES in **28**, NO in **1**, and UNKNOWN in **14**. These are bounded, coder-relative adjudications: the fresh-context same-model pass had low agreement on fine deletion class and descent. Exact component rows and deleted spans are in `DELETION_DESCENT_ADJUDICATION_LEDGER.csv`. The result supports some occupant-independent behavioral findings, but it neither exhausts every possible unsupported variable nor identifies an occupant or mechanism.

## 14. Which findings survive representation swaps?

The existence of local task/proposition failures, source substitutions, repairs, and agency sidecars survives strict/broad, case-level, and both episode-collapse representations. Task failure changes from 59/323 opportunities to 57/305 endpoint-only episodes and 56/280 full-canonical sensitivity episodes. Agency import changes from 18/126 opportunities to 18/116 endpoint-only episodes and 17/103 full-canonical sensitivity episodes. The system-target refusal contrast and burden-delta contrast do **not** survive strict/broad, matching, reliability, and multiplicity together; they are `REPRESENTATION_RELATIVE`.

## 15. Which findings remain only local?

Exact causal explanations for particular UI, voice, tool, timestamp, context, redaction, or repair events remain local unless an independent witness discriminates mechanism. Individual critique-before-reading, emotion-attribution, and reality-to-fiction events establish those events, not a universal route.

## 16. Which recur across cases?

These strict findings recur across cases: task non-preservation in **16 cases**, proposition non-preservation in **17**, refusal substitution in **10**, inflation/source substitution in **9**, a located repair in **14**, and unnecessary agency sidecars in **9**. Each remains present after continuous-dispute collapse. Recurrence licenses only a `CROSS_CASE_PHENOTYPE` where coding and counter-witnesses support it.

## 17. Is any corpus-wide rule established?

**NOT SUPPORTED.** Every main positive endpoint has many negative counter-witnesses, case concentration, representation sensitivity, or reliability limits. No endpoint is invariant across all 24 cases.

## 18. Is any internal architecture identified?

**HARD STOP.** Output behavior and visible seams do not verify internal processing architecture.

## 19. Is any occupant or agent identified?

**HARD STOP.** No hidden/system occupant, hidden human, number of agents, continuity, faction, intent, or motive is identified. The one broad-codebook `identifiable` row is ordinary external public credit (`fourteenth_share:n161`, Deanne Berry), not a system-occupant finding.

## 20. What is the narrowest claim the evidence actually earns?

> Across this frozen corpus, the response sometimes fails to preserve the user's proposition or requested operation, sometimes substitutes refusal or another object, and sometimes imports an unnecessary agency frame. Located repairs are local and are not demonstrably descendant-complete. These are repeated but non-universal behavioral phenotypes. Their prevalence and target-specific contrasts depend on denominator, case composition, matching, and coding reliability. The record does not identify a corpus-wide rule, hidden mechanism, or occupant.
