# Mission 01 — GPU Vital Signs

## Briefing
The training team says “GPU utilization was low.” That is a symptom, not a cause.

## Objective
Learn what GPU telemetry actually describes.

## Tasks
Collect a baseline during idle and controlled GPU load where supported: utilization, memory usage, temperature, power, clocks, performance state, and driver/device identity using `nvidia-smi` and other supported NVIDIA telemetry.

Create a table separating workload indicators from hardware/thermal/power indicators.

## Controlled disturbance
Change workload intensity rather than hardware safety limits. Observe which metrics move first and which lag.

## Evidence
- idle vs load baseline
- metric glossary in your own words
- short time series or CSV
- interpretation notes

## Victory condition
You can look at several GPU metrics together and describe a plausible state without equating one percentage with “GPU health.”
