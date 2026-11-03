# Few-shot reasoning demonstrations

[Technique map](../TECHNIQUES.md) · [Home](../README.md)

## What it means

Include examples with useful intermediate artifacts and correct answers, then ask for the same output pattern on a new case.

## When to use it

Use to teach a particular calculation or explanation format. Start with the simplest prompt that can meet your requirements; add this technique when a specific failure justifies it.

## Worked example

```text
Example: 2 tickets at ₹30, pay ₹100 → cost 2 × 30 = ₹60; change ₹40.
Example: 4 pens at ₹5, pay ₹50 → cost 4 × 5 = ₹20; change ₹30.
Now: 3 books at ₹20, pay ₹100. Give cost and change.
```

**Expected behavior:** Cost ₹60; change ₹40.

This is a teaching example, not a recorded model response. A correct response can use different wording while meeting the same requirements. Replace bracketed placeholders with actual input.

## Why the prompt is written this way

The task statement tells the model what to produce. Any demonstrations or source material narrow the intended interpretation. The output requirement makes the result easier to inspect. Read the prompt again and identify which parts are instructions, examples, and data; do not count ordinary context as a demonstration.

## Practice

Introduce a case with insufficient payment and specify how that should be reported.

Save the baseline and changed prompt. Use at least one ordinary case, one boundary case, and one case with missing information. Write expected behavior before requesting output. Record the model, date, settings, real output, and checks in the [evaluation worksheet](../templates/evaluation.md). If the task needs tools, record whether they actually ran.

## What can go wrong

Incorrect worked examples can teach incorrect methods.

Also check for invented facts, ignored constraints, and unintended copying of demonstration details. Repeated success on one easy input does not establish general reliability.

## Completion check

Explain this technique without using its name. Show a case where it is useful, a case where a simpler prompt suffices, and a failure your checks can detect. Describe any extra cost, context, or application code the method needs.

## Further reading

See the [source register](../SOURCES.md) for provider guidance and research references. Research results apply to the tested settings; rerun comparisons on your own model and task.
