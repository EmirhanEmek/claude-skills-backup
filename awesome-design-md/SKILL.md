---
name: awesome-design-md
description: "Use when the user wants a new UI/screen (web or mobile) to visually resemble a specific known product or brand (e.g. \"make it look like Linear\", \"Stripe-style checkout\", \"Airbnb-like cards\", \"an Expo/Notion mobile feel\"), or asks what design references are available for a given aesthetic. Provides a local library of 73 reverse-engineered DESIGN.md style specs (colors, type, spacing, components, shadows, motion) extracted from real products, each with an HTML preview. Not for general 'make it look good' taste calls with no named reference — use emil-design-eng / design-taste-frontend / impeccable for that."
---

# awesome-design-md reference library

Local, offline clone of [voltagent/awesome-design-md](https://github.com/voltagent/awesome-design-md), cached at:

```
reference/design-md/<slug>/DESIGN.md
reference/design-md/<slug>/preview.html
reference/design-md/<slug>/preview-dark.html
```

Each `DESIGN.md` is a plain-text design-system spec (visual theme, color palette with semantic roles, full typography hierarchy, component styling rules, layout/spacing principles, shadow/elevation system, motion, and guardrails) reverse-engineered from a real product's live site.

## Available references

`apple`, `expo`, `notion`, `linear.app`, `figma`, `framer`, `stripe`, `airbnb`, `cal`, `raycast`, `vercel`, `cursor`, `slack`, `spotify`, `pinterest`, `intercom`, `sentry`, `posthog`, `supabase`, `mongodb`, `clickhouse`, `hashicorp`, `mintlify`, `sanity`, `miro`, `superhuman`, `warp`, `webflow`, `zapier`, `resend`, `composio`, `opencode.ai`, `lovable`, `mastercard`, `coinbase`, `kraken`, `binance`, `revolut`, `wise`, `x.ai`, `claude`, `cohere`, `elevenlabs`, `mistral.ai`, `minimax`, `ollama`, `replicate`, `runwayml`, `together.ai`, `nike`, `shopify`, `uber`, `nvidia`, `dell-1996`, `ibm`, `hp`, `meta`, `tesla`, `bmw`, `bmw-m`, `ferrari`, `lamborghini`, `renault`, `bugatti`, `spacex`, `playstation`, `nintendo-2001`, `theverge`, `wired`, `vodafone`, `starbucks`, `airtable`, `clay`, `voltagent`.

For mobile-app UI work specifically, `expo`, `notion`, `cal`, `raycast`, `superhuman`, and `intercom` are the closest cross-platform/app-shell references (rather than the marketing-site-heavy ones like `nike`/`tesla`/car brands).

## How to use

1. Ask the user (if not already clear) which product's look they want, or infer it from their request.
2. Read `reference/design-md/<slug>/DESIGN.md` to extract the spec. Optionally check `preview.html` / `preview-dark.html` for a visual sanity check before applying it.
3. Copy `DESIGN.md` into the target project's root (this is the convention the source repo expects: "drop one into your project, tell your AI agent to build a page that looks like this").
4. Apply the spec's rules (colors, type scale, spacing, shadows, motion) when generating the UI, adapting web-oriented details (e.g. hover states) to the target platform (native mobile, React Native, etc.) as needed.
5. If no slug matches what the user wants, say so rather than forcing a mismatched reference — fall back to the general taste skills instead.

To refresh this cache later: `git -C reference pull`.
