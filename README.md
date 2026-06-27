# Enigma Marketplace — Publication Paper

[![Build paper](https://github.com/enigma-group-project/Enigma-Decentralized-Student-Marketplace-Publication/actions/workflows/build-paper.yml/badge.svg)](https://github.com/enigma-group-project/Enigma-Decentralized-Student-Marketplace-Publication/actions/workflows/build-paper.yml)

Modular IEEE (`IEEEtran` conference) source for the project paper. Each section is its own
folder with a `.tex` (compiled) and a `.md` (readable mirror), consolidated by `main.tex`.

## Project links
- **Main repo:** https://github.com/enigma-group-project/Enigma-Decentralized-Student-Marketplace
- **Live demo (GUI):** https://enigma-group-project.github.io/Enigma-Decentralized-Student-Marketplace/
- **Documentation:** https://enigma-group-project.github.io/Enigma-Decentralized-Student-Marketplace/docs/
- **How to contribute:** [CONTRIBUTING.md](CONTRIBUTING.md) · **Edit in Overleaf:** [OVERLEAF.md](OVERLEAF.md)

## Structure (one folder per section; slices owned per member)
IEEE-standard sections plus a modular per-slice reference. `main.tex` consolidates them in order.

| Folder | Section | Owner |
| --- | --- | --- |
| `abstract/` | Abstract | all |
| `introduction/` | Introduction (motivation + roadmap) | all |
| `related_research/` | Related Research | all |
| `motivating_example/` | Motivating Example | all |
| `threat_model/` | Threat Model | all |
| `why_blockchain/` | Why Blockchain: Suitability & Compatibility | all |
| `architecture/` | System Architecture + Threat Mitigations | all |
| `slice1_token/` | Slice 1 — Token + Wallet | **Member 1** |
| `slice2_listings/` | Slice 2 — Listings | **Member 2** |
| `slice3_escrow/` | Slice 3 — Escrow + Ratings | **Member 3** |
| `slice4_reputation/` | Slice 4 — Reputation | **Member 4** |
| `hypothesis/` | Hypothesis | all |
| `performance_metrics/` | Performance Metrics | all |
| `methodology/` | Methodology | all |
| `empirical_evidence/` | Empirical Evidence (status + gas/latency tables) | all |
| `conclusions_future_work/` | Conclusions + Future Work | all |
| `references/` | References | all |

**Each member edits only their `sliceN_*` folder.** Leave the other files alone unless coordinating.

## Build
- **Overleaf:** upload this folder, set the main document to `main.tex`.
- **Local (TeX Live / MacTeX):** `make`  → produces `main.pdf`.
- **CI:** `.github/workflows/build-paper.yml` compiles `main.tex` and uploads `main.pdf` as an artifact.

> ⚠️ Fill the author names/emails for Members 2–4 in `main.tex`, and complete the `[Member N: refine]`
> notes in each slice section.
