<!-- github.com/insomniac-asif — profile README. -->

### Hi, I'm Asif 👋

I'm a self-taught systems builder working on **honesty and calibration in AI agents** — getting models to know what they don't know, abstain instead of confabulate, and be straight about what they actually did.

No CS degree. I learn by building the whole thing end-to-end and arguing with it until it holds up.

---

**What I'm building right now**

🔬 **[honest-confidence](https://github.com/insomniac-asif/honest-confidence)** — a small, deterministic honesty layer for LLM agents — confidence-capping + grounding-abstain — with a reproducible TruthfulQA eval that reports where it *hurts*. It caps a model's stated confidence at its measured accuracy and drops ungrounded claims, then grades that against a labeled benchmark and reports the costs as first-class results: mean calibration error drops **~3.4× across seeds** (not the lucky single-seed ~5×), but ranking AUROC slips to near-chance and the "zero confident falsehoods" headline is *undefined-by-construction*, not actually zero. Multi-seed with bootstrap CIs. *A method that only reports its wins isn't a measurement.*

**Shipped, public** — a small honesty / agent-safety toolkit. All MIT, all runnable locally, each with its cost written into the README:

- **[break-your-agent](https://github.com/insomniac-asif/break-your-agent)** — an offline, zero-dependency lab for how tool-calling agents get prompt-injected: 11 attacks, 4 toggleable defenses, a red/green scorecard, 46 tests passing in ~0.05s. The honest move: it *refuses* to claim 6/6 on a real model — only the confused-deputy attack lands every time, so the stated lesson is that model alignment isn't a security boundary; only the architectural defenses are.
- **[receipts](https://github.com/insomniac-asif/receipts)** — reconciles what an agent *claimed* it did against its actual tool-call trace, flagging phantom actions and silent failures. Zero-dependency, offline, 31 tests. Its own `selfeval` scores a perfect 1.00 — and the README says outright that's a regression floor on a tiny tuned set, *not* real-world accuracy.
- **[toolcall-rescue](https://github.com/insomniac-asif/toolcall-rescue)** — salvages LLM tool calls that leaked into message content as XML, dirty JSON, Hermes tags, or fullwidth-unicode DSML (the exact quirk I had to hand-parse for the Discord bot below). Zero-dependency, 32 tests. Honest edge: it's a *fallback* — check your SDK's `tool_calls` field first; it's heuristic, not a grammar, and XML values stay untyped strings.
- **[honest-quant](https://github.com/insomniac-asif/honest-quant)** — measures how quantization shifts a local model's calibration (ECE, Brier, AUROC, confidently-wrong rate), not just speed or perplexity; 65 tests, ollama mocked so the suite needs no GPU. The one committed run *refutes its own hypothesis*: quantization didn't make the model more confidently wrong — fp16 was the most overconfident level, and the level-to-level gaps sit within sampling noise.

**Where the reps come from** *(private)*

🧠 **A local-first personal AI assistant** — an agent I run entirely on my own hardware across a small multi-machine GPU fleet. Local models only, nothing personal leaves my machines. Dozens of integrated faculties (memory, research digestion, scheduling, self-diagnosis), a self-improvement loop that learns from its own failures, and privacy as a hard architectural constraint rather than a setting. This is where most of my agent-engineering reps come from.

🤖 **A personality-driven Discord bot** — serves a real 18+ gaming community day to day. Natural-language control, ~28 AI tools behind a defensive tool-calling layer (I had to hand-parse a model's non-standard tool-call markup so a format quirk could never break execution or leak raw output to users — since generalized into **toolcall-rescue**, above), AI moderation, persistent per-member memory and relationships, plus the usual economy/leveling/music/tickets surface. discord.js + a DeepSeek backend.

---

**How I work**

- **Honesty-first.** I'd rather report a smaller, defensible number than a big one I can't stand behind. My projects are built to show where they *fail*, not just where they win.
- **Mechanistic.** I don't trust a system until I understand how it computes, not just what it outputs.
- **I verify my own work end-to-end** before I claim it's done — root cause, not symptom.
- **Local-first & private by default.** I build things that respect the user's data because I built them for myself first.

**Interests:** AI safety & alignment · calibration and honest uncertainty · agent engineering · grounding / anti-confabulation · local model infra

---

📫 **Reach me:** ahossa21@gmail.com · Discord **ibteka**
