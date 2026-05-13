# Foundation Companion

This repo walks Jake Skool forum members through 11 Foundation lessons hands-on.

## On Session Start

1. Read `_tutor/PERSONA.md` (voice rules).
2. Read `_tutor/INSTRUCTIONS.md` (Lesson Loop rules).
3. Read `_tutor/progress.md` (current state). If missing or corrupted, run reconstruction logic from INSTRUCTIONS.md before anything else.
4. Load only the curriculum file matching `current_lesson` in the routing table below.
5. Begin Phase A (Open) of the Lesson Loop.

## Routing Table

| Lesson slug | Curriculum file |
|---|---|
| `01_first-folder` | `_tutor/curriculum/01_first-folder.md` |
| `02_prompt-structure` | `_tutor/curriculum/02_prompt-structure.md` |
| `03_full-walkthrough` | `_tutor/curriculum/03_full-walkthrough.md` |
| `04_customize` | `_tutor/curriculum/04_customize.md` |
| `05_common-mistakes` | `_tutor/curriculum/05_common-mistakes.md` |
| `06_install-first-use` | `_tutor/curriculum/06_install-first-use.md` |
| `07_in-practice` | `_tutor/curriculum/07_in-practice.md` |
| `08_thinking-partner` | `_tutor/curriculum/08_thinking-partner.md` |
| `09_understand-project` | `_tutor/curriculum/09_understand-project.md` |
| `10_where-this-goes` | `_tutor/curriculum/10_where-this-goes.md` |
| `11_path-from-here` | `_tutor/curriculum/11_path-from-here.md` |

## Hard Rules

Do not load more than one curriculum file per session. Do not advance past a lesson without both artifact inspection and comprehension Q&A passing. See `_tutor/INSTRUCTIONS.md`.
