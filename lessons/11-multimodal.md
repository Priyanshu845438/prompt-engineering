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

## Ask questions the media can answer

For images, specify the region and whether you want transcription, counting, comparison, or interpretation. For audio, specify transcription language, speaker labeling needs, and treatment of uncertain words. For video, request timestamps and distinguish observed events from inferred intent. For PDFs, check page order, tables, scanned text, and missing pages.

Use original-resolution material when small details matter. Preserve uncertainty in extracted fields and review consequential readings manually.
