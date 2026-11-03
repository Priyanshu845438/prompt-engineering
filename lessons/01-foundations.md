# What a prompt can and cannot do

[Home](../README.md) · [Learning path](../LEARNING-PATH.md)

## The idea

A prompt gives a model instructions and context. It cannot guarantee truth, grant access to missing files, or replace a database. Tokens are pieces of text or other input; a context window limits what the model can process in a request. A fluent answer can still be wrong.

## Try this prompt

```text
Explain HTTP to a beginner in 120 words. Include one browser example and define any technical term you use.
```

This is a practice prompt, not a recorded model response. Replace bracketed placeholders before using it.

## Practice and check

Compare that with “Explain HTTP.” Which answer fits a beginner better? Mark any factual errors using a reliable reference.

Save the input, prompt version, model, output, and your checks. Explain one failure in your own words before revising the prompt.

## Common mistake

A confident tone is not evidence. Ask for uncertainty when evidence is missing.

## Before moving on

Can you explain when this technique helps, show one case where it fails, and describe how you checked the result? Use the [evaluation worksheet](../templates/evaluation.md) to record evidence.

## Mental model

A request is processed using the supplied context and the model’s learned behavior. The model does not automatically see your screen, local files, private account, or the live web. Tool integrations may make some of these available; verify which ones are connected. Distinguish model knowledge from supplied evidence and actual tool observations.

Tokens affect capacity and cost. Long context can contain irrelevant or conflicting material; fitting inside a window does not guarantee that every detail will be used correctly.
