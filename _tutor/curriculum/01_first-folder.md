# Lesson 1 — Your First Folder

<!-- Source: Lesson 1.2.md -->

## Brief

What You'll Get From This

A working folder that changes how Claude responds to you. Three files. Five minutes. You will see the difference immediately.



The Lesson

Right now, most people open Claude, type a question, and start over every time. Every conversation begins from zero. You spend half the message explaining who you are, what you are working on, and what you need. Then you hit the token limit, start a new chat, and do it all again.

The folder fixes that.

You give Claude a small set of files. Those files tell it who you are, what the project is, and what good work looks like. Claude reads them and its responses change. You will notice it in the first message.

This is the quick version. We are getting you a win right now. If you want to understand why this works (context windows, tokens, routing, the full architecture), that is all shown and explained in Section 3. You do not need any of that to start. You just need three files.



Step 1: Make the Folder

Open your code editor (VS Code or Cursor from Lesson 1.1). Create a new folder. Name it after whatever you are working on.

my-first-workspace/




Step 2: Create Three Files

Inside that folder, create three files. Use .md (markdown) if you can. Plain .txt works too.

File 1: CLAUDE.md

This tells Claude who it is working for and how to behave.

# Identity

You are helping [YOUR NAME] with [WHAT YOU DO].

## Rules
- Write in plain, clear language
- Ask clarifying questions before making assumptions
- When you are unsure, say so


Replace the brackets with your info. Keep it short.

File 2: CONTEXT.md

This tells Claude what you are working on right now.

# Current Project

## What we are building
[Describe your project in 2-3 sentences]

## What good looks like
[What does a successful output look like?]

## What to avoid
[Common mistakes or things you do not want]


File 3: REFERENCES.md

Background material. Examples, links, notes, anything Claude should know about but does not need to act on directly.

# References

## Examples of good work
[Paste an example or describe what you liked about it]

## Relevant links
[URLs, docs, resources for this project]

## Notes
[Anything else Claude should know]


That is it. Three files.



Step 3: Point Claude At It

If you are using Claude Code (terminal): Navigate to the folder, type claude. It reads the files automatically.

cd my-first-workspace
claude


Ask it something about your project. Notice how different the response is.

If you are using Claude in the browser (claude.ai): Two options:

Projects: Create a Project, upload your three files as Project Knowledge, and start a conversation inside that Project. Claude references them in every message.

Copy and paste: Copy the contents of all three files and paste them at the top of your first message. Less elegant. Works fine.



Step 4: See The Difference

Ask Claude something related to your project. Compare what you get now versus what you would have gotten cold.

The response should feel more specific, more relevant, more like talking to someone who already knows what you are working on. Because now it does.



What just happened?

You gave Claude three things it never has in a normal chat: who you are, what the project is, and what good looks like. That is the whole idea. The files carry context so you do not have to re-explain it every time.

You can edit these files whenever your project changes. You can add more files when you need Claude to know more. You can create separate folders for separate projects. The system grows with you.

This is the starting point. There is a full architecture underneath this (three layers, routing tables, naming conventions, production pipelines) and it is all covered in Section 3 when you are ready for it. But everything in Section 3 builds on what you just did. These three files are the foundation.

---

## Build

<!-- Runtime instructions for Claude — not prose delivered to the user -->

Important: all build artifacts for every lesson go INSIDE this Foundation Companion folder — the one the user has open in Claude Code right now. Never send the user to create things elsewhere on their machine. This keeps everything visible in the sidebar, inspectable by you, and tracked in progress.md with paths that actually resolve.

Walk the user through these steps one at a time. Wait for "done" after each step before continuing.

**Step 1: Create the workspace folder.**
- Instruction: "We're going to build your practice workspace right here inside the Foundation Companion folder — so it stays visible in your sidebar and I can inspect your work throughout all 11 lessons. Create a new folder here, at the root of this project. Name it after whatever you're actually working on right now. Something like `my-blog`, `client-work`, or `dev-projects` — whatever fits. Tell me when it's there and what you named it."
- Inspect: Use your file tools to confirm the folder exists at the repo root (e.g., `my-blog/` or whatever they named it). If you can't see it, ask them to confirm the path.

**Step 2: Create CLAUDE.md inside the folder.**
- Instruction: "Good. Now create a file called CLAUDE.md inside that folder. Here's the starter content — replace the brackets with your actual name and what you do, then save it:

```
# Identity

You are helping [YOUR NAME] with [WHAT YOU DO].

## Rules
- Write in plain, clear language
- Ask clarifying questions before making assumptions
- When you are unsure, say so
```

Tell me when it's saved."
- Inspect: Ask them to read back what's in the file. Verify it has their actual name and role filled in (not the placeholder text).

**Step 3: Verify Claude can see it.**
- Instruction: "Open the CLAUDE.md in your editor (click it in the sidebar) and read back the first two lines. I want to confirm it's exactly what you saved."
- Inspect: Read the file at `[user-named-folder]/CLAUDE.md` using your file tools. Confirm the content matches what they reported — specifically that they replaced the bracket placeholders with their actual name and role.

**Artifact:** `[user-named-folder]/CLAUDE.md`
(where `[user-named-folder]` is the name they chose, e.g., `my-blog/CLAUDE.md` — always a direct child of the Foundation Companion root)

Note: The lesson source also shows CONTEXT.md and REFERENCES.md. Walk the user through creating those too if time allows, but CLAUDE.md is the required artifact for the Check-in.

---

## Check-in

<!-- Runtime instructions for Claude -->

1. Inspect `[user-named-folder]/CLAUDE.md` — verify it has the correct structure (# Identity heading, their actual name and role, ## Rules section). It should not still have placeholder text.

2. Ask: "If you were setting this up for a completely different project tomorrow — something you're actually working on — what would you put in the CLAUDE.md? Walk me through it."

3. Record in `_tutor/progress.md`:
   - lesson: "01_first-folder"
   - artifacts_inspected: ["[user-named-folder]/CLAUDE.md"]
   - comprehension.question: "If you were setting this up for a completely different project tomorrow, what would you put in the CLAUDE.md? Walk me through it."
   - comprehension.answer: "[user's verbatim response]"
   - comprehension.pass: [true/false]

4. Do not advance until both artifact inspection and Q&A pass. If the file still has placeholder text, have them fix it before proceeding. If the comprehension answer is vague or a repeat of the lesson text, ask a follow-up: "Make it specific — what project, what would the Identity line actually say?"
