# Lesson 3 — Full Walkthrough

<!-- Source: Lesson 3.1.md, 3.1 transcript video.md -->

## Brief

What You'll Get From This

A working folder system that tells Claude where it is, what to do, and where to put the work. Three layers. Plain English. No code, no frameworks, no agents.



The Lesson

The problem with how most people use AI

Right now, most people open Claude or ChatGPT, type something, get a response, and start over. Maybe they save a good prompt somewhere and paste it in again next time. Maybe they hit the token limit and have to start a new conversation. Maybe they spend half the message just re-explaining who they are and what they are working on.

That works for quick questions. It falls apart the moment you try to do real, ongoing work. You are burning tokens on stuff that does not matter. You cannot edit what the AI produces at each step. And every conversation starts from zero.

The folder structure fixes all of that.



What tokens are and why this matters

Before we get into the structure, you need to understand one thing: tokens.

A token is roughly three quarters of a word. Sometimes a single word. Sometimes a long word like "hamburger" is three tokens. The term comes from NLP research in the 1990s. Researchers needed a unit smaller than a word because language does not break the same way across every language. They borrowed "token" from linguistics, which borrowed it from old English "taken," meaning a sign or a symbol. A token is just the smallest meaningful chunk of a sentence.

There are only so many tokens an AI can hold in its context window before it starts failing. When people say "context window," they mean how many tokens the AI can see at once. That window is finite.

So if you dump everything into one conversation, an AI writing a blog post is also reading your video production notes. You are wasting tokens on information that has nothing to do with the task. The folder structure solves this by separating your work into areas and only loading what is needed for the task at hand.



The workspace blueprint: three workspaces for three kinds of work

Here is the concept. Instead of one giant conversation or one massive file, you break your work into separate workspaces. Each workspace handles a different kind of work.

For example:




Community — content, docs, community management



Production — scripts, animations, code, builds



Writing Room — blog posts, newsletters, thinking, client work

These are just examples. Your workspaces will look different depending on what you do. A freelancer might have Client Intake, Delivery, and Admin. A developer might have Frontend, Backend, and Docs. The names change. The structure stays the same.



The three layer routing system

This is the core of the whole thing. Three layers. Each one has a job.

Layer 1: The Map (CLAUDE.md)

This is the top-level file. It sits at the root of your project folder. Every time Claude enters this workspace, it reads this file first.

Think of it as the floor plan. You walk into any building, the floor plan is on the wall, and you know where to go. The CLAUDE.md file tells the AI:




What this project is



What the folder structure looks like



Naming conventions for files



Where things go

This is the most important pattern in the whole system. Inside it, you put a simple table that tells the AI: for this task, read these files, skip those files, you might need these skills.

Without this, the AI either reads everything and wastes tokens, guesses wrong about what matters, or produces work you cannot edit along the way. This table eliminates all of those problems.



<!-- From transcript: 3.1 transcript video.md -->
Layer 2: The Rooms (Workspace Context Files)

Each workspace has its own context file. When you tell Claude to work in the Writing Room, it reads the Writing Room context file. When you are in Production, it reads the Production context file. It only loads what it needs for where it is.

These context files describe:




What this workspace is for



What the process looks like (first I do this, then I do that)



What files are in here and how they are organized



What skills or tools to use in this workspace

You can write these by hand or have Claude help you write them. They are plain English. Short documents. A few paragraphs.

You can see what happens with almost no prompting at all. You say "go to writing room, let's start making something" and the AI immediately reads the context file, understands the workspace, loads the right voice and style, and asks what you want to build. One prompt. That is the power of Layer 2.
<!-- End transcript -->

Layer 3: The Tools (Skills, MCP Servers, and Plug-and-Play)

Layer 3 is where skills and tools live. Skills are processes that someone figured out and packaged into a set of files that tell Claude how to do a specific thing. A PowerPoint skill. A humanizer skill. A doc co-authoring skill.

The key here: you do not load every skill into every workspace. You wire skills into the workspaces where they are needed. Your Production workspace might reference a front-end design skill and a web app testing skill. Your Writing Room might reference a humanizer skill and a doc co-authoring skill.

You can reference 15, 20, or 100 skills in a project, but each workspace only loads the ones it needs. That is the plug-and-play idea. And if you need Claude to find a new skill or create one, you can wire that ability in too.



<!-- From transcript: 3.1 transcript video.md -->
Naming conventions that replace databases

One more thing that makes this system work without any code or databases. In your CLAUDE.md, you add naming conventions.

If a blog draft is created, it gets named like: api-auth-guide_draft.md If it is a newsletter, it gets named like: 2026-03-launch-week.md If it is a demo script version 2, it gets named like: demo_v2.md

The AI knows how to find, organize, and move files because the naming tells it everything. You can say "pull my demo v2 and build a spec from it" and Claude knows exactly where to look, what to pull, and what to do next. No SQL. No vector database. No Python injection. Just naming conventions.

The folder becomes your app. This is your UI. What simpler UI than a folder?
<!-- End transcript -->



How to make this yours

The template in the video uses a fake project with fake blog posts and demo scripts. That is intentional. You swap the names and rewrite the context files for your own work. The layers stay the same.

If you are a content creator:




Writing Room → Script Lab



Production → Edit Bay



Community → Distribution Hub

If you are a freelancer:




Swap workspaces for: Client Intake, Delivery, Admin



Your context files describe your client process instead of content production

If you are a developer:




Swap workspaces for: Frontend, Backend, Docs



Wire in the skills you actually use (testing, deployment, code review)

The three-layer routing system (map → rooms → tools) works the same way no matter what you do. You change the labels and the context. The architecture holds.

---

## Build

<!-- Runtime instructions for Claude — not prose delivered to the user -->

This is the densest lesson. Three sequential sub-builds. Run each one, do the mini check, then move to the next.

**Sub-build 1 — The Map (CLAUDE.md)**

- Instruction: "Let's start with Layer 1 — the Map. You already have a CLAUDE.md from Lesson 1. We're going to update it to include a routing table. Open it. Here's the structure to add:

```
# [Your Project Name]

## Folder Structure
- /[workspace-1] — [what you do here]
- /[workspace-2] — [what you do here]

## Routing
| Task | Go to | Read |
|------|-------|------|
| [task type 1] | /[workspace-1] | CONTEXT.md |
| [task type 2] | /[workspace-2] | CONTEXT.md |

## Naming conventions
- Drafts: topic-name_draft.md
- Final: topic-name_final.md
```

Replace the placeholders with your actual work areas. Tell me when it's saved."

- Inspect: Read the updated CLAUDE.md. Confirm it has a routing table with at least one row and at least one workspace listed.
- **Mini check:** "In your own words — what does the Map do? What would happen if it wasn't there?"

**Sub-build 2 — A Room (one workspace folder + CONTEXT.md)**

- Instruction: "Now Layer 2 — one Room. Create one workspace folder relevant to your actual work. Inside it, create a CONTEXT.md file. Here's what to put in it:

```
# [Workspace Name]

## What this workspace is for
[2-3 sentences describing the kind of work that happens here]

## Process
[How you work in this space — first I do X, then Y, then Z]

## What files live here
[Describe the types of files and how they're named]
```

Fill it in for your real work. Tell me when it's saved and give me the path."

- Inspect: Read the CONTEXT.md they created. Confirm it describes actual work, not just placeholders.
- **Mini check:** "What makes this Room different from just having the files in the root folder?"

**Sub-build 3 — A Tool (Layer 3 example)**

- Instruction: "Layer 3 is where skills and tools plug in. You don't need to wire anything in right now — but let's note where they'd go. In your CLAUDE.md routing table, add a Skills column. Even if it says '—' for now, the column should be there.

| Task | Go to | Read | Skills |
|------|-------|------|--------|
| [task] | /[workspace] | CONTEXT.md | — |

Tell me when it's updated."

- Inspect: Confirm the routing table in CLAUDE.md has a Skills column.

**Artifacts:**
- `[user-named-folder]/CLAUDE.md` (updated with routing table)
- `[user-named-folder]/[workspace-name]/CONTEXT.md`

---

## Check-in

<!-- Runtime instructions for Claude -->

1. Inspect both artifacts:
   - `CLAUDE.md`: routing table present with at least one workspace row and a Skills column.
   - `[workspace]/CONTEXT.md`: describes actual work, not placeholder text.

2. Ask: "You've got Map, Room, and a placeholder for Tools. If you were going to actually use this for your real work starting tomorrow — what would you change or add first?"

3. Record in `_tutor/progress.md`:
   - lesson: "03_full-walkthrough"
   - artifacts_inspected: ["[path]/CLAUDE.md", "[path]/[workspace]/CONTEXT.md"]
   - comprehension.question: "You've got Map, Room, and a placeholder for Tools. If you were going to actually use this for your real work starting tomorrow — what would you change or add first?"
   - comprehension.answer: "[user's verbatim response]"
   - comprehension.pass: [true/false]

4. A good answer shows they understand the system well enough to extend it — they'd add another workspace, write more specific context, name real file types. A bad answer is "I don't know" or a repeat of the lesson content.
