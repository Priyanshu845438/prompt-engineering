# Zero-shot reasoning prompts

[Technique map](../TECHNIQUES.md) · [Home](../README.md)

## What it means

Request a decomposition or checkable solution without worked demonstrations. Historically, zero-shot CoT research used a reasoning cue; that cue is not a universal performance guarantee.

## When to use it

Try when a task benefits from explicit verification and no examples are available. Start with the simplest prompt that can meet your requirements; add this technique when a specific failure justifies it.

## Worked example

```text
Find the total duration of sessions lasting 25, 40, and 35 minutes. Show a short equation and the final duration.
```

**Expected behavior:** 25 + 40 + 35 = 100 minutes.

This is a teaching example, not a recorded model response. A correct response can use different wording while meeting the same requirements. Replace bracketed placeholders with actual input.

## Why the prompt is written this way

The task statement tells the model what to produce. Any demonstrations or source material narrow the intended interpretation. The output requirement makes the result easier to inspect. Read the prompt again and identify which parts are instructions, examples, and data; do not count ordinary context as a demonstration.

## Practice

Compare answer-only and equation-plus-answer prompts on several arithmetic cases.

Save the baseline and changed prompt. Use at least one ordinary case, one boundary case, and one case with missing information. Write expected behavior before requesting output. Record the model, date, settings, real output, and checks in the [evaluation worksheet](../templates/evaluation.md). If the task needs tools, record whether they actually ran.

## What can go wrong

Do not assume “think step by step” improves every model or task.

Also check for invented facts, ignored constraints, and unintended copying of demonstration details. Repeated success on one easy input does not establish general reliability.

## Completion check

Explain this technique without using its name. Show a case where it is useful, a case where a simpler prompt suffices, and a failure your checks can detect. Describe any extra cost, context, or application code the method needs.

## Further reading

See the [source register](../SOURCES.md) for provider guidance and research references. Research results apply to the tested settings; rerun comparisons on your own model and task.
