# Project: House Prices - Advanced Regression Techniques

This document provides the steps to set up and run the solution for the "House Prices" Kaggle challenge.

## Prerequisites

*   Python 3.x
*   A Python virtual environment tool (`venv`)
*   For PDF generation: A LaTeX distribution such as [MacTeX](https://www.tug.org/mactex/) (for macOS) or MiKTeX (for Windows/Linux).

## Setup and Execution Steps

All commands should be executed from the root directory of this project (`corsetti-house_prices_advanced_regression_techniques/`).

**1. Create and Activate a Virtual Environment:**

First, create a Python virtual environment to isolate the project dependencies.

```bash
# Create the virtual environment
python3 -m venv .venv

# Activate the environment
source .venv/bin/activate
```
*Note: On Windows, the activation command is `.\.venv\Scripts\activate`.*

**2. Install Dependencies:**

Install all the required Python libraries using the `requirements.txt` file located in the project root.

```bash
pip install -r requirements.txt
```

**3. Run the Jupyter Notebook:**

The entire analysis and modeling process is contained within the `main.ipynb` notebook. To explore the code and results interactively, start the Jupyter Notebook server.

```bash
jupyter notebook
```

This command will open a new tab in your web browser. Navigate to `challenge/main.ipynb` to open the notebook.

## Generating the PDF Report

To generate the final PDF report (`main.pdf`) from the Jupyter Notebook, ensure you have a LaTeX distribution installed.

From the project's root directory, run the following command:

```bash
jupyter nbconvert --to pdf challenge/main.ipynb
```

This will create the `main.pdf` file inside the `challenge/` directory, identical to the one included in the repository.
