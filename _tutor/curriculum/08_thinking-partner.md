# Lesson 4.3 — Claude Desktop as Thinking Partner

<!-- Source: Lesson 4.3.md -->

## Brief

What You'll Get From This

You will stop using Claude Desktop like a vending machine and start using it as a thinking partner. You will work through a real problem, find an insight you did not have before, and understand when to think in Desktop and when to build in Code.



The Lesson

The mistake

Most people use Claude Desktop like a vending machine. Question in, answer out. "Write me a marketing plan." Claude gives you a document. You paste it somewhere. Done.

That works for simple tasks. But it wastes the most powerful thing Claude can do: think with you.

There is a difference between prompting for content and prompting for thinking.

Prompting for content: "Write me a marketing plan." You get a document. It might be good. It might be generic. You will not know until you read it and by then you have already spent the tokens.

Prompting for thinking: "I am trying to reach [audience] with [constraint]. What am I not seeing?" You get clarity. You get your own assumptions challenged. You get the blind spots surfaced before you build anything.



What Desktop excels at

Claude Desktop (the conversational interface) is the best tool for:




Challenging your assumptions



Finding blind spots in your plan



Pressure-testing ideas before you commit



Structuring messy thinking into something clear



Exploring trade-offs between options

None of these require Claude to touch your files. They require Claude to think alongside you. The chat interface is built for exactly this.



Planning, then execution

Here is the workflow that saves the most time.

Without planning: You open Claude Code and start building. Halfway through you realize you are not sure what you actually want. You restart. You try a different approach. You restart again. Three restarts. Two hours.

With planning: You open Claude Desktop and spend 15 minutes thinking through the problem. What are you building? Who is it for? What does success look like? What are the trade-offs? You get clear. Then you open Claude Code and build it. One build. 30 minutes.

The 15 minutes of thinking saves 90 minutes of building the wrong thing. Desktop for decisions. Code for execution.



Desktop Projects

Claude Desktop has a feature called Projects. You can give a Project your key documents, preferences, or background material. Every conversation you start inside that Project has that context already loaded.

This is the lightest version of "giving AI context about your work." If you did 1.2: Your First Folder, you already understand the concept. Projects are the browser-based version of the same idea: persistent context that stays across conversations.

Think of Projects as the seed for what comes next in Session 4. They give Claude background. Session 4 (CLAUDE.md) gives Claude deep project understanding.



Tips

Desktop for decisions. Code for execution. If you are deciding what to build, use Desktop. If you are building it, use Code. If you try to decide and build at the same time, both suffer.

Start with what you are trying to accomplish, not what you want Claude to produce. "I need a marketing plan" is a product request. "I am trying to get 50 signups for a workshop in two weeks with no ad budget" is a problem. Claude is a better thinking partner when it knows the problem.

Push back on the first answer. "What is wrong with this?" "What am I missing?" "What would someone who disagrees with this say?" The first answer is often the obvious one. The second and third answers are where the value lives.

Conversations are disposable. The thinking is not. Do not treat a Claude conversation like a document to save. Treat it like a whiteboard session. The value is the insight you walk away with, not the transcript.

---

## Build

<!-- Runtime instructions for Claude — not prose delivered to the user -->

The artifact for this lesson is a thinking-partner prompt written in the five-part format from Lesson 1.3.

**Step 1: Identify a real problem.**
- Instruction: "Pick a real problem or decision you have been sitting on — something you have been putting off or going back and forth on. What is it?"
- Wait for their answer. If they say "I don't have one" — ask: "Is there anything in your work where you keep second-guessing the direction? Or something you're about to start that you're not 100% sure about?"

**Step 2: Run a thinking session.**
- Instruction: "Now let's run the thinking session. Here's how to structure the prompt — use the five-part framework from Lesson 1.3:

Identity: You are a strategic advisor helping me think through a decision.
Task: Help me identify what I'm not seeing about [your problem].
Context: [describe the problem, the stakes, what you've already considered]
Constraints: Don't solve it for me. Ask questions or identify blind spots. Push back on my assumptions.
Output Format: Give me 2-3 questions I haven't asked myself yet, then identify the one assumption I might be most wrong about.

Run this in Claude Desktop (or right here). Come back with: what was the key insight or question you didn't have before?"

- Wait for their report.

**Step 3: Write the prompt as a file.**
- Instruction: "Now write up that thinking-partner prompt as a reusable file. Save it as `prompts/thinking-partner.md` in your workspace. Use the five-part format — you'll want to customize the Task and Context for your real work, but keep the constraint ('don't solve it for me') and the output format.

Tell me the path when it's saved."

- Inspect: Read the file. Confirm it follows the five-part structure and is specific enough to be useful (not just a copy of the template with no customization).

**Artifact:** `[user-named-folder]/prompts/thinking-partner.md`

---

## Check-in

<!-- Runtime instructions for Claude -->

1. Inspect `[user-named-folder]/prompts/thinking-partner.md` — verify it uses the five-part format and the Task/Context are specific to the user's actual work (not generic placeholders).

2. Ask: "You've now used Claude for both execution (Code) and thinking (Desktop). What's a situation in your work where you'd reach for the thinking-partner prompt first, before opening Claude Code?"

3. Record in `_tutor/progress.md`:
   - lesson: "08_thinking-partner"
   - artifacts_inspected: ["[path]/prompts/thinking-partner.md"]
   - comprehension.question: "What's a situation in your work where you'd reach for the thinking-partner prompt first, before opening Claude Code?"
   - comprehension.answer: "[user's verbatim response]"
   - comprehension.pass: [true/false]

4. A good answer names a specific scenario where thinking comes before building — planning a new project, deciding between approaches, pressure-testing a strategy. A bad answer conflates thinking and building ("I'd use them together").
