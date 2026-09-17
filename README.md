# Research & Development Agent Skills

> Agent skills and governance rules for AI coding assistants. Plan software specs from scratch, audit existing codebases, and enforce human-in-the-loop decision protocols.

[![Agent Skills](https://img.shields.io/badge/Agent%20Skills-Standard%20Package-blue)](https://skills.sh)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](./LICENSE)

---

## Suite Components

| Component | Type | Description | Primary Output |
| :--- | :--- | :--- | :--- |
| **[`global-rules`](./global-rules)** | Global Governance Rule | Human-in-the-loop safeguards, on-demand `/option` evaluation, and stateful `/discuss` $\rightarrow$ `/summary` logging. | `agent.md`, `genius-result.md` |
| **[`pra-dev-research`](./pra-dev-research)** | Agent Skill | Turns your raw ideas into production-ready specifications with batched discovery loops. | `PRD.md`, `Architecture.md`, `Design.md`, `Schema.md`, `rules.md` |
| **[`the-gifted-genius`](./the-gifted-genius)** | Agent Skill | Your brainstorming buddy, He is your know-anything friends that will help you with your projects and guide you to the best way to build it. | `genius-result.md` |

---

## Quick Installation

### 1. Install Skills (via Skills CLI)
Install skills globally using the official [Skills CLI (`npx skills`)](https://skills.sh):

```bash
# Install both skills
npx skills add Wisnawa-Is/research-and-dev -g

# Or install individually
npx skills add Wisnawa-Is/research-and-dev@pra-dev-research -g
npx skills add Wisnawa-Is/research-and-dev@the-gifted-genius -g
```

### 2. Apply Global Governance Rules
Copy [`global-rules/human-in-the-loop-governance.md`](./global-rules/human-in-the-loop-governance.md) to your AI Agent's rule file, for instance:
- **Google Antigravity:** `~/.gemini/GEMINI.md` (or `.agents/rules/governance.md`)
- **Claude Code:** `CLAUDE.md`
- **Cursor:** `.cursorrules`

*(See [`global-rules/README.md`](./global-rules/README.md) for full instructions).*

---

## Usage & Triggers

### 1. For Brand New Project from Scratch (`pra-dev-research`)
```text
"I have an idea for a multi-tenant appointment platform for dental clinics. Run pre-dev research for this."
```

### 2. To Audit an Existing Codebase (`the-gifted-genius`)
```text
"Audit our current backend architecture and database schema. Find bottlenecks and suggest standard optimizations."
```

### 3. Evaluate Trade-Offs On-Demand (`/option`)
Append `/option` to any request to receive 3 distinct, high-signal technical paths (Conservative, Recommended, Alternative) :
```text
"Migrate our session authentication to JWT. /option"
```

### 4. Brainstorm Before Logging (`/discuss` & `/summary`)
Type `/discuss` once to enter an uninhibited brainstorming session. When aligned, type `/summary` to output conclusions and update documentation:
```text
"/discuss Should we switch from REST to tRPC or gRPC for internal services?"
# ... discussion flows naturally ...
"/summary"
```

---

## Repository Architecture

```text
research-and-dev/
├── global-rules/
│   ├── README.md                          # Installation & placement guide
│   └── human-in-the-loop-governance.md    # Governance, 3-Option, & logging protocol
│
├── pra-dev-research/
│   ├── SKILL.md                          # Workflow, discovery loop & rules
│   └── references/                       # Loaded Just-In-Time (JIT) per phase
│       ├── prd_template.md               # Standardized PRD blueprint
│       ├── architecture_template.md      # Architecture & sequence blueprint
│       ├── design_template.md            # UI/UX & design token blueprint
│       ├── schema_template.md            # Mermaid ERD & SQL schema blueprint
│       └── rules_template.md             # Contributor & AI rules blueprint
│
├── the-gifted-genius/
│   ├── SKILL.md                          # Persona, audit modes & web research
│   └── references/                       # Loaded Just-In-Time (JIT)
│       └── report_template.md            # Standardized blueprint for genius-result.md
│
├── .gitignore
├── LICENSE                               # MIT License
├── agent.md                              # Governance & Decision Log
└── README.md                             # Monorepo documentation
```

---

## Technical Highlights

1. **Token-Efficient Execution**:
   - **Batched Discovery**: Questions come with recommended defaults to prevent quadratic context growth ($O(N^2)$).
   - **Just-In-Time (JIT) Templates**: Reference documents load on-demand per phase rather than polluting baseline context.
   - **High-Density Output**: Compact templates preserving diagrams, tables, and interfaces without conversational filler.
   - **In-Place Mutation**: Updates existing specifications directly rather than emitting duplicate files (`PRD_v2.md`).
2. **Web-Grounded Validation**: Validates libraries, versions, and performance claims via autonomous web search (Make sure your AI Agent offers a search feature, or you can install a skill that provides browsing capabilities).
3. **Diagrams Over Verbose Code**: Uses Mermaid diagrams and structured pseudocode to keep specifications clear and maintainable.

---

## 📄 License

This repository is licensed under the [MIT License](./LICENSE).
