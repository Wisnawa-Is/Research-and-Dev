# Global Agent Governance Rules

> Universal governance policy, decision protocol, and stateful session logging rules designed for AI coding assistants (Google Antigravity, Claude Code, Cursor, Windsurf, Copilot).

---

## 🎯 What Does This Rule Do?

1. **Human-in-the-Loop Governance:** Forbids AI assistants from executing destructive or irreversible terminal commands or code alterations without explicit user consent.
2. **On-Demand 3-Option Protocol (`/option`):** 
   - Normal prompts proceed directly and efficiently without wasting tokens.
   - When the user appends `/option`, the agent presents exactly three deeply evaluated technical paths:
     - **Option A (Conservative/Minimal):** Lowest-risk, minimal footprint.
     - **Option B (Recommended/Balanced):** High performance, best long-term maintainability.
     - **Option C (Alternative/Aggressive):** High-reward alternative or modern architectural paradigm.
   - **Zero Fluff:** Eliminates polite filler text to maximize high-signal technical analysis.
3. **Two-Tier Documentation (`agent.md` & `genius-result.md`):**
   - **`agent.md`**: Ultra-lean timeline changelog of decisions and discussion outcomes.
   - **`genius-result.md`**: Living architectural blueprint and deep analysis (no trivial bloat).
   - Eliminates duplicate full transcript files (saves ~60–75% token bloat).
4. **Stateful Discussion Protocol (`/discuss` & `/summary`):**
   - Type `/discuss` once to enter an uninhibited brainstorming and trade-off exploration session without premature file logging.
   - Gracefully integrates with the [`the-gifted-genius`](../the-gifted-genius) skill if installed.
   - Type `/summary` to conclude, summarize to chat, and atomically update documentation.

---

## 📦 Placement & Installation Guide

Depending on your AI coding assistant or IDE, copy the contents of [`human-in-the-loop-governance.md`](./human-in-the-loop-governance.md) into the appropriate configuration file:

### 1. Google Antigravity (AGY)
- **Global (Applies to all projects):**
  - **Path:** `~/.gemini/GEMINI.md`  
  - *(On Windows: `C:\Users\<YourUsername>\.gemini\GEMINI.md`)*
- **Workspace / Project-Level:**
  - **Path:** `.agents/rules/governance.md` or `GEMINI.md` in your project root.

### 2. Claude Code
- **Global:**
  - **Path:** `~/.claude/CLAUDE.md`
- **Project-Level:**
  - **Path:** `CLAUDE.md` in the project root directory.

### 3. Cursor
- **Global / Project-Level:**
  - **Path:** `.cursorrules` (or inside `.cursor/rules/governance.mdc`).

### 4. Windsurf / Cascade
- **Project-Level:**
  - **Path:** `.windsurfrules` in your project root directory.

### 5. GitHub Copilot
- **Project-Level:**
  - **Path:** `.github/copilot-instructions.md`.

---

## ⚡ Command Cheatsheet

| Command | Action | Behavior |
| :--- | :--- | :--- |
| *(Regular Prompt)* | **Direct Execution** | Agent solves the task immediately and efficiently with the best approach. |
| `/option` | **3-Option Evaluation** | Triggers Option A (Conservative), Option B (Recommended), and Option C (Alternative) with deep technical pros/cons. |
| `/discuss` | **Start Discussion** | Enters brainstorming session. AI audits trade-offs without writing file logs prematurely. |
| `/summary` | **Conclude Discussion** | Synthesizes discussion, records timeline in `agent.md`, and updates `genius-result.md` if architectural changes occurred. |
