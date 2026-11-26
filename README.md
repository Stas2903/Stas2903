# Stanislav Kim

AI Engineer in Seoul. I build LLM agents and RAG systems that run in production, and I measure them before and after every change.

In 2026 I led two engineers on the in-house AI team at RAAF Group, building AI tools for the company's business units:

- Cut LLM cost per agent interview by 97% (to about $0.01) after a 4-model bake-off
- Shortened agent interviews from 10–15 min to under 2.5 min, and parse failures from 33% to 5%
- Built an 80-scenario multilingual evaluation harness that gates every release
- Prompt-injection screen: 7 of 7 red-team attacks held, 0 of 36 clean records blocked
- Led the 2.0 rebuild of a multi-agent platform; its test suite grew from 4,060 to 9,553 tests

The production code is private. The repositories below are clean-room rewrites of the same ideas, on synthetic data, that you can run offline.

## Featured projects

| Repository | What it is | Proof |
| --- | --- | --- |
| [agents-automation](https://github.com/Stas2903/agents-automation) | A multi-role LLM assistant for office work: RAG with access control in SQL, an interviewer with an honesty guard, a 3-layer prompt-injection screen | 986 offline tests, 111 unit mutants and 8 eval mutants, all killed |
| [ai-ceo](https://github.com/Stas2903/ai-ceo) | A director loop that runs a team of AI agents: owner approvals for critical actions, spend caps, "done" only with machine-checked proof | 200 tests, mutation check on 13 guards, reproducible eval tables |
| [district-heating](https://github.com/Stas2903/district-heating) | My graduation project: a 24-hour heat-network forecaster and a training-free anomaly detector built from CLIP, physics checks and a Gemini arbiter | 8.31% sMAPE (MASE 0.87) on real data; recall from 27% to 80.5% against pseudo-labels |

## How I work

- **Evaluation first.** Scenario suites, simulated users and cross-family LLM judges come before the feature, and every guard is tested by breaking it on purpose.
- **Humans approve what matters.** Payments, outside contact and irreversible actions wait for a person.
- **Rollback is one line.** Every model or prompt change can be reverted in config.
- **Decisions are written down,** so the next engineer knows why.

## Stack

- **LLMs and agents:** LangGraph, MCP, tool calling, Claude, Qwen, GPT, Gemini, n8n
- **Retrieval:** hybrid BM25 + vector search, pgvector, reciprocal rank fusion, rerankers
- **Serving and evaluation:** vLLM, LiteLLM, Langfuse, LLM-as-judge, mutation testing
- **Engineering:** Python, FastAPI, PostgreSQL, Docker, GitLab CI/CD, GitHub Actions, pytest, AWS
- **Machine learning:** PyTorch, TensorFlow, scikit-learn, XGBoost, LightGBM

## Background

- AI Engineer and Technical Manager at AI GEEKS, an AI consulting firm for industrial clients (6 projects delivered)
- AI instructor at VeraVla edu: 80+ career-changers taught, including a module I added on AI agents
- B.Sc. in Data Science, Hanyang University (full-tuition scholarship), expected Aug 2027

## Contact

Open to AI engineer roles (full-time, remote or in Seoul) and freelance projects.

- Email: kimstanislav2903@gmail.com
- LinkedIn: [linkedin.com/in/stanislav-kim-ai](https://www.linkedin.com/in/stanislav-kim-ai/)
