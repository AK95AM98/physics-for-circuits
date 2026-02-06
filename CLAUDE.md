# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

An intelligent textbook for "Circuits for Signal Processing" (EE 2015) at the University of Minnesota, built with MkDocs Material. The course covers analog electrical systems with emphasis on audio circuits: Kirchhoff's laws, op-amps, phasors, Fourier Series, RLC circuits, and filter networks. The textbook is by James Nilsson & Susan Riedel, "Electric Circuits, 11th Ed."

**Author:** Prof. Sharat Batra

## Current State

The repository is in early setup. The `main` branch contains only this README. A deployed MkDocs Material site exists on the `gh-pages` branch with initial prompt content and a concept list CSV (~150 concepts with dependency mappings).

## Build & Deploy

```bash
# Install dependencies
pip install mkdocs-material

# Local development server
mkdocs serve

# Build static site
mkdocs build

# Deploy to GitHub Pages
mkdocs gh-deploy
```

**Note:** The `mkdocs.yml` config and `docs/` source directory need to be created on `main` before these commands will work. The gh-pages branch was deployed but source files were not committed to main.

## Architecture

This is an MkDocs Material "intelligent textbook" project. Expected structure once set up:

- `mkdocs.yml` — site configuration
- `docs/` — markdown source content
- `docs/prompts/` — course description and concept enumeration prompts
- `docs/learning-graph/` — concept list CSV and learning graph visualizations
- `site/` — build output (gitignored)

## Key Content

The concept list (`prompts/conceptlist.csv` on gh-pages) defines ~150 electrical engineering concepts with dependency relationships, forming the learning graph backbone. Concepts range from foundational physics (charge, current, voltage) through advanced topics (Bode plots, Fourier Series, filter design).
