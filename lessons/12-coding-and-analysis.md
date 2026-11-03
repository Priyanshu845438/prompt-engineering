# Prompt for work you can run and inspect

[Home](../README.md) · [Learning path](../LEARNING-PATH.md)

## The idea

Provide the relevant code, expected behavior, constraints, and a failing example. For data analysis include column meanings and missing-value rules. Ask for executable checks and inspect them before running.

## Try this prompt

```text
Fix this function so empty input returns 0. Preserve other behavior. Provide the smallest change and tests for empty input and a normal case. Code: def average(xs): return sum(xs) / len(xs)
```

This is a practice prompt, not a recorded model response. Replace bracketed placeholders before using it.

## Practice and check

Run the proposed tests in an isolated project. Confirm that the original fails on the empty list and the revision passes.

Save the input, prompt version, model, output, and your checks. Explain one failure in your own words before revising the prompt.

## Common mistake

Generated tests may repeat the same mistaken assumption as generated code. Include independent expected results.

## Before moving on

Can you explain when this technique helps, show one case where it fails, and describe how you checked the result? Use the [evaluation worksheet](../templates/evaluation.md) to record evidence.
