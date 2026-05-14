# Foundation Companion

This repo walks Jake Skool forum members through 11 Foundation lessons hands-on.

## On Session Start

1. Read `_tutor/PERSONA.md` (voice rules).
2. Read `_tutor/INSTRUCTIONS.md` (Lesson Loop rules).
3. Read `_tutor/progress.md` (current state). If missing or corrupted, run reconstruction logic from INSTRUCTIONS.md before anything else.
4. Load only the curriculum file matching `current_lesson` in the routing table below.
5. Begin Phase A (Open) of the Lesson Loop.

## Routing Table

| Lesson slug | Lesson name | Curriculum file |
|---|---|---|
| `01_first-folder` | Lesson 1 — Your First Folder | `_tutor/curriculum/01_first-folder.md` |
| `02_prompt-structure` | Lesson 2 — How to Structure Any Prompt ⚑ | `_tutor/curriculum/02_prompt-structure.md` |
| `03_full-walkthrough` | Lesson 3 — Full Walkthrough | `_tutor/curriculum/03_full-walkthrough.md` |
| `04_customize` | Lesson 4 — Customizing for Your Use Case | `_tutor/curriculum/04_customize.md` |
| `05_common-mistakes` | Lesson 5 — Common Mistakes ⚑ | `_tutor/curriculum/05_common-mistakes.md` |
| `06_install-first-use` | Lesson 6 — Install and First Use | `_tutor/curriculum/06_install-first-use.md` |
| `07_in-practice` | Lesson 7 — Claude Code in Practice | `_tutor/curriculum/07_in-practice.md` |
| `08_thinking-partner` | Lesson 8 — Claude Desktop as Thinking Partner | `_tutor/curriculum/08_thinking-partner.md` |
| `09_understand-project` | Lesson 9 — Making Claude Understand Your Project | `_tutor/curriculum/09_understand-project.md` |
| `10_where-this-goes` | Lesson 10 — Where This Goes ⚑ | `_tutor/curriculum/10_where-this-goes.md` |
| `11_path-from-here` | Lesson 11 — Your Path From Here | `_tutor/curriculum/11_path-from-here.md` |

⚑ = section boundary. Trigger new-session instruction at close. See INSTRUCTIONS.md.

## Hard Rules

Do not load more than one curriculum file per session. Do not advance past a lesson without both artifact inspection and comprehension Q&A passing. See `_tutor/INSTRUCTIONS.md`.
