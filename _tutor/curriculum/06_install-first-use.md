# Lesson 4.1 — Install and First Use

<!-- Source: Lesson 4.1.md, 4.1 transcript video.md -->

## Brief

What You'll Get From This

All three Claude interfaces installed and working on your machine. A clear sense of when to use which one. And your first real task run on your own files.



The Lesson

How most people use Claude

Most people use Claude like a search engine that writes better sentences. You type a question, you get an answer, you copy and paste it somewhere. That works. But it is like using a car to check the mailbox. The car can take you across the country. You just have not left the driveway yet.

Today we leave the driveway.



Three interfaces, one model

This is the thing most people miss. There are three ways to use Claude, and they are not three different AIs. It is one model with three different ways to access it. The difference is what each interface lets that model see and do.

Claude Desktop (or claude.ai)

The downloaded app or the website. A conversational tool. Great for planning, thinking through ideas, getting answers, building drafts. But there is a limit to what it can do at scale. It cannot see your files directly. It cannot run code. It cannot edit anything in your project. Everything goes through copy, paste, or uploads.

That is not because the model is limited. The model is extremely powerful. The problem is the interface. It just cannot reach your stuff. If you have ever felt like Claude kind of gets it but not quite, it is probably because you are working from a pasted excerpt instead of your actual project.

Claude Code in VS Code

This is what I use for almost everything. Your files are on the left. Claude is on the right. It reads your project, edits your files in line, runs commands. You do not copy and paste anything. You describe what you need and it works directly within the files.

VS Code (Visual Studio Code) is a coding environment made by Microsoft. If you have never opened it, do not worry. It is simpler than it looks and we will walk through setup. You do not need to know how to code. VS Code just lets you see your folders as a file tree and open documents without clicking through layers of windows.

If you are familiar with Cursor, Windsurf, Copilot, or Antigravity, those are all built on top of VS Code. They support different models and different processes. Some use Claude, some do not. This course is specifically for Claude's tools inside the Anthropic environment.

Claude Code in the terminal

The same engine under the hood, just a different wrapper. The terminal version is better for when your work does not live in a code project. Processing a folder of documents. Managing files. Cleaning up your downloads folder. Anything where you just need Claude to read a bunch of files and do something with them.

You do not need the terminal version to get value from this course. But if you are already comfortable in the terminal, it is faster for some jobs.



The real difference

The desktop is a conversation layer. VS Code is an editor layer. The terminal is a command line layer. Same brain behind all three.

Interface Best for Can see your files? Can edit your files? Claude Desktop / claude.ai Thinking, planning, quick questions, drafting Only if you upload them No Claude Code in VS Code Building, editing, working inside a project Yes, automatically Yes Claude Code in terminal File processing, quick tasks, non-code projects Yes, in the current folder Yes



Installing everything

Let's get all three working.

Step 1: Claude Desktop

If you do not have it already:

Go to claude.ai/download and download the app for your OS (Mac or Windows). Install it. Sign in with your Claude account.

That is it. You now have the conversational interface.

Step 2: Node.js

You need Node.js before you can install Claude Code. Node.js lets you run JavaScript on your computer and gives you access to the npm command for installing packages.

Go to nodejs.org and download the LTS version. Run the installer.

To verify it worked, open your terminal and type:

node --version


If you see a version number, you are good.

Step 3: Claude Code (terminal)

With Node.js installed, run this command in your terminal:

npm install -g @anthropic-ai/claude-code


Once it finishes, you can type claude in any folder and Claude Code will launch.

<!-- From transcript: 4.1 transcript video.md — Windows architecture check, load-bearing install detail -->
Important for Windows users: Before downloading Claude Desktop, check your architecture. Open Settings → System → About → "System type." You need to know whether you are running x64 (standard) or ARM64. Download the matching version. Installing the wrong version causes problems that are hard to diagnose. Check first, then download.
<!-- End transcript -->

Step 4: Claude Code in VS Code

First, install VS Code if you do not have it:

Go to code.visualstudio.com and download it. Install it. Open it.

Then install the Claude Code extension:




In VS Code, look for the Extensions icon in the left sidebar (the one with squares, one slightly tilted). Or press Ctrl+Shift+X (Windows/Linux) or Cmd+Shift+X (Mac).



Search for "Claude Code"



Click the blue Install button



You may need to restart VS Code

You should now see the Claude Code icon in your sidebar. Click on any file to open a page, then the Claude panel will be available.

One thing that trips people up: When you open a brand new folder in VS Code and nothing is there, the Claude panel might not appear. You need to click on a file or have a page open for the extension to activate. Also, VS Code has its own built-in chat that is separate from Claude Code. Make sure you are using the Claude Code extension, not the VS Code native chat.



Troubleshooting

"npm: command not found" — Node.js did not install correctly. Close your terminal completely, reopen it, and try again. If it still fails, reinstall Node.js.

"Permission denied" during npm install — On Mac/Linux, try: sudo npm install -g @anthropic-ai/claude-code

Claude Code launches but asks for authentication — Follow the link it gives you to sign in. You need a Pro or Max subscription.

VS Code extension does not show Claude panel — Make sure you clicked Install, restarted VS Code, and have a file open. Check that you are using the Claude Code extension, not VS Code's built-in chat.

If you get stuck on any of this, post in the community or Discord with your OS and the error message. Someone has hit the same wall.

---

## Build

<!-- Runtime instructions for Claude — not prose delivered to the user -->

Reframe: the user is already using Claude Code — they're here right now. This lesson is about verifying their setup, not doing a fresh install from scratch.

Start with this reframe: "You already have Claude Code running — you're using it right now. This lesson is about making sure everything is set up correctly and filling in any gaps you may have skipped. Let's verify your setup."

**Step 1: Architecture check (Windows users).**
- Instruction: "First — are you on Windows or Mac?"
  - If Windows: "Go to Settings → System → About → System type. Tell me whether it says x64 or ARM64."
  - If Mac: "You're fine — no architecture check needed on Mac. Skip to Step 2."
- Note what they report.

**Step 2: Verify Claude Code version.**
- Instruction: "Open a terminal (separate from this session). Type: `claude --version`. Tell me what you see."
- Inspect: Note the version number. If they get an error, troubleshoot before continuing.

**Step 3: Verify VS Code extension.**
- Instruction: "Is Claude showing up in the VS Code sidebar, or are you running Claude Code from the terminal? Tell me how you're currently set up."
- Note what they report.

**Step 4: Write setup-verified.md.**
- Instruction: "Create a file called `setup-verified.md` in your workspace folder. Fill it in with what you just found:

```
# Setup Verified

Platform: [Mac / Windows]
Architecture: [x64 / ARM64 / N/A for Mac]
Claude Code version: [version number]
Interface: [VS Code extension / Terminal / Both]
Date verified: [today's date]
```

Save it. Tell me when it's done."

- Inspect: Read the file. Confirm it has real data (not placeholder text) and the platform/architecture fields are filled in.

**Artifact:** `[user-named-folder]/setup-verified.md`

---

## Check-in

<!-- Runtime instructions for Claude -->

1. Inspect `[user-named-folder]/setup-verified.md` — verify all five fields are filled with real data. No placeholder text.

2. Ask: "You've got three interfaces available — Desktop, VS Code, Terminal. Based on the kind of work you described in your workspace setup, which one do you think you'll use most, and for what?"

3. Record in `_tutor/progress.md`:
   - lesson: "06_install-first-use"
   - artifacts_inspected: ["[path]/setup-verified.md"]
   - comprehension.question: "You've got three interfaces available — Desktop, VS Code, Terminal. Based on your work, which one will you use most, and for what?"
   - comprehension.answer: "[user's verbatim response]"
   - comprehension.pass: [true/false]

4. A good answer names a specific interface and a specific use case that fits their work. A bad answer is generic ("I'll use them all for different things") without naming what those things are.
