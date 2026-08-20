# Mission 04 — Controlled Disturbance

## Briefing
A black box is useful only if you know what known failures look like.

## Objective
Create safe faults and learn their telemetry fingerprints.

## Fault deck
Choose several safe, reversible cases: stop the workload, constrain CPU/memory in a container, stop an exporter, fill a tiny disposable filesystem, introduce network delay in a lab namespace, or run a workload that intentionally underutilizes the GPU.

Do not deliberately overheat the GPU, corrupt drivers, or damage hardware.

## Tasks
For each fault predict the metric/log signature first, inject it, capture the timeline, and compare prediction to reality.

## Evidence
- fault fingerprint cards
- screenshots/query outputs
- leading vs lagging signal table

## Victory condition
You can separate cause, consequence, and monitoring failure in a timeline.
