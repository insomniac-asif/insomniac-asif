<!-- github.com/insomniac-asif — profile README. DRAFT for Asif's review. -->

### Hi, I'm Asif 👋

I'm a self-taught systems builder working on **honesty and calibration in AI agents** — getting models to know what they don't know, abstain instead of confabulate, and be straight about what they actually did.

No CS degree. I learn by building the whole thing end-to-end and arguing with it until it holds up.

---

**What I'm building right now**

🔬 **[honest-confidence](https://github.com/insomniac-asif/honest-confidence)** — a small, deterministic honesty layer for LLM agents, *plus a reproducible eval that measures whether it actually works.* It caps a model's stated confidence at its measured accuracy and drops ungrounded claims, then grades that against TruthfulQA — reporting the calibration win **and its cost** (correct answers lost to over-abstention). Multi-seed with bootstrap CIs; the headline is the honest ~3.4× ECE improvement, not the lucky single-seed number. *A method that only reports its wins isn't a measurement.*

🧠 **A local-first personal AI assistant** (private) — an agent I run entirely on my own hardware across a small multi-machine GPU fleet. Local models only, nothing personal leaves my machines. Dozens of integrated faculties (memory, research digestion, scheduling, self-diagnosis), a self-improvement loop that learns from its own failures, and privacy as a hard architectural constraint rather than a setting. This is where most of my agent-engineering reps come from.

🤖 **A personality-driven Discord bot** (private) — serves a real 18+ gaming community day to day. Natural-language control, ~28 AI tools behind a defensive tool-calling layer (I had to hand-parse a model's non-standard tool-call markup so a format quirk could never break execution or leak raw output to users), AI moderation, persistent per-member memory and relationships, plus the usual economy/leveling/music/tickets surface. discord.js + a DeepSeek backend.

---

**How I work**

- **Honesty-first.** I'd rather report a smaller, defensible number than a big one I can't stand behind. My projects are built to show where they *fail*, not just where they win.
- **Mechanistic.** I don't trust a system until I understand how it computes, not just what it outputs.
- **I verify my own work end-to-end** before I claim it's done — root cause, not symptom.
- **Local-first & private by default.** I build things that respect the user's data because I built them for myself first.

**Interests:** AI safety & alignment · calibration and honest uncertainty · agent engineering · grounding / anti-confabulation · local model infra

---

📫 **Reach me:** ahossa21@gmail.com · Discord **ibteka**
