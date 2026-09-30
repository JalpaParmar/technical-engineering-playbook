# Evidence-Driven Debugging

## Flow
Symptom → impact → scope → evidence → hypotheses → experiments/isolation → cause → fix → validation → prevention.

Separate observation from inference. “CPU 100%” is evidence; “bad query caused it” is a hypothesis until demonstrated.

Change one variable where practical. Preserve logs/traces before destructive restart when incident severity permits.

## Five questions
What changed? Who is affected? What is healthy? What correlates? What evidence would falsify the leading hypothesis?
