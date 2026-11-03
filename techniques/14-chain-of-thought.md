# Chain-of-thought: research concept and practical use

[Technique map](../TECHNIQUES.md) · [Home](../README.md)

## What it means

The research technique demonstrates intermediate reasoning along with answers. Modern systems may perform reasoning internally. For everyday use, ask for a concise explanation, equations, or checkable intermediate results rather than private internal deliberation.

## When to use it

Use checkable intermediate artifacts for calculations and multi-step tasks. Start with the simplest prompt that can meet your requirements; add this technique when a specific failure justifies it.

## Worked example

```text
A notebook costs ₹40. I buy three and pay ₹150. Give the total cost, the change, and the equation used.
```

**Expected behavior:** Total ₹120; change ₹30; 150 − 3 × 40 = 30.

This is a teaching example, not a recorded model response. A correct response can use different wording while meeting the same requirements. Replace bracketed placeholders with actual input.

## Why the prompt is written this way

The task statement tells the model what to produce. Any demonstrations or source material narrow the intended interpretation. The output requirement makes the result easier to inspect. Read the prompt again and identify which parts are instructions, examples, and data; do not count ordinary context as a demonstration.

## Practice

Change the quantities and verify independently with a calculator.

Save the baseline and changed prompt. Use at least one ordinary case, one boundary case, and one case with missing information. Write expected behavior before requesting output. Record the model, date, settings, real output, and checks in the [evaluation worksheet](../templates/evaluation.md). If the task needs tools, record whether they actually ran.

## What can go wrong

Verbose reasoning can be wrong; asking for hidden chain-of-thought is unnecessary.

Also check for invented facts, ignored constraints, and unintended copying of demonstration details. Repeated success on one easy input does not establish general reliability.

## Completion check

Explain this technique without using its name. Show a case where it is useful, a case where a simpler prompt suffices, and a failure your checks can detect. Describe any extra cost, context, or application code the method needs.

## Further reading

See the [source register](../SOURCES.md) for provider guidance and research references. Research results apply to the tested settings; rerun comparisons on your own model and task.
