# tools-and-infrastructure

> Utilities, scripts, and custom tools that support the learning process — not learning content itself, but the systems that make learning more efficient.

---

## Purpose

This directory holds **automation, tooling, and infrastructure** that supports the Study Grounds project. Nothing here is course content or study material — it's the machinery that helps you manage, generate, or interact with that content.

## What Belongs Here

- Scripts that automate repository management (file organization, backups, syncing)
- Custom-built study tools (flashcard generators, note formatters, etc.)
- Data processing utilities for course materials
- Configuration files and templates used across the project

## What Does NOT Belong Here

- Course assignments or code (that goes in [Pedagogy](../Pedagogy/README.md) or [Heutagogy](../Heutagogy/README.md))
- Study notes or flashcards (those go in the O-Vault)
- Python virtual environment files (`.venv/` lives at the project root)

## Naming Conventions

- Scripts: Descriptive, lowercase, hyphenated (e.g., `generate-anki-cards.py`)
- Tools: Descriptive directory name (e.g., `flashcard-generator/`)

## Structure

```
tools-and-infrastructure/
├── automation-scripts/     ← Scripts for repo management and workflows
└── study-tools/            ← Custom-built tools to aid studying
```
