# Observability and Performance Plan: [FEATURE NAME]

**Feature**: [Link to spec.md]
**Date**: [DATE]
**Owner**: [Name or role]

## Performance Budget

| Area | Budget | Measurement | Required? |
|------|--------|-------------|-----------|
| Latency | [e.g., p95 < 200 ms] | [tool/test] | [Yes/No/N/A] |
| Throughput | [e.g., 100 req/s] | [tool/test] | [Yes/No/N/A] |
| Memory | [budget] | [tool/test] | [Yes/No/N/A] |
| Startup/rendering | [budget] | [tool/test] | [Yes/No/N/A] |
| Cost/resource use | [budget] | [tool/test] | [Yes/No/N/A] |

## Observability Signals

- **Logs**: [Structured events, fields, redaction rules]
- **Metrics**: [Counters, gauges, histograms, SLIs]
- **Traces**: [Spans, external calls, background work]
- **Alerts**: [User-impacting signals only]
- **Dashboards**: [Required views or N/A]

## Validation

- [ ] Baseline measured or risk accepted
- [ ] Hot paths identified
- [ ] Load/benchmark/profile run or waiver documented
- [ ] Logging avoids secrets and unnecessary personal data
- [ ] Support and incident triage path is clear
