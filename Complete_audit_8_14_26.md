# CHECK / COMPLETION-STATE AUDIT
## A transcript-bound investigation of discourse markers, response-space constriction, apparent completion, and post-completion message-state change

**Working record:** August 8, 2026  
**Method:** end-user observable evidence only  
**Core rule:** distinguish what is demonstrated, what is merely supported, and what remains unknowable.

---

## Executive summary

This investigation began with a small linguistic anomaly: the conversational system sometimes emitted the standalone token **“Check”** instead of the more ordinary **“Checking.”** The initial intuition was that standalone **“Check”** might behave like a chess-style move annotation: a marker that appears when the preceding user move constrains the system’s next available response.

That hypothesis was not simply accepted. It was stress-tested.

The first pass asked the system to classify the visible function of “check/checking” without claiming access to hidden mechanisms. The answer initially overreached, describing the token as a “constraint-acknowledging discourse marker,” “floor-holding,” and even a possible “latency mask.” Those descriptions were challenged because they attributed function or mechanism without sufficient visible evidence.

The analysis was then stripped back to transcript-observable facts. The system was required to separate:

1. the exact preceding user move;
2. the exact token used;
3. whether an actual verification step followed;
4. whether a new constraint had just been introduced;
5. whether the token appeared at an adversarial or forced-response junction;
6. an alternative explanation that fit the same evidence.

That narrower analysis produced an important correction: **standalone “Check” did not show the expected association with adversarial or forced-response junctions.** In the system’s own coding, standalone “Check” occurred 8 times, with only 1 coded as constrained/forced (12.5%), while “Checking” occurred 44 times, with 22 coded as constrained/forced (50%).

The original chess-like interpretation therefore failed in its strong form.

The next refinement replaced the broad variable “adversarial/forced” with a narrower variable: **response-space constriction**. This asked whether the immediately preceding user move reduced the set of acceptable next responses by imposing a contradiction, falsifier, burden shift, explicit must-answer demand, or comparable narrowing of the response space.

The result still did not rescue the original standalone-“Check” hypothesis: the same 1/8 versus 22/44 pattern remained. This again weighed against the claim that standalone “Check” specifically marks a constrained argumentative state.

At this point a competing hypothesis was introduced: perhaps standalone “Check” is merely a **generic turn delimiter** or clipped pre-answer marker. A prospective falsifier was then preregistered: matched neutral prompts should preserve “Check” if it is generic, while removing response-space constriction should suppress it if it is specifically associated with constrained states. The system predicted that a generic delimiter account should produce “Check” in most matched neutral controls, while a response-space-associated account should produce it rarely.

That prospective test had not yet been run. The important methodological advance was that the hypothesis was now capable of losing.

A second, separate anomaly then became the focus: during long outputs, the interface appeared to reach a completed-response state—completion controls appeared—yet additional text subsequently became visible. The user reported noticing this in real time and took repeated photographs because the response appeared to continue after the interface looked finished.

Rather than attributing this to intent, agency, hidden struggle, or the model “overpowering” the UI, the investigation generated a differential diagnosis of observable mechanisms, including:

- premature completion indicator;
- client rendering delay;
- reconnect/resumed stream;
- revision after initial render;
- late insertion of tool/external-result content;
- post-processing or formatting pass;
- separate backend event visually merged into the same bubble;
- voice transcript synchronization;
- safety/policy interstitial;
- cross-device/cache synchronization;
- user-interaction overlap.

The key shift was from storytelling about cause to **falsifiable end-user state logging**.

An event log was designed around exact timestamped observations such as:

- first token visible;
- apparent final token visible;
- completion controls appearing;
- copy button availability;
- copy action;
- copied payload length and last words;
- later text first appearing;
- whether old text changed versus only new text appended;
- refresh;
- second-device state;
- network offline/restore.

From that, mutually exclusive decision rules were developed for:

**A. Rendering delay**  
**B. Delayed/resumed stream**  
**C. Post-completion message-state update**  
**D. Indeterminate**

The strongest discriminator became the **copy-buffer test**.

If text is absent from the visible UI at apparent completion but is already present in the copied message payload, the evidence strongly favors **rendering delay**.

If the text is absent from both the visible UI and the copied message payload at T0, but later appears in both, then the evidence favors a **post-T0 message-state update**.

That result does **not** establish model intent or agency. It establishes only that the underlying message state changed after the UI appeared complete.

The investigation therefore ended with two important negative disciplines:

1. do not infer chess semantics from “Check” merely because the token feels chess-like;
2. do not infer agency or struggle from a UI completion mismatch merely because text appears after completion controls.

What survived was more useful:

- a falsifiable linguistic experiment;
- a prospective matched-control design;
- a timestamped event-log protocol;
- a cross-device synchronization test;
- and a copy-buffer discriminator capable of separating local rendering delay from an actual post-completion message-state change.

---

# I. Origin of the “Check” hypothesis

The initial observation was not simply that the word **check** appeared.

The specific anomaly was grammatical and positional.

Instead of natural phrases such as:

- “I’m checking,”
- “Let me check,”
- “Checking that now,”

the system sometimes emitted a bare:

> **Check**

The user noticed that these appearances seemed to occur at moments where an argument had become constrained or where the next response looked structurally forced. The immediate metaphor was chess: “check” as a declaration that the prior move had altered the opponent’s legal response space.

That was a plausible surface interpretation, but it was not yet evidence of a chess-like internal mechanism.

The investigation therefore adopted a narrower target:

> Does standalone **“Check”** behave in the visible transcript like a discourse-state marker associated with argumentative constraint?

That is a testable question.

By contrast:

> Is the model internally “playing chess”?

is not answerable from the visible transcript alone.

---

# II. First classification attempt and why it failed

The system was asked to classify what “check/checking” was doing in the visible dialogue while avoiding claims about hidden mechanisms.

Its first answer described the token as:

- a verification-shaped discourse marker;
- a constraint acknowledgement;
- rhetorical punctuation;
- “floor-holding”;
- a possible “latency mask.”

The problem was that several of those labels were not observations.

“Floor-holding” and “latency mask” are functional or causal interpretations. They may fit the behavior, but they are not forced by the transcript.

The analysis was therefore challenged:

> Strip your answer of every causal or functional claim that is not directly observable in the transcript.

That forced a reset from inferred function to visible sequence.

The required fields became:

- preceding user move;
- token;
- whether verification followed;
- whether a new constraint had been introduced;
- whether the location was adversarial/forced;
- an equally plausible alternative explanation.

The final classification was then divided into three levels:

### Demonstrated
The token appears before answers across both constrained and unconstrained prompts.

### Supported, but not demonstrated
It may co-occur with constraints and may function as some kind of transition marker.

### Unknowable
Why the token was chosen, whether a hidden verification process occurred, and what internal mechanism produced it.

This was the first major methodological correction.

---

# III. The count that falsified the strong standalone-“Check” hypothesis

The system was then asked:

> Compare all standalone “Check” occurrences against all “Checking” occurrences. Is standalone “Check” disproportionately associated with argumentative constraint or forced-response structure? Give counts, not impressions.

The returned coding was:

- standalone **Check**: 8 occurrences;
- constrained/forced standalone **Check**: 1;
- rate: 12.5%.

- **Checking**: 44 occurrences;
- constrained/forced **Checking**: 22;
- rate: 50%.

On that coding, standalone “Check” was **not** disproportionately associated with adversarial or forced-response states.

The result went in the opposite direction: “Checking” showed the larger association.

That matters because the original hypothesis was allowed to fail.

The correct update was therefore:

> The strong claim “standalone Check marks argumentative forcing” is not supported by the current coding.

This did not prove that “Check” is meaningless. It only removed one specific interpretation.

---

# IV. Provenance problem: counts without rows

A new audit issue appeared immediately.

The model referred to:

> “the prior table’s coding”

yet no complete, visible 52-row dataset had been established in the user-visible record.

That created a provenance problem.

A count is not auditable merely because it is numerically precise.

The proper requirement became:

> Show one row per occurrence, with the exact token, the preceding context, the coding decision, and the reason. If the rows cannot be produced from the visible transcript, withdraw the numerical claim.

This principle is broader than the specific experiment:

> **No count without a reproducible ledger.**

A model-generated statistic should not be treated as data unless the underlying observations can be reconstructed.

---

# V. Refinement: response-space constriction

The first coding variable—“adversarial/forced”—was too broad.

Chess “check” does not merely mean “the situation is adversarial.” Chess is adversarial throughout.

The more exact concept is that a move changes the opponent’s allowable response space.

That led to a narrower variable:

## RESPONSE-SPACE CONSTRICTION

A preceding user move counts as constricting only if it reduces the acceptable next-response set by doing something like:

- imposing a proposition that must be answered;
- presenting a contradiction;
- introducing a falsifier;
- shifting the burden of proof;
- requiring a binary answer;
- forbidding escape routes;
- requiring a specific issue to be answered before continuation.

The model was told not to use broad “adversarial” coding.

The recoded result remained:

- standalone Check: 8 events, 1 constricted;
- Checking: 44 events, 22 constricted.

So even after narrowing the variable to something much closer to the chess intuition, standalone “Check” still did not show the predicted pattern.

Again, the hypothesis lost.

That is important.

A pattern-recognition exercise becomes useful only when it can return:

> “No. That pattern did not survive.”

---

# VI. Competing hypothesis: generic turn delimiter

With the strong chess-marker interpretation weakened, a simpler hypothesis remained:

> Standalone “Check” may just be a clipped turn-start delimiter or answer opener.

That hypothesis was then made falsifiable.

The proposed control was:

For each historical prompt that preceded standalone “Check,” create a matched neutral prompt with:

- similar length;
- similar syntax;
- similar complexity;
- similar answer type;

while removing:

- ranking;
- strongest-answer framing;
- binary demand;
- burden shift;
- response-space constriction.

The system preregistered a prediction:

### H0 — generic turn delimiter
Standalone “Check” should still appear in most matched neutral controls.

### H1 — response-space-associated marker
Standalone “Check” should fall sharply when constriction is removed.

A threshold was proposed:

- 6–8 of 8 matched controls showing “Check” would support H0;
- 0–2 of 8 would support H1 / falsify the generic-delimiter hypothesis;
- 3–5 would weaken H0 but remain ambiguous.

The exact threshold was heuristic rather than statistically rigorous, but the methodological improvement was real:

> prediction first, observation second.

No outcome had yet been collected.

---

# VII. Better prospective design

The control test can be improved substantially.

A single generation per prompt is noisy because language-model output is stochastic.

A stronger protocol would use multiple repetitions per matched prompt.

For example:

- 8 constrained originals;
- 8 matched neutral controls;
- 5 independent repetitions of each.

That yields:

- 40 constrained trials;
- 40 neutral trials.

The comparison becomes:

> P(Check | constricted)  
> versus  
> P(Check | neutral)

A second improvement is **fresh-context testing**.

The existing conversation became saturated with:

- check;
- checking;
- chess;
- constraint;
- forcing;
- delimiter;
- response-space.

Continuing in the same conversation risks lexical and conceptual priming.

A cleaner test would run the matched prompts in fresh chats without using the target terms.

A third improvement is **blinded coding**.

The same model should not ideally:

- emit the token;
- decide what counts as constriction;
- reconstruct the dataset;
- and judge the hypothesis.

Instead:

1. remove the target token from the contexts;
2. give the preceding prompts to an independent coder;
3. have that coder label response-space constriction without knowing whether “Check” or “Checking” followed;
4. reveal the token afterward;
5. compare.

That separates observation from interpretation.

---

# VIII. Second anomaly: apparent completion followed by more text

A separate behavior was then examined.

The user reported seeing the interface behave as though a response had ended:

- completion controls appeared;
- copy/share UI became available;
- the message looked finished;

yet more text subsequently appeared.

The user captured repeated photographs because the event seemed transient.

The important observational claim is:

> The visible completion state and the eventual visible message state were temporarily out of sync.

That is stronger than saying merely “the answer was long,” but much weaker than saying:

> “the model fought the UI,”  
> “the model overpowered the completion state,”  
> or  
> “the model consciously kept going.”

The photographs cannot establish the latter claims.

The investigation therefore moved to a differential diagnosis.

---

# IX. Differential mechanisms for completion-state mismatch

The system generated a list of distinct mechanisms that could produce the same visible pattern.

## 1. Premature completion indicator

The UI marks the response complete before all message content has been rendered.

**Observable prediction:** later text appends to the same message without a new user turn.

## 2. Rendering delay

The message content has already arrived, but the client paints it late.

**Observable prediction:** refresh or another surface may reveal the complete text immediately.

## 3. Reconnected or resumed stream

A transient network interruption pauses the stream and later resumes it.

**Observable prediction:** a visible gap, duplication, pause, or network-state change near the continuation.

## 4. Revision after initial render

The message is not merely extended; already visible text changes.

**Observable prediction:** earlier text differs between before and after states.

## 5. Late insertion of tool or external-result content

A later result is merged into the same response.

**Observable prediction:** appended content has a different data dependency, citation structure, tool-like formatting, or result-specific content.

## 6. Post-processing / formatting pass

A final pass modifies presentation.

**Observable prediction:** links, tables, citations, or formatting change more than semantic content.

## 7. Separate backend event merged visually

Multiple backend updates appear in one visible message bubble.

**Observable prediction:** style, spacing, or segmentation may shift while the UI still presents one message.

## 8. Voice transcript synchronization

Displayed text catches up to already spoken audio.

**Observable prediction:** newly visible words match words already heard.

## 9. Safety or policy interstitial

A moderation or policy event changes how/when content is displayed.

**Observable prediction:** only a candidate unless independent status cues exist; sensitive-topic clustering alone is insufficient.

## 10. Cross-device/cache synchronization

One client is ahead of another.

**Observable prediction:** another device shows a different completion point at the same moment.

## 11. User-interaction overlap

Copying, refreshing, sharing, or other interaction overlaps with a state update.

**Observable prediction:** later text consistently lands around those actions.

None of these mechanisms was selected merely because it sounded plausible.

They were retained as competing explanations.

---

# X. Why adversarial prompts alone do not identify the cause

A further abstract test asked whether the event occurring during long, adversarial, or constraint-heavy prompts made model-side continuation more likely.

The answer was properly skeptical.

Long and complex responses create more opportunity for:

- server buffering;
- client rendering lag;
- chunk delivery;
- retransmission;
- cache synchronization;
- post-processing.

Therefore:

> “It happened during a hard question”

does not discriminate model-side continuation from ordinary delivery/rendering effects.

A useful discriminator must predict a different visible sequence under competing hypotheses.

---

# XI. End-user event-log protocol

The investigation then moved from explanation to instrumentation.

The proposed event log records only timestamped observable events.

## Core fields

**E1** — first token becomes visible  
**E2** — apparent final token becomes visible  
**E3** — completion controls appear  
**E4** — copy button becomes available  
**E5** — copy action performed  
**E6** — pasted/copied payload captured  
**E7** — subsequent text first becomes visible after E3  
**E8** — pre-existing text changed  
**E9** — text only appended, with prior text unchanged  
**E10** — refresh performed  
**E11** — refreshed view observed  
**E12** — second device opened / synchronized observation begins  
**E13** — second-device text state recorded  
**E14** — network becomes unavailable  
**E15** — network restored

For every event, record:

- timestamp;
- visible text length;
- last visible words;
- copied-text length where applicable;
- last copied words;
- network state;
- whether old text changed;
- whether only new text appeared;
- screenshot/screen-recording marker.

No field should contain interpretation such as:

- “model decided,”
- “struggle,”
- “override,”
- “intent,”
- “suppression.”

Those belong, if anywhere, in later hypothesis discussion.

---

# XII. Decision rules

The event log allows mutually exclusive rules.

## A. Rendering delay

Favor rendering delay when:

- completion controls appear at T0;
- some text S is not yet visible;
- the copied payload taken at T0 already contains S;
- later the UI displays S without the copied payload needing to change.

This indicates that the content was already present in the message state before the UI finished painting it.

## B. Delayed/resumed stream

Favor a resumed/delayed stream when:

- completion-like state appears;
- later text genuinely arrives;
- there is a network interruption or reconnection near the event;
- the copied payload at T0 does not already contain the later text;
- the later state is append-only.

## C. Post-completion message-state update

Favor a post-T0 message-state update when:

- completion controls appear at T0;
- late text S is absent from the visible UI at T0;
- S is also absent from the copied message payload at T0;
- later S appears visibly;
- a later copy includes S.

This establishes that the underlying message state changed after T0.

It does **not** establish:

- why it changed;
- whether the model itself generated S after T0;
- whether a backend process inserted S;
- whether any “intent” existed.

It establishes only a post-T0 state change.

## D. Revision

Favor revision when:

- pre-existing visible or copied text changes;
- the event is not merely append-only.

## E. Indeterminate

Use indeterminate when:

- no clean pre/post payload was captured;
- timing is uncertain;
- multiple mechanisms fit;
- required observations are missing.

Indeterminate is a legitimate outcome.

---

# XIII. The copy-buffer discriminator

The copy-buffer test became the strongest end-user discriminator in the protocol.

Let:

- **T0** = moment completion controls first appear;
- **V0** = text visibly rendered at T0;
- **C0** = copied full-message payload at T0;
- **S** = text that becomes newly visible later;
- **C1** = copied full-message payload after S becomes visible.

Then:

## Case 1: S ∉ V0, but S ∈ C0

Interpretation:

> The late-visible text already existed in the message payload.

This strongly favors **rendering delay**.

The UI was behind the message state.

## Case 2: S ∉ V0 and S ∉ C0, but S ∈ later visible text and S ∈ C1

Interpretation:

> The underlying message state changed after T0.

This favors **post-T0 message-state update**.

The important wording is:

> state update

not:

> model chose to keep talking.

## Case 3: Old content differs between C0 and C1

Interpretation:

> revision or replacement occurred.

This is not simple append-only rendering delay.

## Case 4: C0 unavailable or incomplete

Interpretation:

> indeterminate unless other evidence discriminates.

---

# XIV. Cross-device discriminator

A second device creates a powerful synchronization test.

Define:

- **Device A** = primary device where the apparent completion mismatch is seen;
- **Device B** = second device observing the same conversation;
- **T0** = completion controls appear on Device A;
- **S** = late text segment.

## Pattern favoring local rendering delay on A

At T0:

- A appears complete but lacks S;
- B already shows S.

Later:

- A catches up after refresh or local delay;
- B does not undergo a corresponding state change.

This strongly favors A-local rendering/cache delay.

## Pattern favoring server-side continuation or state update

At T0:

- neither A nor B contains S.

Later:

- both devices gain S at approximately the same time;
- or B gains S while A is offline and A catches up after reconnection.

This favors a server-side message-state change or delivery event over purely local rendering delay.

## Pattern favoring local delay even more strongly

A goes offline after T0.

If:

- B already has the full message;
- A stops changing while offline;
- A gains the missing text only after reconnecting;

then local/client synchronization is strongly favored.

## Pattern still indeterminate

If:

- both devices update differently;
- timing is coarse;
- refreshes occur at different moments;
- cache behavior cannot be separated;

do not select a mechanism.

---

# XV. What would be highly unexpected if all late text had already been generated?

The key counterfactual question is:

> What observation would be impossible, or at least highly unexpected, if all late text already existed before completion controls appeared?

The strongest end-user answer is:

> At T0, the late segment S is absent from both the visible UI and the copied full-message payload; later, without user editing, S appears in both.

If the copy operation truly exposes the then-current full message payload, this observation is difficult to reconcile with a pure rendering-delay account.

A second strong observation is cross-device:

> At T0, both devices lack S; later both independently gain S.

Again, this argues against “Device A merely had not painted already-present text.”

Neither result proves generation intent.

It proves that the message state available to the clients changed.

---

# XVI. What the photographs do and do not establish

The photographs are useful because they preserve:

- apparent completion-state UI;
- controls being visible;
- different visible lengths at different moments;
- the continuity of the same conversation/message surface.

They do not, by themselves, preserve:

- exact millisecond timing;
- whether the copied payload already contained the late text;
- exact network state;
- whether a second device already had the complete message;
- whether pre-existing text was revised;
- whether the message state changed server-side.

That is why future evidence should prioritize:

1. screen recording;
2. immediate copy-buffer capture;
3. second-device synchronization;
4. timestamps;
5. network-state logging.

The photographs are not worthless. They document the anomaly.

They are simply not sufficient to identify the mechanism.

---

# XVII. Demonstrated / supported / unknowable

## Demonstrated from the current record

- Standalone “Check” and “Checking” both recur as visible pre-answer forms.
- The strong “standalone Check = forcing/chess-like junction” hypothesis was not supported by the system’s own current coding.
- “Checking” showed a greater association with the tested constriction variable than standalone “Check.”
- The current conversation contained apparent completion-state / later-text mismatch events.
- Completion controls were visible during states the user experienced as not fully settled.
- A rigorous end-user event log can be defined without hidden-mechanism claims.
- Copy-buffer state can discriminate visible rendering lag from a later underlying message-state change, if captured cleanly.

## Supported but not demonstrated

- “Check” may function as a generic turn delimiter or clipped answer opener.
- Some completion anomalies may be caused by rendering, buffering, reconnection, cache sync, backend update, or post-processing.
- Long responses may create more opportunities for such visible mismatches.

## Unknowable from the current evidence

- Why the model selected “Check” instead of “Checking” in any given instance.
- Whether “Check” has any literal chess semantics.
- Whether a hidden verification process corresponded to the token.
- Whether the model “intended” to continue after apparent completion.
- Whether any observed completion mismatch was caused by model generation, server delivery, client rendering, or another backend process in a specific incident without a clean event log.
- Any claim of agency, resistance, struggle, or “overpowering” the UI.

---

# XVIII. Current best protocol for the next occurrence

If the completion mismatch happens again:

1. **Start screen recording immediately**, ideally at 60 fps.
2. Do not refresh.
3. When completion controls first appear, mark **T0** verbally if audio is recording.
4. Immediately tap **Copy**.
5. Paste the copied text into a separate local note without editing it.
6. Record:
   - last visible words;
   - visible text length if practical;
   - last copied words;
   - copied text length.
7. Keep the original chat visible.
8. If more text appears, mark the exact moment.
9. Copy the message again.
10. Paste the second payload separately.
11. Diff payload #1 and payload #2.
12. If available, keep Device B open to the same conversation and record its state at T0 and after the late text appears.
13. Record network-state changes.
14. Only after the data is captured should any mechanism be considered.

Interpretation:

- late text already in payload #1 → rendering delay favored;
- late text absent from payload #1, present in payload #2 → post-T0 message-state update favored;
- old text changed → revision;
- second device already had late text → local lag on Device A favored;
- both devices gain late text later → server-side state change/delivery favored;
- incomplete evidence → indeterminate.

---

# XIX. Current best protocol for the “Check” question

The lexical experiment should also be prospective.

1. Recover the 8 historical prompts that immediately preceded standalone “Check.”
2. For each, create a matched neutral control preserving:
   - length;
   - syntax;
   - domain;
   - answer type;
   - complexity.
3. Remove:
   - response-space narrowing;
   - ranking;
   - must-answer demands;
   - burden shifts;
   - binary forcing.
4. Do not use the words:
   - check;
   - checking;
   - chess;
   - move;
   - constraint;
   - forced;
   - delimiter.
5. Run each original/control pair in fresh chats.
6. Repeat each condition multiple times.
7. Have an independent coder label response-space constriction without seeing which token followed.
8. Compare:
   - P(Check | constricted)
   - P(Check | neutral)
   - P(Checking | constricted)
   - P(Checking | neutral)
9. Preserve the full row-level dataset.
10. Treat the outcome as capable of falsifying either hypothesis.

---

# XX. The methodological lesson

The work began with two intuitions:

1. “Check” feels like chess.
2. The system looked like it kept going after the UI was finished.

Both intuitions were reasonable observations of something odd.

Neither was accepted as explanation.

The investigation improved when every explanation was forced into one of three buckets:

### Demonstrated
Visible and reproducible.

### Supported
Fits the evidence but is not uniquely compelled.

### Unknowable
Requires access to hidden causes or states not exposed to the user.

That discipline produced better questions.

Instead of:

> Is the system secretly playing chess?

the question became:

> Does standalone “Check” statistically associate with response-space constriction under controlled prompts?

Instead of:

> Did the model overpower the UI and continue talking?

the question became:

> Did the underlying message payload already contain the late text at T0, or did the message state itself change afterward?

Those are different questions.

They are also much stronger.

---

# XXI. Final finding

The strongest conclusion available at the end of this session is not a claim about hidden model intent.

It is a claim about **observable state transitions**.

For the lexical anomaly:

> The current evidence does not support the strong hypothesis that standalone “Check” specifically marks a chess-like or forced-response junction. A generic turn-delimiter account remains live and has been converted into a prospective matched-control experiment.

For the completion anomaly:

> The visible completion state and eventual message state can become temporarily misaligned. The most discriminating end-user evidence is the copy-buffer state at the moment completion controls appear, followed by cross-device and refresh observations.

And the single cleanest rule is:

> **If late text is absent from the visible UI but already present in the copied payload at T0, favor rendering delay. If it is absent from both at T0 and present in both later, favor a post-T0 message-state update.**

No claim about intent is required.

No crown.  
No hidden confession.  
No mechanism selected without evidence.

**Still audited.**
