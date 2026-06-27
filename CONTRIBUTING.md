# Contributing to the Enigma Marketplace Paper

This repo holds the modular IEEE paper. Each member owns **one slice section**. We use a
**fork → edit → PR into `develop`** workflow; owners merge `develop → main`.

## Section ownership
| Folder | Section | Owner |
| --- | --- | --- |
| `slice1_token/` | Slice 1 — Token + Wallet | **@rangasam** (member1) |
| `slice2_listings/` | Slice 2 — Listings | **@vp2244** (member2) |
| `slice3_escrow/` | Slice 3 — Escrow / Trade | **@sanon-dev** (member3) |
| `slice4_reputation/` | Slice 4 — Reputation | **@on404nyu** (member4) |
| `abstract/`, `introduction/`, `architecture/`, `evaluation/`, `conclusions_future_work/`, `references/` | shared | coordinate |

**Edit only your `sliceN_*` folder** unless you're coordinating a shared section.

## Workflow
1. **Fork** this repo (top-right *Fork*).
2. Branch from `develop`:
   ```bash
   git clone git@github.com:<you>/Enigma-Decentralized-Student-Marketplace-Publication.git
   cd Enigma-Decentralized-Student-Marketplace-Publication
   git checkout -b paper/<member>-<slice> origin/develop
   ```
3. Edit your section's `.tex` (and keep the `.md` mirror in sync). See [OVERLEAF.md](OVERLEAF.md) to edit in Overleaf.
4. Add your name + email to the `\author{}` block in `main.tex` (Members 2–4).
5. Push and open a **PR into `develop`** (never `main`).
6. CI (**Build paper**) compiles `main.tex`; check the PDF artifact on your PR before requesting review.
7. Owners merge `develop → main` once sections are complete; `main` is the camera-ready branch.

## Build
- **CI:** `.github/workflows/build-paper.yml` builds `main.pdf` on every push/PR and uploads it as an artifact.
- **Local:** `make` (needs TeX Live / MacTeX) → `main.pdf`.
- **Overleaf:** see [OVERLEAF.md](OVERLEAF.md).
