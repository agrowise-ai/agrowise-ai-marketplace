# agrowise-marketing

AgroWise brand + marketing automation. Ships the **brand canon as a loadable lens** plus workflows to evolve the positioning and produce on-brand, source-grounded content. Every output leads with the problem solved, cites extension-grade sources, and stays persona-matched to grower / owner / landscape-manager buyers.

A hosted plugin in the [eflow multi-plugin marketplace](../../plugins/README.md). It lives at `plugins/agrowise-marketing/` and is registered in the root `.claude-plugin/marketplace.json`.

## What's inside

```
plugins/agrowise-marketing/
  .claude-plugin/plugin.json
  skills/
    agrowise-brand/SKILL.md    # the brand canon as a judgment lens (the spine)
  commands/
    agrowise-brand-evolve.md   # evolve positioning from new evidence (gated)
    agrowise-blog-draft.md     # draft an on-brand, source-grounded blog post
    agrowise-content-plan.md   # plan a persona-tagged content calendar / campaign
    agrowise-copy-check.md     # lint any copy against the brand guardrails
  selfheal.manifest.yaml
  README.md
```

The `agrowise-brand` skill is not run directly — the four commands load it as their lens, so brand voice, the segment×persona matrix, and the do/don't guardrails are applied consistently across drafting, planning, and checking.

## Positioning source of truth

The canonical, human-facing brand position lives in the **product repo** at `agrowise-app/docs/brand-positioning.md`. This plugin's `agrowise-brand` SKILL is that positioning *compiled into the automation layer* so it works wherever the plugin runs (including phone/cloud, where the product repo isn't checked out).

`/agrowise-brand-evolve` is the reconciler: it edits the product doc first (operator-gated), then regenerates the SKILL frame. If the two disagree, the product doc wins.

## Install

```
/plugin marketplace add ebizuwo/eflow
/plugin install agrowise-marketing@eflow
```

## Typical loop

1. `/agrowise-content-plan Q3 calendar, focus nurseries` — get a prioritized, persona-tagged plan.
2. `/agrowise-blog-draft container gardenia root rot, for head growers` — draft a grounded post.
3. `/agrowise-copy-check <paste draft or landing copy>` — gate it against the guardrails before it ships.
4. `/agrowise-brand-evolve <new research or win-loss note>` — fold what you learn back into the positioning.

## Authoring

- Commands live in `commands/` as `*.md`, prefixed `agrowise-` to avoid sibling-plugin collisions.
- The brand lens lives in `skills/agrowise-brand/SKILL.md`; evolve it through `/agrowise-brand-evolve`, not by hand, so the product doc stays upstream.
- After changing this plugin's manifest or its commands/skills/agents inventory, regenerate the marketplace index from the repo root:

  ```
  bash bin/generate-index.sh > INDEX.md
  ```

  The `validate-marketplace` CI fails the PR on `INDEX.md` drift.

## Roadmap — automating the company

v1 is the marketing spine. Natural next skills as the company grows: `agrowise-landing-page` (persona landing pages from the matrix), `agrowise-social` (channel-native repurposing of a post), `agrowise-seo-audit` (AI-search authority tracking), `agrowise-win-loss` (structured demo feedback → `/agrowise-brand-evolve`), and sibling plugins for adjacent domains (sales, support) that load the same `agrowise-brand` lens.

## Positioning changelog

- 2026-07-23 — Initial brand canon established (independent agronomy copilot for specialty horticulture; nursery beachhead + landscape PHC second segment). From the 4-stream market/competitor/persona/GTM research; full sources in `agrowise/docs/agrowise-positioning-research-2026-07-23.md`.
