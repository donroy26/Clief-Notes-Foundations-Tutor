# Lesson 7 — Claude Code in Practice

<!-- Source: Lesson 4.2.md -->

## Brief

What You'll Get From This

You will understand what makes Claude Code different from the chat interface, see the iteration loop in action, and walk away with a real deliverable built from your own files.



The Lesson

The real power

Claude Code is not smarter than Claude Desktop. It is the same model. The difference is what it can reach. Claude Code can see your work, touch your files, and iterate on its own output. That changes everything about how you work with it.

The loop looks like this: Read → Think → Write → Check → Adjust. Claude reads your files, thinks about the task, writes output, checks its own work, and adjusts. In the chat interface, that loop runs once and stops. In Claude Code, it runs until the job is done.



Example: meeting notes

Here is a task that shows the difference clearly.

You have 15 meeting notes. You want every decision made this quarter, organized by project.

The Desktop approach: Open file 1. Copy the text. Paste it into Claude. Ask for analysis. Repeat 15 times. Then manually combine all 15 responses into one document. About an hour of work.

The Claude Code approach: One prompt: "Read every file in /meeting-notes/ and summarize all decisions, organized by project." One prompt. 15 files. 90 seconds.

The model gives you the same quality analysis either way. The difference is how much manual work you do around it. Claude Code eliminates the copy-paste layer entirely.



Token math

Claude's context window is roughly 200K tokens. A typical meeting note is about 2,000 tokens. 15 notes is about 30,000 tokens. Well within the window.

In Desktop, you paste one file at a time and lose context between chats. Each conversation starts fresh. You are working against the architecture.

In Claude Code, it loads what it needs from your file system and keeps full context across the task. You are working with the architecture.

This is the same principle from 2.3 (How a 1953 Word Game Explains AI Memory): the context window is working memory. Claude Code lets you fill that working memory from your actual files instead of from your clipboard.



Tips that save hours

Be specific. "Analyze this" is weak. "Identify the three largest cost items and format as a table" is strong. The more specific your instruction, the less Claude has to guess. This is the Task part of the prompting framework from 1.3.

Tell it where to put the output. "Save the result as summary.md in this folder." Claude Code can write files. Let it. If your output lives in a chat window, you still have to copy it somewhere. If Claude writes it directly to a file, it is already where it needs to be.

Output wrong? Do not start over. Say what is wrong. "The summary missed the budget decisions from the March 14 meeting. Add those." Claude iterates. That is the whole point. Starting over throws away all the context Claude has built up about your task.

Claude Code is best for tasks that involve reading and writing files. That is where it shines. If your task is "help me think through a decision," Desktop might be better (that is Session 3). If your task is "read these 15 files and produce a deliverable," Claude Code wins every time.

---

## Build

<!-- Runtime instructions for Claude — not prose delivered to the user -->

The user runs a real Claude Code session on actual files from their work. One specific task, start to finish.

**Step 1: Pick a task.**
- Instruction: "Pick one of these that fits your work — or something similar:
  - 'I have documents or notes. Summarize them.'
  - 'I have a report or proposal. Find the gaps.'
  - 'I have a folder of files. Organize them by [criteria].'

What task do you want to run? Describe it specifically — not 'summarize stuff,' but 'summarize [specific files] to find [specific output].'"

- Wait for their answer. If it's too vague, ask them to narrow it.

**Step 2: Run the session.**
- Instruction: "Now actually run it. Give Claude Code the instruction in this session or in a separate session (your choice). Be specific: name the files or folder, name what you want back, and tell it where to save the output.

Come back when it's done and tell me:
1. What prompt did you use?
2. What did it produce?
3. Was the output what you expected?"

- Wait for their report.

**Step 3: Iteration (if needed).**
- If their output wasn't right: "Don't start over. Tell Claude exactly what's wrong and what to fix. What's the follow-up instruction you'd send?"
- Walk them through writing and sending the follow-up. Let them see the iteration loop in action.

**Step 4: Save the session log.**
- Instruction: "Create a file called `sessions/session-01.md` in your workspace. Write down:
  - The task you ran
  - The prompt you used
  - What it produced
  - What you'd do differently next time (if anything)

Tell me when it's saved."

- Inspect: Read the session log. Confirm it has real content — an actual task, actual prompt, actual result.

**Artifact:** `[user-named-folder]/sessions/session-01.md`

---

## Check-in

<!-- Runtime instructions for Claude -->

1. Inspect `[user-named-folder]/sessions/session-01.md` — verify it documents a real session (not a hypothetical or placeholder). It should have a specific prompt and a description of what Claude produced.

2. Ask: "Based on what you just ran — what's a task in your actual work that you've been doing manually that Claude Code could probably handle? Something you'd normally spend 20-30 minutes on?"

3. Record in `_tutor/progress.md`:
   - lesson: "07_in-practice"
   - artifacts_inspected: ["[path]/sessions/session-01.md"]
   - comprehension.question: "What's a task in your actual work that you've been doing manually that Claude Code could probably handle?"
   - comprehension.answer: "[user's verbatim response]"
   - comprehension.pass: [true/false]

4. A good answer names a specific task from their real work. A bad answer is generic ("I could probably automate a lot of things") without naming the thing.
