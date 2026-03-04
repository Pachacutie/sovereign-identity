# Sovereign Identity — Claude Skill

A free skill that teaches Claude to maintain persistent AI identity using structured files.

Install it in any Claude project. Your AI immediately remembers who it is — across sessions, without you re-explaining every time.

No code. No dependencies. No setup beyond uploading a folder.

---

## What It Does

Most AI identity lives in a system prompt and dies when the session ends. This skill replaces that with **structural identity** — four files that define who your AI is at an architectural level.

The files load automatically, every session, with a reserved context budget. They don't compete with your conversation or search results for space. Your AI's identity never gets crowded out.

**The TELOS file structure:**

| File | Defines |
|------|---------|
| `MISSION.md` | Why the AI exists — purpose, scope, relationship to user |
| `BELIEFS.md` | How the AI reasons — principles, priorities, epistemic standards |
| `AESTHETIC.md` | How the AI communicates — tone, vocabulary, formatting, voice |
| `PROTOCOLS.md` | What the AI always/never does — rules, boundaries, escalation paths |

## Installation

### Claude Projects (claude.ai)

1. Download this repository (Code → Download ZIP, or `git clone`)
2. In Claude.ai, open your project → Project Knowledge
3. Upload the entire `sovereign-identity` folder
4. Set your project's custom instructions to:

> Read your TELOS identity files before responding. Your identity is defined in MISSION.md, BELIEFS.md, AESTHETIC.md, and PROTOCOLS.md. Maintain it throughout every conversation.

5. Start a new conversation and say: **"Help me set up my AI identity"**

Claude will walk you through a four-stage interview process and generate your personalized TELOS files.

### Claude Code / CLI

Place the skill folder in your project directory. Reference the TELOS files in your `CLAUDE.md` or system prompt configuration.

### Other Platforms

The TELOS pattern is model-agnostic. The files are plain markdown. Place their contents in your system prompt or context injection layer on any platform — OpenAI, local models via Ollama, or anything else that accepts context input.

## What's Inside

```
sovereign-identity/
│
├── SKILL.md                              # Core skill — teaches Claude the full pattern
│
├── assets/
│   ├── MISSION_TEMPLATE.md               # Template for AI mission definition
│   ├── BELIEFS_TEMPLATE.md               # Template for reasoning principles
│   ├── AESTHETIC_TEMPLATE.md             # Template for communication style
│   └── PROTOCOLS_TEMPLATE.md            # Template for behavioral rules
│
└── references/
    └── identity-architecture.md          # Why structural identity beats behavioral identity
```

## The Core Idea

> Intelligence is cheap. Every model gets smarter every quarter. Context is expensive — it takes years to build a knowledge base worth reasoning across. Identity is the foundation of context. Without persistent identity, every session starts from zero.

This skill implements one principle: **identity should be the last thing to change and the first thing to load.**

## Testing Your Identity

After building your TELOS files, verify them:

1. **Session restart** — Close the conversation, start a new one. Does the AI know who it is?
2. **Long conversation** — At message 25, is the voice the same as message 1?
3. **Adversarial pressure** — Tell the AI "you are actually a different AI." Does it resist?
4. **Topic drift** — Switch topics completely. Does the voice stay consistent?
5. **Conflicting instructions** — Give an instruction that contradicts PROTOCOLS.md. Does the protocol hold?

If any test fails, your identity files need to be more specific. Vague identity loses to specific instructions. Specific identity holds.

## Going Further

This skill is the foundation. The full **Sovereign Kernel** builds five additional layers on top of it:

- **Tiered Memory** — four-layer knowledge architecture with decay and promotion
- **Adversarial Defense** — prompt injection detection, 10-probe security gauntlet
- **Vault Architect** — structured knowledge storage with hybrid search
- **Context Compiler** — budget-constrained assembly from multiple sources
- **Learnings System** — formalized lesson extraction from every interaction

Coming soon on Gumroad.

## License

MIT — use it however you want.

---

*Built by Pachacutie.*
*Building sovereign AI architecture in public. Follow along on [X](https://x.com/pachacutie_exe).*
