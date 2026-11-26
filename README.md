# Stanislav Kim

AI Engineer in Seoul. I build multilingual LLM agents and hybrid RAG, and I measure them before and after every change.

In 2026 I led a 3-person AI team (2 engineers and me) at RAAF Group in Kazakhstan, on a fixed-term contract. We built LLM tools that were piloted in two of the group's business units:

- An agent that turns staff interviews in Russian, Kazakh and English into process steps, piloted with 20+ employees
- LLM cost per interview cut from about $0.33 to about $0.01 (97%) at the same 90%+ eval pass rate: a 4-model bake-off showed a smaller Qwen model could replace Claude; prompt caching and batched post-processing did the rest
- Extended reasoning turned off and each agent turn merged into one schema-validated JSON reply: model time per interview from 10–15 min to under 2.5 min, invalid replies from 33% to 5%, all fixed by one automatic retry
- An 80-scenario evaluation harness in three languages, co-built with a teammate, with a spot-checked LLM judge; releases shipped only after passing it
- Guardrails against prompt injection: the tool plan is locked before user input is processed, plus a 3-layer filter; all 7 red-team attacks blocked, 0 of 36 clean records flagged
- The 2.0 rebuild of a multi-agent platform, which I led

That work is not public. The two agent repositories below are independent projects written on my own time: they use synthetic data, contain no employer code or data, and run offline.

## Featured projects

| Repository | What it is | Proof in the repo |
| --- | --- | --- |
| [agents-automation](https://github.com/Stas2903/agents-automation) | A multi-role LLM assistant for office work: RAG with access control in SQL, an interviewer with an honesty guard, a 3-layer prompt-injection screen | 986 offline tests; 111 unit mutants and 8 eval mutants, all caught; CI with mypy --strict |
| [ai-ceo](https://github.com/Stas2903/ai-ceo) | A director loop that runs a team of AI agents: owner approvals for critical actions, spend caps, "done" only with an automated completion check | 200 offline tests; mutation check on 13 critical guards; reproducible eval tables |
| [district-heating](https://github.com/Stas2903/district-heating) | My graduation project: a 24-hour heat-network forecaster and a training-free anomaly detector built from CLIP, physics checks and a Gemini arbiter | On private real data: 8.31% sMAPE (MASE 0.87); recall from 27% to 80.5% against pseudo-labels. The repo itself runs on synthetic data |

## How I work

- **Evaluation first.** Scenario suites, simulated users and cross-family LLM judges come before the feature, and every guard is tested by breaking it on purpose.
- **Humans approve what matters.** Payments, outside contact and irreversible actions wait for a person.
- **Rollback is one line.** Every model or prompt change can be reverted in config.
- **Decisions are written down,** so the next engineer knows why.

## Stack

- **LLMs and agents:** LangGraph, tool calling, structured outputs, prompt engineering, Claude, Qwen, OpenAI API, Gemini, n8n
- **Retrieval:** hybrid BM25 + vector search, pgvector, chunking, reciprocal rank fusion, rerankers
- **Serving and evaluation:** vLLM, LiteLLM, Langfuse, prompt caching, LLM-as-judge, prompt-injection guardrails, mutation testing
- **Engineering:** Python, FastAPI, PostgreSQL, Docker, GitLab CI/CD, GitHub Actions, pytest, AWS
- **Machine learning:** PyTorch, TensorFlow, scikit-learn, XGBoost, LightGBM, LSTM

## Background

- AI Geeks, an AI consulting startup in Seoul (full-time contractor, remote, 2024–2026). Technical Manager on 6 AI and data projects (3 of 6 clients came back with follow-on work), then AI Engineer: a resume-to-role matching agent that agreed with recruiters' top pick for 96.6% of 46 resumes
- Part-time evening AI instructor at VeraVla edu: 80+ career-changers taught, including a module I added on AI agents
- B.Sc. in Data Science, Hanyang University (scholarship): final semester with a light course load, graduating Aug 2027

## Contact

Open to AI engineer roles from December 2026: full-time in Seoul, or remote from KST (UTC+9) as a contractor or through an employer of record. Also open to freelance projects. F-4 visa, no sponsorship needed in Korea.

- Email: kimstanislav2903@gmail.com
- LinkedIn: [linkedin.com/in/stanislav-kim-ai](https://www.linkedin.com/in/stanislav-kim-ai/)
