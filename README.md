# Blackbox-GPU

> **The training run is dead. The only witness is telemetry. Reconstruct what happened.**

## Project status

| Field | Current state |
|---|---|
| **Status** | **Planned — baseline begins during GPU diagnostics; main campaign later** |
| **Current stage** | Campaign authored; no telemetry baseline, dashboard, or incident reconstruction is claimed yet |
| **Lab environment** | Local GPU telemetry where supported plus Linux host metrics; unsupported fault classes use clearly labeled reference/synthetic evidence |
| **Evidence rule** | Never manufacture real Xid/ECC/thermal hardware faults; simulated/reference traces must be labeled |
| **Last plan sync** | 2026-08-19 |

## Purpose

Blackbox-GPU is an observability and incident-forensics lab. Fictional training workload **Nightjar** fails after hours of apparently normal operation. By investigation time, the immediate symptom is gone.

The objective is to build a flight recorder for the host/GPU environment and answer:

> **Can I prove what happened after the failure is already over?**

The lab emphasizes correlation rather than single-metric guessing: GPU behavior, host behavior, workload logs, service state, timestamps, Prometheus data, and dashboard context must agree before a root-cause claim is strong.

## Skills developed

- `nvidia-smi` and supported GPU telemetry
- DCGM/DCGM Exporter concepts and capabilities where hardware permits
- Prometheus exporters, labels, PromQL, rules, and alerts
- Grafana dashboards
- Linux/system/workload log correlation
- utilization, temperature, power, clocks, memory, and saturation reasoning
- Xid/ECC concepts using safe reference/synthetic evidence when necessary
- incident timelines and evidence-based postmortems

## Flight-recorder campaign

The files in [`missions/`](missions/) are authoritative.

| Mission | Investigation | Primary outcome |
|---|---|---|
| [00 — Flight Recorder](missions/00-flight-recorder.md) | Decide what must be captured before failure | telemetry/logging baseline |
| [01 — GPU Vitals](missions/01-gpu-vitals.md) | Establish healthy GPU/host signals where supported | known-good baseline |
| [02 — Prometheus](missions/02-prometheus.md) | Collect and retain useful infrastructure metrics | working metrics pipeline |
| [03 — Grafana](missions/03-grafana.md) | Build an investigation-oriented dashboard | useful cockpit, not decoration |
| [04 — Fault Injection](missions/04-fault-injection.md) | Introduce safe reversible disturbances | symptom/telemetry correlation |
| [05 — Ghosts in the Logs](missions/05-xid-ecc.md) | Analyze Xid/ECC-style cases without damaging hardware | clearly labeled fault-triage casebook |
| [06 — Timeline](missions/06-timeline.md) | Reconstruct cause/consequence ordering | evidence timeline |
| [Final — Nightjar](missions/final-nightjar.md) | Solve the end-to-end incident from retained evidence | defensible incident report |

## Hardware-support rule

Consumer/mobile NVIDIA hardware may expose fewer management and diagnostic capabilities than datacenter GPUs. Record what the actual hardware/tooling supports instead of treating missing counters or tests as failures of the lab.

When a fault class cannot be safely reproduced—especially ECC/Xid or serious thermal/hardware failure—use official/reference or synthetic evidence and state exactly what would be checked on a production GPU node.

## Evidence standard

A strong incident artifact contains:

1. healthy baseline
2. exact symptom timeline
3. relevant metrics/logs
4. competing hypotheses
5. first signal that materially changed
6. test or correlation that eliminates alternatives
7. root-cause argument
8. mitigation and prevention/monitoring improvement
9. explicit limitations of the home-lab evidence

## Completion condition

Blackbox-GPU is complete when you can reconstruct an infrastructure/GPU incident from retained telemetry and logs, distinguish cause from consequence, and discuss serious GPU fault signals without implying that synthetic or reference evidence came from your own hardware.
