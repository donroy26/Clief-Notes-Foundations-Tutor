# Lesson 10 — Where This Goes

<!-- Source: Lesson 4.5.md -->

## Brief

What You'll Get From This

You will see how the CLAUDE.md scales from one project to a full workspace architecture. You will set up two scoped contexts and watch Claude behave differently in each one. And you will know exactly where to go next.



The Lesson

What you have built so far

Across the first four sessions, you set up three interfaces (Desktop, VS Code, Terminal), ran real tasks on your own files, used Desktop for thinking and Code for building, and wrote a CLAUDE.md that gives Claude project-level context.

That is more than most people will ever set up. And it works.



But what if...

You have 10 projects. Or a complex workflow with different types of tasks. Or a team that needs the same quality from Claude across everyone's work.

One CLAUDE.md per project still works. But there is a level above that.



Task routing

In my workspace, different tasks load different context. Automatically.

"Write a script" → loads voice docs only. "Build an animation" → loads the design system and component library. "Build a course module" → loads the curriculum and guidelines.

Same Claude. Same context window. Different context per task. The routing table in the CLAUDE.md decides what loads based on what you ask for.

This is the three-layer architecture from Section 3 in full operation:




Layer 1 (CLAUDE.md) — The map. Routes every task to the right workspace.



Layer 2 (Workspace context files) — The rooms. Each workspace has its own CONTEXT.md describing what happens there.



Layer 3 (Skills and tools) — Plug-and-play. Loaded per workspace, not globally.

If you went through Section 3, this is what it looks like when you run it with Claude Code. If you skipped Section 3 and jumped straight to the Claude Code sessions, this is your introduction to the architecture. Go back to Section 3.1 for the full walkthrough.



Why this matters at scale

200K tokens sounds huge until you fill it with irrelevant files. If Claude is writing a blog post but also reading your animation specs and your client contracts, you are burning tokens on context that has nothing to do with the task. The output gets noisier. The quality drops.

Task routing solves this. Each task loads only the context it needs. Clean input, clean output.

Three principles that make it work:




One fact, one location. Information lives in one place. No duplication across context files. No drift where one file says one thing and another says something different.



New sessions start clean. When you start a new conversation in Claude Code, it reads the CLAUDE.md fresh. The routing table sends it to the right workspace. No leftover context from a previous task bleeding into the current one.



Hand it to a team and everyone gets the same quality. When the context lives in files, not in someone's head, anyone who opens the folder gets the same Claude experience. This is how you scale from one person to a team without losing consistency.



Try the smallest version

You do not need the full architecture to start. Here is the lightest way to test workspace routing.

If you have two distinct areas in your work, create two separate folders. Give each one its own CLAUDE.md with context specific to that area.

area-a/
├── CLAUDE.md  (context for Area A)
└── [your files]

area-b/
├── CLAUDE.md  (context for Area B)
└── [your files]

Run a task in Area A. Then run a task in Area B. Watch Claude behave differently in each one. That difference is workspace routing at its simplest.

When you are ready to put both under one roof with a single routing table, that is the full architecture from 3.1. You already have the pieces. You just need to combine them.

---

## Build

<!-- Runtime instructions for Claude — not prose delivered to the user -->

The user creates a second scoped context and observes how Claude behaves differently in each.

**Step 1: Identify a second area.**
- Instruction: "You already have a workspace set up. Now think about a second, distinct area of your work — something different enough that you'd want Claude to have different context. What would that be?"
- Wait for their answer. Examples: a second project, a different type of work (writing vs. coding), a client vs. internal work.

**Step 2: Create the second folder and CLAUDE.md.**
- Instruction: "Create a second folder for that area. Give it its own CLAUDE.md — but make it specific to that area, not a copy of your first one. Tell me when it's there."
- If they're not sure what to put in it: "Use the same five-element template from Lesson 9. What's the overview? What's different about how Claude should behave here?"

**Step 3: Run a comparison.**
- Instruction: "Now run the same task in both folders. Pick something like: 'Summarize what you know about this project and list three things I should do next.'

Run it in folder 1. Then run it in folder 2. Tell me: how did Claude respond differently in each one?"

- Wait for their report. If they didn't notice a difference, ask them to look at what each CLAUDE.md says and compare.

**Step 4: Write the planning file.**
- Instruction: "Last step: create a file called `next-steps-draft.md` in your workspace. Based on everything you've built across these four sessions — where do you want to take this next? Not the official 'where to go next' paths — just your honest answer for your own work. Two to three sentences.

Tell me when it's saved."
- Inspect: Read the file. Confirm it's their actual next step, not a copy from the lesson.

**Artifact:** `[user-named-folder]/next-steps-draft.md`

---

## Check-in

<!-- Runtime instructions for Claude -->

1. Inspect `[user-named-folder]/next-steps-draft.md` — verify it's specific to their actual work (not a generic "keep learning" statement). It should name something concrete.

2. Ask: "You said [reference their answer about where they want to take this]. What's the one thing you'd need to figure out or set up to actually get there?"

3. Record in `_tutor/progress.md`:
   - lesson: "10_where-this-goes"
   - artifacts_inspected: ["[path]/next-steps-draft.md"]
   - comprehension.question: "What's the one thing you'd need to figure out or set up to actually get there?" (tailored to their answer)
   - comprehension.answer: "[user's verbatim response]"
   - comprehension.pass: [true/false]

4. A good answer names a specific obstacle or next action. A bad answer is vague ("I just need to use it more") or circular ("I need to learn more").

**Section boundary:** This is Lesson 10 — a section boundary. After both checks pass, go to Phase E (Close) and deliver the restart phrasing from PERSONA.md.
