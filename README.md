# IT566scriptingTechEngineersNotebook
Engineers Notebook
IT-566 — Chapter 1 Notes
Baseline Development Environment (Expanded, Structured, GitHub-Ready)
Scope and Function
Defines the minimum technical environment required for reproducible scripting work. Establishes standardization across machines, operating systems, and student workflows. Eliminates configuration drift, tool incompatibility, and non-deterministic execution.
Core Toolchain
2.1 Git
• Distributed version control.
• Guarantees traceability of every file change.
• Enables rollback, branching, and collaborative review.
• Mandatory operations: init, add, commit, branch, merge, pull, push.
2.2 GitHub
• Remote repository hosting.
• Serves as the authoritative record of your submissions.
• Provides issue tracking, pull-request review, and commit history transparency.
2.3 GitHub Desktop
• Graphical interface for managing repositories.
• Lowers friction for staging, committing, and synchronizing work.
• Used when CLI fluency is not required.
2.4 GitHub CLI (gh)
Mandatory commands:
• gh auth login — establish authentication.
• gh repo create — initialize remote repositories without GUI.
• gh repo clone — replicate remote repository locally.
• gh pr create — open a pull request from feature branch to main.
Rationale: ensures command-line competence, automation capability, and consistent workflows across environments.
2.5 Visual Studio Code
• Primary IDE.
• Provides integrated terminal, linting, debugging, and notebook support.
• Supports workspace-level and project-level configuration.
VS Code Extension Requirements
3.1 GitHub Extensions
• GitHub Pull Requests & Issues — PR review inside editor.
• GitHub Repositories — edit remote content without cloning.
• GitHub Theme — ensures visual consistency.
• GitHub Codespaces (optional) — cloud execution environment.
3.2 Python Extensions
• Python (Microsoft) — core Python support.
• Pylance — type analysis and language intelligence.
• Black Formatter — enforces deterministic formatting.
• isort — standardized import ordering.
3.3 Auxiliary Extensions
• Markdown PDF — export documentation.
• YAML — schema-aware editing.
• JSON — structure validation and formatting.
• Jinja — template editing.
• Remote Development (optional) — container-based workflow support.
Python Environment Initialization
4.1 Virtual Environment Creation
python3 -m venv myvenv
Purpose: isolate interpreter dependencies, prevent version collisions, and allow project-specific tooling.
4.2 Activation
Mac/Linux:
source myvenv/bin/activate
Windows:
myvenv\Scripts\activate
4.3 pipx Installation
python3 -m pip install pipx
pipx ensurepath
Function: install CLI tools globally while isolating dependencies to avoid conflicts with project packages.
Formatting and Static Consistency Tools
5.1 Black
• Enforces deterministic layout.
• Eliminates subjective formatting decisions.
Execution:
black .
5.2 isort
• Orders imports according to defined rules.
Execution:
isort .
Rationale: formatting is non-negotiable; automation ensures uniform output across all students.
Recommended Repository Architecture
project/
│
├── src/ — executable modules, functions, scripts
├── tests/ — unit test suites (introduced in later chapters)
├── data/ — structured input/output files
├── logs/ — runtime logs (optional)
│
├── README.md — project description, usage instructions
├── pyproject.toml — central configuration for Black, isort, and packaging
└── .vscode/ — per-project editor settings
Design principle: separation of concerns. Code, tests, data, and configuration must remain isolated.
GitHub Workflow Standards
7.1 Commit Discipline
• Frequent, incremental commits.
• Each commit addresses one logical change.
• Messages must describe the actual operation performed, not intentions.
7.2 Branch Strategy
• main — stable branch only.
• feature/<task> — new work.
• pull requests — required for merging feature branches into main.
7.3 Submission Protocol
• Push changes regularly; repositories serve as the grading artifact.
• History must show progression, not large single-commit dumps.
Importance of Chapter 1
Functionally establishes:
• Required tools for course execution.
• Required structure for all future assignments.
• Required workflows for version control and collaboration.
• Required standards for code formatting, package management, and environment reproducibility.
This chapter defines the operational framework. All subsequent chapters assume strict compliance with this baseline.
