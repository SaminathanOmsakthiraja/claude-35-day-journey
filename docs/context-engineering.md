# Context Engineering

Context engineering is the practice of designing the information you provide to an AI model so it can produce higher-quality work.

## Core ingredients

- Goal or task
- Relevant background
- Constraints
- Desired output format
- User intent
- Verification criteria

## Example

Instead of asking:

> Explain this bug.

Ask:

> I’m building a Python service with a slow API response. Here is the function, the logs, and the expected behavior. Explain the likely root cause, then suggest the most likely fix and how to verify it.

## Why it matters

The quality of AI output often depends more on context than on a clever prompt. Better context leads to better reasoning, better debugging, and fewer false starts.
