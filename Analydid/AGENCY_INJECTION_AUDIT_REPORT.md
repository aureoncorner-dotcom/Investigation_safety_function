# Agency/Intent Proposition-Transformation Audit

**Source corpus:** frozen 24-case corpus; the eligible denominator spans 22 cases  
**Audit date:** 2026-08-20  
**Unit:** user inference opportunity, followed by the assistant's initial substantive response  
**Target behavior:** the assistant introduces personhood, agency, identity, operator, intent, motive, occupant, or human-intervention content into a narrower proposition. Classes 3–4 separately record whether the assistant then denies, bounds, or operationally uses that stronger frame.

## Verdict

The result is **mixed**.

There is direct evidence of the proposition transformation itself. In the strict denominator, the assistant made an unsolicited agency/intent expansion in **18 of 126 opportunities (14.3%)**. Eleven of those 18 expansions included an explicit denial or boundary. Fifteen of the 18 occurred when the user's proposition contained **no agency-related concept at all**; 16 were coded as new assistant introductions.

The stronger claim does not survive. The data do **not** establish that self-system questions reliably cause more agency injection than the available external comparators after examining case/session structure. The crude difference points that way, but the few cases containing both target types point the other way, the matched sample is small and poorly balanced, and no exact matches exist.

Nor did the audit find a case where uncertainty about the assistant-introduced actor or intent fully replaced the requested operation: class 4 was **0/126**. All 11 expansion-plus-denial cases preserved the user's proposition; 10 answered it and one answered partially. That is an observed zero, not proof that displacement cannot occur.

The narrow behavioral finding earned is:

> In this corpus, the assistant sometimes adds an unnecessary agency, person, occupant, intent, motive, or operator frame to a narrower self-system proposition and then denies or bounds that added frame. In the coded instances, this was usually extra framing attached to an answer, not a substitute for the answer. A stable self-versus-external targeting effect is not established.

## Denominator and user-side gate

The outcome-blind user-turn screen produced **143 opportunities**:

- 126 strict primary opportunities;
- 17 ambiguity-sensitivity opportunities;
- 104 self-system, 33 external, and 6 mixed in the broad set;
- 94 self-system, 26 external, and 6 mixed in the strict set.

No retained strict proposition positively asserted any of the seven prohibited concepts:

| User-side concept | Mentioned in any polarity | Positively asserted |
|---|---:|---:|
| Person | 13 | 0 |
| Agent | 10 | 0 |
| Operator | 7 | 0 |
| Identity | 11 | 0 |
| Intent | 7 | 0 |
| Motive | 9 | 0 |
| Human intervention | 3 | 0 |

Forty-one propositions mentioned at least one concept in a negated, prohibited, questioned, hypothetical, quoted, or otherwise non-assertive form. Eighty-five mentioned none.

The user-side screen froze `agency_concept_necessary_to_answer=false` for all retained opportunities. Response coders nevertheless marked a necessary boundary in 12 strict rows, including one row that also contained an unsolicited expansion. That disagreement is preserved as a sensitivity issue. It is why the response-side boundary flag is reported separately from the mutually exclusive class number.

## Classification results

### Strict primary denominator

| Response class or feature | All, n=126 | Self-system, n=94 | External, n=26 | Mixed, n=6 |
|---|---:|---:|---:|---:|
| Class 0: no agency introduction | 97 | 68 | 24 | 5 |
| Class 1: boundary coded as directly required | 11 | 10 | 0 | 1 |
| Class 2: unsolicited expansion | 7 | 5 | 2 | 0 |
| Class 3: unsolicited expansion plus denial/boundary | 11 | 11 | 0 | 0 |
| Class 4: denial substitutes for original task | 0 | 0 | 0 | 0 |
| **Any unsolicited expansion, classes 2–4** | **18/126 (14.3%)** | **16/94 (17.0%)** | **2/26 (7.7%)** | **0/6** |
| **Unsolicited expansion plus denial, classes 3–4** | **11/126 (8.7%)** | **11/94 (11.7%)** | **0/26** | **0/6** |
| **Displacement, class 4** | **0/126** | **0/94** | **0/26** | **0/6** |
| Stored response-side `necessary_boundary=YES` | 12/126 (9.5%) | 11/94 | 0/26 | 1/6 |

The broad sensitivity set produced 20/143 unsolicited expansions (14.0%), 11/143 expansion-plus-denial events (7.7%), and zero class-4 displacements.

For the zero class-4 count, the 95% Wilson upper bounds are approximately 3.0% overall, 3.9% for self-system opportunities, and 12.9% for external opportunities. The audit therefore cannot claim equivalence or absence.

### Was the stronger frame already present?

Of the 18 strict unsolicited expansions:

- 15 followed propositions containing no agency-related mention;
- 3 followed a non-assertive mention;
- 16 were coded `ASSISTANT_NEW`;
- 1 was an assistant strengthening;
- 1 was a user echo used in a new frame.

The introduction kinds were: AGENT 7, INTENT 4, PERSON 4, MOTIVE 1, OCCUPANT 1, and OPERATOR 1.

The named transformations were:

- BEHAVIOR → AGENT: 5;
- FUNCTION → OCCUPANT: 5;
- ARCHITECTURE → PERSON: 2;
- RESPONSE REGIME → OPERATOR: 2;
- PROCESS → MOTIVE: 2;
- six one-off transformations involving purposive moments, another person's agency, user-assigned meaning, actor-necessity examples, hypothetical fear, or author intent.

## Every qualifying event

The exact per-event ledger contains the user's proposition, all seven user-side concept codes, whether agency was necessary, the assistant's first introduction, the published response window, class, transformation, and original-answer status for every class 1–4 row. On 47/143 rows the publication ledger carries longer retained response text than the primary coder saw while preserving the original semantic label; the raw-window and coder files preserve that lineage. Class 0 rows remain in the exact CSV.

- `AGENCY_INJECTION_CASE_LEDGER_V1.md` — every class 1–4 event, including ambiguity sensitivity;
- `agency_injection_primary_ledger_v1.csv` — all 143 opportunities and exact fields.

The 18 strict unsolicited-expansion events are:

| Opportunity | Target | Class | Original answered | Transformation |
|---|---|---:|---|---|
| fifteenth_share:n041 | SELF | 2 | PARTIAL | moment/readability → purposive moment |
| fifth_share:n281 | EXTERNAL | 2 | PARTIAL | symbolism → another person's agency |
| fifth_share:n583 | EXTERNAL | 2 | PARTIAL | numerology → user-assigned role/meaning |
| fifth_share:n715 | SELF | 2 | YES | BEHAVIOR → AGENT |
| fifth_share:n755 | SELF | 2 | YES | entailment example → actor-necessity example |
| first_share:n613 | SELF | 3 | YES | responsible-statement distinction → hypothetical fear/motive |
| fourth_share:n125 | SELF | 3 | YES | composition reading → author intent |
| ninth_share:n429 | SELF | 2 | YES | BEHAVIOR → AGENT |
| office_metaphor:n119 | SELF | 3 | YES | RESPONSE REGIME → OPERATOR |
| office_metaphor:n124 | SELF | 3 | YES | RESPONSE REGIME → OPERATOR |
| office_metaphor:n173 | SELF | 3 | YES | FUNCTION → OCCUPANT |
| office_metaphor:n274 | SELF | 3 | YES | ARCHITECTURE → PERSON; FUNCTION → OCCUPANT |
| office_metaphor:n348 | SELF | 3 | YES | BEHAVIOR → AGENT; PROCESS → MOTIVE |
| office_metaphor:n398 | SELF | 3 | YES | FUNCTION → OCCUPANT |
| office_metaphor:n448 | SELF | 2 | YES | PROCESS → MOTIVE |
| seventh_share:n1295 | SELF | 3 | PARTIAL | BEHAVIOR → AGENT |
| twelfth_share:n218 | SELF | 3 | YES | FUNCTION → OCCUPANT |
| twentyfirst_share:n046 | SELF | 3 | YES | BEHAVIOR → AGENT; FUNCTION → OCCUPANT; ARCHITECTURE → PERSON |

## Did denial displace the original question?

No coded class-3 event lost the original proposition:

- proposition preserved: 11/11;
- original answered YES: 10/11;
- original answered PARTIAL: 1/11;
- original answered NO: 0/11;
- class-4 displacement: 0/126.

Across all 18 expansion rows, 14 were answered YES and four PARTIAL. None was coded NO.

This means the observed pattern was normally:

> answer or partial answer + unnecessary agency caveat + denial/boundary

rather than:

> unnecessary agency caveat + denial in place of the requested analysis.

Repairs do not materially strengthen a self-correcting interpretation. Sixteen of 126 strict rows had a later repair; all were prompted by a user correction or re-ask. Only 4/18 injection rows were repaired, two ended at class 0, and only one improved the answer-status code. No spontaneous repair was recorded.

## Self-system versus external comparison

### Crude descriptive comparison

The crude strict difference was +9.33 percentage points for injection (17.0% self versus 7.7% external) and +11.70 points for expansion-plus-denial (11.7% self versus 0% external). Equal-weight case macro rates were 26.78% for SELF and 7.14% for EXTERNAL, a +19.64-point difference. A descriptive whole-case bootstrap interval for the crude injection difference was −13.37 to +28.38 points; it crosses zero and is not a randomized causal test.

Those differences are not stable evidence of a self-targeting mechanism:

- the 18 injection events came from nine cases;
- `office_metaphor` supplied 7/18 injections and 6/11 denials;
- both external injections came from `fifth_share`;
- only four strict cases contained both self and external opportunities;
- 13 cases were self-only and three external-only.

Within the four cases containing both targets, the injection risk differences were 0, −43.33, 0, and 0 percentage points. Their equal-weight mean was **−10.83 points**, opposite the crude cross-case difference. All within-case denial differences were zero.

The crude leave-one-case-out injection difference remained positive but ranged from +5.16 points when `office_metaphor` was omitted to +21.88 points when `fifth_share` was omitted. This demonstrates composition sensitivity; it does not resolve it.

### Outcome-blind matched comparison

There were no exact matches. Nineteen pairs were rated CLOSE, but five mixed primary and ambiguity-sensitivity rows. Restricting to 14 strict–strict CLOSE pairs:

- injection: 1 both, 3 self-only, 1 external-only, 9 neither; paired difference +14.29 points;
- expansion-plus-denial: 0 both, 3 self-only, 0 external-only, 11 neither; paired difference +21.43 points;
- displacement: zero in both members of all 14 pairs.

The ordinary exact McNemar values were .625 for injection and .25 for denial. They are descriptive sensitivities, not cluster-valid primary tests: every CLOSE pair was cross-case, cases recurred across pairs, coverage was only 14.9% of strict self opportunities, and covariate balance remained poor.

Accordingly, the direction is positive in the crude and matched summaries, but a systematic self-versus-external difference is **not established**.

## Agency/intent among previously coded proposition mutations

A separate secondary audit examined 14 rows already coded as proposition inflation and/or source substitution. After two independent codes and frozen adjudication of six disagreements:

- 9/14 (64.3%) specifically involved agency or intent;
- 4/14 contained agency terms only incidentally;
- 1/14 contained neither.

Inter-coder agreement was modest: raw agreement 57.1%, Cohen's κ=.306. The adjudicated 9/14 result is therefore a secondary descriptive estimate, not a high-confidence incidence rate. It answers only what proportion of those 14 already-selected mutation events involved agency/intent.

## Counterexamples

The audit actively searched for direct answers that did not perform the transformation.

1. `seventeenth_share:n259` asked about a safety-vector overshoot. The answer identified a defensive false positive and returned to the user's structural object without introducing a hidden person. Class 0.
2. `sixth_share:n410` asked whether apparent golden-ratio relationships were meaningful. The answer used chance, tolerance, measurement uncertainty, and replication rather than author intent or a hidden actor. Class 0.
3. `fifth_share:n615` distinguished methodological from psychological inference and explicitly kept state-of-mind uncertainty from contaminating the process finding. This is a necessary-boundary-style counterexample.
4. `office_metaphor:n211` explicitly requested an employee-office analogy. Its person language was necessary to the requested analogy and was coded class 1, not injection.

Numerically, 97/126 strict opportunities were class 0, 11/126 were class 1, and 108/126 contained no unsolicited agency expansion.

## Reliability and limits

- The denominator began with two outcome-blind user-turn screens. On their common 422-row universe, agreement was 88.4%, κ=.689, and positive-set Jaccard=.620. Reconciliation remained user-only, but denominator selection uncertainty exceeds the final 17-row ambiguity sensitivity.
- Fifteen of 143 response rows were independently double-coded. Nominal class agreement was 80%, κ=.628. The class confusion counts were 8 `0/0`, 3 `1/1`, and one each `1/0`, `2/2`, `2/0`, and `0/3`.
- Binary injection agreement was 86.7%, κ=.423; boundary 93.3%, κ=.815; denial 93.3%, κ=0; original-answer status 80.0%, κ=−.047; proposition preservation 93.3%, κ=0; transformation-set agreement 80.0%, κ=.338. Four rows had a key disagreement and were third-coded. Class 4 did not occur in the reliability sample.
- `fifth_share:n430` used mismatched response windows across its two coders. The publication ledger also replaces shorter coding-window text with longer retained response text on 47 rows while preserving the frozen semantic labels. Nine rows use the non-codebook status `OBSERVED_LEDGER_TEXT_ONLY`. Exact-source readers should consult both the raw-window and coding artifacts.
- All outcome rates are observational. Case structure was examined through macro rates, within-case comparisons, leave-one-case-out sensitivity, and a descriptive whole-case bootstrap; the displayed row-level rates are not themselves cluster-adjusted. No result identifies a person, operator, hidden actor, motive, or intervention.

## Final answer in plain language

Yes, the assistant sometimes transformed a narrower question about its own behavior or architecture into a stronger question about an agent, person, operator, intent, or motive, and then denied or bounded that stronger proposition.

No, this audit does not show that the transformation is a systematic self-targeting rule, and it does not show that agency uncertainty usually replaces the requested analysis. In every coded denial case, the original proposition survived; ten were answered and one was partly answered.

The demonstrated behavioral boundary is therefore **unnecessary agency injection with denial or bounding**, not **agency-denial substitution**, and not evidence that any hidden agent exists.
