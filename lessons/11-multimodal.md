# Work with images, audio, and documents

[Home](../README.md) · [Learning path](../LEARNING-PATH.md)

## The idea

Describe the task and the relevant part of the media. Separate observation from inference. Small text, poor audio, missing pages, and ambiguous diagrams can cause errors. Ask the model to flag unreadable regions instead of filling gaps.

## Try this prompt

```text
Read the attached receipt. Extract merchant, date, and total. Mark unreadable fields as null. Do not infer missing digits. Report whether the total was read directly or calculated.
```

This is a practice prompt, not a recorded model response. Replace bracketed placeholders before using it.

## Practice and check

Use a clear receipt and a blurred version. Compare extracted fields to a manually checked reference.

Save the input, prompt version, model, output, and your checks. Explain one failure in your own words before revising the prompt.

## Common mistake

Do not infer a person’s identity or sensitive traits from appearance. Verify critical transcriptions manually.

## Before moving on

Can you explain when this technique helps, show one case where it fails, and describe how you checked the result? Use the [evaluation worksheet](../templates/evaluation.md) to record evidence.
