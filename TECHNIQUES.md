# Prompt types and technique map

[Home](README.md) · [Learning path](LEARNING-PATH.md)

There is no single official list of every prompt type. Names overlap, and new methods appear. This guide separates ways of writing a prompt from multi-call workflows and training methods. It covers commonly used families and important research concepts without claiming that every named variant needs a separate workflow.

## Start with shot count

A **shot** is a demonstration example, usually an input paired with the desired output. It is not a conversation turn, an instruction, or a paragraph of background.

| Type | Demonstrations | A useful starting point |
| --- | --- | --- |
| Zero-shot | 0 | Clear, familiar task |
| One-shot | 1 | Show a specific transformation or style |
| Few-shot | A small set | Cover multiple patterns and boundaries |
| Many-shot | A larger set; no universal cutoff | Test whether extra coverage justifies context and cost |

A prompt can be few-shot, role-based, grounded, and structured-output at the same time. These labels describe different dimensions rather than mutually exclusive categories.

## Detailed guides

1. [Zero-shot prompting](techniques/01-zero-shot.md)
2. [One-shot prompting](techniques/02-one-shot.md)
3. [Few-shot prompting](techniques/03-few-shot.md)
4. [Many-shot prompting](techniques/04-many-shot.md)
5. [Direct instruction prompting](techniques/05-instruction.md)
6. [Role and persona prompting](techniques/06-role.md)
7. [Contextual prompting](techniques/07-contextual.md)
8. [Delimited and tagged prompting](techniques/08-delimited.md)
9. [Structured-output prompting](techniques/09-structured.md)
10. [Constraint-based prompting](techniques/10-constraints.md)
11. [Negative prompting and exclusions](techniques/11-negative.md)
12. [Conversational and multi-turn prompting](techniques/12-conversational.md)
13. [Clarification-first prompting](techniques/13-clarification.md)
14. [Chain-of-thought: research concept and practical use](techniques/14-chain-of-thought.md)
15. [Zero-shot reasoning prompts](techniques/15-zero-shot-reasoning.md)
16. [Few-shot reasoning demonstrations](techniques/16-few-shot-reasoning.md)
17. [Task decomposition and plan-then-execute](techniques/17-decomposition.md)
18. [Least-to-most prompting](techniques/18-least-to-most.md)
19. [Step-back prompting](techniques/19-step-back.md)
20. [Self-consistency](techniques/20-self-consistency.md)
21. [Tree of Thoughts](techniques/21-tree-of-thoughts.md)
22. [ReAct: reasoning and acting](techniques/22-react.md)
23. [Tool-augmented and program-aided prompting](techniques/23-tool-augmented.md)
24. [Prompt chaining](techniques/24-chaining.md)
25. [Routing prompts](techniques/25-routing.md)
26. [Critique-and-revise / self-refinement](techniques/26-critique-revise.md)
27. [Verification prompting](techniques/27-verification.md)
28. [Retrieval-augmented prompting](techniques/28-retrieval.md)
29. [Generated-knowledge prompting](techniques/29-generated-knowledge.md)
30. [Contrastive examples](techniques/30-contrastive.md)
31. [Multilingual prompting](techniques/31-multilingual.md)
32. [Multimodal prompting](techniques/32-multimodal.md)
33. [Meta-prompting and prompt optimization](techniques/33-meta-prompting.md)
34. [Soft prompts, prefix tuning, and fine-tuning](techniques/34-soft-prompts.md)

## Choose by failure

| Problem | Try first | Then check |
| --- | --- | --- |
| Task misunderstood | Direct instructions and relevant context | Correctness on a simple case |
| Style or labels wrong | One-shot, then representative few-shot examples | Unseen boundary cases |
| Output hard to parse | Structured output plus validation | Schema and facts separately |
| Missing knowledge | Retrieval or an authorized lookup tool | Actual evidence and permissions |
| Complex dependencies | Decomposition or least-to-most | Each intermediate artifact |
| Unsupported facts | Grounding and verification | Claim-to-source support |
| Different workflows needed | Routing | Mixed intent and fallback |
| Repeated quality failures | Evaluation, then targeted revision | Held-out cases and regression checks |

Do not use a role, more examples, or a longer explanation to compensate for unavailable evidence or missing tool permissions.
