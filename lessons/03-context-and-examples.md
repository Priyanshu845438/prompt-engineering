# Give context and show the pattern

[Home](../README.md) · [Learning path](../LEARNING-PATH.md)

## The idea

Zero-shot means asking without demonstrations. Few-shot means showing example inputs and outputs. Examples help communicate a pattern, but can also introduce bias or accidental rules. Keep examples representative and separate them from the new input.

## Try this prompt

```text
Classify each message as billing, technical, or other. Example: “Charged twice” → billing. Example: “Page will not open” → technical. New message: “Can I change my invoice address?” Return one label.
```

This is a practice prompt, not a recorded model response. Replace bracketed placeholders before using it.

## Practice and check

Add an ambiguous message and an unrelated message. Compare results with and without examples.

Save the input, prompt version, model, output, and your checks. Explain one failure in your own words before revising the prompt.

## Common mistake

Do not let every example belong to the same class. Keep evaluation cases separate from demonstrations.

## Before moving on

Can you explain when this technique helps, show one case where it fails, and describe how you checked the result? Use the [evaluation worksheet](../templates/evaluation.md) to record evidence.
