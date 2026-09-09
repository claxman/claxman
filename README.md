# Chaitanya Laxman

AI researcher and Principal AI Engineer. Indian, based in Dubai. My work sits where post-training, agents, evaluation, and inference meet: training open-weight models to do specific jobs well, building the systems that run them in production, and measuring whether they actually got better. I contribute upstream to the projects that stack depends on.

## Research and models

Fine-tuned and shipped Qwen3.6-27B with QLoRA/SFT, then on-policy context distillation from a 24.8K-token expert-rule corpus. Merged adapters into a standalone bf16 checkpoint and served it on H100s with vLLM at 73K context.

Built the self-improving loop around it: production generations become critic-ranked Best-of-N preference pairs and broken-to-repaired training examples for DPO and RLVR/GRPO, with deterministic verifiable rewards and frozen held-out gates deciding whether a candidate model is promoted or rejected. On a locked 30-task by 3-seed harness, rule distillation cut mean defects 54% (0.79 to 0.36 per output) and raised strict zero-defect passes from 17% to 53%.

[DeepField](https://deepfield.one): an independent research program on whether the early signatures of significant events can be detected ahead of consensus.

Earlier, a CNN for object amplification in IBM Watson PowerAI Vision.

## Systems I've built

**CiaraAI.** Stateful agent platform running autonomous multi-step workflows across CRM, lead routing, scheduling, payments, voice, WhatsApp, and chat. 200K+ interactions, 97% automation, sub-2s responses, about 70% lower cost than the stack it replaced.

**[Claws](https://github.com/Laxcorp-Research/claws).** Visual multi-agent orchestration on the OpenClaw runtime for manager-worker-reviewer teams. Workflow definitions compile to executable agent configs with concurrent execution, tool integrations, runtime monitoring, and failure recovery.

**[Raven](https://github.com/Laxcorp-Research/project-raven).** Open-source AI meeting copilot: system audio plus mic capture, WebRTC AEC3 echo cancellation, real-time transcription, live assistance. 400+ stars.

**Evaluation and observability.** A 559-rule learning-science evaluation framework catching about 92% of defects before human QC, and root-cause instrumentation across 500K+ production AI failures, turned into regression signals.

**Stack.** Python, TypeScript, PyTorch, Unsloth, vLLM, LangGraph, PostgreSQL, Kubernetes, AWS, GCP. Claude Certified Architect (Foundations).

[LinkedIn](https://linkedin.com/in/chaitanyalaxman) · [@dantelaxman](https://x.com/dantelaxman) · chaitanyalaxman118@gmail.com

<!-- oss-wins:start -->

## Open-source contributions

4 merged upstream across 2 repos, 18 open. Updated 2026-09-09.

| Repo | PR | What changed |
|---|---|---|
| [e2b-dev/E2B](https://github.com/e2b-dev/E2B) | [#1824](https://github.com/e2b-dev/E2B/pull/1824) | Validate sandbox create options before requiring an API key |
| [unslothai/unsloth](https://github.com/unslothai/unsloth) | [#10505](https://github.com/unslothai/unsloth/pull/10505) | Recover compare-pane settings when the chat is on a snapshot path |
| [unslothai/unsloth](https://github.com/unslothai/unsloth) | [#10447](https://github.com/unslothai/unsloth/pull/10447) | Restore saved context after Switch Back to a snapshot-path model |
| [unslothai/unsloth](https://github.com/unslothai/unsloth) | [#10445](https://github.com/unslothai/unsloth/pull/10445) | Keep queued prompts when the user stops generation |

[All merged](https://github.com/pulls?q=is:pr+author:claxman+is:merged) · [Open](https://github.com/pulls?q=is:pr+author:claxman+is:open)

<!-- oss-wins:end -->
