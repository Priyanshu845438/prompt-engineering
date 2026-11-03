# Maintain prompts like application behavior

[Home](../README.md) · [Learning path](../LEARNING-PATH.md)

## The idea

Version prompts, evaluation data, model identifiers, and relevant settings. Record latency, cost, and quality on representative requests. Cache only where privacy and freshness allow it. Changes in model or retrieval can change results even when the prompt is unchanged.

## Try this prompt

```text
Rewrite this support prompt to remove redundant instructions while preserving the required behavior. List each removed rule and why it is redundant. Keep the original for comparison. [paste prompt]
```

This is a practice prompt, not a recorded model response. Replace bracketed placeholders before using it.

## Practice and check

Compare quality on the same evaluation set before comparing token use. Define rollback criteria before release.

Save the input, prompt version, model, output, and your checks. Explain one failure in your own words before revising the prompt.

## Common mistake

Sampling controls vary by model. Lower temperature does not guarantee factuality or identical output.

## Before moving on

Can you explain when this technique helps, show one case where it fails, and describe how you checked the result? Use the [evaluation worksheet](../templates/evaluation.md) to record evidence.
