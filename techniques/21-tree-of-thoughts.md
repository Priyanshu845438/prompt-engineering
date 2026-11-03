# Tree of Thoughts

[Technique map](../TECHNIQUES.md) · [Home](../README.md)

## What it means

Explore candidate intermediate states, evaluate them, and search or backtrack toward a solution. A faithful implementation needs a controller and state evaluation, not merely a request to list ideas.

## When to use it

Use when branching alternatives and recovery from dead ends matter. Start with the simplest prompt that can meet your requirements; add this technique when a specific failure justifies it.

## Worked example

```text
Propose three candidate schedules satisfying these constraints. Score each against the constraints. Expand only feasible candidates and discard violations. Constraints: [scheduling problem].
```

**Expected behavior:** A candidate-state exercise with explicit feasibility checks; not a claim of implementing the full research algorithm.

This is a teaching example, not a recorded model response. A correct response can use different wording while meeting the same requirements. Replace bracketed placeholders with actual input.

## Why the prompt is written this way

The task statement tells the model what to produce. Any demonstrations or source material narrow the intended interpretation. The output requirement makes the result easier to inspect. Read the prompt again and identify which parts are instructions, examples, and data; do not count ordinary context as a demonstration.

## Practice

Implement a small search loop and compare it with a single-pass answer.

Save the baseline and changed prompt. Use at least one ordinary case, one boundary case, and one case with missing information. Write expected behavior before requesting output. Record the model, date, settings, real output, and checks in the [evaluation worksheet](../templates/evaluation.md). If the task needs tools, record whether they actually ran.

## What can go wrong

More branches increase calls and can amplify a poor evaluator.

Also check for invented facts, ignored constraints, and unintended copying of demonstration details. Repeated success on one easy input does not establish general reliability.

## Completion check

Explain this technique without using its name. Show a case where it is useful, a case where a simpler prompt suffices, and a failure your checks can detect. Describe any extra cost, context, or application code the method needs.

## Further reading

See the [source register](../SOURCES.md) for provider guidance and research references. Research results apply to the tested settings; rerun comparisons on your own model and task.
