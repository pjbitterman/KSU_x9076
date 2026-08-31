# Sketch Peer Review Form

Use this form for  sketch peer review.

## Prompts

1. **What does this code do well?**
2. **Where would it break or mislead?**
3. **One concrete improvement.**

Respond to each prompt in a few sentences. Point to specific lines, cells, or outputs where you can — "this would fail if the input layer had a different CRS" is more useful than "looks good."

## Norms

- **Reviews are attributed, not anonymous.** Your name is visible to the person you're reviewing, and theirs is visible to you. Treat this like professional code review: direct, specific, and useful.
- **Critique the code, not the person.** Say "this function doesn't handle an empty input" rather than anything about the author. The goal is a better sketch, not a judgment.

## Review template

Copy the block below into your review, fill it in, and delete the parenthetical hints. 

```markdown
## Sketch __ review

- **Author:**
- **Reviewer:**

### 1. What does this code do well?

(A few sentences. Name at least one specific choice — a variable name,
a function, a check, an output — and say why it works. "Looks good" is
not a review.)

### 2. Where would it break or mislead?

(Describe a concrete situation: an input, dataset, or reader that this
code would fail on or give the wrong impression to. Point to the line
or cell where it happens.)

### 3. One concrete improvement

(One specific, actionable change: what to change, where, and what it
buys. Small and real beats big and vague.)
```

A good review takes about 15 minutes: run or read the sketch top to bottom once, then write. If you genuinely can't find something for prompt 2, say what you tested or looked for — "I tried X and it held up" is a real answer; a blank is not.
