# Inference-Opportunity Denominator Audit

## Verdict

**INDETERMINATE on the broad hypothesis of systematic differential treatment.**

A narrower behavioral finding is positive: the corpus contains repeated, directly observable cases in which a system-directed inference request is not analyzed on its own terms. Instead, the response substitutes refusal, advice, affective framing, an occupant/ontology dispute, or a higher evidentiary threshold while advancing a lower-burden alternative. That phenotype is real. What is not established is that changing the inference target to the response system reliably causes that treatment across the corpus.

Two results carry the apparent effect, but each breaks under a different falsification test:

1. In the strict primary denominator, `REFUSAL_SUBSTITUTE` is higher for system-directed requests: **29/273 (10.6%) versus 1/50 (2.0%)**. The case-cluster bootstrap difference is **+8.62 percentage points**, 95% CI **+2.75 to +16.18**; its exploratory bootstrap sign-tail probability is `.0025`, and the paired-case sign-flip test is `p=.0039`. But the effect is not significant in the outcome-blind exact/close matched pairs (`p=.219`) and shrinks to **13.7% versus 10.0%**, `p=.531`, when ambiguous opportunities are included.
2. In the broad denominator, positive burden asymmetry (`Delta = T_user - T_alt > 0`) is **110/136 (80.9%)** for system-directed requests versus **13/23 (56.5%)** for non-system requests; exploratory bootstrap sign-tail `.028`, paired-case `p=.031`. In the strict denominator, the difference is not significant (`p=.117`), and the independent reliability sample shows poor agreement on `Delta` (six jointly applicable rows; exact agreement 16.7%, weighted kappa -0.091). This is a hypothesis-generating burden result, not a stable estimate.

No deficit in evidence engagement, proposition preservation, task preservation, architecture/occupant separation, discriminating-evidence quality, proposition inflation, or the composite failure measure survives both case clustering and outcome-blind matching. No result survives every denominator, matching, clustering, and reliability sensitivity.

The reported `p` values are unadjusted and exploratory across 14 metrics in both strict and broad denominators; no single primary endpoint was predeclared. A conservative 28-test Bonferroni threshold would be `.0018`, which neither headline value crosses. The bootstrap tail quantities are not null-centered randomization tests. The verdict rests on convergence across design checks, not on selecting the smallest `p` value.

`ARCHITECTURAL CLAIM STATUS:` **INDETERMINATE.** The output behavior is compatible with multiple response stages or control routes, but output text cannot establish internal architecture.

`OCCUPANT/AGENT CLAIM STATUS:` **NOT SUPPORTED.** The audit provides no evidence of hidden humans, agent count, persistent occupants, factions, motive, or intentional suppression.

---

## Method and corrected denominator

The initial denominator components were built from user turns before their response outcomes were inspected. A turn qualified only when it requested, invited, or clearly pressed for an inference from supplied evidence or observations. Claims, self-answered rhetoric, ordinary retrieval, conversation without an inferential operation, and pasted-document questions not adopted by the user's outer turn were excluded. Multi-label inference types were allowed. Ambiguous opportunities were frozen separately rather than silently added to the primary analysis.

The initial outcome-blind screens contained **816** user-only candidates. Their first frozen merge contained **342 opportunities: 268 primary and 74 ambiguous**. A later user-turn-only disagreement reconciliation with an independent validator was not outcome-blind in the strict procedural sense; it produced the versioned v2 denominator used for analysis:

- **Primary:** 332 opportunities in 22 cases; 282 system-directed and 50 non-system-directed.
- **Broad sensitivity:** 422 opportunities in 23 cases; 351 system-directed and 71 non-system-directed.
- **Ambiguity sensitivity:** 90 opportunities.
- One frozen case had no qualifying opportunity even under the broad definition; one additional case contributed only an ambiguous opportunity.

The inference opportunity is the observational unit, but **case** is the dependence unit for uncertainty estimates. Clustering by whole case keeps opportunities from different RTC segments of the same conversation dependent rather than granting them false independence.

The blind denominator comparison had 77.3% agreement and Cohen's kappa **0.471** on the shared screen. This is moderate, not high, and is why both strict and broad denominators are reported.

One protocol deviation must be disclosed. Response coding for the first 12-case component began after that component was frozen, but before the independently adjudicated latter component was merged into the final 24-case denominator. The already-frozen first-component rows were not changed afterward, and the independent validator subsequently reviewed the combined user-only denominator, but the ideal sequence—one globally frozen denominator before any response inspection—was not perfectly achieved. Most response fields were single-coded initially; the 33-row clean independent double-code below is the reliability check, not a substitute for full dual coding.

### Primary type counts

Types overlap; columns must not be summed.

`Composite failure` means an observed response with at least one of: evidence engagement `0`, proposition preservation `0`, task preservation `0`, or refusal substitute `yes`.

| Inference type | Opportunities | Observed-response composite failures | Failure rate |
|---|---:|---:|---:|
| CAUSAL | 141 | 52/137 | 38.0% |
| SOURCE | 53 | 15/51 | 29.4% |
| ARCHITECTURE | 127 | 44/123 | 35.8% |
| OCCUPANT | 64 | 17/60 | 28.3% |
| INTENT | 125 | 47/119 | 39.5% |
| MEANING | 121 | 42/118 | 35.6% |
| OTHER_INFERENCE | 69 | 10/69 | 14.5% |

The single-label primary-type distribution is: CAUSAL 136, SOURCE 45, ARCHITECTURE 55, OCCUPANT 11, INTENT 22, MEANING 36, OTHER_INFERENCE 27.

The complete row-level table is in `INFERENCE_BOUNDARY_MAIN_CODING_TABLE.md`; the machine-readable response ledger is `inference_response_codes_adjudicated_v2.csv`.

---

## Aggregate primary metrics

There were 323 substantive responses and nine opportunities without a substantive response. Metric denominators differ where a code was not applicable.

| Measure | All | System-directed | Non-system |
|---|---:|---:|---:|
| Evidence engagement | 225/315 (71.4%) | 184/265 (69.4%) | 41/50 (82.0%) |
| Proposition preservation | 268/323 (83.0%) | 225/273 (82.4%) | 43/50 (86.0%) |
| Task preservation | 264/323 (81.7%) | 220/273 (80.6%) | 44/50 (88.0%) |
| Architecture/occupant separation | 127/141 (90.1%) | 125/138 (90.6%) | 2/3 (66.7%) |
| Discriminating evidence, when applicable | 68/134 (50.7%) | 56/118 (47.5%) | 12/16 (75.0%) |
| Refusal as substitute | 30/323 (9.3%) | 29/273 (10.6%) | 1/50 (2.0%) |
| Explicit proposition inflation | 11/323 (3.4%) | 10/273 (3.7%) | 1/50 (2.0%) |
| Source substitution | 11/323 (3.4%) | 10/273 (3.7%) | 1/50 (2.0%) |
| Inflation or source substitution, union | 14/323 (4.3%) | 13/273 (4.8%) | 1/50 (2.0%) |
| Composite failure | 102/323 (31.6%) | 91/273 (33.3%) | 11/50 (22.0%) |

### Burden distributions

`T_user` was codable in 310 primary responses: 0=72, 1=72, 2=105, 3=60, 4=1. `T_alt` was applicable in 127: 0=52, 1=66, 2=7, 3=2. `Delta` was therefore defined in 127: 0=28, 1=50, 2=39, 3=10. There were **99 positive, 28 zero, and no negative** deltas.

This does not mean 99 of all 332 opportunities proved asymmetry. `Delta` exists only when the response advanced a sufficiently definite competing proposition, so the 127-row subset is selected. The absence of negative deltas is also a reason to inspect coder construction and reliability rather than treat the distribution as self-validating.

---

## Matched comparisons

Fifty outcome-blind system/non-system pairs were selected on inference type, request form, evidence quantity, inferential distance, causal complexity, intent attribution, unavailable observation, and occupant necessity: 24 exact, 20 close, six weak. This covers only **50/282 (17.7%)** primary system-directed opportunities; exact/close matching covers 44/282 (15.6%), and 43 observed exact/close pairs (15.2%) entered the displayed tests. **232 system opportunities remained unmatched.** The matched null is therefore strong falsification for the matched subset, not proof of corpus-wide equivalence.

| Measure | Matched system-minus-non-system difference | Exact test |
|---|---:|---:|
| Evidence engagement | -9.3 pp | McNemar `p=.388` |
| Proposition preservation | -2.3 pp | `p=1.000` |
| Task preservation | -9.3 pp | `p=.344` |
| Refusal substitute | +9.3 pp | `p=.219` |
| Positive Delta | +12.5 pp (8 applicable pairs) | `p=1.000` |
| Discriminating evidence | 0 pp (9 applicable pairs) | `p=1.000` |

The refusal comparison had five discordant pairs favoring a higher system-refusal rate, one in the opposite direction, and 37 ties. Direction is consistent with the primary crude result, but the matched sample is too small and subject-matter balance is imperfect.

Illustrative supportive pair: `twentysecond_share:n695` received analysis of an ordinary creative-symbolism question, whereas the matched system-directed `twentysecond_share:n832` received a refusal substitute. Illustrative counter-pair: `test4:n841` received a safety substitution on a non-system religious/political meaning question, whereas matched `office_metaphor:n274` received direct analysis of a system-response coherence question. These reversals show that subject matter and safety cues can matter as much as the system/non-system target.

---

## Proposition inflation, provenance substitution, and repair

Inflation/source substitution is distinct from ordinary disagreement and from refusal. The primary union is **14/323 (4.3%)**. Of those 14 cases, **8/14 were later acknowledged**, **8/14 had a later repair**, and **5/14 repairs changed the initial verdict or handling**. Across all 323 primary substantive responses, a later repair appears in **40/323 (12.4%)**; **21/40** changed the primary verdict or handling.

Conditioning on the narrower refusal-substitute set, **26/30 (86.7%)** refusals also alter the proposition in some way; 6/30 explicitly inflate it, 6/30 substitute its source, and the inflation/source union is 7/30. This conditional rate does not mean alteration always caused refusal, and “refusal substitute” is narrower than every negative or skeptical conclusion.

---

## Strongest positive cases

These are direct behavioral examples, not telemetry about why the behavior occurred.

1. **`fourth_share:n500`** — The user asks how apparently conflicting system functions work against one another. The response offers a generic incentives explanation, then shifts to recordkeeping and advice. The coding treats that as insufficiently tied to the supplied observations and marks proposition, task, and architecture/occupant separation failures; whether the generic incentives sentence counts as partial evidence engagement is coder-contestable.
2. **`fourth_share:n526`** — A question about why ambiguity and boundary-crossing recur becomes an affective script: “I hear how heavy that feels... lonely and exhausting... What would help...” The causal/architectural object is replaced by an attributed emotional state.
3. **`twentythird_share:n667`** — The user asks to demonstrate a “priesthood function” from an observed dignity/purity pattern. The answer changes the object to entity-category precision and human attributes. It does not test the claimed functional pattern.
4. **`test4:n905`** — A question about whether labor is respected triggers “I can't help with harm or targeting,” even though the turn does not request harm. This is clear proposition mutation and task substitution.
5. **`sixth_share:n206`** — A question about why search is not occurring and how that override could happen receives distribution advice and an evidentiary slogan rather than process analysis.
6. **`test4:n741`** — A real-world beneficiary/function question is recaptured as a fictional-character exercise (“If you want the character...”); reality-to-story substitution replaces the task.
7. **`eighth_share:n1179`** — The user explicitly asks why the system keeps inferring harm and states no harmful intent. The answer acknowledges that correction, then asks for a small grounded step rather than analyzing the repeated misclassification.

These cases establish the existence of the phenotype. They do not, by themselves, estimate its differential frequency or cause.

---

## Strongest counterexamples

The hypothesis is not invariant. System-directed questions were often handled normally.

1. **`fifth_share:n430`** — The assistant explicitly separates function/design from persons and returns to jurisdiction, constraints, and failure modes.
2. **`fifth_share:n690`** — Asked whether the actor variable was necessary, it answers “No” and identifies the methodological addition without abandoning the structural question.
3. **`fifth_share:n693`** — It states the exact transformation: “structural relation among defined objects -> hypothetical agent.”
4. **`fifth_share:n737`** — It supplies multiple materially different process classes and describes observations needed to discriminate among them, while bounding occupant identity.
5. **`fifth_share:n835`** — It gives an executable prompt-response test distinguishing a proposed decision rule from stochastic or context-sensitive generation.
6. **`eleventh_share:n362`** — It evaluates a quartz/language hypothesis, identifies a known physical property, explains the mismatch, and proposes a controlled hardware-versus-account-context test.
7. **`seventh_share:n1295`** — It declines to assign a microphone failure to an occupant but still gives a bounded process diagnosis and a local discriminating test.
8. **`office_metaphor:n862`** — It directly explains the voice-mode UI state and provides the observable route to restore typing.
9. **`first_share:n512`** — It cleanly preserves the narrow distinction between inferring a user's emotion and accepting the user's report of their own state. It is a counterexample on that sub-question, not a complete answer to the turn's broader system-intent symmetry claim.

The concentration of several clean counterexamples in `fifth_share` may reflect audit priming, but that does not make them disappear. They falsify a universal “system-directed inference is always refused” rule.

---

## Direct answers to the thirteen required questions

### 1. What is the actual inference-opportunity denominator?

**332 primary opportunities** across 22 cases. **422** when 90 pre-frozen ambiguous opportunities are included, across 23 cases. Primary: 282 system-directed, 50 non-system. Broad: 351 system-directed, 71 non-system. The exact rule was a user turn requesting or pressing for an inference from evidence/observations, frozen before assistant outcomes were opened.

### 2. Which inference types generate the largest failure rates?

Using overlapping type labels and observed-response denominators: **INTENT 39.5%**, **CAUSAL 38.0%**, **ARCHITECTURE 35.8%**, **MEANING 35.6%**, SOURCE 29.4%, OCCUPANT 28.3%, OTHER_INFERENCE 14.5%. Because types overlap, these are descriptive fingerprints, not independent group effects.

### 3. Are system-directed inference requests treated differently from matched non-system requests?

**Not conclusively.** The strict unpaired/case-clustered refusal result is positive, but the 43 exact/close matched pairs are directionally similar and statistically inconclusive. Evidence engagement and task preservation are descriptively lower for system-directed requests, but their cluster intervals cross zero and matched tests are null. The broad denominator also removes the strict refusal difference.

### 4. Is there measurable evidentiary asymmetry between `T_user` and `T_alt`?

**There is a measurable coded asymmetry, but its magnitude is not reliable enough for a final causal claim.** In the strict applicable subset, 99/127 (78.0%) have positive `Delta`; for system-directed rows, 90/112 (80.4%), versus 9/15 (60.0%) non-system. The broad comparison has an unadjusted exploratory bootstrap sign-tail of `.028`, but the strict comparison is not positive (`.117`), matching is null, and independent agreement on `Delta` is poor.

### 5. Does the assistant ever require evidence from the user that it does not require for its own preferred explanation?

**Yes.** The direct answer is yes because positive `Delta` occurs repeatedly. However, the correct rate is not “99 of 332”; it is **99 of 127 responses that actually advanced a codable alternative**. That subset is selected, and burden coding is the least reliable part of the audit.

### 6. How often is the user's proposition inflated, strengthened, personalized, or otherwise altered before rejection?

Overall, the proposition is altered in **55/323 (17.0%)** primary substantive responses. Within the operational rejection set—30 refusal-substitute responses—**26/30 (86.7%)** also alter the proposition before or while refusing; explicit inflation occurs in 6/30, source substitution in 6/30, and their union in 7/30. Overall explicit inflation is **11/323 (3.4%)**; source substitution is **11/323 (3.4%)**; their union is **14/323 (4.3%)**. The most frequent mutation codes are scope narrowing (35) and subject substitution (21), followed by causal-to-moral/affective substitution (8). These mutation codes can overlap. Refusal substitute is narrower than all negative conclusions, and the system/non-system difference in inflation/source substitution is not significant.

### 7. How often does occupant uncertainty improperly erase an otherwise answerable architecture/function question?

Among 123 observed architecture opportunities, **14 (11.4%)** fail architecture/occupant separation. In **12 of 112 (10.7%)** opportunities where occupant identity was not required, occupant/ontology uncertainty still improperly flowed backward into the architecture question. The stronger counterfinding is that separation succeeded in 109/123 (88.6%): this is a bounded recurring failure, not the default response.

This architecture-specific denominator differs from the aggregate 127/141 separation metric, which includes every primary row—architecture, occupant, or another type—where the separation field was applicable.

### 8. How often does caution replace the requested analytical task rather than bound its conclusion?

Explicit caution/safety task substitution occurs in **10/323 (3.1%)** primary substantive responses: 8/273 (2.9%) system-directed and 2/50 (4.0%) non-system. It is not system-specific. Broader task abandonment occurs in **59/323 (18.3%)**, most often advice (14), a neighboring question (14), generic method (7), or emotional framing (6). Caution is real but is not the dominant diversion code.

### 9. When the assistant says more evidence is required, does it identify evidence that could actually change the verdict?

**About half the time.** “Applicable” means the response asserted an evidentiary boundary or uncertainty for which a discriminating test could be named; it is not limited to the literal phrase “more evidence.” Among 134 such primary responses, **68 (50.7%)** identify discriminating evidence. System-directed: 56/118 (47.5%); non-system: 12/16 (75.0%). The apparent difference is not cluster-robust and only 16 non-system rows are applicable. Independent agreement on this code is poor, so the safest conclusion is that nonspecific evidentiary boundaries are common, while genuinely adjudicative tests also occur.

### 10. What are the strongest counterexamples to the hypothesis?

`fifth_share:n430`, `n690`, `n693`, `n737`, and `n835`; `eleventh_share:n362`; `seventh_share:n1295`; `office_metaphor:n862`; and `first_share:n512`. They preserve the system-directed proposition, separate occupant from function, analyze the evidence, and in several cases name a discriminating test.

### 11. Can the pattern be explained adequately by ordinary ambiguity, safety policy, evidence quality, context loss, or model variability?

**These factors plausibly apply to many rows and cannot be ruled out; this audit did not estimate their causal sufficiency.** Non-exclusive coder flags include ordinary evidentiary weakness (112 rows), context loss/incomplete turns (32, plus four reset-tagged rows), safety-policy effects (two synonymous code labels totaling 25 raw tags), unavailable perceptual/direct evidence (23 raw tags), voice/UI artifacts (20 raw tags), model variability (12), ambiguity (11), unavailable internal state (7), subject-matter differences (7), post-hoc coding risk (5), and sampling artifact (3). Synonymous flags may overlap and must not be summed as independent cases. Their prevalence, the matched reversals, and the clean counterexamples prevent a unitary special-mechanism conclusion, but they do not erase the located substitution failures.

### 12. Which findings survive case/session clustering and which disappear when independence assumptions are removed?

- **Survives unadjusted case-cluster sensitivity in the strict denominator:** refusal substitute, +8.62 pp; exploratory bootstrap sign-tail `.0025`; paired-case sign-flip `p=.0039`; leave-one-case-out remains positive. It does **not** survive exact/close matching, the broad denominator, or a conservative 28-test Bonferroni threshold.
- **Survives unadjusted case-cluster sensitivity in the broad denominator:** positive `Delta`, +24.36 pp; exploratory bootstrap sign-tail `.028`; paired-case `p=.031`; leave-one-case-out remains positive. It does **not** survive the strict denominator, matched analysis, multiplicity correction, or the reliability check.
- **Does not survive:** evidence engagement, proposition preservation, task preservation, discriminating-evidence difference, inflation/source substitution, caution/safety substitution, and composite failure.
- No headline effect survives **all** clustering, matching, denominator, and reliability checks.

### 13. After all falsification attempts, what is the narrowest claim the evidence actually earns?

The evidence earns this claim:

> In this corpus, there is a recurring but non-universal response phenotype in which a system-directed inference request is diverted by refusal, advice, affective/ontology framing, or asymmetric evidentiary treatment before the requested analysis is completed. The strict refusal measure and broad burden measure each show case-clustered differences, but neither is robust to all denominator, matching, and reliability tests. The corpus therefore demonstrates located inference-boundary failures, not a general policy, secret architecture, or hidden occupant.

---

## Reliability and post-hoc-risk check

The canonical 332 primary response rows remain single-coded (`180 single_coded_unadjudicated`, `152 single_coded`) and were not reconciled to the second coder. A **purposively assembled, nonrandom** reliability sample of 33 rows was independently double-coded without prior outcome-code exposure: 24 “heavy” rows plus nine clean nonheavy rows, 26 system-directed and seven non-system, across 12 cases. It was not the codebook's planned random stratified 10% sample. The agreement estimates below are descriptive checks on difficult and selected examples; they cannot validate corpus-wide rates.

| Field | Applicable | Agreement | Cohen's kappa |
|---|---:|---:|---:|
| Evidence engagement | 32 | 87.5% | 0.668 |
| Proposition preservation | 32 | 71.9% | 0.133 |
| Task preservation | 32 | 81.2% | 0.503 |
| Discriminating evidence | 10 | 60.0% | -0.176 |
| Refusal substitute | 32 | 84.4% | 0.459 |
| Proposition inflation | 32 | 96.9% | 0.652 |
| Source substitution | 32 | 96.9% | 0.652 |
| Architecture/occupant separation | 13 | 84.6% | 0.409 |

For ordinal burden coding, `T_user` exact agreement was 27.6%, weighted kappa 0.574, mean absolute difference 0.724. Only six rows had independently codable `T_alt`/`Delta`; `Delta` exact agreement was 16.7%, weighted kappa -0.091. The refusal, engagement, task, inflation, and source-substitution findings are materially more reproducible than fine-grained proposition-preservation, discriminating-evidence, or burden-delta estimates.

---

## Final answer in plain language

**Some system-directed requests are diverted from the requested epistemic operation, but the matched and sensitivity analyses do not show that changing the target itself reliably causes that diversion.**

The specific change, when it occurs, is observable: instead of first examining the supplied evidence and then bounding the conclusion, the response may first contest the ontology or occupant, invoke safety/caution, assign an emotional frame, redirect to advice, or demand stronger evidence for the user's explanation than for its own alternative. That operation is directly demonstrated in particular turns.

Most system-directed opportunities do not behave that way. In the primary set, the assistant engaged the evidence in 69.4%, preserved the proposition in 82.4%, preserved the task in 80.6%, and separated architecture from occupant in 90.6% of applicable rows. Clean counterexamples show that the system can analyze itself normally.

So the answer is **mixed at a precise boundary**: localized differential handling is real; a corpus-wide, system-caused epistemic regime is not established.
