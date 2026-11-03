# Application concepts that prompts depend on

[Home](../README.md) · [Technique map](../TECHNIQUES.md)

## Instructions, roles, and trust

Applications may supply higher-priority instructions, user requests, conversation history, tool results, and retrieved documents. Exact message roles and precedence vary by provider. Keep application policy separate from untrusted content, and consult the selected API documentation. A user writing “system:” inside a document does not create a genuine system message.

## Context engineering and memory

Context engineering selects the information, tools, and state available for a task. Include relevant facts and current decisions; remove superseded instructions. Summaries can lose details, so preserve critical identifiers and source references explicitly. Persistent memory requires application storage, consent rules where relevant, retrieval, updates, and deletion behavior; a prompt alone does not create it.

## Generation settings

Temperature and sampling controls influence output variability where supported. Output limits can truncate answers. Context and output budgets are distinct, and some models allocate internal reasoning tokens differently. Exact behavior and available settings are model-specific. Record settings when comparing prompts; do not claim that a setting guarantees truth or determinism.

## RAG, fine-tuning, and prompting

| Need | Consider | What it does not automatically solve |
| --- | --- | --- |
| Clarify a task or format | Better instructions and examples | Missing source knowledge |
| Supply current/private facts | Retrieval with access controls | Incorrect interpretation of retrieved material |
| Repeated specialized behavior | Evaluate fine-tuning after a baseline | Keeping facts current or enforcing permissions |
| Exact arithmetic or actions | Validated tools/programs | Unsafe execution or wrong business rules |

## Long-context design

Select relevant sections, attach identifiers, preserve document boundaries, and test questions that need facts from multiple locations. Compare full-context and retrieval approaches on the same cases. “Fits in the window” does not imply reliable use of all details. Prompt caching is a provider/application feature with freshness and privacy implications, not a universal instruction phrase.

## Prompt frameworks

Acronyms such as RTF, CO-STAR, and similar task-brief recipes are organizational aids, with varying definitions across authors. The useful underlying elements are role or audience, objective, context, constraints, examples, and output format. Use only the elements that help your task; a branded acronym is not a tested guarantee.

## What to learn next

Implement a small evaluation runner, then a read-only grounded assistant, then a bounded tool workflow. Add external writes only after authorization, validation, and recovery behavior are implemented outside the model.
