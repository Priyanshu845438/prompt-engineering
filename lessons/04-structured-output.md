# Ask for data you can validate

[Home](../README.md) · [Learning path](../LEARNING-PATH.md)

## The idea

A requested JSON shape improves clarity, but a prompt alone does not guarantee valid output. Where available, use the provider’s schema-constrained output feature and validate results in code. Schema validity and factual correctness are different checks.

## Try this prompt

```text
Extract only facts in this note. Return an object with name and date, using null for missing values. Do not guess. Note: Asha booked a call; the date has not been agreed.
```

This is a practice prompt, not a recorded model response. Replace bracketed placeholders before using it.

## Practice and check

Check that the result parses, has exactly the expected keys, and contains a null date. Try a note with quotation marks and a contradictory date.

Save the input, prompt version, model, output, and your checks. Explain one failure in your own words before revising the prompt.

## Common mistake

Never run model-generated SQL or commands just because the output has a valid schema.

## Before moving on

Can you explain when this technique helps, show one case where it fails, and describe how you checked the result? Use the [evaluation worksheet](../templates/evaluation.md) to record evidence.
