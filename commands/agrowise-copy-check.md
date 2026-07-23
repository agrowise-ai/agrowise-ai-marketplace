---
description: "Lint any AgroWise marketing copy against the brand guardrails before it ships. Loads the agrowise-brand canon and checks the copy on six axes — leads with the problem (not the tech), persona-matched, every agronomic claim sourced, no standalone-hardware pitch, no invented facts, transparent pricing language — returning a pass/fail per axis with specific fixes. The gate any human- or agent-written copy passes through."
---

# /agrowise-copy-check

The brand's quality gate. Paste in copy — a blog post, landing page, email, ad, social post, deck slide — and get a specific, guardrail-by-guardrail verdict with fixes. Works on copy written by a human or by another agent.

## Input

`$ARGUMENTS` — the copy to check (inline, or a path/URL to read). If the intended persona isn't obvious from the copy, infer it and note the assumption.

## Steps

1. **Load the canon.** Read the `agrowise-brand` skill for the guardrails, persona matrix, and voice.

2. **Score each axis** — for every one, give PASS / FAIL / WEAK, quote the offending line, and give the concrete fix:
   - **Problem-first** — opens on the reader's pain, not "AI/robotics/IoT" or product features.
   - **Persona-matched** — one clear persona; pain, angle, and proof all match the matrix (grower = production, owner = margin, manager = crew/callbacks/PHC).
   - **Sourced** — every substantive agronomic claim has a real, extension-grade citation. Un-sourced claims are the most serious failure — flag each one.
   - **No standalone-hardware pitch** — Canopy framed as the data feed inside AgroWise, never sold as sensors.
   - **Positioning discipline** — claims the niche ("agronomy copilot for wholesale growers/nurseries"), not a broad "ag-AI platform"; copilot-beside-the-expert stance, not "replace your agronomist."
   - **Voice & pricing** — plain grower-to-grower credibility, no hype adjectives; any pricing language is transparent, not opaque/sales-led.

3. **Verdict.** Overall SHIP / REVISE / REWRITE, with the one or two changes that matter most. If REWRITE, offer to redraft via `/agrowise-blog-draft` (for posts) or inline.

4. **Be strict on sourcing and honest on voice.** A confident, well-written paragraph that makes an un-sourced agronomic claim still fails — trust is the moat. Don't wave copy through because it reads well.

## Guardrails

- Un-sourced agronomic claim = automatic FAIL on the Sourced axis; never a soft pass.
- Quote the specific line for every finding — no vague "tighten the messaging."
- This command judges; it doesn't rewrite unless asked.
