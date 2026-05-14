# Lesson 5 — Common Mistakes

<!-- Source: Lesson 3.3.md -->

## Brief

What You'll Get From This

The seven mistakes people make most often when setting up the folder architecture, and how to fix each one before it wastes your time.



The Lesson

Every one of these comes from real community members. People post their setups, run into walls, and ask for help. The same problems show up over and over. If you read this before you finalize your structure from 3.2, you will skip most of them.



Mistake 1: Making the CLAUDE.md too long

The CLAUDE.md is a routing file. It tells Claude where things are and where to go. That is its job. It is not a project brief. It is not a style guide. It is not a brain dump of everything you want Claude to know.

When the CLAUDE.md gets too long, two things happen. First, Claude burns tokens reading information that is not relevant to the current task. Second, the signal gets buried in noise. The routing instructions (the part that actually matters) get lost in paragraphs of background context.

The fix: Your CLAUDE.md should fit on one screen. Identity, folder structure, routing table, naming conventions. That is it. Everything else belongs in a workspace CONTEXT.md where it only gets loaded when Claude is actually working in that area. If your CLAUDE.md is longer than 40-50 lines, you have context files hiding inside it. Pull them out.



Mistake 2: Skipping the routing table

Some people set up the folders, write the context files, and never put a routing table in the CLAUDE.md. They assume Claude will figure it out.

Sometimes Claude does figure it out. But "sometimes" is the problem. Without a routing table, Claude has to guess which files to read and which to skip. It might read everything (wasting tokens) or read the wrong context file (getting confused about what workspace it is in). The output gets inconsistent. Some responses are great, some are off, and you cannot tell why.

The fix: The routing table does not need to be complicated. Three columns: task, where to go, what to read. One row per type of work. Claude reads the table, matches the task, goes to the right place. Every time.

| Task | Go to | Read |
|------|-------|------|
| Write content | /script-lab | CONTEXT.md |
| Build something | /production | CONTEXT.md |
| Publish or schedule | /distribution | CONTEXT.md |


If you added skills (Layer 3), add a fourth column. Otherwise, three is enough.



Mistake 3: Too many workspaces

Someone sets up eight workspaces for a project that really only has two or three modes of work. They have a workspace for research, a workspace for notes, a workspace for drafts, a workspace for editing, a workspace for final review, a workspace for publishing. Each one has its own CONTEXT.md. The CLAUDE.md has a routing table with twelve rows.

Now the overhead of maintaining the system is bigger than the work itself. Context files go stale. Claude spends more time navigating between workspaces than working in them. The whole point of the architecture was to reduce complexity, and instead it multiplied it.

The fix: Start with two or three workspaces. You can always add more. The question to ask: "Do I shift mental modes between these tasks?" Writing and building are different mental modes. That is two workspaces. Drafting and editing are the same mental mode at different stages. That is one workspace with a process inside it, not two workspaces.

If you are not sure whether something deserves its own workspace, it does not. Keep it as a subfolder inside an existing workspace. You can always split it out later if the work grows.



Mistake 4: Writing context files that describe what AI should be instead of what the work is

This one is subtle. People write context files full of instructions about Claude's personality. "Be creative. Be concise. Be professional. Think step by step. Use a warm tone." They spend 30 lines describing how Claude should behave and two lines describing the actual project.

Claude responds to context about the work far more than context about itself. Telling Claude "you are a senior copywriter" gives it a role. Telling Claude "the audience is mid-market HR directors who have tried three other tools and are skeptical of AI claims" gives it something to actually work with. The second one changes the output more than the first.

The fix: Flip the ratio. Spend 80% of your context file describing the work: what the project is, who the audience is, what has already been done, what good output looks like, what to avoid. Spend 20% or less on behavioral instructions. If your context file reads like a personality quiz, rewrite it. If it reads like a project brief that a new team member could pick up and start working from, you are in the right place.



Mistake 5: Never updating the context files

Someone sets up the folder in week one. Writes the context files. Gets great results for two weeks. Then the project evolves. New requirements, new direction, new constraints. But the context files still say what they said on day one. The output starts drifting. Claude is still working from old context. The member thinks Claude "got worse" when really Claude is doing exactly what the context tells it to do. The context is just stale.

The fix: Treat context files like working notes. When the project changes, edit the context. When you learn something new about what Claude needs to know, add it. When a constraint no longer applies, remove it. This takes 30 seconds per edit. It is the single highest-leverage habit in the whole system.

Some people add a "Last updated" line at the top of each context file. Simple but effective. When you open a workspace and see "Last updated: six weeks ago," you know to review it before working.



Mistake 6: Putting everything in one folder and hoping the CLAUDE.md sorts it out

The opposite of too many workspaces. Everything lives in one flat directory. Fifty files. No subfolders. The CLAUDE.md tries to route between them using file names alone. Claude reads the whole directory listing, picks what it thinks is relevant, and often picks wrong.

This is the equivalent of dumping every document on one desk and asking someone to find the right one. They can do it. It just takes longer, they make more mistakes, and they get frustrated.

The fix: If you have more than 8-10 files at the same level, you need subfolders. Group by workspace (what kind of work), then by stage or type within the workspace. The folder structure is the architecture. It tells Claude what belongs together. Let it do that job.



Mistake 7: Building the whole system before using it

The most common mistake. Someone reads 3.1 and 3.2, gets inspired, and spends an entire weekend building a perfect folder architecture with six workspaces, detailed context files, naming conventions, skills wired into every workspace, and a routing table with twenty rows. They have not used Claude once during this process. They built the factory without ever making a product.

Then they start using it and realize half the decisions they made do not match how they actually work. The workspace boundaries are wrong. The context files describe what they thought they would need, not what they actually need. They have to rebuild.

The fix: Build the minimum. One CLAUDE.md, one or two workspaces, one CONTEXT.md per workspace. Start working. After a few days, you will know what is missing. Add it then. After a week, you will know what is wrong. Fix it then.

The best folder setups in the community were all built incrementally. They started simple and grew based on real work. The ones that stalled were the ones that tried to be complete before day one.

Your first version should take 15 minutes. If it took longer, you over-built.



The pattern across all seven

If you look at these together, they all point in the same direction. Keep the system small. Keep it focused on the work, not on Claude. Update it as you go. Let the structure grow from use, not from planning.

The folder architecture is powerful because it is simple. Folders and text files. The moment it starts feeling heavy or complicated, something went wrong. Go back to the three layers from 3.1: map, rooms, tools. If your CLAUDE.md is the map, your context files are the rooms, and your skills are the tools, and each one is doing only its job, the system stays clean.

---

## Build

<!-- Runtime instructions for Claude — not prose delivered to the user -->

The user audits their own workspace from Lessons 3.1 and 3.2 against all seven mistakes. Walk through each mistake one at a time.

**For each of the seven mistakes:**
- Read the mistake description (chunk it — 1-2 mistakes per turn).
- After each: "Does your setup have this problem? Open your CLAUDE.md or CONTEXT.md and tell me what you see."
- If they find an issue, help them fix it before moving to the next mistake.

**Step 1: Mistakes 1 and 2 — Length and routing table.**
- Check their CLAUDE.md line count. If over 50, identify what to move to a CONTEXT.md.
- Check for routing table. If missing, add one together.

**Step 2: Mistake 3 — Too many workspaces.**
- Ask how many workspaces they have. If more than 3-4 for a solo workflow, discuss which could be collapsed.

**Step 3: Mistake 4 — AI personality vs. work description.**
- Have them read back their CONTEXT.md. Ask: "What percentage of this is about what Claude should be, and what percentage is about the actual work?"
- If the ratio is off, help them rewrite toward describing the work.

**Step 4: Mistake 5 — Stale context files.**
- Instruction: "Add a 'Last updated: [today's date]' line to the top of your CONTEXT.md. It's a habit worth starting now."

**Step 5: Mistake 6 — Everything in one folder.**
- Ask them to count files at the root level. If over 10, identify what should move into subfolders.

**Step 6: Mistake 7 — Building before using.**
- Reflection question: "Have you actually used this workspace for real work yet, or are you still setting it up?" If they haven't used it — that's the assignment: use it for something real today.

**Step 7: Write self-audit.md.**
- Instruction: "Now create a file called `self-audit.md` in your workspace. One line per mistake. Format:

```
Mistake 1 (CLAUDE.md too long): [fine / needs fix / fixed]
Mistake 2 (no routing table): [fine / needs fix / fixed]
Mistake 3 (too many workspaces): [fine / needs fix / fixed]
Mistake 4 (AI personality vs work): [fine / needs fix / fixed]
Mistake 5 (stale context files): [fine / needs fix / fixed]
Mistake 6 (everything in one folder): [fine / needs fix / fixed]
Mistake 7 (built before using): [fine / needs fix / fixed]
```

Fill in your honest assessment. Tell me when it's saved."

- Inspect: Read the self-audit.md. Confirm all seven entries are there with a status.

**Artifact:** `[user-named-folder]/self-audit.md`

---

## Check-in

<!-- Runtime instructions for Claude -->

1. Inspect `[user-named-folder]/self-audit.md` — verify all seven mistakes are listed with a status (fine / needs fix / fixed). No blanks.

2. Ask: "Now that you've gone through all seven — which one is most likely to bite you if you're not paying attention? Which one feels like the hardest habit to keep?"

3. Record in `_tutor/progress.md`:
   - lesson: "05_common-mistakes"
   - artifacts_inspected: ["[path]/self-audit.md"]
   - comprehension.question: "Which of the seven mistakes is most likely to bite you if you're not paying attention? Which one feels like the hardest habit to keep?"
   - comprehension.answer: "[user's verbatim response]"
   - comprehension.pass: [true/false]

4. A good answer identifies a specific mistake and explains why it would be hard to avoid (e.g., "Mistake 5 — I'll forget to update context files because I don't have a trigger for it"). A bad answer is "all of them" or "I don't know."

**Section boundary:** This is Lesson 5 — a section boundary. After both checks pass, go to Phase E (Close) and deliver the restart phrasing from PERSONA.md.
