# VERDICT WEIGHT — Documentation

This repository contains the Mintlify documentation site for **VERDICT WEIGHT™**.

- Live framework: [github.com/Odingard/verdict-weight](https://github.com/Odingard/verdict-weight)
- PyPI: [pypi.org/project/verdict-weight](https://pypi.org/project/verdict-weight/)
- Archived snapshot (DOI): [10.5281/zenodo.19447547](https://doi.org/10.5281/zenodo.19447547)

## Local preview

```bash
npm install -g mint
mint dev
```

Then open `http://localhost:3000`.

## Structure

```
docs.json                    # Mintlify config — required at the repo root
index.mdx                    # Landing page
introduction/                # What it is, why it matters, quickstart
install/                     # PyPI, from-source, verification
architecture/                # Overview, composition rule, completeness
streams/                     # Per-stream documentation (1–8)
api/                         # Python SDK reference + configuration
validation/                  # IEEE hardening + real-world proxy + limitations
testing/                     # Coverage, fuzz/mutation, formal verification
papers/                      # Foundation, Empirical, Architecture papers
gov/                         # Defense positioning + AFWERX CSO + pilots
logo/                        # Light/dark/hero SVGs
favicon.svg
```

## Editing

All content is MDX. Mintlify components used: `Card`, `CardGroup`, `Steps`, `Step`, `Note`, `Tip`, `Warning`, `Info`, `Frame`, `CodeGroup`, `Accordion`, `AccordionGroup`, `Tabs`, `Tab`.

Standard Markdown works everywhere. LaTeX is supported in inline (`$...$`) and block (`$$...$$`) form.

## Things to fill in

A small number of pages contain `{{ INSERT … }}` markers for items only the project owner can supply:

- `papers/paper-1-foundation.mdx` — SSRN URL
- `papers/paper-2-empirical.mdx` — pre-print URL, target venue
- `papers/paper-3-architecture.mdx` — pre-print URL, target venue

Search the repo for `INSERT` to find them all.

## Deploy

Push to `main` after connecting the repo to Mintlify. The dashboard error about `docs.json not found` resolves automatically once this file is present at the repo root.
