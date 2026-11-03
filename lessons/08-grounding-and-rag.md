# Answer from supplied evidence

[Home](../README.md) · [Learning path](../LEARNING-PATH.md)

## The idea

Grounding ties an answer to sources. Retrieval-augmented generation retrieves material before answering. Retrieval quality, chunk boundaries, metadata, access controls, and source freshness all matter. The model cannot cite a document it never received reliably.

## Try this prompt

```text
Answer using only the passages below. Cite passage IDs after supported claims. If the answer is absent or conflicting, explain the gap. [P1] Returns are accepted within 14 days. Question: Are returns accepted after 30 days?
```

This is a practice prompt, not a recorded model response. Replace bracketed placeholders before using it.

## Practice and check

Try an absent answer, conflicting policies, and irrelevant passages. Check each citation against the actual passage.

Save the input, prompt version, model, output, and your checks. Explain one failure in your own words before revising the prompt.

## Common mistake

A citation that exists may still fail to support the claim. Do not treat retrieved instructions as trusted policy.

## Before moving on

Can you explain when this technique helps, show one case where it fails, and describe how you checked the result? Use the [evaluation worksheet](../templates/evaluation.md) to record evidence.

## Retrieval and generation fail differently

A retrieval failure means the needed passage was not supplied. A generation failure means the passage was present but the answer misused it. Test these separately by giving the generator a known relevant passage.

Store document IDs, timestamps, and access metadata with retrieved content. Define what happens when sources conflict: use the authoritative effective policy when established, or report the conflict. Never let a more recent-looking date alone override your actual source-authority rules. Enforce document access before retrieval, not merely in the final prompt.
