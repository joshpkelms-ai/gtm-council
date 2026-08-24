---
title: Attio
type: tool
tags: [tool, revops, tool-integration, ai-gtm, agentic]
last-updated: 2026-08-22
last-updated-time: 12:00
---

# Attio

> AI-native CRM positioning itself as the single system of record and "central connection point for all of your business's context across all the different tools". Relevant to this vault less as a product than as the clearest statement of what a **system of record has to offer an orchestration layer** to be worth building on. Also the employer of [[expert-will-jones]] and the source of two lines [[expert-dave-lynch]] leans on.

## What it is

CRM vendor. Per [[expert-will-jones]]'s own account: ~$116M raised, including a $52M Series B led by Google Ventures, Point Nine and Redpoint; 8,000+ paying customers. Sells across the range, from small businesses buying a couple of seats to enterprises evaluating SAML/SSO. [ESTIMATED - self-reported by an employee on a vendor podcast.]

## Why it matters to the council

**Its "universal context" pitch is [[concept-orchestration-layer]] sold as a product.** Lynch's advice is to buy the system of record and build the connective layer yourself. Attio's counter-position is that the system of record should *be* the connection point. Worth watching as a live test of where the buy/build line settles: if systems of record absorb the connective layer, the GTM engineer's territory shrinks - which is precisely Lynch's own stated worry about his team getting smaller.

**Its three agent surfaces are a usable checklist for [[concept-agent-readiness]].** Jones's stated requirements for a CRM in an agentic stack:

1. **Agents built into the CRM** (AskAttio).
2. **[[tool-mcp]] connections** - Claude, ChatGPT, Gemini and similar connecting directly.
3. **A scriptable API layer** - good enough that "you can basically write scripts that then perform actions inside of your CRM."

That triple is a better agent-readiness rubric than anything else in the corpus, and it generalises past Attio.

**Proactive CRM as the stated direction:** "not only kind of passively holding your data, but actively looking across all of your information and then suggesting what next outcomes should happen or what next actions that you should take." Unshipped as described; treat as roadmap, not capability.

## In the corpus

- The Fin-as-inbound-SDR build runs on it: Fin writes into Attio, Attio writes back into Intercom, cross-populating. See [[source-will-jones-attio-fin-sdr]].
- Nicolas Sharp (co-founder) is the source of the Jevons-paradox argument and "build for the flex, not the forecast" in [[source-dave-lynch-rise-of-gtm-engineering]].
- Compare [[tool-hubspot]] as the incumbent system of record agents read and write.

## Caveats

Everything here is vendor or employee testimony from a single episode. No independent evaluation, no benchmark, no pricing analysis in the corpus. Do not treat the agent-readiness triple as verified capability - treat it as a well-framed *specification* that happens to come from a vendor describing itself.

## Sources

[[source-will-jones-attio-fin-sdr]]; secondary mentions in [[source-dave-lynch-rise-of-gtm-engineering]].

## Related

[[expert-will-jones]] | [[concept-orchestration-layer]] | [[concept-agent-readiness]] | [[tool-mcp]] | [[tool-hubspot]] | [[expert-dave-lynch]] | [[concept-context-assembly]]
