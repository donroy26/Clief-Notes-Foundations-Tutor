# Lesson 2 — How to Structure Any Prompt

<!-- Source: Lesson 1.3.md -->

## Brief

What You'll Get From This

A framework for building prompts that get useful results on the first try. Five parts. Works for writing, coding, research, or anything else you throw at Claude.



The Lesson

A prompt is an instruction set. The clearer the instruction, the better the result. Most people write prompts the way they send a text message. That works for simple questions. It falls apart the moment you want Claude to do real work.

If you went through Section 1.2: Your First Folder, you already know that giving Claude structured context changes the output. The folder handles the big picture: who you are, what the project is, what good looks like. This lesson handles the individual ask. Each time you need Claude to do something specific, how do you phrase it so you get something useful back?

Five parts. You will not use all five every time. But knowing them means you always know which one is missing when the output is not right.



Part 1: Identity — Who is Claude right now?

Tell Claude what role to fill. This shapes the vocabulary, the depth, and the assumptions it makes.



You are a senior copywriter who writes for B2B SaaS companies.



You are a research assistant helping me prepare a literature review.



You are a Python developer who writes clean, well-documented code.

If you set up a CLAUDE.md file in 1.2, this part is already handled for your project. The file does this work for you in every conversation. But for one-off tasks or tasks where you need Claude to shift roles, you add identity at the top of your prompt.

One note: identity is the part most people skip. They jump straight to "write me a blog post" without telling Claude who is writing it. The output is always more generic without it.



Part 2: Task — What needs to get done?

Be specific. "Help me write something" is vague. "Write a 200-word product description for [X] targeting [Y] audience" gives Claude something to work with.

Good tasks have three things:




A clear action — write, review, analyze, compare, build, fix, summarize



A defined scope — how long, how many, what format, what section



Enough detail that someone unfamiliar with your project could attempt it

If you read your task out loud and a stranger could not start working on it without asking you five follow-up questions, the task is too vague.



Part 3: Context — What does Claude need to know?

This is the background. The constraints. The audience. Prior decisions. Relevant data. Anything Claude needs to do the task well that it would not know on its own.

If you are using the folder structure from 1.2, your CONTEXT.md handles the project-level stuff. But for individual prompts, you can also give context directly:



We are a 15-person startup. Our customers are mid-market HR directors. We just launched a feature that automates onboarding checklists. Here is the feature spec: [paste spec]

The more relevant context you give, the less Claude has to guess. Guessing is where AI outputs go sideways. If the output feels generic or off-target, the fix is almost always more context, not a better prompt.



Part 4: Constraints — What should Claude avoid?

This is the part where most people leave value on the table. Telling Claude what you do NOT want is just as useful as telling it what you do want.



Do not use jargon. Write at an 8th grade reading level.



Do not suggest solutions that require a paid API. Everything should use free tools.



Keep it under 300 words. No bullet points. Write in paragraphs.



Do not start with "In today's world" or any variation of it.

Constraints save you editing time. Every constraint you give is a mistake Claude will not make. Think about the last three times an AI output annoyed you. Those annoyances are constraints you did not set.



Part 5: Output Format — What should the result look like?

Tell Claude the shape of the answer. A list? A table? Three options to choose from? A code block with comments? A draft with placeholder sections?



Give me three headline options, each under 10 words, followed by a one-sentence explanation of the angle.



Return this as a markdown table with columns for Task, Owner, Deadline, and Status.



Write the first draft with [PLACEHOLDER] wherever I need to fill in company-specific details.



Give me the answer as a numbered list, then add a one-paragraph summary at the end.

Output format is the difference between getting something you can use immediately and getting something you have to reformat for 20 minutes.



When to use which parts

You do not need all five in every prompt. Here is the shortcut:

If your task is... You probably need... Simple and quick (rename this, fix this typo) Task only Creative (write this, design this) Identity + Task + Constraints + Output Format Complex (build this system, analyze this data) All five Ongoing (a project over many messages) Identity and Context in your folder files. Task and Constraints in each prompt.

Notice the last row. That is where the folder structure from 1.2 and this prompting framework connect. Your files carry the persistent stuff (identity, project context, rules). Your prompts carry the per-task stuff (what to do right now, what to avoid this time, what shape the output should take).

The folder is memory. The prompt is direction. They work together.



Chunking: breaking big projects into prompts

If your project is bigger than a single prompt can handle, break it into steps.

The rule: each prompt should ask for one clear thing.

Too much at once: "Write me a full marketing strategy with a content calendar, email sequences, and social posts for the next quarter."

Claude will try to do all of it. The output will be shallow across the board because it is spreading its effort too thin.

Chunked into steps:




"Here is our product and audience. Outline the three main themes for Q2 content."



[You review. You adjust. You pick a direction.]



"Take theme 1 and draft a 4-week content calendar."



[You review. You adjust.]



"Write the first email in the nurture sequence for theme 1."

Each step builds on the last. You review and correct between steps. Claude gets cleaner input each time because you narrowed the scope. And if something goes wrong at step 3, you only redo step 3, not the whole thing.

This is the same principle behind the folder architecture. You do not dump everything into one giant file. You break it into layers. Prompting works the same way.



A real example: one prompt, five parts

Here is what it looks like when you put all five parts together. This is a single prompt:

You are a technical writer who explains complex topics to a non-technical audience.
(Identity)

Write a 300-word explanation of how API keys work and why someone would need one.
(Task)

This is for a community of people who are learning to use AI tools. Most of them
have never written code. They are encountering API keys for the first time because
they are setting up Claude Code.
(Context)

Do not use jargon without explaining it. Do not assume they know what a server is.
Keep sentences short.
(Constraints)

Start with a one-sentence analogy, then explain the concept, then give them the
three steps to get their first API key. End with a one-line reassurance that this
is easier than it sounds.
(Output Format)


You will not always write prompts this long. But when you are getting vague or unhelpful responses, you can look at this structure and ask: which part am I missing?

---

## Build

<!-- Runtime instructions for Claude — not prose delivered to the user -->

Walk the user through building a complete five-part prompt for something in their actual work. One step at a time.

**Step 1: Name the five parts.**
- Instruction: "Before we write anything — say back to me the five parts of the framework. Just the names, in order."
- Inspect: Confirm they can name all five: Identity, Task, Context, Constraints, Output Format. If they miss any, give them a hint and have them try again before moving on.

**Step 2: Pick a real task.**
- Instruction: "Good. Now pick something you actually need to do in your work this week. One specific task. Tell me what it is."
- Wait for their answer. Confirm it's specific enough (not "write some emails" — "write a follow-up email to a client who hasn't responded in two weeks").

**Step 3: Build each part, one at a time.**
Walk through each of the five parts in sequence:
- "Let's start with Identity. What role should Claude be in for this task? Write that line."
  - [User writes it. Give feedback if it's too vague.]
- "Now Task. Write the specific action, scope, and enough detail a stranger could attempt it."
  - [User writes it. Check for specificity.]
- "Now Context. What background does Claude need that it wouldn't know on its own?"
  - [User writes it.]
- "Now Constraints. What do you NOT want Claude to do? What would annoy you if it showed up in the output?"
  - [User writes it.]
- "Now Output Format. What should the result look like? Shape, length, structure."
  - [User writes it.]

**Step 4: Assemble and save.**
- Instruction: "Put all five parts together into one prompt. Save it as a file in your workspace folder from Lesson 1. Name it something like `prompts/[topic].md` or just `my-first-prompt.md`. Tell me the path when it's saved."
- Inspect: Read the saved file. Verify all five parts are present and the prompt is coherent.

**Artifact:** `[user-named-folder]/prompts/[prompt-name].md` (or equivalent path)

---

## Check-in

<!-- Runtime instructions for Claude -->

1. Inspect the prompt file at the path the user gave. Verify:
   - All five parts are present (Identity, Task, Context, Constraints, Output Format).
   - The Task is specific (not vague).
   - At least one Constraint is stated.
   - Output Format describes the shape of the result.

2. Ask: "The next time you get a vague or unhelpful response from Claude — what's the first thing you'd check in your prompt?"

3. Record in `_tutor/progress.md`:
   - lesson: "02_prompt-structure"
   - artifacts_inspected: ["[path to their prompt file]"]
   - comprehension.question: "The next time you get a vague or unhelpful response from Claude — what's the first thing you'd check in your prompt?"
   - comprehension.answer: "[user's verbatim response]"
   - comprehension.pass: [true/false]

4. Do not advance until both artifact inspection and Q&A pass. A good answer identifies a specific part (e.g., "I'd check if I gave enough Context" or "I'd look at whether my Task is specific enough"). A bad answer is "I'd rewrite the whole thing" or "I don't know."

**Section boundary:** This is Lesson 2 — a section boundary. After both checks pass, go to Phase E (Close) and deliver the restart phrasing from PERSONA.md.
