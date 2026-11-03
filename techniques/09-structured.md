# Structured-output prompting

[Technique map](../TECHNIQUES.md) · [Home](../README.md)

## What it means

Request a stable representation such as JSON, a table, or a schema. Use application validation and provider constraints when available.

## When to use it

Use when downstream code needs predictable fields. Start with the simplest prompt that can meet your requirements; add this technique when a specific failure justifies it.

## Worked example

```text
Extract name and age. Return JSON with exactly those keys; use null for absent facts. Text: Mina attended the workshop.
```

**Expected behavior:** {"name":"Mina","age":null}

This is a teaching example, not a recorded model response. A correct response can use different wording while meeting the same requirements. Replace bracketed placeholders with actual input.

## Why the prompt is written this way

The task statement tells the model what to produce. Any demonstrations or source material narrow the intended interpretation. The output requirement makes the result easier to inspect. Read the prompt again and identify which parts are instructions, examples, and data; do not count ordinary context as a demonstration.

## Practice

Try malformed text and ensure the result is parsed and validated before use.

Save the baseline and changed prompt. Use at least one ordinary case, one boundary case, and one case with missing information. Write expected behavior before requesting output. Record the model, date, settings, real output, and checks in the [evaluation worksheet](../templates/evaluation.md). If the task needs tools, record whether they actually ran.

## What can go wrong

Valid JSON can contain false facts.

Also check for invented facts, ignored constraints, and unintended copying of demonstration details. Repeated success on one easy input does not establish general reliability.

## Completion check

Explain this technique without using its name. Show a case where it is useful, a case where a simpler prompt suffices, and a failure your checks can detect. Describe any extra cost, context, or application code the method needs.

## Further reading

See the [source register](../SOURCES.md) for provider guidance and research references. Research results apply to the tested settings; rerun comparisons on your own model and task.
