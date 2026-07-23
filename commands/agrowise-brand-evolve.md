---
description: "Evolve the AgroWise brand positioning from new evidence — market research, customer/win-loss feedback, competitor moves, or a founder decision. Loads the agrowise-brand canon, weighs the new signal against it, proposes a gated diff to the canonical brand doc (agrowise-app/docs/brand-positioning.md) FIRST, then regenerates the plugin's brand SKILL frame to match. The continuous-improvement loop for positioning — never rewrites the brand silently."
---

# /agrowise-brand-evolve

Evolve the brand positioning deliberately, with a human gate. Positioning is the company's most load-bearing asset — this command proposes changes and shows its reasoning; it never edits the canon without confirmation.

## Input

`$ARGUMENTS` — the new evidence or intent. Examples: a link/paste of new research, a win-loss note ("lost 3 nursery demos because they thought we were just another sensor company"), a competitor move ("IUNU launched a sub-$5k tier"), or a direct instruction ("tighten the landscape message around warranty callbacks").

## Steps

1. **Load the canon.** Read the `agrowise-brand` skill (this plugin) and, if the product repo is on disk, `agrowise-app/docs/brand-positioning.md`. Note which is upstream (the product doc wins on conflict).

2. **Locate the evidence.** If `$ARGUMENTS` references a file or URL, read/fetch it. If it's a raw note, take it at face value. If it's a research request rather than a finding, say so and point the operator at the `ermias.biz:deep-research` skill first — don't evolve positioning on a hunch.

3. **Diagnose the delta.** State plainly: what does this evidence confirm, complicate, or contradict in the current positioning? Tie it to a specific pillar, persona, or guardrail. If it changes nothing, say that and stop — resist positioning drift.

4. **Draft the change.** Propose the smallest edit that captures the learning — a sharpened pillar, a new persona pain, a guardrail, a category-language tweak. Show it as a before/after diff against the product doc's exact wording. Keep the three-pillar spine unless the evidence genuinely breaks it (flag loudly if so).

5. **Gate.** Present the diff and the rationale. Wait for the operator to accept, edit, or reject. Do not write on assumption.

6. **Apply, upstream-first.** On acceptance: edit `agrowise-app/docs/brand-positioning.md` first (via that repo's worktree/PR flow — this is a product change), then regenerate the matching sections of `skills/agrowise-brand/SKILL.md` so the automation frame stays in sync. If the product repo isn't on disk, write the SKILL frame, flag the product doc as pending, and record what still needs to land there.

7. **Log the evolution.** Append a dated one-line entry to this plugin's `README.md` changelog (or a `CHANGELOG.md` if present): what changed in the positioning and why. Positioning history is decision history — keep it.

## Guardrails

- Upstream-first: the product doc is canonical; never let the SKILL frame silently diverge.
- Smallest-change bias: evolve, don't rewrite. A brand that changes every week has no position.
- Evidence-gated: no positioning change without a stated, sourced reason.
