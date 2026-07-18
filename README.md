<!-- github.com/insomniac-asif — profile README -->

### Asif Hossain

Self-taught systems builder working on **AI-agent reliability** — honesty, calibration, and grounding tooling that gets models to know what they don't know, abstain instead of confabulate, and be straight about what they actually did.

Alongside that I run **ABL**, a local-first personal-AI system that lives entirely on my own hardware (local models only, nothing personal leaves the machine), and I build applied agents — a multi-server Discord bot and a crypto news event-study engine.

I'm on leave from a CS degree, spending the time building and shipping real systems end-to-end instead. The work below is where that time went.

---

**What I build**

*Honesty & calibration — measuring where models are (over)confident*

- **[honest-confidence](https://github.com/insomniac-asif/honest-confidence)** — a deterministic honesty layer (confidence-capping + grounding-abstain) with a reproducible TruthfulQA eval. On a 4-seed run it cut calibration error ~3.4× (0.48 → 0.14 ECE) — and reports the cost right next to the win: ranking AUROC slips toward chance, and the "zero confident falsehoods" result is undefined-by-construction, not actually zero.
- **[honest-quant](https://github.com/insomniac-asif/honest-quant)** — measures how quantization shifts a local model's calibration (ECE, Brier, AUROC, confidently-wrong rate), not just speed. Fully offline test suite, Ollama mocked. The one committed run refutes its own hypothesis: quantization didn't reliably increase overconfidence.

*Agent-reliability tooling — small, zero-dependency, runs offline*

- **[receipts](https://github.com/insomniac-asif/receipts)** — reconciles what an agent *claimed* it did against its actual tool-call trace, flagging phantom actions and silent failures.
- **[toolcall-rescue](https://github.com/insomniac-asif/toolcall-rescue)** — salvages tool calls that leaked into message content as XML, dirty JSON, Hermes tags, or fullwidth-unicode DSML. A fallback for when a model ignores the structured `tool_calls` field.
- **[break-your-agent](https://github.com/insomniac-asif/break-your-agent)** — an offline lab for how tool-calling agents get prompt-injected: 11 attacks, 4 toggleable defenses, a red/green scorecard. The honest finding: model alignment isn't a security boundary — only the architectural defenses hold every time.

*Applied systems*

- **[doll-bot](https://github.com/insomniac-asif/doll-bot)** — one Discord bot for many servers: AI that does real admin work, but every tool is permission-tiered (MOD/ADMIN/OWNER) and destructive ones are confirm-gated. Node / discord.js.
- **[abl-demo](https://github.com/insomniac-asif/abl-demo)** — a clean-room showcase of ABL's multi-agent architecture: a peer bus and a propose → challenge → execute protocol that requires 3/3 consensus, with a human as the only tiebreaker.
- **[news-crypto-engine](https://github.com/insomniac-asif/news-crypto-engine)** — ingests crypto news, classifies events into 8 categories, and runs an event study on whether they move price. Most category/window combinations show no signal — and it says so.

Each repo's README writes its own limitations and costs in as first-class results. A method that only reports its wins isn't a measurement.

---

**Tech:** Python · JavaScript · FastAPI · local LLMs / Ollama · SQLite & vector search · discord.js

**How I work:** honesty-first — I'd rather report a smaller number I can defend than a big one I can't. Mechanistic — I don't trust a system until I understand how it computes, not just what it outputs. And I verify my own work end-to-end before I call it done.

📫 ahossa21@gmail.com
