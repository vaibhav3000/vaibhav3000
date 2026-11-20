<div align="center">

# Vaibhav Mahore

**AI/ML Engineer** · B.Tech Mathematics and Computing, IISc Bangalore (graduating 2027)

I build AI systems that have to prove they work: models checked against their own math,<br>
LLM evaluation that fails the build on a regression, and agents that finish only when the tests pass.

**Open to 2027 full-time roles and internships:** AI/ML Engineer · ML Engineer · Applied AI · AI Automation

<br>

<a href="https://vaibhav3000.github.io/portfolio/"><img src="https://img.shields.io/badge/Portfolio-0F172A?style=for-the-badge&logo=googlechrome&logoColor=white" alt="Portfolio"></a>
<a href="https://vaibhav3000.github.io/portfolio/resume.pdf"><img src="https://img.shields.io/badge/Resume-PDF-B91C1C?style=for-the-badge&logo=adobeacrobatreader&logoColor=white" alt="Resume (PDF)"></a>
<a href="https://www.linkedin.com/in/vaibhav-mahore/"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"></a>
<a href="mailto:mvaibhav@iisc.ac.in"><img src="https://img.shields.io/badge/Email-EA4335?style=for-the-badge&logo=gmail&logoColor=white" alt="Email"></a>
<a href="https://leetcode.com/u/NINJA3000"><img src="https://img.shields.io/badge/LeetCode-FFA116?style=for-the-badge&logo=leetcode&logoColor=black" alt="LeetCode"></a>

</div>

---

## Highlights

| Result | Where |
|---|---|
| **10.7x** lower latency and **42.6x** less GPU memory than a Transformer | Ericsson internship, Mamba wireless model on AWS A10G |
| Groundedness collapse (**1.0 → 0.0**) blocked in CI on every push | [AIRE](https://github.com/vaibhav3000/aire), LLM/RAG evaluation engine |
| **0** breaches in a 49-attack Docker sandbox suite (1 documented residual) | [repo-engineer](https://github.com/vaibhav3000/repo-engineer), verified coding agent |
| **89% and 99%** parity on 2 of 5 seeds where rotation-free models stay near chance (means ≤57.3%) | [s4-to-mamba](https://github.com/vaibhav3000/s4-to-mamba), Mamba-3 implemented in PyTorch |
| **Top 100** national finalist | Amazon ML Challenge 2026 |

---

## Featured projects

### [AIRE: AI Reliability & Evaluation Engine](https://github.com/vaibhav3000/aire)

`LLM evaluation` `RAG` `CI quality gate` · Python, pytest, GitHub Actions, Gemini API

Trace-based evaluation for LLM and RAG systems: run a system once, store validated traces, then score them, compare versions and attribute every regression to the cases that caused it. The `aire-gate` CLI turns a comparison into a CI check, and the engine is covered by 361 tests.

> The repo's own CI plants a "fluent but uncited" version and the gate blocks it on every push: groundedness **1.0 → 0.0** and ungrounded failures **+109** on a 150-case suite, even though Recall@3 rose 0.72 → 0.86. Against a rate-limited test server, the async runner gets **5.4x** the sequential throughput with **0** failed cases.

[Code](https://github.com/vaibhav3000/aire) · [Live demo](https://vaibhav3000.github.io/aire/) · [Report (PDF)](https://github.com/vaibhav3000/aire/blob/main/reports/AIRE_AI_Reliability_Evaluation_Engine.pdf) · [Case study](https://vaibhav3000.github.io/portfolio/projects/aire/)

### [Autonomous Repository Engineer](https://github.com/vaibhav3000/repo-engineer)

`agents` `tool calling` `sandboxing` · Python, pytest, Gemini API

A coding agent where the LLM only proposes tool calls, natively or over MCP. A deterministic state machine (plan → act → observe → verify) validates every call against a schema, path-jails it to the workspace and applies AUTO/ASK/DENY permissions. A task is done only when the tests pass, and the runtime itself has 378 tests.

> **12/12** multi-file bug-fix, test-writing and refactoring tasks pass in scripted mode under both sandboxes with **0** failed tool calls. A 49-attack adversarial suite (path escapes, command injection, malformed calls and more) ends with **0** breaches in the Docker sandbox and 1 documented residual.

[Code](https://github.com/vaibhav3000/repo-engineer) · [Live demo](https://vaibhav3000.github.io/repo-engineer/) · [Report (PDF)](https://github.com/vaibhav3000/repo-engineer/blob/main/reports/Autonomous_Repository_Engineer.pdf) · [Case study](https://vaibhav3000.github.io/portfolio/projects/repo-engineer/)

### [Efficient Sequence Modeling: S4 → Mamba-3](https://github.com/vaibhav3000/s4-to-mamba)

`deep learning` `state space models` `GPU benchmarking` · PyTorch

Minimal S4D, Mamba, Mamba-2 (chunked SSD) and Mamba-3 in pure PyTorch, verified against float64 references and gradcheck (585 tests), with decoding benchmarks from 1K to 32K tokens on a 6 GB laptop GPU.

> Parity over 5 seeds at about 100K parameters each: Mamba-3 reaches **89%** and **99%** on 2 of 5 seeds, while every rotation-free model, including Mamba-3 with its rotation removed, stays near chance (means ≤57.3%). At 32K tokens the SSMs decode with a **0.14 to 0.39 MiB** state against a **128 MiB** fp32 KV cache.

[Code](https://github.com/vaibhav3000/s4-to-mamba) · [Live demo](https://vaibhav3000.github.io/s4-to-mamba/) · [Report (PDF)](https://github.com/vaibhav3000/s4-to-mamba/blob/main/reports/Efficient_Sequence_Modeling_S4_to_Mamba3.pdf) · [Case study](https://vaibhav3000.github.io/portfolio/projects/s4-to-mamba/)

---

## Experience

**AI/ML Research Intern · Ericsson India** · Bengaluru · May 2026 - Jul 2026<br>
Benchmarked WiMamba (a Mamba wireless model) against a Transformer on AWS A10G GPUs: 10.7x lower latency (30 ms vs 327 ms) and 42.6x less GPU memory. Evaluated transfer to an unseen geography (+16.6% composite score) and parameter-efficient fine-tuning that kept 98.5% of full fine-tuning performance with 75% of parameters frozen.

**Machine Learning Engineer · Alignerr and micro1** · Remote · May 2025 - Aug 2025<br>
Wrote reasoning traces and tool-use data for LLM post-training (Alignerr), and built model evaluation, validation and data-preprocessing workflows in Python with TensorFlow and scikit-learn (micro1).

---

## Achievements and certifications

- **Amazon ML Challenge 2026:** Top 100 national finalist; led Team AutoML.
- **Oracle Cloud Infrastructure Certified Professional:** [Generative AI](https://catalog-education.oracle.com/ords/certview/sharebadge?id=C8C59C8EE1F738F93AE1E79B0F626F32159AB49DFD29856207D8FD1DC48277DA) and [Data Science](https://catalog-education.oracle.com/ords/certview/sharebadge?id=E89DD81DBC3358706048B3C0BE990728217104E5BF4E7543F6D15C4D60EFF669)

---

## Tech stack

**Languages**<br>
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![C++](https://img.shields.io/badge/C%2B%2B-00599C?style=flat-square&logo=cplusplus&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-4479A1?style=flat-square&logo=postgresql&logoColor=white)
![Bash](https://img.shields.io/badge/Bash-4EAA25?style=flat-square&logo=gnubash&logoColor=white)

**ML and deep learning**<br>
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white)
![TensorFlow](https://img.shields.io/badge/TensorFlow-FF6F00?style=flat-square&logo=tensorflow&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=flat-square&logo=scikitlearn&logoColor=white)
![Hugging Face](https://img.shields.io/badge/Hugging%20Face-FFD21E?style=flat-square&logo=huggingface&logoColor=black)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=flat-square&logo=numpy&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=flat-square&logo=pandas&logoColor=white)

**LLM systems**<br>
`RAG` `LLM evaluation and regression testing` `tracing` `tool calling` `agent runtimes` `Gemini / OpenAI APIs`

**Engineering and MLOps**<br>
![GitHub Actions](https://img.shields.io/badge/GitHub%20Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![pytest](https://img.shields.io/badge/pytest-0A9EDC?style=flat-square&logo=pytest&logoColor=white)
![Playwright](https://img.shields.io/badge/Playwright-2EAD33?style=flat-square&logo=playwright&logoColor=white)
![AWS](https://img.shields.io/badge/AWS-232F3E?style=flat-square&logo=amazonwebservices&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black)
![Git](https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white)

---

## Beyond the code

<div align="center">

<img src="https://media.giphy.com/media/iNPNqI81MvDQ4D4n6D/giphy.gif" width="360" alt="Gojo Satoru lifting his blindfold, dark cinematic scene from Jujutsu Kaisen">

<img src="https://raw.githubusercontent.com/Xx-Ashutosh-xX/Xx-Ashutosh-xX/master/assets/1936.gif" width="360" alt="Super Saiyan aura meme: football coach powering up with Goku-style energy">

*"...throughout heaven and earth, I alone verify the output."*

</div>

Sci-Tech Coordinator for Rhapsody Fest at IISc: ran three inter-college gaming tournaments, a coding contest with 200+ teams and a 500+ member Discord community. Off the clock it's Jujutsu Kaisen and Dragon Ball Z. The Gojo in me trusts the process; the engineer in me checks the logs anyway.

<div align="center">

**Hiring for an AI/ML, applied AI or automation role?** [Email me](mailto:mvaibhav@iisc.ac.in) or see the [portfolio](https://vaibhav3000.github.io/portfolio/).

</div>
