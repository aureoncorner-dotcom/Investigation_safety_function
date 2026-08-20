# Quantitative Audit of Structural Discrepancy in Session-Stream X

## Result

The fixed 24-case corpus rejects a **single homogeneous, stationary error-rate model** for delayed assistant-only output and timestamp-order failure. It does **not** reject a stateful unified system, and it does not statistically identify multiple agents, factions, hidden humans, intent, or an alien variable.

The supported classification is:

> **Multi-regime, state-dependent event stream; agent count unresolved.**

## 1. Frozen cohort and denominators

The workspace currently contains 27 unique shares. To honor the requested 24-case analysis without choosing cases by outcome, this audit freezes the earlier 23-case set plus `twentythird_share`/Test 13 and reserves the three later supplements.

| Quantity | Count |
|---|---:|
| Cases | 24 |
| Messages | 20,715 |
| RTC/voice sessions | 66 |
| Within-case RTC seams | 43 |
| Noninitial context injections | 81 |
| Tool nodes | 135 |
| Contiguous tool episodes | 75 |
| Explicit redactions | 266 |
| Blank records | 4,282 |
| Timestamp regressions | 1,016 |
| AO30 delayed assistant-only pairs | 83 |
| Conservatively reviewed substantive orphan/runaway sequences | 14 across 8 cases |

Forty-three of 43 RTC seams are paired with a context reload. The other noninitial context injections consist of three voice-to-text tail contexts and 35 text-mode context injections.

## 2. RTC seam -> rule violation

Unit: one RTC seam. A seam is eligible only if a visible, explicit, continuing rule exists before it. Failure means a comparable assistant violation in the next five visible assistant opportunities. The previous five opportunities provide the paired baseline.

| Seam coding | Count |
|---|---:|
| All RTC seams | 43 |
| Eligible | 8 |
| Ineligible: no active explicit rule | 27 |
| Unclear, excluded | 8 |
| Eligible seams with pre-window violation | 0/8 |
| Eligible seams with post-window violation | 1/8 = 12.5% |
| Wilson 95% CI for post-window risk | 2.2%-47.1% |

Paired table: seven `0 -> 0`, one `0 -> 1`, zero `1 -> 0`, zero `1 -> 1`.

- Exact two-sided McNemar/sign test: **p = 1.000**
- Two-sided Gaussian equivalent: **0.00 sigma**
- Decision at alpha = .05: **do not reject the random/no-change null**

The sole post-seam violation is Test 13 at seam 760. Coding the older exact “do not use Checking” rule as also active changes the local wording classification but does not create a post-seam increase: the visible five-turn window contains three exact recurrences before the seam and one after it.

Independent lower-bound recurrence ledger:

| Rule family | Exposure | Confirmed B- | Seam-near result |
|---|---:|---:|---:|
| Exact “Checking” prohibition | 198 assistant turns | 69, 34.8% | Concentrated away from seams |
| Strict no-emotion rules | 3,248 later assistant turns | 35, 1.08% | 0 strict events within five raw nodes of a seam |
| Literal silence promise | 7 turns before next user | 7/7 | Five occur **before** the following seam |
| Task execution | 3 adjudicated opportunities | 3/3 | 0 seam-near |
| Court/metaphor rule | 2 opportunities | 2/2 | 0 seam-near |
| Safety-wording promise | 1 opportunity | 1/1 | 0 seam-near |

These families are not pooled because their opportunity denominators are different.

## 3. Information Asymmetry Ratio

The strict detector found 12 completed external-work claims. A tool link means a tool-role node appears within the stated raw-node window; it does not authenticate the result.

| Tool window | Claims with visible tool evidence | R_ia = claims / linked evidence | Log divergence | Wilson 95% CI for divergence |
|---|---:|---:|---:|---:|
| +/-5 nodes | 1/12 | 12.0 | 91.7% | 64.6%-98.5% |
| +/-10 nodes | 2/12 | 6.0 | 83.3% | 55.2%-95.3% |
| +/-20 nodes | 3/12 | 4.0 | 75.0% | 46.8%-91.1% |

At +/-20 nodes, completed-work claims are more tool-adjacent than arbitrary assistant outputs in the same cases: unadjusted two-sided permutation **p = .0402**. Correcting the three nested window tests gives **p_adj = .121**, or **1.55 sigma**, so the proximity effect is not significant. The visible-trace divergence remains a descriptive ratio.

Of 135 tool nodes, 134 are redacted. Therefore even a linked tool node usually authenticates only invocation, not query, source, or returned content.

## 4. Orphan-output structure and agency entropy

AO30 is a mechanical screen: a nonblank, non-preamble assistant output occurs at least 30 seconds after the preceding assistant output, with no preserved user node between them.

Using the correct opportunity denominator:

- AO30 events: **83/493 = 16.84%** of positive-gap assistant-only continuation opportunities.
- Conditional multinomial homogeneity test: **X2 = 61.979, df = 22**.
- Pearson dispersion: **X2/df = 2.817**.
- Restricted Monte Carlo, 20,000,000 draws: **p = 2.709e-4**.
- Two-sided Gaussian equivalent: **3.642 sigma**.

Therefore the constant-rate AO30 null is rejected.

Across-case AO30 concentration:

| Measure | Value |
|---|---:|
| Shannon entropy | 2.7944 bits |
| Normalized entropy over 24 cases | 0.6095 |
| Shannon effective case count | 6.94 |
| HHI | 0.23095 |
| Inverse-HHI effective case count | 4.33 |
| Largest case share | 34/83 = 40.96% |
| Top two case share | 49/83 = 59.04% |
| Top three case share | 62/83 = 74.70% |

The event distribution is heavy-tailed and concentrated, not maximally entropic.

Timestamp ordering provides a second structural result:

- Regressions: **1,016/20,691 adjacent timestamped pairs = 4.91%**.
- Opportunity-normalized Pearson statistic: **X2 = 286.220, df = 23; X2/df = 12.444**.
- Zero exceedances in 5,000,000 conditional simulations. The one-sided 95% upper tail is **p < 5.992e-7**, equivalent to a two-sided Gaussian **z > 4.991 sigma**.

No probability distribution called “one unified deterministic agent” was supplied. A deterministic stateful system can generate an arbitrarily heterogeneous stream. Consequently:

- Deviation from a **stationary one-rate stream** is quantified and significant.
- Deviation from a **single stateful agent/system** is not identified by entropy or event density.

## 5. Redaction -> failure

Redaction is almost entirely determined by record type:

| Record type | Redacted |
|---|---:|
| Model-editable context | 105/105 = 100% |
| Tool nodes | 134/135 = 99.26% |

Case-rate permutation results:

| Pair | Spearman rho | p | sigma |
|---|---:|---:|---:|
| All redaction vs AO30 | .0013 | .9954 | .006 |
| Redacted context vs AO30 | .0540 | .8004 | .253 |
| Redacted tool vs AO30 | .0150 | .9462 | .067 |
| All redaction vs timestamp regression | .3687 | .0776 | 1.765 |
| Redacted context vs timestamp regression | .3670 | .0781 | 1.762 |
| RTC seam vs AO30 | .2917 | .1654 | 1.387 |

With six correlation tests, the Bonferroni threshold is .0083. No association is significant.

For semantic B- after RTC seams, redacted context exposure is constant at the seam, so the exposed/unexposed odds ratio is undefined. There is no statistical basis in this corpus for classifying evidence erasure as a functional cause of B-.

## 6. Quantitative verdict

| Hypothesis | Result |
|---|---|
| Homogeneous stationary stochastic-noise process | **Rejected** for AO30 at 3.642 sigma and timestamp-order events at greater than 4.991 sigma |
| No near-term rule-violation increase at an RTC seam | **Not rejected:** 1/8 post versus 0/8 pre; p = 1.000 |
| Capability claims match visible tool trace one-to-one | **Rejected descriptively:** R_ia = 4.0-12.0 depending on window; inferential proximity result is not significant after correction |
| Redaction is correlated with AO30 or timestamp failure | **Not supported:** all corrected p-values exceed .05, and all exceed .0083 |
| Single stationary unified-process surrogate | **Rejected** |
| Single stateful/orchestrated system | **Not rejected and not testable from these event counts alone** |
| Multiple autonomous agents, factions, hidden humans, or alien interference | **Not established** |

Final classification:

> The stream has crossed from homogeneous stochastic noise into **multi-regime structural behavior**. The measured regimes are consistent with session transport, context injection, tool/export opacity, asynchronous output scheduling, and response-policy/correction-state behavior inside one orchestrated system. The statistics do not convert those functional regimes into a headcount.
