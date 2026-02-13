# O-Vault

> The Obsidian knowledge layer — where raw course materials become organized, personal understanding through notes, study guides, and exam prep.

---

## Purpose

The O-Vault is the **Obsidian vault** that sits alongside the repository's source files. While the repo root holds code, textbooks, syllabi, and assignments, the vault holds **your understanding** of that material — notes you've written, study guides you've built, flashcards you've created.

It mirrors the same Pedagogy/Andragogy/Heutagogy structure as the repo root but contains only knowledge artifacts, not source materials.

## What Belongs Here

- Markdown notes (chapter summaries, lecture notes, concept explanations)
- Study guides and cheat sheets
- Flashcard sets (Markdown-based or Anki import files)
- Research paper annotations and analysis
- Any Obsidian-native content (notes that benefit from wikilinks, tags, and graph view)

## What Does NOT Belong Here

- Source code or assignment submissions (those stay in the repo root)
- PDFs, textbooks, or syllabi (those stay in `Pedagogy/Semester #/Textbooks/` or `Syllabi/`)
- Large binary files (images, videos, datasets)

## Naming Conventions

- Notes: Descriptive titles, spaces allowed (Obsidian-friendly)
- Directories: Match the course code or topic they cover

## Structure

```
O-Vault/
├── Learning/
│   ├── Pedagogy/
│   │   └── UNC/
│   │       └── s4/            ← Semester 4 courses
│   │           ├── COMP110/
│   │           ├── DATA120/
│   │           ├── PSYC101/
│   │           └── STOR155/
│   ├── Andragogy/
│   └── Heutagogy/
│       ├── courses/
│       └── research-notes/
└── Navigation Index/          ← Central hub linking to all READMEs
```
