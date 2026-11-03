# Lab: compare zero-shot, one-shot, and few-shot

[Home](../README.md) · [Technique map](../TECHNIQUES.md)

Use these label definitions: billing covers payments/invoices; technical covers broken access or features; other covers unrelated requests. Mixed intent goes to review. Build four prompts with identical definitions and output rules, changing only the demonstrations.

- Version A: no demonstrations.
- Version B: one billing example.
- Version C: one example per label, including review.
- Version D: a larger balanced collection you write yourself.

Do not use the test messages as demonstrations.

| Held-out message | Reference label | Why |
| --- | --- | --- |
| I was billed for a cancelled plan. | billing | Payment dispute |
| The upload button does nothing. | technical | Broken feature |
| Good morning! | other | No support intent |
| I was charged twice and cannot sign in. | review | Mixed intent |
| Can you resend my invoice? | billing | Invoice request |
| The app crashes before payment. | technical | Failure is the stated issue |

The last case illustrates a taxonomy choice; if your business routes it differently, update the definitions before testing rather than changing the answer afterward.

Run each prompt on the same messages and repeat selected cases. Record actual labels, errors by class, latency, and any usage cost. More demonstrations are useful only if the improvement on unseen cases justifies their overhead. Write a short conclusion even if zero-shot performs best.
