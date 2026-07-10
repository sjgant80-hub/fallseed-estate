# FallSeed Estate / Letting Agent

> **A Progressive Web App (PWA) seed for UK Estate firms.**
> One HTML file. Four base tools + LLM-agnostic build engine + Fork Seed packager. MIT. Sovereign.

**Live:** https://sjgant80-hub.github.io/fallseed-estate/

## What this is

`fallseed-estate` is a single HTML file you can save to your desktop or install as a PWA. It bundles:

- The four base tools of the Estate wedge (anchor / onboard / paper / practice)
- A build engine that generates new tools on demand using any LLM (WebLLM in-browser, ollama / LM Studio local, Groq / OpenRouter free cloud, or BYOK paid)
- A Fork Seed packager that lets you mutate the seed for a different vertical or client

## Vertical context

Estate agency · letting · property (UK).

## Base tools

| Role | Tool | Purpose |
|---|---|---|
| anchor | [`fallestate`](https://sjgant80-hub.github.io/fallestate/) | Property register · sales / lettings pipeline · deposit log (TDS / DPS) · S.21 / S.8 diary · RTR records · CMP · 12-pt compliance |
| onboard | [`fallestateonboard`](https://sjgant80-hub.github.io/fallestateonboard/) | Client onboarding · CDD / KYC · vendor / landlord ID · source-of-funds · TOBA · vulnerable-customer flag · consent capture |
| paper | [`fallestatepaper`](https://sjgant80-hub.github.io/fallestatepaper/) | TOBA · AST · MA · S.21 · S.8 · S.13 · prescribed information · How to Rent · EPC notice · gas safety notice · DPS / TDS receipts |
| practice | [`fallestatepractice`](https://sjgant80-hub.github.io/fallestatepractice/) | Workflow · diary · reconciliation · CMP · redress scheme + ombudsman log · file reviews · property file audit · KPI tracker |

## Architecture

- **One HTML file** — no build step, no server, no install
- **IDB primary** — every record lives in `IndexedDB` (`fallseed-estate-v2`) on your device
- **BroadcastChannel mesh** — `fall-estate` for cross-tool sync; `fall-signal` for global hello
- **P3 audit chain** — `prevHash` + SHA-256 chained entries on every mutation
- **8-provider LLM cascade** — WebLLM (T1) → ollama / LM Studio (T2) → Groq / OpenRouter free / Google / Cerebras (T3-free) → Anthropic (T3-paid)
- **Streaming** — SSE token-by-token output
- **Fork Seed packager** — serialises a mutated SEED back into a new self-contained HTML

## Sovereignty

- MIT-licensed
- No telemetry, no analytics, no tracking
- All data stays on your device (IDB) — nothing posted unless you wire an external LLM
- Works offline once installed as PWA
- access; upgrades optional

## Cosmology

Prime **1151**, spine-clean mod 127. Mesh channel **`fall-estate`**. Bundle roles **anchor / onboard / paper / practice**. Seal **◊·κ=1**.

Part of the FallSeed family — see [www.ai-nativesolutions.com](https://www.ai-nativesolutions.com).

## Licence

MIT © Simon Gant.


## What kind of seed is this?

A **level-0** seed in the FallSeed family. Built on the Fork Seed primitive — see [the spec](https://www.ai-nativesolutions.com/spec.html) for the four invariants of replication, the SEED schema, and the six-step fork protocol that every conforming seed implements.
