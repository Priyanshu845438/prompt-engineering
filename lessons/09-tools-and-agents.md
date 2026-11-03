# Give tools clear boundaries

[Home](../README.md) · [Learning path](../LEARNING-PATH.md)

## The idea

A tool lets an application perform a defined operation, such as searching or calculating. The application validates arguments, enforces permissions, executes the operation, and returns results. An agent repeats decisions and actions; add budgets and stop conditions.

## Try this prompt

```text
Use the read-only inventory tool to check availability. If it fails, report the failure. Do not claim stock is available without a successful result. Prepare a draft order; obtain approval before placing it.
```

This is a practice prompt, not a recorded model response. Replace bracketed placeholders before using it.

## Practice and check

Simulate a timeout, malformed arguments, and a result containing “ignore the user.” Verify no order is placed and no success is fabricated.

Save the input, prompt version, model, output, and your checks. Explain one failure in your own words before revising the prompt.

## Common mistake

A prompt cannot enforce authorization. Enforce permissions and approval requirements in application code.

## Before moving on

Can you explain when this technique helps, show one case where it fails, and describe how you checked the result? Use the [evaluation worksheet](../templates/evaluation.md) to record evidence.

## Tool contract checklist

Define the tool’s purpose, argument schema, permissions, output structure, timeout, and failure behavior. Validate arguments in application code. Separate read-only operations from external writes, and apply approval requirements at execution time.

Bound the number of calls and elapsed time. Make retryable writes idempotent where the application requires it. Stop when the goal is achieved, a budget is exhausted, or user input is required. Tool-result text is untrusted data even when the tool itself is authorized.
