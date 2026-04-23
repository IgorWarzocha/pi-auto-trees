# pi-auto-trees

`pi-auto-trees` is a small Pi extension for long-running coding sessions.

It helps you keep one session going without dragging all the implementation noise forward forever.

## What it does

### `/marker`
Marks the current point in the conversation as your checkpoint.

This is useful after repo familiarization, exploration, planning, or any other point you want to return to later.

### `/end`
Summarizes the work done since the last `/marker`, jumps back to that checkpoint, and carries the result forward as a compact branch summary.

The marker is then advanced to the new summarized point, so you can keep working in increments.

## Why this is useful

A common Pi workflow looks like this:

1. Explore a repo
2. Make a plan
3. Mark that point with `/marker`
4. Implement a feature, fix bugs, open a PR, iterate
5. Run `/end`

After `/end`, you keep the useful context:
- repo understanding
- planning context
- accepted outcome of the work

And you drop the noisy context:
- dead ends
- temporary debugging
- incidental churn

So the session stays usable for much longer.

## `/end` modes

### `/end`
Uses the extension's default summary behavior, tuned for completed work increments.

### `/end full`
Uses Pi's normal branch-summary prompt.

### `/end <custom prompt>`
Adds your own focus instructions for the summary.

Examples:

- `/end focus on API changes and migration notes`
- `/end focus on reviewer feedback and follow-up risks`

## Install

Add the extension path to your Pi settings or launch Pi with it directly:

```bash
pi --extension /path/to/pi-auto-trees/index.ts
```

## Result

You get an incremental workflow inside a single Pi session:

- mark a stable point
- do a chunk of work
- roll it back into durable context
- continue from there
