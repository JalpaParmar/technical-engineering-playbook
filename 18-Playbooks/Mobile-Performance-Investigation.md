# Mobile Performance Investigation Playbook

## Trigger
Slow launch, jank, freezes, high memory/CPU, battery drain, slow API-perceived experience or store/user complaints.

## Process
1. Define the exact user-visible symptom and affected cohort.
2. Establish baseline and reproducible measurement.
3. Profile the relevant path.
4. Separate network latency, server time, client CPU, rendering, disk/database and contention.
5. Rank bottlenecks by evidence and user impact.
6. Change one meaningful factor where practical.
7. Re-measure.
8. Validate on representative devices and production telemetry.

## Common mistake
Optimizing code that “looks slow” without measurement can increase complexity while leaving the actual bottleneck untouched.
