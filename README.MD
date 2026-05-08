# Cursor IDE Setup – Portfolio Task

## What this project is about

This is a documentation of how I set up my development environment using Cursor IDE, Claude Code, and OpenAI Codex.  
Instead of just listing steps, I also included the issues I ran into and how I worked through them using research and troubleshooting.

The goal was to simulate a real-world setup process where things don’t always work on the first try.

---

## Tools I ended up using

- Cursor IDE
- Claude Code (extension + CLI via npm)
- OpenAI Codex (Cursor extension)
- Node.js
- Git for Windows
- GitHub (repo + version control)

---

## What I did

### Cursor setup
I started by installing Cursor IDE and logging in. At first, I wasn’t fully familiar with its extension system, so I had to explore the interface a bit.

Since I’ve used VS Code before, I naturally tried `Ctrl + Shift + X`, which luckily also works in Cursor and opened the extensions panel.

---

### Claude Code extension
I installed the Claude Code extension by Anthropic.

Login was where I first hit a limitation:
- Claude.ai login required a Pro subscription
- I also tried Anthropic Console login, which worked partially, but access was limited due to low credits

At this point, I noted that while installation worked, actual usage depends on account access.

---

### Claude Code CLI (terminal setup)

Since I wanted to test the CLI version as well, I installed Node.js (fresh install on my machine).

Then I installed Claude CLI globally:

```bash
npm install -g @anthropic-ai/claude-code
```

When I tried running `claude`, I ran into this issue:

> PowerShell script execution is disabled on this system

After some research, I found that this is caused by Windows PowerShell security settings. I fixed it using:

```powershell
Set-ExecutionPolicy -Scope CurrentUser RemoteSigned
```

After that, the `claude` command started working properly.

However, login still required a Pro account / credits, so I couldn’t fully use it beyond setup.

---

### OpenAI Codex setup

Next, I installed the Codex extension in Cursor.

Login was a bit different here:
- Phone verification via WhatsApp was not an option for me
- So I switched to API key authentication instead

I generated an API key from OpenAI’s platform and used that to successfully log in.

---

### GitHub setup

I created a public GitHub repository and cloned it into Cursor.

After opening it in the editor, I created this `README.md` file directly in the project and committed everything through Git.

---

## Issues I ran into (and how I handled them)

### 1. Cursor extension unfamiliarity
I initially wasn’t sure where extensions were located, so I explored the UI and used my VS Code experience to find the correct panel.

---

### 2. PowerShell execution policy
Claude CLI wouldn’t run because PowerShell was blocking scripts.

Fix:
```powershell
Set-ExecutionPolicy -Scope CurrentUser RemoteSigned
```

---

### 3. Claude login limitations
Even after setup, full usage was blocked due to subscription / credit limitations.

---

### 4. Codex login method change
WhatsApp verification wasn’t available, so I switched to API key authentication instead.

---

## What I learned from this

Most of the setup wasn’t just “install and done” — it involved:
- figuring out unfamiliar tools
- reading documentation
- fixing environment issues on Windows
- switching authentication methods when needed

A lot of the work was really about troubleshooting rather than just installation.

---

## Final result

In the end, I was able to:

- Set up Cursor IDE successfully
- Install and configure Claude Code (CLI + extension)
- Install and log into Codex using API key
- Resolve PowerShell and environment issues
- Use Git and GitHub for version control
- Document everything in a structured way inside a repository