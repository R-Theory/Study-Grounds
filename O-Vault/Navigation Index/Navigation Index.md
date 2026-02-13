# Navigation Index

> The central hub for understanding how **Study Grounds** is organized. Every directory in the project has a `README.md` spec inside it describing its purpose, what belongs there, and organizational criteria.

---

## How This Project Is Organized

Study Grounds is organized around three methods of learning, each represented by a top-level directory in both the **repository root** and the **Obsidian vault** (`O-Vault/`):

| Method | Who Decides What to Learn? | Where It Lives |
|---|---|---|
| **Pedagogy** | The instructor (formal courses) | `Pedagogy/` |
| **Andragogy** | You, with expert guidance (online courses, certifications) | `Andragogy/` |
| **Heutagogy** | Entirely you (self-driven research & projects) | `Heutagogy/` |

The **repository root** holds source code, textbooks, syllabi, and assignments.
The **O-Vault** holds notes, study guides, flashcards, and exam prep — the knowledge layer.

> Every directory contains a `README.md` that serves as its spec. Navigate to any directory and read its README to understand its purpose.

---

## Repository Root — Directory Map

### Learning Methods

| Directory | Purpose |
|---|---|
| `Pedagogy/` | Formal university coursework |
| `Andragogy/` | Guided self-directed learning |
| `Heutagogy/` | Self-determined learning & research |

### Pedagogy — Semester Structure

| Directory | Purpose |
|---|---|
| `Pedagogy/Semester 4/` | Spring 2026 — current semester |
| `Semester 4/Repos/course-repos/` | Active course assignment repositories |
| `Semester 4/Repos/sandbox-repos/` | Experimental projects tied to coursework |
| `Semester 4/Syllabi/` | Course syllabi (PDFs) |
| `Semester 4/Textbooks/` | Textbooks organized by course |
| `Semester 4/Course Scheduals/` | Calendar and scheduling files |

### Pedagogy — Courses (Semester 4)

| Course | Description | Repo | Vault Notes |
|---|---|---|---|
| COMP110 | Programming Fundamentals | `course-repos/COMP110/` | [[Learning/Pedagogy/UNC/s4/COMP110/README\|COMP110 Notes]] |
| DATA120 | Data Science | `course-repos/DATA120/` | [[Learning/Pedagogy/UNC/s4/DATA120/README\|DATA120 Notes]] |
| PSYC101 | Intro to Psychology | `course-repos/PSYC101/` | [[Learning/Pedagogy/UNC/s4/PSYC101/README\|PSYC101 Notes]] |
| STOR155 | Intro to Statistics | `course-repos/STOR155/` | [[Learning/Pedagogy/UNC/s4/STOR155/README\|STOR155 Notes]] |

### Heutagogy — Subdirectories

| Directory | Purpose |
|---|---|
| `Heutagogy/courses/` | Self-selected structured courses |
| `Heutagogy/projects/` | Personal hands-on projects |
| `Heutagogy/research-notes/` | Research paper deep dives |

### Infrastructure

| Directory | Purpose |
|---|---|
| `tools-and-infrastructure/` | Automation scripts and study utilities |

---

## Obsidian Vault — Directory Map

### Vault Overview

| Directory | Purpose |
|---|---|
| `O-Vault/` | The Obsidian knowledge layer |
| `O-Vault/Learning/` | Root content directory |

### Study Material Pattern

Every course in the vault follows this repeating structure:

```
<Course>/
└── Exams/
    └── <Exam>/
        ├── README.md                       ← Exam study hub spec
        ├── Exam_#_Master_Study_Guide.md    ← Central summary
        ├── notes/                          ← Chapter-by-chapter notes
        │   └── README.md
        └── resources/
            └── my-resources/               ← Flashcards, Anki imports
                └── README.md
```

### Vault Heutagogy

| Directory | Purpose |
|---|---|
| [[Learning/Heutagogy/courses/README\|Heutagogy/courses/]] | Notes from self-selected courses |
| [[Learning/Heutagogy/research-notes/README\|Heutagogy/research-notes/]] | Research paper breakdowns |

---

## Quick Reference

| If you're looking for...       | Go to...                                           |
| ------------------------------ | -------------------------------------------------- |
| Course assignments & code      | `Pedagogy/Semester 4/Repos/course-repos/`          |
| Textbooks & syllabi            | `Pedagogy/Semester 4/Textbooks/` or `Syllabi/`     |
| Exam study guides & flashcards | `O-Vault/Learning/Pedagogy/UNC/s4/<COURSE>/Exams/` |
| Self-taught course notebooks   | `Heutagogy/courses/`                               |
| Research paper notes           | `O-Vault/Learning/Heutagogy/research-notes/`       |
| Scripts & automation           | `tools-and-infrastructure/`                        |
| **Any directory's purpose**    | **Open its `README.md`**                           |

---

*Every directory has its own `README.md` spec. A companion file-level documentation index is planned for the future.*
