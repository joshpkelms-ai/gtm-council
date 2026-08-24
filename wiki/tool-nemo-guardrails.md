---
title: "Tool: NVIDIA NeMo Guardrails"
type: tool
tags: [tool, agentic, ai-gtm, automation, tool-integration]
last-updated: 2026-06-13
last-updated-time: 15:00
---

# Tool: NVIDIA NeMo Guardrails

> Open-source toolkit for adding programmable guardrails to LLM-based conversational applications. In agentic GTM the relevant use: keep customer-facing or pipeline-embedded AI agents on-topic, on-script, and protected against prompt injection.

## What it is

NVIDIA NeMo Guardrails is a Python library (`pip install nemoguardrails`) that sits between application code and an LLM. You define rails in **Colang** (a Python-like dialog-modelling language), and the library enforces them at runtime without requiring changes to the rest of the application.

Five rail types:

1. **Input rails** -- screen or alter user input before the LLM sees it. Practical use: detect prompt injection from a prospect trying to manipulate an outbound bot; mask sensitive PII in inbound data.
2. **Dialog rails** -- steer the LLM toward predefined conversational paths using Colang flows. Practical use: enforce a qualification script (BANT, MEDDIC) so an AI SDR cannot wander off-topic.
3. **Retrieval rails** -- filter or alter chunks in a RAG pipeline before they reach the LLM. Practical use: block off-brand or confidential documents from a sales-enablement agent.
4. **Execution rails** -- validate input and output for tool/action calls the LLM makes. Practical use: prevent an agent from calling a CRM write function with malformed or out-of-policy data.
5. **Output rails** -- review and optionally block or alter the LLM's response before it is returned. Practical use: self-check facts in a RAG-based content-generation agent; run hallucination detection.

The library ships with a built-in guardrails library covering jailbreak detection, content and topic safety (NVIDIA safety models), fact-checking, hallucination detection, and integrations with ActiveFence, PolicyAI, and AlignScore. An `nemoguardrails evaluate` CLI supports vulnerability scanning against the configured rail set.

## GTM-relevant angles

No vault expert currently references NeMo Guardrails by name. The relevance is structural and inferred, not demonstrated by the council:

- **Customer-facing AI agents.** Any agent that takes unstructured input from prospects (chat qualification bots, inbound triage, email reply classifiers) needs input rails against adversarial or off-script prompts. Dialog rails map directly to sales playbook enforcement.
- **Agentic pipeline integrity.** [[concept-silent-failures]] (Wolfe) argues the prize in agentic pipelines is the auditability layer. Execution and output rails are one concrete implementation: a gate the agent must pass before a write lands in the CRM or a message sends via [[tool-heyreach]].
- **RAG-based sales or enablement agents.** Retrieval rails and output fact-checking are the guardrail answer to the hallucination risk flagged across [[concept-context-assembly]] (Tittarelli) and [[framework-three-rs-enablement]] (Bell).
- **Prompt injection surface.** Any GTM workflow that feeds external data (scraped sites, enriched profiles, inbound emails) into an LLM prompt has an injection surface. Input rails are the architectural response.

[INFERRED] These connections are derivable from the library's design and the council's agent-safety themes; no council member has tested or recommended NeMo Guardrails specifically.

## Scope note

The vault's tool pages are normally grounded in a named practitioner's usage. This is a reference page for a legitimate infrastructure tool at the edge of the GTM-engineering scope: it belongs in "AI-GTM and agentic selling" in so far as guardrails are part of building safe, production-grade GTM agents, but it is not a GTM-native tool and the council is silent on it. Treat claims about its GTM fit as [INFERRED] until a practitioner source appears.

## Source

GitHub README: NVIDIA-NeMo/Guardrails (v0.21.0 at time of clipping). Documentation: docs.nvidia.com/nemo/guardrails. EMNLP 2023 paper: Rebedea et al., "NeMo Guardrails: A Toolkit for Controllable and Safe LLM Applications with Programmable Rails."

## Related

[[concept-silent-failures]] | [[concept-context-assembly]] | [[framework-three-rs-enablement]] | [[tool-claude-code]] | [[tool-mcp]] | [[concept-earn-the-right-to-automate]] | [[framework-sales-orchestration]]
