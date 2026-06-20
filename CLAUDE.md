# Project: Дисциплина (distciplina)

Single-page web project. The entire site lives in `index.html`.

## Design skills — use on EVERY interface task

This repo has two design skills installed in `.claude/skills/`. For **any** task that
touches the UI/interface (layout, typography, spacing, color, motion, components,
copy, redesign, polish, accessibility, responsive behavior), you MUST use them:

1. **`design-taste-frontend`** (taste-skill) — anti-slop frontend craft. Read the
   brief, infer the right design direction, and ship interfaces that don't look
   templated. Use it when creating or substantially redesigning UI.

2. **`impeccable`** — design language, anti-pattern detection, and iteration
   commands (`audit`, `critique`, `polish`, `animate`, `layout`, `typeset`,
   `bolder`, `quieter`, etc.). Use it to audit/critique/polish existing UI and to
   verify changes are free of design anti-patterns.

### Working rule
- Before shipping any interface change, run the impeccable detector and resolve
  its findings:
  `node .claude/skills/impeccable/scripts/detect.mjs index.html`
- A `PostToolUse` hook (`.claude/settings.json`) runs this detector automatically
  after each Edit/Write to UI files and surfaces findings as system reminders.
  Treat those findings as blocking unless there's a deliberate reason to ignore them.
- Prefer the conventions and tokens already present in `index.html`; branch out
  only when the UX wins.
