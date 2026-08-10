# Guardrails Web Experience (`grw`)

A focused BMad module for customer journeys, landing/home page references with ordered sections and cinematics, static and video-source scroll-driven visual storytelling, licensed video sourcing and frame packages, verified asset rights, visual quality, search, web delivery, paid media, organic social content, creative video, and AI image generation. It guards against generic journeys, anonymous pages, unsupported ranking promises, unplanned posts, and unmeasured spend.

This is a focused BMad module in the [Guardrails](https://github.com/mlarese/bmad-module-guardrails)
bundle. It keeps the same behavior and shared memory while installing only the figures and
workflows for the web experience area.

> **Generated.** This repository is produced by `tools/build_modules.py` in the
> [bmad-module-guardrails](https://github.com/mlarese/bmad-module-guardrails) repository.
> Make changes there and regenerate; local changes here will be overwritten.

## Agents

| Agent | Role | Skill | Focus |
| ----- | ---- | ----- | ----- |
| 👁️ Iris | Design Critic | `grl-agent-ui-critic` | UI, landing pages, markup, CSS, typography, palettes, density, and layout. |
| 🔎 Nora | SEO Strategist & Search Systems Auditor | `grl-agent-seo` | Search intent, crawling, indexing, content, structured data, and Search Console. |
| 📣 Dalia | Media Manager & Paid Advertising Strategist | `grl-agent-ads` | Google Ads, paid advertising, audiences, creative, tracking, consent, budgets, and policies. |
| 📱 Sofia | Social Media & Content Strategist | `grl-agent-social` | Organic strategy, content pillars, calendars, posts, captions, community, and metrics. |
| 🎬 Marco | Advertising Creative Director & Short-form Video Producer | `grl-agent-creative` | Advertising concepts, design, scripts, storyboards, shot lists, Reels, TikToks, and Shorts. |
| 🖼️ Elio | AI Image Generation & Post-production Specialist | `grl-agent-imaging` | Nano Banana, Imagen, GPT Image, Photoshop, prompts, masks, subject consistency, provenance, and export. |
| 🧭 Marea | Customer Journey & Visual Storytelling Strategist | `grl-agent-customer-journey` | Client story, location, business placement, landing/home page reference packages, ordered sections, CTAs, customer journeys, visual narratives, static and video-source scroll cinematics, timecode/frame plans, online asset sources and rights gates, and contextual search systems; no upload or publication is implicit. |

## Skills and workflows

| Skill | Purpose |
| ----- | ------- |
| `grw-profile` | Project profile | Collects the project context shared by every installed figure. |
| `grw-board` | Multidisciplinary review | Convenes the relevant figures on one artifact and returns a review summary or release verdict. |
| `grl-web` | Web experience delivery | Moves landing pages and websites from a conversion brief through visual review, accessibility, SEO, and delivery. |
| `grl-video-to-scroll` | Video-to-scroll frame packages | Runs a tool preflight, asks before installing missing capabilities, collects the customer journey, searches for usable video sources, extracts authorized local frames, and hands a validated scroll specification to web delivery. |
| `grl-ads` | Paid media operations | Audits, plans, tracks, optimizes, preflights, and applies paid-media change sets behind approval and rollback gates. |
| `grl-social` | Organic social strategy | Builds social strategies, calendars, content, audits, and measurement plans without scheduling or publishing. |
| `grl-social-creative` | Social creative production | Turns a brief into producible concepts, scripts, storyboards, shot lists, specifications, and channel variants. |
| `grl-automation` | Controlled automation | Routes work from read-only checks through dry-run to observable execution, with explicit approvals and rollback. |

## Installation

```
bmad install grw
```

As a first step, run `grw-profile`. It collects the project profile — sector, data,
market, stack, and criticality — so each figure can calibrate its review. Without a profile,
the default remains `normal` and the figures start without context.

## Shared memory

The profile lives in `{project-root}/_bmad/memory/grl-shared/project-profile.md`, together
with `decisions.md` and `accepted-risks.md`. All Guardrails modules use the same path, so two
installed modules still share one profile.

## Using it with the bundle

This module installs skills with **the same names** as the `grl` bundle — `grl-agent-ui-critic`
is identical in both. Do not install the full bundle and thematic modules in the same project:
choose the complete bundle, or only the thematic modules you need.

## License

MIT.
