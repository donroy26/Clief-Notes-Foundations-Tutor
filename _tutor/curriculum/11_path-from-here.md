# Lesson 11 — Your Path From Here

<!-- Source: Lesson 5.1.md -->

## Brief

What You'll Get From This

A clear picture of where to go next based on what you want to build.



You finished The Foundation.

You have tools installed (1.1), a folder system that gives Claude context (1.2), a prompting framework (1.3), six videos explaining the ideas underneath all of it (Section 2), the full folder architecture (Section 3), and Claude Code running on your machine (Section 4).

That is a working system. Everything from here builds on it.



Level 2 — Implementation Playbooks

Unlock by engaging in the community. Hands-on courses where you build real projects.

Building Animations The full pipeline for creating video animations with Claude Code and Remotion. Script to spec to build to render. Four lessons including a community challenge.

The Ultimate Browser (Claude Extension) Claude running inside Chrome. Pull data from any page, teach Claude your workflows, automate inbox and scheduling. Four lessons with real use cases.



Level 3 — Building Your Stack

For members who have built with Level 2 and want to push further.

Custom UI for Claude (or Other AI) Build your own front-end interface for Claude. The build process, Claude Code in action, scoping your design, and open-source references to study.

Remote Access for Claude Want to control your Claude Code on your Desktop from your phone? This course teaches you how.



Premium — The Vault ($27/month)

Every downloadable asset in the community. Two structured courses. Discord access.

The Library:




Workspace Blueprint (full production folder template with routing tables and context files)



Production CLAUDE.md examples for different use cases



Folder Organization Guide



Prompting Framework Guide (one-page reference)



Animation spec templates



Workflow starter packs (content pipeline, consulting, development)



Claude Skills Manual + Resource Index



New resources added weekly

Courses:




The 60/30/10 Framework — The business methodology for deciding where AI fits. Real case studies.



Building Your First Workflow End to End — From folder structure to working multi-step system.

Community:




Discord access (Premium channels)



Premium discussion threads

Free content teaches the ideas. Premium gives you the assets, the templates, and the guided builds to apply them.



VIP — The Drawing Room ($97/month)

Personal access. Everything in Premium plus three things:

Afternoon Tea Live sessions every two weeks. Bring your project, your problem, your build. Small group. We work through it together.

Bespoke Builds Fill out the questionnaire. I build a custom folder setup or workflow designed for your specific work. Your context, your use case, your system.

Discord: Drawing Room Channels Smaller. More direct. Async access between sessions.

The Drawing Room is not a content library. You are paying for proximity and personal attention. You show up, you get help, you build.



Not sure which path?

I want to... Start here Build animations or video content → Level 2: Building Animations Automate browser tasks → Level 2: The Ultimate Browser Build my own AI interface → Level 3: Custom UI Get templates, assets, and structured courses → Premium: The Vault Get live help on my specific project from Jake → VIP: The Drawing Room

Keep learning for free → Go back through Sections 1-4 and do every check-in. Engage in the community. Level 2 unlocks with participation.

---

## Build

<!-- Runtime instructions for Claude — not prose delivered to the user -->

This is the final lesson. The build is a planning document — the user writes, in their own words, where they are going next.

**Step 1: Take stock.**
- Instruction: "Before we write anything — let's see what you've built across these 11 lessons. Tell me:
  - What's the folder structure you have now?
  - What's one thing you understand about working with Claude that you didn't understand before?
  - What's one thing you'd build or do differently now compared to when you started?"

- Listen to their answers. Acknowledge what they've accomplished.

**Step 2: Pick a path.**
- Instruction: "Looking at the paths in this lesson — Level 2, Level 3, Premium, or just continuing with the free content — which one fits where you want to go? Or is it something not on the list?

Don't give me the 'official' answer. Tell me what you actually want to build or figure out next."

- Wait for their answer.

**Step 3: Write path_forward.md.**
- Instruction: "Now write it down. Create a file called `path_forward.md` in your workspace. In your own words — not copied from the lesson — answer three questions:
  1. What do you understand now that you didn't before? (One or two sentences.)
  2. What does your current folder/workspace setup look like?
  3. What are you going to do with this next?

This is for you, not for me. Be honest about what you actually want.

Tell me when it's saved."

- Inspect: Read the file. Confirm it's in their own words — specific, honest, not a copy of the lesson content.

**Artifact:** `[user-named-folder]/path_forward.md`

---

## Check-in

<!-- Runtime instructions for Claude — FINAL GATE -->

1. Inspect `[user-named-folder]/path_forward.md` — verify it's written in their own words and answers all three questions with specifics.

2. **Gate questions — both must pass before this lesson is marked complete:**

   **Gate question 1:** "In your own words — not the vocabulary from the lesson — describe the three-layer architecture from Section 3. What is it, and what does each layer do?"
   
   Expected: They describe Map / Rooms / Tools (or equivalent plain-language concepts) without being prompted. They do not need to use those exact words. They need to demonstrate that they understand the system.

   **Gate question 2:** "In your own words, describe the five-part prompting framework from Lesson 2. What are the parts and why does each one matter?"
   
   Expected: They can name and explain Identity / Task / Context / Constraints / Output Format (or equivalent). Again, exact vocabulary is not required — understanding is.

   **If either gate question fails:**
   Do not pass the lesson. Tell the user: "I want to make sure this landed before we wrap up. Let's go back over [the part they couldn't explain]. Which part is fuzzy?"
   
   Work through it with them. Try again. If after two passes they still cannot articulate both concepts in their own words — this is Stop Condition 3 from the work order. Surface to the human owner. Do not ship.

3. Record in `_tutor/progress.md`:
   - lesson: "11_path-from-here"
   - artifacts_inspected: ["[path]/path_forward.md"]
   - comprehension.question: "Describe the three-layer architecture and the five-part prompting framework in your own words."
   - comprehension.answer: "[user's verbatim response — record both gate answers]"
   - comprehension.pass: [true only if BOTH gate questions pass]

4. **If both gates pass:** Update `current_lesson` in progress.md to `"complete"`. Deliver a close that acknowledges the full arc of what they built. Then: "Happy learning."
