# Foundations of Data Science & Causal ML — Quarto Book

This repository contains a [Quarto](https://quarto.org) book project. It uses a Python virtual environment (`venv`), `requirements.txt` for dependencies, and a `chapters/` folder to organize the content.

---

## Project Structure

```
.
|-- .quarto
|-- .venv
|-- README.md
|-- _book/               # rendered HTML output
|-- _quarto.yml          # main Quarto configuration
|-- chapters/            # book chapters (.qmd files)
|   └── 01_ch01.qmd
|-- index.qmd            # book landing page
|-- references.bib       # bibliography file
|-- requirements.txt     # Python dependencies
```

---

## Setup Instructions

### 1. Create a Virtual Environment

From the project root:

```bash
python3 -m venv venv
source venv/bin/activate   # on Linux/Mac
# OR
venv\Scripts\activate      # on Windows (PowerShell)
```

### 2. Upgrade pip and Install Requirements

```bash
pip install --upgrade pip
pip install -r requirements.txt
```

This installs Python packages (e.g., Jupyter, matplotlib, etc.) required for code execution in `.qmd` files.

### 3. Create a New Quarto Project (if starting fresh)

If you were starting from scratch:

```bash
quarto create-project
```

Create a `chapters` folder.

### 4. Configure `_quarto.yml`

The `_quarto.yml` file defines the book structure. Example:

```yaml
project:
  type: book
book:
  chapters:
    - index.qmd
    - chapters/01_ch01.qmd
bibliography: references.bib
output-dir: _book
```

Adjust this list to match your chapters.

### 5. Edit `index.qmd`

This is the book’s landing page. Use it for your title, subtitle, author, and introduction.

Example:

```markdown
---
title: "Foundations of Data Science & Causal ML"
author: "Caio Velasco"
---

Welcome to the book! Use this space for an introduction.
```

### 6. Preview Locally

Start a live preview server:

```bash
quarto preview
```

Open the provided local URL in your browser. Changes to `.qmd` files will update automatically.

### 7. Render the Book

To build the static site into the `_book/` folder:

```bash
quarto render
```

This generates HTML files (and optionally PDF/EPUB if configured).

### 8. Publish with GitHub Pages (gh-pages branch)

To publish via GitHub Pages using Quarto’s built-in workflow:

```bash
quarto publish gh-pages
```

This pushes the contents of `_book/` to a `gh-pages` branch that GitHub Pages serves automatically.

---

## Tips

- Keep your virtual environment (`venv/`) out of Git by adding it to `.gitignore`.
- Store sensitive variables (if any) in a `.env` file (not committed).
- Use `references.bib` to manage citations.
- Add more chapters inside the `chapters/` folder and update `_quarto.yml` accordingly.
