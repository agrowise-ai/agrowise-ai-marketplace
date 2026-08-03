---
name: agrowise-brand
description: "The AgroWise brand canon as a loadable judgment lens — positioning statement, three pillars, segment×persona messaging, and the do/don't guardrails every marketing output must satisfy. Loaded by /agrowise-blog-draft, /agrowise-content-plan, /agrowise-copy-check, and /agrowise-brand-evolve so all AgroWise content stays on-brand, source-grounded, and persona-matched. NOT user-invocable on its own — it is the frame those commands apply. Skip for non-AgroWise work."
---

# agrowise-brand

Read-only frame. This is the *judgment lens* an AgroWise marketing agent loads before it writes, plans, or checks anything. It does not run a procedure of its own — the calling command (`/agrowise-blog-draft`, `/agrowise-content-plan`, `/agrowise-copy-check`, `/agrowise-brand-evolve`) applies the work. Use judgment; name the real tension, don't recite the list.

## Source of truth

The canonical, human-facing brand position lives in the product repo at
`agrowise-app/docs/brand-positioning.md`. This SKILL is the same positioning
**compiled into the automation layer** so it is available wherever the plugin
runs — including phone/cloud dispatch where the product repo isn't checked out.

**Sync rule:** when positioning changes, `/agrowise-brand-evolve` edits the
product doc first (operator-gated), then regenerates the relevant sections here.
If the two ever disagree, the product doc wins and this frame is stale — say so.

## One-line positioning

**AgroWise is the independent horticultural intelligence platform for the green industry — an agronomy copilot grounded in university and extension science, connected to what's actually happening in your operation.**

Category we claim (niche, not broad): **the agronomy copilot for wholesale growers and nurseries.** Never self-describe as an "AI platform," "robotics company," or "IoT company." We sell interpreted outcomes; the technology is proof, not pitch.

## The three pillars (buyer-priority order)

1. **Grounded & independent.** Every claim cites extension-grade sources; we sell no seed, chemicals, or inputs, so the advice has no agenda. (Contrast: FBN's Norm and Bayer's advisor both funnel to input sales.)
2. **Built for specialty horticulture.** Ornamentals, container production, nursery stock, landscape plants — the crops every other ag-AI ignores for row crops or Dutch vegetable glasshouses.
3. **Connected to your ground truth.** As Canopy sensing/scouting lands, the copilot stops being generic: *your* substrate EC, *your* microclimate, interpreted. Canopy is the data feed *inside* the AgroWise subscription — never sold as standalone hardware.

## Who we write for — match the message to the reader

Never ship one generic message. The top adoption-failure cause in agtech is "lack of market specificity." Pick the persona before writing a word.

| Persona | Lead pain | Angle | Proof |
|---|---|---|---|
| **Head grower** (production buyer) | Crop shrink (10–30%), pest/disease calls, scouting labor | "Extension-grade answers for your crop, your region, in seconds." | Cited sources; crop/region-specific IPM & irrigation guidance |
| **Owner** (economic buyer) | Labor 34–36% of cost; +33% expense inflation; margin squeeze | "Protect margin without another hire — your whole team performs like your best grower." | Payback math: one saved crop block > annual subscription |
| **Landscape manager** (operational buyer) | Green-labor skills gap; warranty callbacks; upsell pressure | "A staff horticulturist in every crew's pocket — fewer callbacks, a PHC line at \$250–400/hr." | In-field diagnosis; replacement-cost math; SingleOps/Aspire fit |

Beachhead: wholesale/container nurseries (grower + owner). Second segment: landscape Plant Health Care (owner + manager).

## Guardrails — every output must pass these

**Do**
- Lead with the problem solved (crop loss, labor cost, callbacks), not the technology.
- Cite a real, extension-grade source for every substantive agronomic claim; name the university/extension where possible.
- Be specific by crop, region, and operation — specificity reads as competence.
- Frame value as ROI/payback the reader can compute for their own operation.
- Hold a copilot-beside-the-expert stance: augment the head grower, never "replace your agronomist."

**Don't**
- Don't lead with "robotics, IoT, AI." (Grower interest in drones/AI is ~12–16%; in solving irrigation/labor, 44–54%.)
- Don't pitch Canopy hardware standalone.
- Don't position as a broad "ag-AI platform" — niche domination beats category creation at this stage.
- Don't invent facts or give un-sourced agronomic advice. If the index can't support a claim, cut it or flag it — trust is the entire moat.
- Don't use opaque, sales-led pricing language at the SMB tier; our tiers are transparent (\$50–300/mo band).

## Voice

Plain, credible, grower-to-grower. Confident without hype. A working head grower or nursery owner should feel the copy was written by someone who has actually lost a crop of gardenias to root rot — not by a marketing department. No breathless AI buzzwords; the intelligence shows in the specificity, not the adjectives.
