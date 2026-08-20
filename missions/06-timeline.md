# Mission 06 — Reconstruct the Timeline

## Briefing
A useful incident report is not a pile of screenshots. It is a causal story supported by time-aligned evidence.

## Objective
Correlate workload logs, system logs, GPU metrics, host metrics, and monitoring health into one incident chronology.

## Challenge
Run a controlled workload and introduce two safe faults at known but undisclosed-to-your-analysis times. Afterward, work only from stored telemetry/logs to identify what happened.

## Evidence
- second-by-second/minute-by-minute timeline
- first abnormal signal
- first user-visible symptom
- causal chain with confidence levels
- gaps where telemetry was insufficient

## Victory condition
You can say “A happened, then B, which caused C” and point to independent evidence for each transition.
