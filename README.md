# MLOps Project – Milestone 0

A reproducible Python environment with automated CI validation.

![CI](https://github.com/ZifengC/mlops-project/actions/workflows/ci.yml/badge.svg)

## Setup

### Prerequisites
- Python 3.10 or higher
- Git

## Quick Start

1. Clone the repository
   `git clone https://github.com/ZifengC/mlops-project.git` 
   `cd mlops-project`

2. Create virtual environment: `python -m venv venv`
3. Activate:
   - Linux / macOS: `source venv/bin/activate`
   - Windows: `venv\Scripts\activate`
4. Install dependencies: `pip install -r requirements.txt`
5. Run tests: `pytest tests/`

## Reproducibility Principles Applied

This project applies three key reproducibility practices:

1. **Dependency Pinning:**  
   Dependency pinning guarantees that the exact same library versions are used whenever the project is installed. By fixing versions in requirements.txt, we avoid unexpected behavior caused by upstream package updates and reduce “works on my machine” issues.

2. **Environment Isolation:**  
   Virtual environments isolate project dependencies from system Python and other projects.

3. **Automated Validation:**  
   GitHub Actions CI runs tests in a fresh environment on every push, catching integration issues early.This simulates a new user or deployment environment and quickly exposes hidden assumptions or missing dependencies.

# How environment reproducibility supports ML lifecycle reliability
All six stages depend on consistent behavior across systems. Environment reproducibility ensures that the same code and data produce the same results regardless of who runs them or where they are executed. In this way, metrics and evaluation results truly reflect model changes rather than hidden dependency differences. Moreover, reproducibility saves time for developers throughout the ML lifecycle, enabling faster iteration and more flexible collaboration across the team.

# Connects environment management to deployment success
Environment management is directly connected to deployment success because it ensures that the production environment matches the development and training environments. When dependencies, library versions, and configurations are consistent, models behave predictably after deployment.

## Project Structure

```text
.
├── .github/
│   └── workflows/
│       └── ci.yml          # CI workflow
├── src/                    # Source code
├── tests/                  # Test files
├── requirements.txt        # Pinned dependencies
└── README.md               # Project documentation

