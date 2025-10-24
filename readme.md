# Lawind Ismail's Resume

This repository contains the LaTeX source code for my professional resume. It is configured with a GitHub Actions workflow that automatically compiles the LaTeX document into a PDF and creates a new release every time a change is pushed to the `main` branch.

[![Build Resume PDF](https://github.com/lawindismail/resume/actions/workflows/build.yml/badge.svg)](https://github.com/lawindismail/resume/actions/workflows/build.yml)

## 📄 View the Latest Resume

The latest version of my resume can always be found on the **[Releases page](https://github.com/lawindismail/resume/releases/latest)**.

The PDF is automatically generated and attached to a new release upon every update.

## ✨ Features

-   **Professionally Typeset**: Written in LaTeX for a clean, high-quality, and ATS-friendly format.
-   **Automated CI/CD**: Uses a GitHub Actions workflow to handle the entire build and release process.
-   **Version Control**: The entire history of my resume is tracked with Git, making it easy to see changes over time.
-   **Single Source of Truth**: This repository serves as the definitive source for my resume, ensuring the latest version is always available.

## ⚙️ How It Works

The automation is handled by a workflow defined in `.github/workflows/build.yml`. The process is as follows:

1.  **Trigger**: The workflow is triggered on any `push` to the `main` branch.
2.  **Checkout Code**: The repository's source code is checked out.
3.  **Compile LaTeX**: The `resume.tex` file is compiled into `resume.pdf` using a dedicated LaTeX action.
4.  **Create Release**: A new release is created on GitHub, tagged with a timestamp (e.g., `2025-10-24-12-30-00`).
5.  **Upload Artifact**: The generated `resume.pdf` is uploaded as an asset to the newly created release.

## 🛠️ Usage and Local Development

While the primary purpose is automated builds, the resume can also be compiled locally.

### Prerequisites

-   A LaTeX distribution such as [TeX Live](https://www.tug.org/texlive/), [MiKTeX](https://miktex.org/) (for Windows), or [MacTeX](https://www.tug.org/mactex/) (for macOS).
-   A text editor like VS Code with a LaTeX extension (e.g., LaTeX Workshop).

### Steps to Compile Locally

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/lawindismail/resume.git
    cd resume
    ```

2.  **Compile the document:**
    You can use `pdflatex` to compile the `resume.tex` file. It may need to be run a couple of times to ensure all references are correct.
    ```bash
    pdflatex resume.tex
    ```