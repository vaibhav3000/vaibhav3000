# Vaibhav Mahore

**B.Tech Mathematics and Computing @ IISc Bangalore**

AI/ML Engineer | Applied AI | AI Systems

I build and verify AI systems end to end: efficient sequence architectures implemented from first principles and tested against their own math, evaluation engines that turn "it seems better" into measured trade-offs, and tool-using agents that only call something done when the test suite is green. Currently in my final year at IISc, with research-intern experience benchmarking state space models at Ericsson.

[LinkedIn](https://www.linkedin.com/in/vaibhav-mahore/) · [Email](mailto:mvaibhav@iisc.ac.in) · [LeetCode](https://leetcode.com/u/NINJA3000)

---

## Featured Projects

Each project is self-contained: committed benchmark results, tests, reproducible scripts, and honest limitations sections.

### [Efficient Sequence Modeling: From S4 to Mamba-3](https://github.com/vaibhav3000/s4-to-mamba)

First-principles PyTorch implementations of S4D, Mamba, Mamba-2 (chunked SSD) and Mamba-3 (complex-valued transitions), with equivalence tests that verify the parallel and recurrent forms against each other, and 1K-32K sequence-length benchmarks on a 6GB GPU.

- Reproduced the Mamba-3 paper's capability claim: complex transitions solve parity tracking at **98.3%** where real-transition SSMs and Transformers stay at chance (<=56%)
- Measured the real cost of quadratic attention: 30 ms per training step at 1K tokens vs 186 s at 32K
- Honest scope: S4D (not full NPLR S4), educational scans, OOM limits recorded not hidden

`Python` `PyTorch` `State Space Models` `Benchmarks`

### [AIRE: AI Reliability & Evaluation Engine](https://github.com/vaibhav3000/aire)

Trace-based evaluation engine for LLM and RAG systems: run the system once, store validated traces, then evaluate, compare versions and detect regressions forever on the stored data. Ships 13 deterministic metrics, a failure taxonomy, a relative-threshold regression engine with per-case attribution, and static HTML reports.

- Deliberate "fluent but uncited" RAG regression caught: groundedness **0.57 -> 0.00**, ungrounded failures +22
- Live Gemini evaluation on the same 26-case suite: abstention **0.0 -> 1.0**, groundedness **0.57 -> 1.0**, at 15 s/case latency and ~605 tokens per case: the evaluator prices the whole trade-off, not a single number

`Python` `LLM Evaluation` `RAG` `Regression Testing` `Observability`

### [Autonomous Repository Engineer](https://github.com/vaibhav3000/repo-engineer)

A verified tool-using coding agent: a deterministic state machine wraps the planner (scripted recipes or a live Gemini LLM), which only proposes actions. Seven schema-validated tools, a workspace path jail, AUTO/ASK/DENY permission policies, a test-command allowlist, and completion gated on green tests, never model claims.

- Deterministic benchmark: **4/4** SWE tasks (bug fix, failing test, missing test, refactor) with zero failed tool calls
- Live Gemini planner: **2/2** on the same validated runtime, absorbing two provider rate-limit errors mid-run; integration demonstration, not a leaderboard

`Python` `AI Agents` `Tool Use` `Sandboxing` `LLM Integration`

---

## Experience Highlights

**AI/ML Research Intern, Ericsson** (May 2026 - Jul 2026): benchmarked WiMamba vs Transformer on AWS A10G GPUs (10.7x lower latency, 42.6x less GPU memory at 4x4 patch size); geographic OOD transfer evaluation; soft-unfreezing PEFT strategy retaining 98.5% of full fine-tuning performance with 75% of parameters frozen.

**ML Engineer (AI Data Trainer), Alignerr** (May 2025 - Aug 2025): authored structured reasoning traces and training data improving LLM decision-making and tool selection.

**ML Engineer, micro1** (May 2025 - Aug 2025): data annotation, evaluation and model validation workflows for frontier AI systems.

---

## Technical Stack

| | |
|---|---|
| **Languages** | Python, C++, SQL |
| **Deep Learning** | PyTorch, TensorFlow |
| **ML** | Scikit-learn, NumPy, SciPy, Pandas |
| **AI Systems** | LLM evaluation, RAG, tool-using agents, sequence modeling (Transformers, SSMs) |
| **MLOps / Cloud** | Docker, AWS (EC2, S3), Linux, Git/GitHub |

---

## Research / Technical Interests

Efficient sequence models (state space models) · LLM evaluation and reliability · agentic systems with verified tool use · reproducible ML engineering

---

## Certifications

[Oracle Generative AI Professional](https://catalog-education.oracle.com/ords/certview/sharebadge?id=C8C59C8EE1F738F93AE1E79B0F626F32159AB49DFD29856207D8FD1DC48277DA) · [Oracle Data Science Professional](https://catalog-education.oracle.com/ords/certview/sharebadge?id=E89DD81DBC3358706048B3C0BE990728217104E5BF4E7543F6D15C4D60EFF669)

---

*Portfolio narrative: deep model understanding -> AI evaluation and reliability -> verified agentic AI.*
