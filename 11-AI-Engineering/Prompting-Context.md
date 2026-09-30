# Prompting, Context & Structured Output

## Prompt design
Specify goal, relevant context, constraints, output contract and examples only where they improve behavior. More prompt text is not automatically better.

## Context engineering
Give the model the **right** information at the right time. Retrieval, conversation state, tool results and summaries can matter more than clever wording.

## Structured output
When downstream software consumes output, prefer schema-constrained/validated structures where the platform supports them. Validate required fields/types and handle refusal/failure paths.

## Prompt injection
Retrieved/user content can contain instructions. Treat external content as data, preserve instruction hierarchy and constrain tool permissions.
