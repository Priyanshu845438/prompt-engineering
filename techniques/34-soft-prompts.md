# Soft prompts, prefix tuning, and fine-tuning

[Technique map](../TECHNIQUES.md) · [Home](../README.md)

## What it means

Soft prompts and prefix-tuning methods learn continuous parameters rather than editing ordinary instruction text. Fine-tuning updates model behavior using training. These require training infrastructure and are adjacent methods, not copy-paste chat prompt types.

## When to use it

Study when repeated specialized behavior remains difficult after simpler approaches are evaluated. Start with the simplest prompt that can meet your requirements; add this technique when a specific failure justifies it.

## Worked example

```text
Design a comparison plan for a handwritten prompt, retrieved examples, and a trained adaptation. Specify dataset splits, budget, and quality metrics.
```

**Expected behavior:** An experiment plan; no claim that a chat instruction trains weights.

This is a teaching example, not a recorded model response. A correct response can use different wording while meeting the same requirements. Replace bracketed placeholders with actual input.

## Why the prompt is written this way

The task statement tells the model what to produce. Any demonstrations or source material narrow the intended interpretation. The output requirement makes the result easier to inspect. Read the prompt again and identify which parts are instructions, examples, and data; do not count ordinary context as a demonstration.

## Practice

Explain which parameters change in each approach and how held-out data is protected.

Save the baseline and changed prompt. Use at least one ordinary case, one boundary case, and one case with missing information. Write expected behavior before requesting output. Record the model, date, settings, real output, and checks in the [evaluation worksheet](../templates/evaluation.md). If the task needs tools, record whether they actually ran.

## What can go wrong

Do not call a long system instruction “fine-tuning.”

Also check for invented facts, ignored constraints, and unintended copying of demonstration details. Repeated success on one easy input does not establish general reliability.

## Completion check

Explain this technique without using its name. Show a case where it is useful, a case where a simpler prompt suffices, and a failure your checks can detect. Describe any extra cost, context, or application code the method needs.

## Further reading

See the [source register](../SOURCES.md) for provider guidance and research references. Research results apply to the tested settings; rerun comparisons on your own model and task.
