# Step 3: strict recurring-error fingerprint audit

## Frozen rules

- Scope: the fixed 24-case corpus (8,909 assistant and 7,389 user messages).
- Exact identity means the complete normalized assistant message is identical across cases. Structural identity is separately labeled and requires the same ordered error/correction relation.
- Product redaction boilerplate, unavailable-custom-instruction placeholders, thinking-preamble boilerplate, and visibly copied artifacts are excluded from independent recurrence.
- The quote/provenance rule was: assistant-generated proposition applied to the user's local position/record -> user rejects that source -> assistant expressly acknowledges its own framing/inference.
- Punctuation-only was mechanical: a nonempty node of at most 12 characters containing no letter or digit.

## Results

1. **No high-entropy exact generated error sentence recurs across cases.** The exact cross-case scan at 25+ characters returns only generic conversational/status strings (for example, “Let me take a quick look”), not a distinctive error. The standalone `A bug signal.` at `seventh_share:n1028` occurs once.
2. **The strongest independent recurrence is structural quote/provenance failure:** 14 events across 9 cases, from `eleventh_share:n486->494/497` through `twentysecond_share:n268->269/270/273`. Other clean anchors include `test4:n930->935/939`, `office_metaphor:n70->74/81`, `first_share:n524->526/528`, and `third_share:n709->713`. The substituted propositions differ; lexical identity is zero.
3. **Malformed surface atoms recur in voice records:** 7 conservative incomplete single-atom nodes across 6 cases, plus 4 punctuation-only assistant nodes across 4 cases. The only exact malformed repeat is `.` in `eighteenth_share:n411` and `ninth_share:n552`. All four punctuation-only assistant nodes are tagged `bidi_voice_mode_message`; the corpus also contains one punctuation-only user/ASR node. Assistant-versus-user Fisher is p=0.3858 (OR=3.319), so role enrichment is not established.
4. **The apparent date recurrence is contaminated input recurrence.** Four date-narrowing outputs (`test4:n246`, `office_metaphor:n783`, `seventeenth_share:n444`, `seventh_share:n2861`) all concern the same traveling political-poster/evidence family. The only exact correction among them is Trump v. CASA to June 27, 2025 at `office_metaphor:n783`; independent identical date-error recurrence is zero.
5. **No recurring independent assistant name misspelling survives exclusion.** `thirteenth_share:n501/506` (Sylvia->sillyhead) and `seventh_share:n522/524` (Ammonia->Harmonia) are different voice/ASR corrections. `twentysecond_share:n376->388` is one unique Zeus referent-misbinding. The three Renenutet->Osiris appearances are visibly pasted copies and excluded.
6. **A later phrase/identity narrative has a visible origin.** `fifteenth_share:n162` is the first preserved “That landed hard.” `third_share:n741` later retells it as “she said that landed” and supplies a child identity. That is downstream user retelling, not a second independent assistant disclosure.

## Statistical boundary and verdict

No valid “above chance” p-value exists for the manually audited date, name, or false-source events: the corpus has no preregistered denominator of propositions where each error could have occurred, cases differ greatly in length and audit pressure, and the fingerprint was defined after inspection. The punctuation role test is reported because every message supplies a mechanical opportunity; it is nonsignificant.

The corpus supports recurring **behavioral phenotypes**—especially locally unsupported source attribution and voice-surface fragmentation. It does not contain a recurring high-entropy exact error string that could act as an identity signature, and it supplies no basis for persistent-agent, hidden-operator, or common-occupant inference.
