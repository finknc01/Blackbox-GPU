# Mission 00 — Establish the Flight Recorder

## Briefing
Nightjar failed while nobody was watching. The first lesson is brutal: telemetry you never collected cannot be reconstructed later.

## Objective
Define what must be recorded before the next run starts.

## Tasks
Inventory host time, kernel/service logs, GPU availability, workload start/end markers, process exit status, and basic system resource metrics. Verify clocks/timezones are consistent. Create a small test workload with unmistakable start/stop markers.

## Twist
Run the workload once with poor logging and once with your improved recording. Compare what questions can and cannot be answered afterward.

## Evidence
- telemetry/data-source map
- timestamp convention
- example workload lifecycle log
- “questions we still cannot answer” list

## Victory condition
You can explain why incident response begins before the incident.
