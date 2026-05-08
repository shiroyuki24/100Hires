# Cursor IDE Portfolio Setup Task

## Overview
This project documents the installation and setup of Cursor IDE, Claude Code, and OpenAI Codex, along with troubleshooting steps encountered during the setup process. The goal was to demonstrate the ability to independently install developer tools, resolve environment issues, and follow documentation to complete a full setup workflow.

---

## Tools Installed

- Cursor IDE
- Claude Code (Anthropic extension + CLI)
- Codex (OpenAI extension)
- Node.js
- Git for Windows
- GitHub account + repository

---

## Steps Completed

### 1. Cursor IDE Setup
- Installed Cursor IDE from https://cursor.com/
- Logged into the application successfully
- Familiarized myself with the UI and extension system

### 2. Claude Code Extension Installation
- Initially unfamiliar with Cursor extensions
- Used prior VS Code knowledge (Ctrl + Shift + X) to open extensions panel
- Installed “Claude Code” by Anthropic
- Attempted login via:
  - Claude.ai subscription (required Pro access)
  - Anthropic Console login (partially successful but limited by credits)

---

### 3. Claude Code CLI Installation (Terminal Usage)
- Installed Node.js (system was newly formatted)
- Installed Claude CLI globally using:

```
npm install -g @anthropic-ai/claude-code
```

- Encountered issue:

> PowerShell script execution blocked due to security policy

- Resolved using:

```
Set-ExecutionPolicy -Scope CurrentUser RemoteSigned
```

- After fix, `claude` command worked successfully
- Login still required paid access / limited credits

---

### 4. Codex Extension Setup (OpenAI)
- Installed Codex extension in Cursor
- Attempted login via phone verification (WhatsApp method unavailable)
- Switched to API key authentication
- Generated API key via OpenAI platform
- Successfully logged into Codex using API key

---

### 5. GitHub Repository Setup
- Created public GitHub repository
- Cloned repository into Cursor
- Opened project folder inside IDE
- Created and edited `README.md`

---

## Issues Encountered & Solutions

### 1. Missing knowledge of Cursor extensions
- Researched how extensions work in Cursor
- Used experience from VS Code to navigate extension system

### 2. PowerShell execution policy error
- Claude CLI was blocked from running scripts
- Fixed using:
```
Set-ExecutionPolicy -Scope CurrentUser RemoteSigned
```

### 4. Claude Code login limitation
- Required Claude Pro / sufficient credits
- Logged in successfully but unable to fully use due to subscription limits

### 5. Codex login issue
- WhatsApp verification not available
- Resolved by using API key authentication instead

---

## Research & Problem Solving

During setup, I independently researched issues using:
- Google search
- Official documentation (Node.js, Git, OpenAI, Anthropic)
- Community solutions for PowerShell execution policies and npm CLI tools

This helped me resolve:
- Node.js installation process
- npm global package usage
- Windows PowerShell script restrictions
- API key authentication for OpenAI tools

---

## Outcome

Despite encountering authentication and environment setup issues, I was able to:
- Install all required tools
- Configure CLI and IDE environment
- Resolve system-level Windows issues
- Use alternative authentication methods when needed
- Successfully set up a working development environment