# SSCC 2026 QC Getting‑Started Site
## Repository setup and usage

This repository contains the getting‑started and reference documentation
for the Quantum Chemistry hands‑on sessions of the
CSC Spring School on Computational Chemistry 2026 (SSCC 2026).

The repository is intentionally lightweight and text‑centric.
It does not contain training notebooks or software code; instead,
it provides stable instructions that complement:

- the live course HedgeDoc (base camp)
- the notebook‑based hands‑on materials

---

## Purpose of this repository

This site provides:

- A short orientation for hands‑on participants
- Instructions on how to access the computing environment
- A clear description of how the hands‑on sessions are structured
  (core session vs. optional sessions)
- Reference instructions for supporting tools (Avogadro2)

This site intentionally does not contain:

- Detailed scientific instructions (these are inside the notebooks)
- The live course schedule or announcements (handled via HedgeDoc)
- Training notebooks or software installation instructions

---

## Repository structure

    .
    ├── docs/
    │   ├── index.md          # Landing page / orientation
    │   ├── environment.md    # Access to CSC Jupyter for Courses
    │   ├── workflow.md       # Session structure and how to run the hands-on
    │   └── avogadro.md       # Avogadro2 via Mahti Open OnDemand
    ├── mkdocs.yml            # MkDocs configuration
    └── .github/workflows/
        └── mkdocs.yml        # GitHub Actions publishing workflow

All documentation content lives under docs/.

---

## Site generator

The site is built using MkDocs with the Material for MkDocs theme.

MkDocs:
- Converts Markdown files in docs/ into static HTML
- Generates navigation based on mkdocs.yml
- Produces a static site suitable for GitHub Pages

---

## Publishing model (current setup)

### Automatic publishing via GitHub Actions

The repository is configured so that every commit to the main branch
automatically rebuilds and republishes the site.

This is implemented using the workflow:

    .github/workflows/mkdocs.yml

### What happens on each push to main

1. GitHub Actions checks out the main branch
2. MkDocs and required dependencies are installed
3. The site is built from the Markdown files in docs/
4. The generated HTML is pushed to the gh-pages branch
5. GitHub Pages serves the updated site

As a result:

- Local edits followed by git push publish the site automatically
- Edits made directly via the GitHub web interface also publish automatically
- No manual deployment command is required

---

## Branch roles

    Branch      Purpose
    ---------   ----------------------------------------
    main        Source Markdown files (docs/)
    gh-pages    Generated static HTML (do not edit manually)

The gh-pages branch contains only generated output and may be
overwritten at any time by the deployment workflow.

---

## Recommended editing workflow

### Local editing

    git add docs
    git commit -m "Update SSCC 2026 QC documentation"
    git push

The site is rebuilt and published automatically after the push.

### Browser-based editing

- Edit files under docs/ in the GitHub web interface
- Commit to the main branch
- The site is rebuilt and published automatically

---

## Alternative deployment options

The following alternatives are valid, but not active in this repository.

### Alternative 1: Manual MkDocs deployment (mkdocs gh-deploy)

In this deployment model, publishing is done manually from a local
development machine. This can be useful when one wants to preview
the site carefully before publishing, or when automatic deployment
is not desired.

#### Prerequisites

- MkDocs installed locally (for example via pip)
- All required MkDocs plugins and themes installed
- Git configured with push access to the repository

#### Typical workflow

1. Make local changes to the documentation under docs/

2. Preview the site locally using the built‑in development server:

       mkdocs serve

   This starts a local server (typically at http://127.0.0.1:8000)
   and allows interactive preview while editing.

3. Build the static site locally:

       mkdocs build

   This generates the static HTML under the site/ directory.

4. Publish the site to GitHub Pages:

       mkdocs gh-deploy --force

   This command builds the site (if needed) and overwrites the
   gh-pages branch with the generated HTML.

#### Notes

- The gh-pages branch is treated as generated output and is
  intentionally overwritten on each deployment.
- Any commits made directly to gh-pages may be lost.
- When this model is used, the GitHub Actions workflow
  .github/workflows/mkdocs.yml must be removed or disabled
  to avoid double deployment.

---

### Alternative 2: GitHub Pages rendering directly from main/docs

GitHub Pages can be configured to render Markdown directly from
main/docs without using MkDocs.

This approach is not recommended here because:

- Navigation is limited
- MkDocs features (search, structured navigation, anchors) are lost
- Rendering differs from local MkDocs previews

---

## Recommended mode going forward

For SSCC 2026 and similar training events:

- Use GitHub Actions automatic deployment
- Treat main as the single source of truth
- Treat gh-pages as generated output only
- Do not manually edit the gh-pages branch
- Do not use mkdocs gh-deploy while automatic deployment is enabled

This minimizes friction during the course and allows quick fixes via
browser edits if needed.

---

## Relationship to other course resources

### HedgeDoc
Live schedule, announcements, Q&A, and coordination

### Training notebooks
All scientific and computational instructions

### This site
Stable reference for environment access, session structure,
and supporting tools

Each component has a clearly separated role to avoid duplication
and inconsistencies.

---

## Summary

This repository is intentionally simple:

- Markdown content under docs/
- Built with MkDocs
- Automatically published on every push to main
- Designed to support, not replace, live course materials

Any changes to the publishing model should be made deliberately
and documented here to avoid ambiguity.
