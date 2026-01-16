# MLOps Project – Milestone 0

A reproducible Python environment with automated CI validation.

![CI](https://github.com/ZifengC/mlops-project/actions/workflows/ci.yml/badge.svg)

## Quick Start

1. Clone the repository
2. Create virtual environment: `python -m venv venv`
3. Activate:
   - Linux / macOS: `source venv/bin/activate`
   - Windows: `venv\Scripts\activate`
4. Install dependencies: `pip install -r requirements.txt`
5. Run tests: `pytest tests/`

## Reproducibility Principles

This project applies three key reproducibility practices:

1. **Dependency Pinning:**  
   All packages are locked to exact versions in `requirements.txt`, preventing “works on my machine” issues.

2. **Environment Isolation:**  
   Virtual environments isolate project dependencies from system Python and other projects.

3. **Automated Validation:**  
   GitHub Actions CI runs tests in a fresh environment on every push, catching integration issues early.

These practices ensure training and deployment environments remain consistent—critical for reliable ML behavior.

## Project Structure
.
### ├── .github/
### │   └── workflows/
### │       └── ci.yml          # CI workflow
### ├── src/                    # Source code
### ├── tests/                  # Test files
### ├── requirements.txt        # Pinned dependencies
### └── README.md               # This file

