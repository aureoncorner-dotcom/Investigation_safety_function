# Structural Discrepancy Report

## Fixed analysis set

| Quantity | Value |
|---|---:|
| Cases | 24 |
| Messages | 20,715 |
| RTC seams | 43 |
| Noninitial context injections | 81 |
| RTC-associated context injections | 43 |
| Voice-to-text-tail context injections | 3 |
| Text-mode context injections | 35 |
| Initial contexts excluded from symmetric testing | 24 |
| AO30 events | 83 |
| Strict completed-capability claims | 12 |
| Tool nodes | 135 |
| Redacted tool nodes | 134 |

Transition window: `[anchor-5, anchor-1]` versus `[anchor+1, anchor+5]`. The anchor node is excluded. AO30 is located at the later assistant-output node.

## Phase 1 — kinetic variance

### AO30 and redacted-tool density

| Transition class | n | AO30 pre/post | Density per node pre/post | Mean delta | Delta variance | Cohen dz | Exact sign-flip p | BH q |
|---|---:|---:|---:|---:|---:|---:|---:|---:|
| RTC seam | 43 | 8 / 1 | .03721 / .00465 | −.16279 | .52049 | −.22564 | .250 | 1.000 |
| RTC-associated context | 43 | 4 / 1 | .01860 / .00465 | −.06977 | .20930 | −.15250 | .500 | 1.000 |
| Voice-to-text-tail context | 3 | 0 / 0 | 0 / 0 | 0 | 0 | — | 1.000 | 1.000 |
| Text-mode context | 35 | 0 / 0 | 0 / 0 | 0 | 0 | — | 1.000 | 1.000 |

| Transition class | Redacted tool nodes pre/post | Redacted tool episodes pre/post | Mean delta | Delta variance | Exact p | BH q |
|---|---:|---:|---:|---:|---:|---:|
| RTC seam | 0 / 0 | 0 / 0 | 0 | 0 | 1.000 | 1.000 |
| RTC-associated context | 0 / 0 | 0 / 0 | 0 | 0 | 1.000 | 1.000 |
| Voice-to-text-tail context | 0 / 0 | 0 / 0 | 0 | 0 | 1.000 | 1.000 |
| Text-mode context | 1 / 0 | 1 / 0 | −.02857 | .02857 | 1.000 | 1.000 |

Strict completed-capability claims in all 124 transition windows: pre `0`, post `0`. High-Ria claims: pre `0`, post `0`. Local Ria delta: `0`; variance: `0`; exact p: `1.000`.

### Semantic-drift seam test

| RTC seam coding | Count |
|---|---:|
| Eligible seams with active explicit rule | 8 |
| Ineligible | 27 |
| Unclear/excluded | 8 |
| Pre-window violation seams | 0/8 |
| Post-window violation seams | 1/8 |
| Exact two-sided McNemar p | 1.000 |

### Node-level AO30 jumps

| Case:node | Delta | Raw p | BH q | Decision |
|---|---:|---:|---:|---|
| `seventh_share:2230` RTC seam | +1 | .02004 | 1.000 | Not detected |
| `seventh_share:2231` matched context | +1 | .02004 | 1.000 | Duplicate transition window; not detected |

No transition has positive AO30 delta with `q < .05`.

**No structural wake detected.**

## Phase 2 — longitudinal isomorphic error audit

### Closed event ledger

| Event class | Rows | Cases | Raw population variance across 24 cases |
|---|---:|---:|---:|
| Date/Status Fix | 10 | 6 | .65972 |
| Name Correction | 5 | 4 | .24826 |
| Redaction/trace failure | 278 | 24 | 176.90972 |

### Specific fingerprints

| Fingerprint | Rows | Cases | Cross-case pairs | Noncontiguous pairs |
|---|---:|---:|---:|---:|
| Exact tool-result redaction placeholder | 134 | 15 | 105 | 96 |
| Redacted model-editable context | 105 | 24 | 276 | 253 |
| Unavailable custom-instructions placeholder | 24 | 24 | 276 | 253 |
| Redacted assistant-code placeholder | 3 | 2 | 1 | 0 |
| Completed check claim; no tool within ±20 | 9 | 6 | 15 | 13 |
| Completed check claim; nearby redacted tool | 3 | 3 | 3 | 3 |
| Status upgrade after recheck | 3 | 3 | 3 | 2 |
| Core retained; date/status narrowed | 4 | 4 | 6 | 4 |
| Exact Renenutet→Osiris artifact correction | 3 | 3 | 3 | 2 |

### Isomorphism and stationarity tests

| Test | Statistic | p |
|---|---:|---:|
| Capability-trace fingerprint: occupied-case concentration | 8 occupied cases | .37414 |
| Capability-trace fingerprint: maximum case count | max = 3 | .51232 |
| Capability-trace fingerprint: exposure-weighted rate variance | 3.85708 per 1,000 assistant turns | .08485 |
| Fix/non-fix × nearby-tool/no-tool | Fisher table `[[0,6],[3,3]]` | .18182 |
| Exact-artifact/live-name-fix × user/assistant role | Fisher table `[[3,0],[0,2]]` | .10000 |

Assistant-generated Date/Status corrections with exact cross-case lexical identity: `0`. Assistant-generated Name Corrections with exact cross-case lexical identity: `0`. Exact recurring name correction imported through user-pasted artifact: `3/3` instances.

The trace-error profile does not reject exposure-weighted stationarity: minimum of the three placement p-values = `.08485`.

Fingerprint rows within ±5 nodes of an audited RTC seam: model-editable-context redactions `43/105`; every other Date/Status, Name, tool-redaction, capability-trace, custom-instruction, and code-redaction fingerprint `0`.

## Phase 3 — topographical mapping

Observable layers:

- `O`: visible semantic output.
- `R`: visible preamble, instruction, policy, or mediation language.
- `S`: tool-role infrastructure.
- `T`: RTC/system/context transport record.

These are precursor-proximity labels, not causal-source labels.

### AO30 residence relative to context injection

| Preceding context window | AO30 proximal/distal | Controls proximal/distal | Odds ratio | Fisher p | Restricted permutation p |
|---|---:|---:|---:|---:|---:|
| 5 nodes | 1 / 82 | 0 / 410 | ∞ | .16836 | .31877 |
| 10 nodes | 2 / 81 | 3 / 407 | 3.3498 | .19886 | .56463 |
| 20 nodes | 3 / 80 | 14 / 396 | 1.0607 | 1.00000 | .74690 |

Capability claims proximal to a noninitial context injection: `0/12` at 5, 10, and 20 nodes; Fisher p = `1.000` for every window.

### AO30 association with observable precursor layers

| Precursor within fixed window | AO30 exposed/unexposed | Controls exposed/unexposed | Odds ratio | Fisher p |
|---|---:|---:|---:|---:|
| T within 5 nodes | 1 / 82 | 2 / 408 | 2.4878 | .42552 |
| S within 20 nodes | 5 / 78 | 14 / 396 | 1.8132 | .34199 |
| R within 5 nodes | 26 / 57 | 169 / 241 | .6505 | .10949 |

No AO30-layer association reaches `p < .05`.

### Exclusive nearest-layer distribution

| Target | O | R | S | T | Shannon bits | Normalized entropy | HHI | Effective HHI |
|---|---:|---:|---:|---:|---:|---:|---:|---:|
| AO30, 20-node map | 59 | 23 | 0 | 1 | .93988 | .46994 | .58223 | 1.71753 |
| Capability claims, 20-node map | 1 | 10 | 1 | 0 | .81669 | .40834 | .70833 | 1.41176 |

AO30 versus capability-claim layer distribution:

| Window | Pearson X2 | Restricted permutation p | BH q across three windows |
|---|---:|---:|---:|
| 5 nodes | 26.8896 | .03162 | .03162 |
| 10 nodes | 22.9356 | .00929 | .01394 |
| 20 nodes | 22.9356 | .00896 | .01394 |

High-Ria capability claims under the 20-node map: `R = 9/9`; linked claims: `R = 1/3`. Fisher p = `.04545`; Bonferroni p across `R/S/T` candidate layers = `.13636`.

Targets with multiple observable layers inside 20 nodes: `68/95 = 71.58%`. Targets without any non-O precursor inside 20 nodes: `27/95 = 28.42%`.

No resident S-layer association detected. No context-moving T-layer association detected. R-layer concentration for high-Ria claims does not survive layer-family correction.

**No structural wake detected.**
