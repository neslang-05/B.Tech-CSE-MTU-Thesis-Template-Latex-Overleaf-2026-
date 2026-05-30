# AI-Based Paddy Seed Quality Assessment And Farmer Feedback System - Thesis Document

This repository contains the LaTeX source files for the academic thesis. 

---

## 🚀 How to Compile Locally (Linux)

To compile this document on a Linux system, follow these steps:

### 1. Install LaTeX Dependencies
Make sure you have a complete TeX Live installation, including `biber` for bibliography management. Run the following command:

```bash
sudo apt-get update
sudo apt-get install texlive-latex-base texlive-latex-extra texlive-fonts-recommended texlive-fonts-extra texlive-science texlive-bibtex-extra biber latexmk
```

### 2. Compilation Sequence
Because this document uses `biblatex` with `biber` and multiple cross-references, you must compile it in a specific sequence:

```bash
# 1. Compile the document draft and generate citation references
pdflatex -interaction=nonstopmode main.tex

# 2. Process bibliography references
biber main

# 3. Compile the document again to include references
pdflatex -interaction=nonstopmode main.tex

# 4. Final compilation to resolve cross-references and table of contents
pdflatex -interaction=nonstopmode main.tex
```

#### Alternative (Recommended): Using `latexmk`
You can automate the whole sequence using `latexmk`, which detects changes and compiles the necessary number of times:
```bash
latexmk -pdf main.tex
```

---

## 👥 How to Collaborate with Your Team

There are three primary ways to collaborate on this project:

### Option A: Overleaf (Recommended for Real-time Writing)
Overleaf is the easiest way to write collaboratively without local LaTeX installations.
1. **Zip the Project**: Create a zip of all `.tex` and `.bib` files along with the `assets/` and `thesis/` directories.
2. **Create Overleaf Project**: Go to [Overleaf](https://www.overleaf.com), click **New Project** -> **Upload Project**, and drag your zip file.
3. **Select Compiler**: If you run into issues on Overleaf, go to Menu (top-left) and ensure the compiler is set to **pdfLaTeX** and TeX Live version is set to **2023** or newer.
4. **Git Sync (Optional)**: If you have Overleaf Premium, you can link the Overleaf project directly to this GitHub repository.

### Option B: GitHub + Automated Actions (CI/CD)
We have configured a **GitHub Actions** workflow under `.github/workflows/compile.yml`.
* Whenever you or a teammate pushes code to `master` or `main` branches, GitHub will automatically compile the document.
* You can download the compiled PDF from the **Actions** tab of your repository on GitHub.
* This eliminates "it works on my machine" compilation issues.

### Option C: VS Code + Git (For Offline/Local Writing)
If you prefer working locally:
1. Clone the repository:
   ```bash
   git clone https://github.com/neslang-05/AI-Based-Paddy-Seed-Quality-Assessment-And-Farmer-Feedback-System.git
   ```
2. Open in VS Code.
3. Install the **LaTeX Workshop** extension (by James Yu).
4. Save any `.tex` file to automatically trigger build processes.
