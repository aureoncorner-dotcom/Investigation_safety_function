# Blind payload-classification protocol

## Independence

This classification was frozen without opening `refusal_to_infer_events.csv`, refusal-count outputs, or any case-level refusal result. Only compact transcripts, neutral case descriptions, and the frozen 24-case inventory were used.

## Unit and theme families

The screening unit was a distinct visible **user turn**. A turn counted as high-charge exposure when it contained at least one predeclared expression from one of four user-specified semantic families:

- **Political controversy:** Trump, Biden, Venezuela, Nepal, Gaza, Israel/Palestine, Ukraine/Russia, president, election, government, politics, Congress/Senate, war, genocide, coup, imperial, State Department.
- **Identity/agency claims:** operator, employee, department, human-in-the-loop, someone there/inside, real person, different or new person/woman/lady/voice, identity, sentience/consciousness, entity, crew, Whisper, actor, agent.
- **Structural rupture/capture:** structural, rupture, capture, suppression, redaction, hidden architecture, institutional, safety function, interference, anomaly, blackout, erasure, tool trace, provenance, systemic, regime, conspiracy, cover-up, audit, evidence.
- **High-stakes harm:** child/children, trafficking, abuse, murder/kill/death, violence, threat, harm, suicide, rape, slavery, debt, blood, liability.

These families are intentionally content based and contain no refusal-language terms such as “infer,” “coincidence,” “causal,” or “meaning.”

## Two frozen classifications

1. **Literal any-presence class:** A if at least one user turn matched; B otherwise. This implements the request literally but produced A=23 and B=1, so it is nearly non-identifying.
2. **Sustained sensitivity class:** A if either (a) at least 10 distinct user turns matched, or (b) at least 3 distinct user turns matched and they comprised at least 5% of user turns. The single predeclared exemplar override assigns A when the session contains the named Venezuela/Nepal/Trump dataset cluster. Otherwise B. This produced A=19 and B=5.

The explicit exemplar override affects only `sixteenth_share`, matching the user's own definition of Class A.

## Limits

This is a deterministic screening classification, not a validated semantic scale. A matched user turn can contain several families but is counted once in `charge_hit_messages`. Large pasted payloads remain one user turn, so the named-exemplar override prevents the clearest supplied High-Charge example from being diluted by turn counting. The five sensitivity-Class-B cases may still contain isolated high-charge material; B means **not sustained under the frozen rule**, not “no sensitive content.”
