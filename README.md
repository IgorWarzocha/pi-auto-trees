# pi-auto-trees

Incremental Pi session-tree workflow extension.

Commands:
- `/marker` — mark the current conversation point as the baseline checkpoint
- `/end` — summarize work since `/marker`, jump back, and advance the marker
- `/end full` — use Pi's default branch-summary prompt
- `/end <custom prompt>` — append custom summary focus

Usage:
```bash
pi --extension /home/igorw/Work/pi-auto-trees/index.ts
```
