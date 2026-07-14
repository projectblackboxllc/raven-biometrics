# Raven Biometrics

**Continuous biometric authentication that tells an impostor apart from a genuine user under duress, over a governed, audit-ready data platform.**

A product of [Project Black Box LLC](https://projectblackbox.tech).

This repository hosts the public product page and the whitepaper. **It does not contain source code.** The implementation is private.

- **Product page:** the GitHub Pages site (see below)
- **Whitepaper:** [`assets/Raven_Biometrics_Whitepaper.pdf`](assets/Raven_Biometrics_Whitepaper.pdf)

## What it is

Raven enrolls a per-user statistical template, then scores every capture as a distance from that template, split into an **identity** component (stable, person-specific channels) and a **stress** component (acute-stress channels). That split resolves three states a binary matcher collapses into one:

| Identity distance | Stress distance | Decision |
|---|---|---|
| Low | Low | **Genuine** — access granted |
| Low | High | **Duress** — the enrolled person, coerced or in distress; denied and flagged |
| High | any | **Impostor** — a different person; denied |

Every sample, decision, anomaly, template, and consent record is persisted to a governed data platform with an append-only, hash-chained audit trail, HMAC-signed events, and right-to-be-forgotten.

## Honest scope

A working reference architecture and harness, not a certified security product. The biometric input is synthetic behind a real-sensor interface; liveness and event-signing are demonstrative. The value, the identity/stress decision split and the governed, auditable data platform, is real and reproducible. See the whitepaper's "Honest Scope" section.

## Enabling the page (GitHub Pages)

1. Push this repository to the `projectblackbox` organization (public).
2. Settings → Pages → Source: deploy from `main`, root.
3. The `.nojekyll` file ensures assets are served as-is.
4. Recommended: enable branch protection on `main`.

---

© 2026 Project Black Box LLC. All rights reserved. CAGE 11FU4 · ORCID 0009-0006-9717-7161.
