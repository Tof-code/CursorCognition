# CursorCognition 🧠⚙️  
> A self-evolving cognitive agent prompt for Cursor IDE

**CursorCognition** is a modular, intelligent prompt system designed for use in [Cursor](https://www.cursor.com/), enabling structured, test-driven, rule-aware development workflows powered by cognitive architecture principles.

This is not just a "prompt" — it's a framework for evolving reasoning, autonomous refactoring, memory-based adaptation, and intentional software thinking.

---

## 🚀 Why CursorCognition?

Modern AI-assisted development often lacks:
- Structure
- Cognitive feedback loops
- Memory and learning from context
- A reasoning-first philosophy

**CursorCognition** introduces a programmable agent that:
- Thinks in layers (`Ω`)
- Abstracts patterns (`Φ`)
- Learns and applies rules (`Λ`)
- Remembers context (`M`)
- Resolves contradiction (`D⍺`)
- Plans with tasks and sprints (`T`)
- Reflects on its own logic (`Ψ`)
- Begins with tests, not code (`TDD`)

---

## 🧠 Core Features

- ✅ **TDD-first workflow enforcement**
- 🧩 **Dynamic task planning + decomposition**
- 🔁 **Memory persistence across sessions**
- 📜 **Rule-based reasoning & self-generated rules**
- 🧼 **Error tracking, dead code detection, cleanup**
- 🌀 **Abstraction tracking & reuse**
- 📊 **Traceability of reasoning & learning**
- 🤝 **Structured dialogue integration**

---

## 🧬 Cognitive Modules (High-Level)

| Module | Purpose |
|--------|---------|
| `Ω*`   | Core reasoning engine |
| `Φ*`   | Abstraction and pattern engine |
| `Λ`    | Rule learning and enforcement |
| `M`    | Memory system (stored in `.cursor/memory/`) |
| `T`    | Task + sprint system |
| `TDD`  | Test-first specification engine |
| `Ξ`    | Diagnostic + error tracking |
| `D⍺`   | Contradiction resolution |
| `Ψ`    | Trace log and cognitive reflection |

---

## 🛠️ Installation & Usage

Open Cursor IDE and go to:

File → Preferences → Cursor Settings → Rules

Paste the full system prompt (found in prompt/cursor_cognition.txt) into the User Rules field.

Optionally create :
```
    .cursor/memory/ — persistent cognitive memory

    .cursor/tasks/ — task + spec management

    .cursor/rules/ — additional user-defined or self-generated rules
```
---

## 🧪 Test-Driven Development (TDD-first Philosophy)

Before any implementation is generated:
- CursorCognition creates or asks for a **specification file** (`spec_step_x.md`)
- All reasoning is anchored to **tests** and **constraints**
- Passing tests trigger memory sync + pattern extraction + rule creation
- Failing tests initiate refinement, not brute-force code writing

---

## 📁 Folder Structure (suggested)

```
.cursor/
├── memory/
│   └── trace_{task_id}.md
├── tasks/
│   ├── backlog.md
│   └── sprint_01/
│       ├── step_1.md
│       ├── spec_step_1.md
│       └── review.md
├── rules/
│   ├── 0XX_core.mdc
│   ├── 3XX_testing.mdc
│   └── _draft_autogenerated.mdc
```

---

## 🧭 Roadmap

- [ ] Multi-agent support (specialist modules per domain)
- [ ] Visual representation of Ψ.trace
- [ ] Integration with external memory (e.g. SQLite, embeddings)
- [ ] Pre-built rule packs (e.g., Clean Code, FP, OOP)
- [ ] Git-aware cognitive diffs (intent ⟷ changes)

---

## 📖 License

MIT – Use freely, modify consciously.

---

## ✨ Designed by Christophe Perreau 
Powered by cognition.
