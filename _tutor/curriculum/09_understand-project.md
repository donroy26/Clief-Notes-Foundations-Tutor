# Lesson 4.4 — Making Claude Understand Your Project

<!-- Source: Lesson 4.4.md -->

## Brief

What You'll Get From This

You will write a CLAUDE.md file that makes Claude Code behave like it has been on your project for a month. One file. Ten minutes. The difference is immediate.



The Lesson

One file changes everything

In Session 1 you installed Claude Code. In Session 2 you used it on real tasks. In Session 3 you used Desktop for thinking. All of that worked. But there is a problem you have probably already noticed: Claude Code does not know your project.

It does not know your conventions. It does not know your file structure. It does not know which libraries you use, which commands to run, or what you consider good work. Every time you start a new conversation, Claude is a smart stranger. It can do the work, but it guesses at all the things a team member would already know.

The fix is one file: CLAUDE.md.



What a CLAUDE.md is

A markdown file that sits in the root of your project folder. Claude Code reads it automatically every time it starts. It tells Claude what this project is, how it works, and what matters. Think of it as an onboarding document for a new hire. Except the new hire reads the entire thing in two seconds and follows every word.



What goes in it

Five things. Keep it short. 15 lines is enough. 10 minutes to write.

1. Project overview — Two to three sentences. What is this? What does it do?

2. Tech stack — What languages, frameworks, databases, tools.

3. How to run things — Dev server, tests, build commands. The commands Claude needs to know.

4. Key conventions — Naming patterns, file structure, architectural patterns you follow.

5. What to avoid — Things Claude should not do. Libraries you do not use. Patterns you have moved away from.



Example CLAUDE.md

# My Web App

React 18 + Express + PostgreSQL + TypeScript

## Commands
npm run dev | npm run api | npm test

## Conventions
Functional components only. Routes in src/api/.
All database queries go through src/db/queries/.

## Avoid
No class components. Don't modify db/migrations directly.
Don't use Moment.js (we use date-fns).

That is it. Fifteen lines. Ten minutes. The difference in Claude's behavior is immediate.



Tips

Write it for a smart person who just joined your project. That is literally what Claude is. If a new team member would need to know it on day one, put it in the CLAUDE.md.

Update it when your project changes. The CLAUDE.md is a living document. When you add a new convention, change a library, or shift your architecture, update the file. This is the same advice from 3.3 (Common Mistakes): stale context files are the most common reason Claude starts "getting worse."

Do not overthink it. A mediocre CLAUDE.md beats no CLAUDE.md every time. You can always improve it later. The first version takes 10 minutes. Each edit takes 30 seconds. Start now.

This is not just for code projects. If your project is a folder full of documents, the CLAUDE.md describes what those documents are, how they are organized, and what you are using them for. The same principle applies to any structured folder, whether it contains code, writing, research, or client files.

---

## Build

<!-- Runtime instructions for Claude — not prose delivered to the user -->

The user already has a CLAUDE.md from earlier lessons. This lesson deepens it with project-specific context.

**Step 1: Open their existing CLAUDE.md.**
- Instruction: "Open the CLAUDE.md you already have in your workspace. Read it back to me — I want to see what's in it."
- Inspect: Note what's already there. Is it from the basic template in Lesson 1.2, or has it grown?

**Step 2: Add the five elements.**

Walk through each element one at a time. If it's already covered, confirm it. If it's missing, help them add it.

- "Let's check the Project Overview — two to three sentences about what this project is. Does your CLAUDE.md have that? What does it say?"
  - If missing: "Add a two to three sentence overview at the top. What is this folder for? What kind of work happens here?"
  
- "Tech stack or document types — what tools, formats, or languages are you working with in this folder?"
  - If it's a code project: list languages and frameworks.
  - If it's a document folder: list document types and formats.
  
- "How to run things — for a code project, that's the dev/test/build commands. For a document folder, it's 'how do I use these files?' What should Claude know about the mechanics here?"
  
- "Key conventions — how do you name files? What patterns do you follow? What should Claude do by default when creating new content?"
  
- "What to avoid — what would annoy you if Claude did it? What patterns or behaviors should it never use in this folder?"

- Instruction after all five: "Update your CLAUDE.md with everything we just covered. Tell me when it's saved."

**Step 3: Inspect the updated file.**
- Read back the updated CLAUDE.md. Confirm all five elements are present and filled in with real content (not placeholders).

**Artifact:** Updated `[user-named-folder]/CLAUDE.md`

---

## Check-in

<!-- Runtime instructions for Claude -->

1. Inspect `[user-named-folder]/CLAUDE.md` — verify all five elements are present (overview, stack/types, how to run things, conventions, avoid). Confirm the content is specific to their actual project.

2. Ask: "If you started a second project tomorrow — a totally different folder — what's the one thing from this CLAUDE.md that you'd keep the same across both, and what would change?"

3. Record in `_tutor/progress.md`:
   - lesson: "09_understand-project"
   - artifacts_inspected: ["[path]/CLAUDE.md"]
   - comprehension.question: "If you started a second project tomorrow — a totally different folder — what's the one thing from this CLAUDE.md that you'd keep the same across both, and what would change?"
   - comprehension.answer: "[user's verbatim response]"
   - comprehension.pass: [true/false]

4. A good answer shows they understand which parts of a CLAUDE.md are portable (general conventions, identity) versus specific to the project (tech stack, file structure, specific avoid rules). A bad answer treats the whole file as either completely reusable or completely disposable.
