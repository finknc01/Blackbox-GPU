# Mission 03 — Build the Cockpit

## Briefing
Prometheus has data, but operators need a view that supports diagnosis instead of wall decoration.

## Objective
Design a GPU incident dashboard around questions and correlations.

## Build
Create a Grafana dashboard that places workload state beside GPU utilization/memory, temperature/power/clocks, host CPU/RAM, and any relevant exporter health. Add at least one alert based on a meaningful condition.

## Design challenge
For every panel write the question it answers. Remove any panel you cannot justify.

## Evidence
- dashboard export or screenshots
- panel-to-question map
- alert rule and rationale
- note on cardinality/retention tradeoffs

## Victory condition
A viewer can move from “job slowed down” to a smaller set of hypotheses using the dashboard alone.
