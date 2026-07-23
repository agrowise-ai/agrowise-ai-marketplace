---
description: "Draft an on-brand, source-grounded AgroWise blog post for a given topic and persona. Loads the agrowise-brand canon, drafts to the voice + guardrails (leads with the problem, cites extension-grade sources, persona-matched, no un-sourced claims), and returns a review-ready draft — matching the product's human-in-the-loop blog pipeline (no auto-publish)."
---

# /agrowise-blog-draft

Draft a blog post that could sit on the AgroWise site tomorrow — grounded, specific, and unmistakably on-brand.

## Input

`$ARGUMENTS` — the topic, and ideally the target persona and any source material. E.g. "container gardenia root rot, for head growers" or "why plant warranties eat landscape margin, for owners." If persona is unstated, infer the most likely one and say which you chose.

## Steps

1. **Load the canon.** Read the `agrowise-brand` skill. Fix the target persona (head grower / owner / landscape manager) and its lead pain from the messaging table.

2. **Ground it.** Identify the agronomic claims the post will make. For each, find a real extension-grade source — land-grant university extension, USDA, peer-reviewed horticulture. If the AgroWise RAG index / corpus is reachable, retrieve from it; otherwise use `WebSearch`/`WebFetch` against extension domains. **A claim with no citable source does not go in the post** — cut it or mark it `[NEEDS SOURCE]` for the operator.

3. **Draft.** Structure: a problem-first hook in the persona's language → the agronomic explanation with inline citations → what a grower does about it → a soft, non-hypey tie to how AgroWise helps (copilot-beside-the-expert, never "replace your agronomist"). Match the brand voice: plain, credible, grower-to-grower.

4. **Self-check against guardrails.** Before returning, run the draft through the `/agrowise-copy-check` guardrails yourself: leads with the problem (not the tech), every claim sourced, persona-matched, no standalone-hardware pitch, no invented facts. Fix violations.

5. **Return review-ready.** Output the draft with a short header: target persona, primary sources used, and any `[NEEDS SOURCE]` gaps. Do **not** publish — the product pipeline keeps a human approval gate. Offer to save it as a draft where the operator wants (e.g. the product's drafts table or a file).

## Guardrails

- No auto-publish. Human review is a brand-trust feature, not a bottleneck.
- No un-sourced agronomic claim. Ever.
- One persona per post — specificity over reach.
