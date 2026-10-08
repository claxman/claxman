# Chaitanya Laxman

AI researcher and Principal AI Engineer. Indian, based in Dubai. My work sits where post-training, agents, evaluation, and inference meet: training open-weight models to do specific jobs well, building the systems that run them in production, and measuring whether they actually got better. I contribute upstream to the projects that stack depends on.

<!-- oss-wins:start -->

## Open-source contributions

20 merged upstream across 4 repos. Updated 2026-10-08.

| Repo | Merged | Summary |
|---|---|---|
| [unslothai/unsloth](https://github.com/unslothai/unsloth) | [12 merged](https://github.com/unslothai/unsloth/pulls?q=is%3Apr%20author%3Aclaxman%20is%3Amerged) | Fixes rough edges in the chat and studio UI: stopped or queued prompts stay put, snapshot-path models keep their context and compare settings, and uninstall, eject, and streaming paths behave more predictably. |
| [google/adk-python](https://github.com/google/adk-python) | [5 merged](https://github.com/google/adk-python/pulls?q=is%3Apr+author%3Aclaxman) | Fixes edge cases across agent config, auth, MCP, and LiteLlm so ADK fails early on bad settings (candidate_count) and behaves correctly in less-common setups (Windows VCS paths, public OIDC clients, non-Gemma tool-result roles, MCP grounding metadata). |
| [twentyhq/twenty](https://github.com/twentyhq/twenty) | [2 merged](https://github.com/twentyhq/twenty/pulls?q=is%3Apr%20author%3Aclaxman%20is%3Amerged) | Fixes edge cases around the percent sign: percentage field values entered with a trailing "%" now save correctly, and array containsIlike filters treat "%" as a SQL wildcard as intended. |
| [e2b-dev/E2B](https://github.com/e2b-dev/E2B) | [1 merged](https://github.com/e2b-dev/E2B/pulls?q=is%3Apr%20author%3Aclaxman%20is%3Amerged) | Sandbox creation now checks the options you pass before it asks for an API key, so a bad config fails fast with a clear error instead of an unrelated auth complaint. |

<!-- oss-wins:end -->

## Research and models

Fine-tuned and shipped Qwen3.6-27B with QLoRA/SFT, then on-policy context distillation from a 24.8K-token expert-rule corpus. Merged adapters into a standalone bf16 checkpoint and served it on H100s with vLLM at 73K context.

Built the self-improving loop around it: production generations become critic-ranked Best-of-N preference pairs and broken-to-repaired training examples for DPO and RLVR/GRPO, with deterministic verifiable rewards and frozen held-out gates deciding whether a candidate model is promoted or rejected. On a locked 30-task by 3-seed harness, rule distillation cut mean defects 54% (0.79 to 0.36 per output) and raised strict zero-defect passes from 17% to 53%.

[DeepField](https://deepfield.one): an independent research program on whether the early signatures of significant events can be detected ahead of consensus.

Earlier, a CNN for object amplification in IBM Watson PowerAI Vision.

## Systems I've built

**[CiaraAI](https://ciaraai.com).** Stateful agent platform running autonomous multi-step workflows across CRM, lead routing, scheduling, payments, voice, WhatsApp, and chat. 200K+ interactions, 97% automation, sub-2s responses, about 70% lower cost than the stack it replaced.

**[Claws](https://buildclaws.ai).** Visual multi-agent orchestration on the OpenClaw runtime for manager-worker-reviewer teams. Workflow definitions compile to executable agent configs with concurrent execution, tool integrations, runtime monitoring, and failure recovery.

**[Raven](https://github.com/Laxcorp-Research/project-raven).** Open-source AI meeting copilot: system audio plus mic capture, WebRTC AEC3 echo cancellation, real-time transcription, live assistance. 400+ stars.

**Evaluation and observability.** A 559-rule learning-science evaluation framework catching about 92% of defects before human QC, and root-cause instrumentation across 500K+ production AI failures, turned into regression signals.

**Stack.** Python, TypeScript, PyTorch, Unsloth, vLLM, LangGraph, PostgreSQL, Kubernetes, AWS, GCP. [Claude Certified Architect (Foundations)](https://www.credly.com/badges/0ce8c344-b7bd-4cbc-bcdb-1a77865319bf).

[LinkedIn](https://linkedin.com/in/chaitanyalaxman) · [@dantelaxman](https://x.com/dantelaxman) · chaitanyalaxman118@gmail.com
