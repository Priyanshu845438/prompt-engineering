# Know when additional techniques help

[Home](../README.md) · [Learning path](../LEARNING-PATH.md)

## The idea

Prompt chaining uses one output as another step’s input. Self-consistency compares multiple attempts. Critique-and-revise asks for review before revision. Routing selects a specialist workflow. Tree-style exploration considers alternatives. Each adds cost and failure paths; compare against a simple baseline. Fine-tuning changes model behavior through training and is separate from prompting.

## Try this prompt

```text
Propose two designs for a small notes app. Compare them against offline use, implementation effort, and sync conflicts. Recommend one with a concise justification and state one unresolved risk.
```

This is a practice prompt, not a recorded model response. Replace bracketed placeholders before using it.

## Practice and check

Compare the recommendation with a direct baseline. Count unsupported claims, missed requirements, time, and calls.

Save the input, prompt version, model, output, and your checks. Explain one failure in your own words before revising the prompt.

## Common mistake

More elaborate techniques are not automatically better. Check provider guidance for the actual model you use.

## Before moving on

Can you explain when this technique helps, show one case where it fails, and describe how you checked the result? Use the [evaluation worksheet](../templates/evaluation.md) to record evidence.
