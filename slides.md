---
theme: slidev-theme-neocarbon
title: Agentic Engineering, Supercharged
info: A hands-on introduction to opencode & oh-my-opencode
transition: slide-left
layout: cover
mdc: true
---

# Agentic Engineering, Supercharged

Agentic coding in 2026

<div style="position: absolute; bottom: 2.5rem; left: 0; right: 0; text-align: center; font-size: 0.7rem; color: rgba(255,255,255,0.3); font-style: italic;">
  *No humans were involved in creating this presentation
</div>

---
layout: center
---

<div style="display: flex; flex-direction: column; align-items: center; text-align: center; justify-content: center; gap: 0.5rem;">
  <div style="font-size: 1.5rem; opacity: 0.6; font-weight: 500;">It's been</div>
  <div style="display: flex; align-items: baseline; gap: 1rem; line-height: 0.9; margin: 1rem 0;">
    <span style="font-size: 5rem; font-weight: 900; letter-spacing: -0.04em;">0</span>
    <span style="font-size: 5rem; font-weight: 900; letter-spacing: -0.02em;">DAYS</span>
  </div>
  <div style="font-size: 1.5rem; opacity: 0.6; font-weight: 500;">since the last coding agent launched</div>
</div>

---
layout: default
---

# The Landscape (2025-2026)
<p style="opacity: 0.5; font-size: 1.1rem; margin-top: -0.5rem; font-style: italic;">Everyone and their dog shipped a coding agent</p>

<div style="display: flex; gap: 1.5rem; margin-top: 1rem; height: 70%;">
  <div style="flex: 1; padding: 1.2rem; border: 1px solid rgba(227,6,19,0.2); background: rgba(227,6,19,0.04); border-radius: 8px;">
    <div style="display: flex; align-items: center; justify-content: space-between; margin-bottom: 1rem;">
      <h3 style="font-size: 1.1rem; font-weight: 700; margin: 0;">IDE Agents</h3>
      <span style="font-size: 2rem; font-weight: 900; opacity: 0.15;">16</span>
    </div>
    <div style="display: flex; flex-wrap: wrap; gap: 0.5rem; font-size: 0.85rem;">
      <NcBadge type="accent" v-for="t in ['Cursor', 'GitHub Copilot', 'Windsurf', 'JetBrains AI', 'Amazon Q Developer', 'Sourcegraph Cody', 'Tabnine', 'Augment Code', 'Supermaven', 'Zed AI', 'Continue', 'Kiro', 'Roo Code', 'Void', 'PearAI', 'Trae']" :key="t">{{ t }}</NcBadge>
    </div>
  </div>
  <div style="flex: 1; padding: 1.2rem; border: 1px solid rgba(0,150,255,0.2); background: rgba(0,150,255,0.04); border-radius: 8px;">
    <div style="display: flex; align-items: center; justify-content: space-between; margin-bottom: 1rem;">
      <h3 style="font-size: 1.1rem; font-weight: 700; margin: 0;">CLI Agents</h3>
      <span style="font-size: 2rem; font-weight: 900; opacity: 0.15;">12</span>
    </div>
    <div style="display: flex; flex-wrap: wrap; gap: 0.5rem; font-size: 0.85rem;">
      <NcBadge type="info" v-for="t in ['Claude Code', 'opencode', 'Aider', 'Codex CLI', 'Gemini CLI', 'Goose', 'Cline', 'Kilo Code', 'GPT-Pilot', 'Plandex', 'Mentat', 'Smol Developer']" :key="t">{{ t }}</NcBadge>
    </div>
  </div>
</div>

<div style="margin-top: 0.75rem; padding: 0.5rem 0.75rem; border: 1px solid rgba(255,200,50,0.3); background: rgba(255,200,50,0.06); border-radius: 4px; font-size: 0.65rem; color: rgba(255,220,100,0.7); line-height: 1.4;">
  ⚠️ This slide may contain information that is out of date. Reason: <span style="font-style: italic;">it has been more than 12 hours since it was last edited.</span> <span style="opacity: 0.5;">[update]</span>
</div>

---
layout: default
---

# So many ways to give them your money
<p style="opacity: 0.5; font-size: 1.1rem; margin-top: -0.5rem; font-style: italic;">The "Shut up and take my compute" starter pack</p>

<div style="display: flex; flex-direction: column; gap: 1.5rem; margin-top: 2rem;">

  <div style="display: flex; align-items: center; border-bottom: 1px solid rgba(255,255,255,0.05); padding-bottom: 1.5rem;">
    <div style="width: 140px; font-weight: 800; color: #E30613; font-size: 1.2rem; text-transform: uppercase; letter-spacing: 2px; line-height: 1.2;">
      The<br/>Brains
    </div>
    <div style="flex: 1; display: flex; flex-wrap: wrap; gap: 0.6rem; font-family: monospace;">
      <span v-for="m in ['GPT-5.4', 'o3', 'Claude Opus 4.6', 'Claude Sonnet 4.6', 'Gemini 3.1 Pro', 'Grok 4', 'DeepSeek V4', 'DeepSeek R1', 'Codestral', 'Qwen3-Coder']" :key="m" style="padding: 0.25rem 0.75rem; background: rgba(255,255,255,0.03); border: 1px solid rgba(255,255,255,0.1); border-radius: 4px; font-size: 0.85rem; color: #ddd;">{{ m }}</span>
    </div>
  </div>

  <div style="display: flex; align-items: center; border-bottom: 1px solid rgba(255,255,255,0.05); padding-bottom: 1.5rem;">
    <div style="width: 140px; font-weight: 800; color: #E30613; font-size: 1.2rem; text-transform: uppercase; letter-spacing: 2px; line-height: 1.2;">
      The<br/>Bundles
    </div>
    <div style="flex: 1; display: flex; flex-wrap: wrap; gap: 1rem;">
      <span v-for="s in ['Cursor Pro', 'GitHub Copilot', 'Windsurf Pro', 'JetBrains AI Pro', 'Augment', 'Tabnine Pro', 'Amazon Q Pro']" :key="s" style="font-weight: 600; font-size: 1.05rem; border-bottom: 3px solid rgba(227,6,19,0.4); padding-bottom: 2px;">{{ s }}</span>
    </div>
  </div>

  <div style="display: flex; align-items: center;">
    <div style="width: 140px; font-weight: 800; color: #E30613; font-size: 1.2rem; text-transform: uppercase; letter-spacing: 2px; line-height: 1.2;">
      The<br/>Meter
    </div>
    <div style="flex: 1; display: flex; flex-wrap: wrap; gap: 0.6rem;">
      <span v-for="a in ['OpenRouter', 'Anthropic API', 'OpenAI API', 'Google AI Studio', 'AWS Bedrock', 'Azure OpenAI', 'Fireworks', 'Together AI']" :key="a" style="padding: 0.3rem 0.9rem; border: 1px solid rgba(227,6,19,0.3); border-radius: 20px; font-size: 0.8rem; text-transform: uppercase; letter-spacing: 1px; background: rgba(227,6,19,0.05);">{{ a }}</span>
    </div>
  </div>

</div>

<div style="margin-top: 2rem; padding: 0.5rem 0.75rem; border: 1px solid rgba(255,200,50,0.3); background: rgba(255,200,50,0.06); border-radius: 4px; font-size: 0.65rem; color: rgba(255,220,100,0.7); line-height: 1.4;">
  ⚠️ This slide may contain information that is out of date. Reason: <span style="font-style: italic;">it has been more than 24 hours since it was last edited.</span> <span style="opacity: 0.5;">[update]</span>
</div>

---
layout: center
---

# Disambiguation

<div style="display: flex; flex-direction: column; gap: 0.9rem; font-size: 1.15rem; margin-top: 1.5rem;">
  <div style="display: flex; align-items: center; gap: 1rem; padding: 0.6rem 1.2rem; border-left: 3px solid rgba(0,210,255,0.4); background: rgba(0,210,255,0.04); border-radius: 0 6px 6px 0;">
    <span style="font-size: 1.4rem; font-weight: 800; opacity: 0.25; font-variant-numeric: tabular-nums;">01</span>
    <span style="font-weight: 600;">Model</span>
  </div>
  <div style="display: flex; align-items: center; gap: 1rem; padding: 0.6rem 1.2rem; border-left: 3px solid rgba(0,210,255,0.4); background: rgba(0,210,255,0.04); border-radius: 0 6px 6px 0;">
    <span style="font-size: 1.4rem; font-weight: 800; opacity: 0.25; font-variant-numeric: tabular-nums;">02</span>
    <span style="font-weight: 600;">Tokens</span>
  </div>
  <div style="display: flex; align-items: center; gap: 1rem; padding: 0.6rem 1.2rem; border-left: 3px solid rgba(0,210,255,0.4); background: rgba(0,210,255,0.04); border-radius: 0 6px 6px 0;">
    <span style="font-size: 1.4rem; font-weight: 800; opacity: 0.25; font-variant-numeric: tabular-nums;">03</span>
    <span style="font-weight: 600;">LLM vs Agent</span>
  </div>
  <div style="display: flex; align-items: center; gap: 1rem; padding: 0.6rem 1.2rem; border-left: 3px solid rgba(0,210,255,0.4); background: rgba(0,210,255,0.04); border-radius: 0 6px 6px 0;">
    <span style="font-size: 1.4rem; font-weight: 800; opacity: 0.25; font-variant-numeric: tabular-nums;">04</span>
    <span style="font-weight: 600;">Harness</span>
  </div>
  <div style="display: flex; align-items: center; gap: 1rem; padding: 0.6rem 1.2rem; border-left: 3px solid rgba(255,180,50,0.4); background: rgba(255,180,50,0.04); border-radius: 0 6px 6px 0;">
    <span style="font-size: 1.4rem; font-weight: 800; opacity: 0.25; font-variant-numeric: tabular-nums;">05</span>
    <span style="font-weight: 600;">Enhancements</span>
    <span style="opacity: 0.35; font-size: 0.8rem; margin-left: auto;">tools / skills / MCPs</span>
  </div>
  <div style="display: flex; align-items: center; gap: 1rem; padding: 0.6rem 1.2rem; border-left: 3px solid rgba(255,80,80,0.4); background: rgba(255,80,80,0.04); border-radius: 0 6px 6px 0;">
    <span style="font-size: 1.4rem; font-weight: 800; opacity: 0.25; font-variant-numeric: tabular-nums;">06</span>
    <span style="font-weight: 600;">Context Window</span>
  </div>
</div>

---
layout: split-heading
---

::left::

# The Model

::right::

<DisambigProgress :step="1" />

A statistically magnificent autocomplete engine. You give it text, it predicts the next text. That is the whole trick. Everything else is marketing.

- `claude-sonnet-4-6` — the overachiever who bills by the syllable
- `gpt-4o` — the crowd favorite (peaked in 2024, still showing up)
- `gemini-2.5-pro` — 1M token memory, still cannot remember your name

It does not "think." It does not "understand." It plays the world's most expensive game of *what word comes next?*

> Zero memory between calls. Every conversation starts from scratch. It is a goldfish with a PhD — and you are paying per thought.

---
layout: split-heading
---

::left::

# Tokens

::right::

<DisambigProgress :step="2" />

Not words. Not characters. Vibes-based chunks that the model reads, like syllables invented by an alien accountant.

| Input             | Approx. tokens |
| ----------------- | -------------- |
| `"opencode"`      | ~2             |
| `"Hello!"`        | ~3             |
| Your entire repo  | ~goodbye wallet |

**Rule of thumb:** 1 token ≈ 4 characters ≈ ¾ of a word ≈ $0.000003 of regret

- Every token costs money — input AND output. Yes, you pay for the parrot to read AND talk.
- Your 200-file monorepo? That is a LOT of tokens.
- There is no "free tier" for overthinking. The meter is always running 🚕

> You will never look at a verbose stack trace the same way again.

---
layout: comparison
---

<DisambigProgress :step="3" />

::left::

### 💬 LLM

You ask → it answers → it forgets you exist.

One shot. No loops. Like texting a genius who deletes the conversation after every message.

Has the emotional permanence of a Snapchat story.

::right::

### 🤖 Agent

You ask → it thinks → uses tools → reads results → thinks again → **loops until done** (or until your budget is done)

Autonomous. Dynamic. Occasionally terrifying.

**The memory is a LIE.** It looks like it remembers — it does not. The harness just replays the entire conversation every turn. Your agent has amnesia. Every. Single. Time.

---
layout: split-heading
---

::left::

# The Harness

::right::

<DisambigProgress :step="4" />

The software between **you** and the **parrot**. Someone has to keep this thing from `rm -rf /`-ing your project.

It runs the loop: assemble context → call model → execute tools → replay everything → repeat. Yes, the ENTIRE conversation gets replayed every turn. Told you the memory was a lie.

- Decides what the model sees (system prompt, files, history)
- Executes tool calls and feeds results back
- Handles retries, token budgets, and the word "no"

Examples: **opencode**, Cursor, Claude Code, Cline, Aider

> The model is the engine. The harness is the adult in the room who hides the car keys.

---
layout: section
---

<DisambigProgress :step="5" />

# Enhancements

Tools · Skills · MCPs

---
layout: default
---

<DisambigProgress :step="6" />

# Tools

How the parrot touches grass.

Remember: the model cannot actually DO anything. It is a brain in a jar. It *asks nicely*, and the harness does the dirty work:

```text
Parrot:  "Please run: read_file('src/index.ts')"
Babysitter: → reads the file, returns contents
Parrot:  "I see the bug on line 42. Edit it like this..."
Babysitter: → edits the file, confirms
Parrot:  "Done. Shall I also refactor the entire codebase?"
Babysitter: → "No."
```

Common tools in opencode:

- 📂 Read / write files (it WILL read your entire repo if you let it)
- 💻 Run shell commands (yes, with real consequences)
- 🔍 Grep the codebase (see: token meter, above)

> Without tools, it is just a chatbot. With tools, it is a chatbot that can delete your database.

---
layout: split-heading
---

::left::

# Skills

::right::

<DisambigProgress :step="7" />

Instruction sets you inject so the parrot stops improvising and starts following YOUR rules. Think crib notes for an amnesiac genius.

- Loaded on demand — not always wasting precious context
- Carry domain knowledge, conventions, workflows
- "How WE write code" not "how the internet circa 2023 writes code"

```text
skill: frontend-design
→ Parrot now knows your component patterns,
  design tokens, and naming conventions
  (instead of hallucinating its own)
```

> Skills shape **behavior**. Like onboarding a new hire — except they forget everything by next conversation. Every. Single. Time.

---
layout: split-heading
---

::left::

# MCPs

::right::

<DisambigProgress :step="8" />

**Model Context Protocol** — a standardized plug for your parrot.

Remember how USB killed the "50 different charger" problem? MCP does that for agent integrations. One protocol, anything plugs in.

- An MCP server exposes tools over a lightweight protocol
- The babysitter discovers and calls them like built-in tools
- Suddenly your parrot can talk to databases, browsers, APIs, and probably your toaster

```text
MCP: postgres-server
  → tool: run_query('SELECT * FROM regrets')
MCP: dev-browser
  → tool: screenshot(), click(), navigate()
```

> MCPs extend **what it can do** — Skills extend **how it thinks**. Together: a very expensive employee with an ever-expanding job description.

---
layout: default
---

<DisambigProgress :step="9" />

# Context Window

Everything the parrot can "see" in a single turn. If it is not in here, it does not exist. Period.

```text
[ system prompt | conversation history | file contents | tool results | your message ]
                          ↑ all of this counts toward the limit
                          ↑ all of this gets replayed EVERY turn (remember: the memory is a LIE)
```

- `claude-sonnet-4-6` → **200k tokens** · `gemini-2.5-pro` → **1M tokens**
- Bigger ≠ better — **context pollution** makes the parrot dumber, not smarter
- Every stale file, verbose stack trace, and forgotten conversation eats space AND attention
- Exceed the limit? Content gets silently dropped. Good luck debugging THAT.

> This is the goldfish bowl. The parrot, the meter, the babysitter, the hands, the cheat sheets, the USB ports — they all fight for space in here. Manage it, or it manages your wallet.

---
layout: section
---

# Let's set it up

Live, from scratch

---
layout: default
---

# Installation

```bash
# Install opencode
npm install -g opencode

# Launch it
opencode
```

That's it. The TUI loads, you pick a model, you start working.

---
layout: section
---

# Demo Time 🚀

---
layout: default
---

# Demo 1 — Understand a Codebase

Open a real project you've never touched. Ask:

> _"What does this project do and how is it structured?"_

**Watch it:**

1. Autonomously read files across the project
2. Build a mental map
3. Give you a clear, accurate summary

No context-setting. No manual file passing. It just figures it out.

---
layout: default
---

# Demo 2 — Make a Real Change

Point it at a real problem:

> _"Add input validation to this API endpoint"_

**Watch the full loop:**

1. 🔍 Read the relevant files
2. 🧠 Plan the change
3. ✏️ Edit the file
4. ✅ Ask for your confirmation before saving

---
layout: default
---

# Demo 3 — Run & Iterate

Let it own the feedback loop:

> _"Run the tests and fix any failures"_

**Watch it:**

1. Run the test command
2. Read the error output
3. Diagnose the cause
4. Fix the code
5. Re-run until green ✅

This is agentic engineering — not autocomplete.

---
layout: section
---

# oh-my-opencode

The community layer on top

---
layout: default
---

# What is oh-my-opencode?

Like **oh-my-zsh**, but for opencode.

<NcFeatureGrid :features="[
  { icon: '🎨', title: 'Themes', description: 'Make the TUI look great' },
  { icon: '🤖', title: 'Pre-built Agents', description: 'Code reviewer, test writer, and more' },
  { icon: '⚙️', title: 'Community Configs', description: 'Battle-tested setups, ready to use' },
  { icon: '🔌', title: 'Plugins', description: 'Extend opencode with community tooling' }
]" />

---
layout: default
---

# Tips & Gotchas

<NcFeatureGrid :features="[
  { icon: '🎯', title: 'Be specific', description: 'Vague in = vague out. Give context.' },
  { icon: '📋', title: 'Use system prompts', description: 'Set project context once, not every time.' },
  { icon: '👀', title: 'Review diffs', description: 'Always check before confirming changes.' },
  { icon: '📦', title: 'Watch your context', description: 'Do not dump your entire repo at once.' },
  { icon: '🏚️', title: 'Great for legacy code', description: 'Not just greenfield projects.' }
]" />

---
layout: end
---

# Thanks

Let's build something together.

[opencode.ai](https://opencode.ai) · [github.com/oh-my-opencode](https://github.com/oh-my-opencode)
