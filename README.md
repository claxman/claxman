# Chaitanya Laxman

AI researcher and Principal AI Engineer. Indian, based in Dubai. My work sits where post-training, agents, evaluation, and inference meet: training open-weight models to do specific jobs well, building the systems that run them in production, and measuring whether they actually got better. I contribute upstream to the projects that stack depends on.

<!-- oss-wins:start -->

## Open-source contributions

9 merged upstream across 4 repos. Updated 2026-09-22.

| Repo | Merged | Summary |
|---|---|---|
| [unslothai/unsloth](https://github.com/unslothai/unsloth) | [6 merged](https://github.com/unslothai/unsloth/pulls?q=is%3Apr%20author%3Aclaxman%20is%3Amerged) | These changes stop the chat and studio UI from losing state: queued or stopped prompts, saved context, compare-pane settings, and sandbox files survive interruptions, model switches, and snapshot paths, and the CLI API key is reused across runs. |
| [e2b-dev/E2B](https://github.com/e2b-dev/E2B) | [1 merged](https://github.com/e2b-dev/E2B/pulls?q=is%3Apr%20author%3Aclaxman%20is%3Amerged) | Sandbox creation now checks the options you pass before it asks for an API key, so a bad config fails fast with a clear error instead of an unrelated auth complaint. |
| [google/adk-python](https://github.com/google/adk-python) | [1 merged](https://github.com/google/adk-python/pull/7039) | Adds a test that LlmAgent still accepts candidate_count on generate_content_config. |
| [twentyhq/twenty](https://github.com/twentyhq/twenty) | [1 merged](https://github.com/twentyhq/twenty/pulls?q=is%3Apr%20author%3Aclaxman%20is%3Amerged) | Percentage fields now save correctly when a user types a value with a trailing percent sign, so entering "50%" no longer gets dropped or mangled on write. |

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
