# ReAct: reasoning and acting

[Technique map](../TECHNIQUES.md) · [Home](../README.md)

## What it means

Alternate decisions, tool actions, and observations so external results inform the next action. In production, keep internal deliberation private and expose concise action summaries and tool evidence.

## When to use it

Use when the task needs fresh data or external operations. Start with the simplest prompt that can meet your requirements; add this technique when a specific failure justifies it.

## Worked example

```text
Check the order status using the read-only lookup tool. If the ID is absent, ask for it. If lookup fails, report the failure. Summarize only the returned status.
```

**Expected behavior:** An actual lookup followed by a status grounded in its result, or an honest request/error.

This is a teaching example, not a recorded model response. A correct response can use different wording while meeting the same requirements. Replace bracketed placeholders with actual input.

## Why the prompt is written this way

The task statement tells the model what to produce. Any demonstrations or source material narrow the intended interpretation. The output requirement makes the result easier to inspect. Read the prompt again and identify which parts are instructions, examples, and data; do not count ordinary context as a demonstration.

## Practice

Simulate missing IDs, failed tools, and malicious text inside results.

Save the baseline and changed prompt. Use at least one ordinary case, one boundary case, and one case with missing information. Write expected behavior before requesting output. Record the model, date, settings, real output, and checks in the [evaluation worksheet](../templates/evaluation.md). If the task needs tools, record whether they actually ran.

## What can go wrong

A model writing “Action: lookup” is not evidence that a tool executed.

Also check for invented facts, ignored constraints, and unintended copying of demonstration details. Repeated success on one easy input does not establish general reliability.

## Completion check

Explain this technique without using its name. Show a case where it is useful, a case where a simpler prompt suffices, and a failure your checks can detect. Describe any extra cost, context, or application code the method needs.

## Further reading

See the [source register](../SOURCES.md) for provider guidance and research references. Research results apply to the tested settings; rerun comparisons on your own model and task.
