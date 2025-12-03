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

Use the provided `Untitled.ipynb` (or create new notebooks) to run experiments inside this environment. The current notebook walks through:

1. Printing the active interpreter path (`Cell 1`).
2. Printing the TensorFlow version (`Cell 2`).
3. Querying the available GPU by calling `tf.test.gpu_device_name()` (`Cell 3`).
4. Importing `numpy`/`time`, building a 5k x 5k random NumPy array, and benchmarking 10 repeated `np.matmul` multiplications (`Cells 4-8`).
5. Building a similarly sized TensorFlow tensor and benchmarking 10 repeated `tf.matmul` calls (`Cells 9-10`).

> **Tip:** In the final benchmark loop, ensure you multiply `tf_array` rather than the NumPy array so the test actually runs on TensorFlow tensors.

The large matrices consume a few hundred MB of RAM; adjust the shape if you hit memory pressure.

## Housekeeping

- The `.gitignore` excludes virtual-environment folders, caches, and editor artifacts.
- Commit only project-specific scripts or notebooks; avoid tracking entire environments.
