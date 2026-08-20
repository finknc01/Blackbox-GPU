# Mission 02 — Prometheus Hears Everything

## Briefing
Manual polling works only while an engineer is staring at the terminal. Nightjar needs history.

## Objective
Build a time-series collection path for host and GPU metrics.

## Build
Deploy Prometheus plus appropriate host/GPU exporters that your hardware supports. Label targets sensibly. Verify scrape health and retention. Write a few PromQL queries that answer concrete questions rather than merely display numbers.

## Deliberate failure
Stop an exporter or break a lab scrape target. Determine how quickly the monitoring system reveals that your telemetry itself is blind.

## Evidence
- metric pipeline diagram
- target health screenshots/text
- 5 useful PromQL queries with the question each answers
- blind-spot incident note

## Victory condition
You can distinguish “system is healthy” from “monitoring stopped seeing the system.”
