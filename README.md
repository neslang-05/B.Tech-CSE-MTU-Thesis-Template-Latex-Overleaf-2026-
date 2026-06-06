# Manipur Technical University (MTU) - B.Tech CSE Thesis Template

This is the official-style LaTeX thesis template for the **Department of Computer Science & Engineering**, **Manipur Technical University (MTU)**, Imphal, for the award of the **Bachelor of Technology (B.Tech)** degree.

It is structured to comply with MTU B.Tech thesis guidelines, including pre-formatted title pages, bonafide certificates, dynamic declaration pages for multiple authors, table of contents, list of tables, list of figures, symbols/nomenclature, and IEEE/bibliography styling.

---

## 📁 Project Structure

*   `main.tex` — The master entry document that orchestrates the entire compilation.
*   `thesis-details.tex` — **The only configuration file you need to edit.** All metadata (Title, Authors, Supervisor, HOD, Year, etc.) is defined here.
*   `assets/` — Contains institutional assets (like `logo.png` for Manipur Technical University).
*   `bibliography/` — Contains `references.bib` (BibLaTeX bibliography database).
*   `chapters/` — Individual thesis chapters:
    *   `title-page.tex` — Configures the front page layout.
    *   `dedication.tex` — Dedication section.
    *   `bonafide-certificate.tex` — Dynamic certification page.
    *   `declaration.tex` — Dynamic declaration pages for up to 4 group authors.
    *   `acknowledgement.tex` — Dynamic acknowledgement section.
    *   `abstract.tex` — Abstract and keyword guidelines.
    *   `abbreviations.tex` — List of nomenclature and abbreviations.
    *   `chapter1.tex` to `chapter5.tex` — Core chapters (Introduction, Literature Review, System Design, Implementation, Results).
    *   `conclusion.tex` — Conclusion and future scope.
*   `example_paddy_thesis/` — **A complete compiled example thesis** ("AI-Based Paddy Seed Quality Assessment...") for reference.

---

## 🛠️ How to Customize (Quick Start)

Open `thesis-details.tex` and customize the metadata commands:

```latex
% --- THESIS DETAILS ---
\newcommand{\thesisTitle}{YOUR PROJECT TITLE IN TITLE CASE}
\newcommand{\degree}{Bachelor of Technology}
\newcommand{\branch}{Computer Science and Engineering}
\newcommand{\department}{Department of Computer Science \& Engineering}
\newcommand{\university}{Manipur Technical University}
\newcommand{\universityAddress}{Imphal, Manipur -- 795004}
\newcommand{\submissionDate}{Month, Year} % e.g. May, 2026

% --- SUPERVISOR & HOD DETAILS ---
\newcommand{\supervisorName}{Dr. Supervisor Name}
\newcommand{\hodName}{Mrs. Tayenjam Aerena}

% --- AUTHOR / STUDENT DETAILS ---
% Supports 1 to 4 authors. Comment out/leave empty if not needed:
\newcommand{\authorA}{Student A Name}
\newcommand{\authorAReg}{2201CSXXXX}
\newcommand{\authorB}{} % Leave empty if not applicable
\newcommand{\authorBReg}{}
```

The system will dynamically generate the correct certificate table, declaration pages (one dedicated page for each student), and acknowledgement list based on these variables!

---

## 💻 Local Compilation Instructions

You need a TeX distribution (e.g., TeX Live, MiKTeX, MacTeX) installed on your system.

### Option 1: Using `latexmk` (Recommended)
`latexmk` handles all bibliography and table of contents cross-references automatically.
```bash
latexmk -pdf main.tex
```

### Option 2: Standard Command Loop
If you prefer running commands manually:
```bash
pdflatex main.tex
biber main
pdflatex main.tex
pdflatex main.tex
```

---

## 🚀 How to Publish as a Template on Overleaf

Overleaf is the most popular online LaTeX editor and hosting service. You can publish this project as a template for other students at MTU:

### Step 1: Create a ZIP Archive of the Project
Compress the project files into a single `.zip` file. Exclude LaTeX auxiliary build files (`.aux`, `.log`, `.pdf`, `.toc`, etc.).
You can use the provided zip file: `mtu_btech_cse_thesis_template.zip` (generated at the root of this workspace).

### Step 2: Upload to Overleaf
1. Go to [Overleaf](https://www.overleaf.com) and log in.
2. Click on **New Project** -> **Upload Project**.
3. Select and upload the ZIP archive.

### Step 3: Publish in Overleaf Gallery (To make it public)
If you want to publish this template so that it is searchable in the official Overleaf template gallery for everyone:
1. Open your project on Overleaf.
2. Click on the **Menu** button (top-left).
3. Find the **Publish** or **Share** section.
4. Click **Publish as Template**.
5. Fill out the submission form:
    *   **Title:** Manipur Technical University (MTU) B.Tech CSE Thesis Template
    *   **Description:** A professional, variable-driven LaTeX thesis template designed for Manipur Technical University B.Tech Computer Science and Engineering students.
    *   **Tags:** Thesis, Template, University, India, Manipur Technical University, Computer Science.
6. Submit it. Overleaf's curation team will review and publish it within a few days!

### Step 4: Alternative Quick Share (Read-Only Link)
If you don't want to wait for Overleaf curation, you can share it instantly:
1. Open your project in Overleaf.
2. Click **Share** (top-right).
3. Turn on **Share with read-only link**.
4. Copy the link and share it with your university peers. Anyone can click the link and choose **Copy Project** to start their own thesis!
