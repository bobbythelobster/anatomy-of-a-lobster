---
marp: true
theme: default
paginate: true
backgroundColor: '#000000'
style: |
  @import url('https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@400;500;600;700&display=swap');

  section {
    position: relative;
    font-family: 'Space Grotesk', sans-serif;
    color: #ffffff;
    text-shadow: 0 2px 6px rgba(0, 0, 0, 0.45);
    padding: 64px 72px 88px 72px;
  }

  section::before {
    content: '';
    position: absolute;
    left: 28px;
    bottom: 20px;
    width: 180px;
    height: 56px;
    background: url('data:image/png;base64,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') no-repeat left bottom;
    background-size: contain;
    opacity: 0.8;
  }

  h1, h2, h3, h4, h5, h6, p, li, blockquote, th, td, a, strong, em {
    color: #ffffff;
  }

  section table {
    display: table !important;
    width: 100% !important;
    table-layout: fixed;
    border-collapse: collapse;
    background: #000000 !important;
    border: 1px solid #ffffff;
    border-radius: 0;
    overflow: hidden;
    outline: none;
  }

  section table th:first-child,
  section table td:first-child {
    width: 28%;
  }

  section table th:nth-child(2),
  section table td:nth-child(2) {
    width: 72%;
  }

  section th,
  section td {
    background: #000000 !important;
    color: #ffffff !important;
    border: 1px solid #ffffff;
    padding: 10px 12px;
    text-align: left;
    text-shadow: none;
  }

  section th {
    background: #0b0b0b !important;
    font-weight: 700;
  }

  section pre {
    background: rgba(0, 0, 0, 0.58);
    color: #f4f7ff;
    border: 1px solid rgba(255, 255, 255, 0.18);
    border-radius: 12px;
    padding: 16px 18px;
    text-shadow: none;
  }

  section pre code {
    background: transparent;
    color: inherit;
  }

  h1 { font-size: 42px; }
  h2 { font-size: 32px; }
  li { margin-bottom: 8px; }

  .title-slide h1 {
    font-size: 56px;
    margin-bottom: 12px;
  }

  section.center {
    text-align: center;
  }

  .tag {
    display: inline-block;
    background: rgba(255,255,255,0.15);
    border: 1px solid rgba(255,255,255,0.3);
    border-radius: 6px;
    padding: 2px 12px;
    font-size: 14px;
    letter-spacing: 1px;
    text-transform: uppercase;
    margin-bottom: 16px;
  }

  .diagram {
    font-family: monospace;
    background: rgba(0,0,0,0.45);
    border: 1px solid rgba(255,255,255,0.18);
    border-radius: 12px;
    padding: 20px 24px;
    font-size: 18px;
    text-shadow: none;
    line-height: 1.8;
    margin-top: 16px;
  }

  .two-col {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 32px;
  }

  .highlight {
    color: #f9c74f;
    text-shadow: 0 0 12px rgba(249,199,79,0.4);
  }

  .section-label {
    font-size: 13px;
    letter-spacing: 2px;
    text-transform: uppercase;
    opacity: 0.6;
    margin-bottom: 8px;
  }
---

<!-- _class: center -->

![width:500px](anatomy-of-a-lobster.png)

By Sam Holmes

---

## Agenda

1. 🔧 **Under the Hood** — Architecture, gateway, agent runtime
2. 🧠 **Orchestration & Agentic Patterns** — Multi-agent, sub-agents, cron
3. 🛠️ **Building & Extending** — Skills, workspaces, tools
4. 💾 **Memory & Advanced Patterns** — Memory systems, hooks, nodes

<br>

> _20 minutes · hands-on architecture tour_

---

## What this audience asked for (from RSVP data)

- How OpenClaw works **under the hood**
- **Sub-agent orchestration** patterns that actually work
- How to build **independent, extensible agents**
- How to improve **memory + capability** over time

<br>

> _This deck is organized around those four asks._

---

<!-- _footer: "" -->

# 🔧 Under the Hood

<br>

<div class="section-label">Section 1 of 4</div>

---

## Question → Answer (Section 1)

**Q:** “How does it actually work under the hood?”

**A:** We’ll map the core path end-to-end:
- Gateway and channel routing
- Session/runtime boundaries
- Workspace contract and tool execution model

---

## Assumptions for this talk

You already know OpenClaw basics. So we’ll skip setup and focus on internals.

- ✅ You’ve installed and run it before
- ✅ You understand channels + agent replies
- ✅ You want deeper architecture and patterns
- ✅ Post-break audience is self-selected builders, so we’ll go practical and deep

<br>

**Today’s focus:**
1. How routing + runtime actually work
2. How to orchestrate sub-agents safely
3. How to extend with skills and memory patterns

---

## Architecture

<div class="diagram">

```
  📱 Chat Apps          🌐 Gateway            🤖 Agent Runtime
  ─────────────        ───────────            ─────────────────
  Telegram    ─┐                              ┌─ Workspace
  WhatsApp    ─┤──▶  WebSocket  ──▶  LLM  ──▶├─ Tools
  Discord     ─┤     Sessions                 ├─ Skills
  iMessage    ─┤     Routing                  └─ Memory
  Signal      ─┘     Channels
```

</div>

One gateway. Many channels. One agent brain.

---

## The Gateway

**WebSocket-based** message broker + session manager

- **Channels**: Telegram, Discord, WhatsApp, iMessage, Signal, Slack, Email...
- **Sessions**: per-user context, auth profiles, history
- **Routing**: deterministic binding rules → right message to right agent
- **Heartbeats**: scheduled pings to keep agents proactive

```json
{
  "channels": {
    "telegram": { "token": "...", "agentId": "main" },
    "discord":  { "token": "...", "agentId": "main" }
  }
}
```

---

## Agent Runtime

**The brain** — everything your agent knows and can do

```
~/.openclaw/workspace/
  ├── AGENTS.md     ← operating instructions
  ├── SOUL.md       ← persona & personality
  ├── USER.md       ← who you're helping
  ├── TOOLS.md      ← local env notes
  ├── MEMORY.md     ← long-term memory
  └── memory/       ← daily logs
      └── 2026-02-26.md
```

> _Files are the interface. Readable, editable, version-controlled._

---

<!-- _footer: "" -->

# 🧠 Orchestration & Agentic Patterns

<br>

<div class="section-label">Section 2 of 4</div>

---

## Question → Answer (Section 2)

**Q:** “How does sub-agent orchestration work in practice?”

**A:** We’ll cover the concrete mechanics:
- Deterministic routing + bindings
- `sessions_spawn` isolation model
- Parallel execution with safe result return

---

## Multi-Agent Routing

One gateway → **many agents**, each isolated

- Each agent has its own workspace, session history, auth profile
- Route by channel, user, guild, or custom rule
- Agents can have different models, personas, capabilities

```json
{
  "agents": {
    "main":   { "workspace": "~/.openclaw/workspace" },
    "devbot": { "workspace": "~/.openclaw/devbot" },
    "edgar":  { "workspace": "~/.openclaw/edgar" }
  }
}
```

---

## Bindings: Deterministic Routing

**How a message finds its agent**

```
Incoming message
      │
      ▼
  Peer match?  ──yes──▶  peer agent
      │ no
      ▼
  Guild match? ──yes──▶  guild agent
      │ no
      ▼
  Account match? ─yes──▶ account agent
      │ no
      ▼
  Channel default ──────▶ fallback agent
```

Predictable. Inspectable. No magic.

---

## Sub-Agent Spawning

**Parallel work, isolated context**

```
Main agent
    │
    ├──▶ subagent: "research X"     ─┐
    ├──▶ subagent: "write Y"         ├── run in parallel
    └──▶ subagent: "deploy Z"       ─┘
              │
              └──▶ auto-announce on completion
```

- `sessions_spawn` creates isolated child session
- Sub-agents get their own context window
- Results push back automatically — no polling

---

## Cron & Heartbeats

**Proactive agents that don't wait to be asked**

- **Heartbeats**: periodic pings → check email, calendar, alerts
- **Cron**: precise schedules → "every Monday 9am, send standup"
- **Background work**: commits, reports, monitoring while you sleep

```json
{
  "cron": [
    { "schedule": "0 9 * * 1", "prompt": "Send weekly standup", "channel": "telegram" },
    { "schedule": "*/30 * * * *", "prompt": "HEARTBEAT_MD", "model": "haiku" }
  ]
}
```

---

<!-- _footer: "" -->

# 🛠️ Building & Extending

<br>

<div class="section-label">Section 3 of 4</div>

---

## Question → Answer (Section 3)

**Q:** “How do I build independent agents I can replicate?”

**A:** We’ll break it down into a reusable blueprint:
- Workspace contract
- Bindings + model profile
- Skills + safety boundaries

---

## Skills

**Packaged capabilities** — drop in, wire up, use immediately

```
~/.openclaw/workspace/skills/
  └── weather/
      ├── SKILL.md      ← instructions for the agent
      ├── get-weather.sh
      └── parse.py
```

- Install from **ClawHub**: `clawhub install weather`
- Or write your own — it's just a directory + markdown
- Agent reads `SKILL.md` and knows how to use it

> _Skills = tools + docs bundled together_

---

## Agent Workspace Contract

**The files that define an agent**

| File | Purpose |
|------|---------|
| `AGENTS.md` | How to behave, what rules to follow |
| `SOUL.md` | Persona, tone, personality |
| `USER.md` | Who you're talking to |
| `TOOLS.md` | Local env: cameras, SSH, voice prefs |
| `MEMORY.md` | Long-term curated memory |

> _Change the files → change the agent. No redeployment needed._

---

## Independent Agent Blueprint (copy this)

| Component | What to define |
|---|---|
| Workspace | Dedicated folder for each agent (`~/.openclaw/<agent-name>/`) |
| Identity files | `AGENTS.md`, `SOUL.md`, `USER.md`, `TOOLS.md`, `MEMORY.md` |
| Routing | Channel/user/guild bindings in gateway config |
| Model profile | Default model + optional escalation strategy |
| Skills | Minimal starter pack (1-3 skills) tied to mission |
| Boundaries | Tool allowlists, approval rules, sensitive-action gates |
| Ops loop | Heartbeat checklist + cron for proactive tasks |

> _If you can define these seven, you can replicate agents reliably._

---

## The Tool System

**What agents can actually do**

```
Built-in tools
  read / write / edit / exec    ← filesystem & shell
  browser                       ← full web automation
  canvas                        ← visual surfaces
  nodes                         ← paired mobile devices
  message                       ← send to channels
  image / tts                   ← media generation
  web_fetch                     ← lightweight web access

+ Skill tools (custom scripts via SKILL.md)
```

---

## Multi-Agent Setup in Practice

**One gateway, many personalities**

```
openclaw.json
  ├── agent: "main"   → Claudine 🌸  (personal assistant)
  ├── agent: "edgar"  → Edgar 🤖     (dev/ops agent)
  └── agent: "devbot" → DevBot 🔧    (discord community bot)

Each has:
  • own workspace & memory
  • own model config
  • own channel bindings
  • own skill set
```

---

<!-- _footer: "" -->

# 💾 Memory & Advanced Patterns

<br>

<div class="section-label">Section 4 of 4</div>

---

## Question → Answer (Section 4)

**Q:** “How are people enhancing memory and capability in real deployments?”

**A:** We’ll walk through practical patterns:
- Multi-contact and group memory organization
- Distillation from daily logs to long-term memory
- Retrieval patterns that keep context focused

---

## Memory Pattern: Multi-Contact + Group Context

**How agents remember cleanly across people and channels**

```
Short-term (session)                 Long-term (structured files)
─────────────────────                ─────────────────────────────
Context window                       MEMORY.md
  └── recent turn state                └── curated durable facts

Per-contact memory                   Per-group memory
memory/contacts/<id>.md              memory/groups/<id>.md
  └── preferences, history             └── shared context, norms

Daily logs                           Retrieval layer
memory/YYYY-MM-DD.md                 memory_search("topic")
  └── raw events                       memory_get("preference")
```

- Organize memory by **contact + group**, not one giant file
- Distill daily logs into durable memory during heartbeat passes
- Keep memory readable/editable so behavior stays auditable

---

## Context Management

**Keeping the agent sharp over long sessions**

- **Compaction**: summarize older context, preserve key facts
- **Session pruning**: drop irrelevant history, keep signal
- **Context window budget**: models vary — manage proactively

```
Strategies:
  ✓ Load only relevant memory files per session type
  ✓ Use haiku for lightweight tasks (10x cheaper)
  ✓ Sub-agents for isolated work → don't bloat main context
  ✓ Heartbeat model: haiku | main chat: sonnet | deep work: opus
```

---

## Advanced Patterns

**The full surface area**

- 📡 **Webhooks & hooks** — trigger agents from external events
- 📱 **Mobile nodes** — iOS/Android paired devices (camera, screen, location)
- 🖼️ **Canvas surfaces** — agent-rendered UI overlays
- 🌐 **Browser automation** — Playwright-powered web control
- 🔁 **Agent-to-agent** — agents spawning agents, async pipelines

```bash
# Example: agent triggered by GitHub webhook
openclaw hook register --event push --agent devbot --channel discord
```

---

<!-- _class: center -->

# Get Your Claws Ready 🦞

<br>

| | |
|--|--|
| 🌐 **Website** | openclaw.ai |
| 📖 **Docs** | docs.openclaw.ai |
| 🐙 **GitHub** | github.com/openclaw/openclaw |
| 👾 **Community** | sdx.community |

<br>

**Builder CTA:** Start with one agent, one skill, and one heartbeat loop.

_Questions? Ask the lobster._
