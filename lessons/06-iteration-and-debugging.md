# Improve one failure at a time

[Home](../README.md) · [Learning path](../LEARNING-PATH.md)

## The idea

Save a baseline prompt and real failures. Decide whether each failure comes from unclear instructions, missing information, retrieval, tool behavior, or model capability. Change one likely cause and retest old cases too.

## Try this prompt

```text
Review this draft against these criteria: preserves facts, states the next action, and stays below 100 words. Identify specific failures, then produce one revised draft. Draft: [paste draft].
```

This is a practice prompt, not a recorded model response. Replace bracketed placeholders before using it.

## Practice and check

Keep the original output and revision. Did fixing length remove an important fact? Record the tradeoff.

Save the input, prompt version, model, output, and your checks. Explain one failure in your own words before revising the prompt.

## Common mistake

Repeatedly asking “try harder” gives little information. Describe the actual failure.

## Before moving on

Can you explain when this technique helps, show one case where it fails, and describe how you checked the result? Use the [evaluation worksheet](../templates/evaluation.md) to record evidence.
