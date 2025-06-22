# Blog Notes

## 2025-06-21T14:57:04-04:00 — PCA Workflow Analysis

**Task Title / Objective:**
- Analyze and document the workflow and structure of `PCA.ipynb`.

**Technical Summary:**
- The notebook is designed for predicting machine failure using sensor data from a manufacturing environment.
- Workflow includes: connecting to a SQLite database, extracting and loading sensor data into pandas, exploring and visualizing data distributions, checking table structures, splitting features/targets, rebalancing data, and reducing dimensionality with PCA.
- The pipeline is structured for end-to-end modeling: from data import, EDA, preprocessing, PCA training, model building, evaluation (metrics/confusion matrix), to deployment (saving/loading models and scoring new data).

**Bugs & Obstacles:**
- No critical bugs observed in the notebook structure itself. Potential challenge: managing high-dimensional sensor data and ensuring the database path is correct.

**Key Deliberations:**
- The notebook is modular, with clear markdown sections for each major ML workflow stage, supporting iterative development and easy debugging.
- Chose to use PCA for dimensionality reduction to address the curse of dimensionality and improve model interpretability.

**Color Commentary:**
What a playbook! The PCA.ipynb notebook reads like a textbook example of a robust ML workflow. From SQL data wrangling to pipeline deployment, each section builds on the last—setting the stage for insightful analysis and future productionization. The modularity and clarity in structure make it a breeze to follow and extend.

## 2025-06-21T14:56:26-04:00 — Environment Setup & LFS Tracking

**Task Title / Objective:**
- Set up project environment and prepare database file for version control with Git LFS.

**Technical Summary:**
- Installed `sqlite3` for local database manipulation.
- Removed the old `cwn` conda environment and created a fresh `py312` environment with Python 3.12.
- Installed essential plotting libraries (`seaborn`, `matplotlib`) in the new environment.
- Provided clear steps for tracking a database file using Git LFS, ensuring large files are versioned efficiently.

**Bugs & Obstacles:**
- Encountered a missing `sqlite3` binary, resolved by installing via `apt`.
- Needed to ensure the `.db` file would not be ignored by `.gitignore` if present.
- Deactivation of the conda environment required the correct command (`conda deactivate`).

**Key Deliberations:**
- Considered whether to reuse the old environment or start fresh—opted for a clean slate for reliability.
- Chose Git LFS for database versioning to avoid repository bloat and maintain performance.

**Color Commentary:**
The project is off to a strong start! After a few command-line hurdles and a quick environment reset, the groundwork is set for reproducible, large-data-friendly development. The decision to use Git LFS for the database file marks a professional touch, ensuring the codebase remains nimble as the project grows.
