# Editing the Paper in Overleaf (via your GitHub fork)

Overleaf can sync directly with a GitHub repo, so you can edit your section in Overleaf's visual
editor and push the `.tex` back to GitHub for the CI build. **Always go through your fork**, not the
org repo directly.

## One-time setup
1. **Fork** this repo on GitHub (see [CONTRIBUTING.md](CONTRIBUTING.md)).
2. In Overleaf: **New Project → Import from GitHub** (requires linking your GitHub account once under
   *Account Settings → GitHub*).
3. Pick your fork `…/Enigma-Decentralized-Student-Marketplace-Publication`.
4. In Overleaf **Menu → Main document**, set it to `main.tex`.
5. Overleaf compiles `main.tex` and shows the live PDF.

## Edit → push cycle
1. Edit **only your `sliceN_*/sliceN_*.tex`** in Overleaf.
2. **Menu → GitHub → Push Overleaf changes to GitHub** — commit to a branch named
   `paper/<member>-<slice>` on your fork (not `main`).
3. On GitHub, open a **PR from your fork's branch into this repo's `develop`**.
4. The **Build paper** workflow compiles and attaches `main.pdf` — verify it before review.

## Keep in sync
- Pull others' merged changes back into Overleaf: **Menu → GitHub → Pull GitHub changes into Overleaf**.
- Keep each section's `.md` mirror roughly in step with the `.tex` for readable diffs.

> The **canonical PDF** is the one built by CI from `main` — not a manual Overleaf export. Overleaf is
> the editor; GitHub is the source of truth.
