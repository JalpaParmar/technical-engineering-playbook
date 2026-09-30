# Troubleshooting Decision Trees

## API errors spike
All endpoints or one? → all regions or one? → new deployment/config? → dependency latency/errors? → DB/resource saturation? → auth/provider? Use telemetry to narrow, not intuition.

## Mobile crash spike
New version only? → OS/device cohort? → feature-flag cohort? → symbolicated stack commonality? → recent code/config/API change? → pause rollout/disable feature if impact warrants.

## Queue backlog
Producer surge or consumer slowdown? → poison messages? → downstream latency? → worker capacity? → retry amplification? Scaling consumers is unsafe if downstream is already saturated.
