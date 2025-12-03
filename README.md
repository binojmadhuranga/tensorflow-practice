# TensorFlow Virtual Environment

This workspace hosts a Python virtual environment configured for TensorFlow experimentation.

## Getting Started

1. **Activate the environment**
   - PowerShell: `Scripts\Activate.ps1`
   - Command Prompt: `Scripts\activate.bat`
2. **Verify Python/TensorFlow**
   - Launch Jupyter or Python, then run:
     ```python
     import sys, tensorflow as tf
     print(sys.executable)
     print(tf.__version__)
     ```

## Notebooks

Use the provided `Untitled.ipynb` (or create new notebooks) to run experiments inside this environment.

## Housekeeping

- The `.gitignore` excludes virtual-environment folders, caches, and editor artifacts.
- Commit only project-specific scripts or notebooks; avoid tracking entire environments.
