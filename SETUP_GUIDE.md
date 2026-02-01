# Credit Risk Prediction Notebook — Setup & Run Guide

This guide walks you through creating an environment and running **Credit Risk prediction.ipynb**.

---

## What the notebook does

- **Data:** Loads `UCI_Credit_Card.csv` (credit card default data).
- **Libraries:** Uses `numpy`, `pandas`, `matplotlib`, `seaborn`, and `scikit-learn` for EDA, preprocessing, and a logistic regression model for default prediction.

---

## 1. Environment creation

Use **one** of the options below.

### Option A: Conda (recommended if you use Anaconda/Miniconda)

```bash
# Create a new environment with Python 3.10
conda create -n credit_risk python=3.10 -y

# Activate it
conda activate credit_risk

# Install dependencies
pip install -r requirements.txt

# Install Jupyter in this environment (if not already)
pip install jupyter notebook
```

### Option B: Python venv (no Conda)

```bash
# From the project folder: Test project
cd "/Users/aumsamel/Documents/Test project"

# Create virtual environment
python3 -m venv venv

# Activate it
# On macOS/Linux:
source venv/bin/activate
# On Windows:  venv\Scripts\activate

# Upgrade pip, then install dependencies
pip install --upgrade pip
pip install -r requirements.txt
pip install jupyter notebook
```

---

## 2. Data file

The notebook expects **`UCI_Credit_Card.csv`** in the **same folder** as the notebook.  
You already have this file in the project directory, so no extra step is needed.  
If you open the notebook from a different directory later, either:

- Copy/move the notebook into the folder that contains `UCI_Credit_Card.csv`, or  
- Change the path in the notebook from `'UCI_Credit_Card.csv'` to the full path to the CSV.

---

## 3. How to run the notebook

1. **Activate your environment** (do this every time you open a new terminal):
   - Conda: `conda activate credit_risk`
   - venv: `source venv/bin/activate` (or `venv\Scripts\activate` on Windows)

2. **Start Jupyter** from the project folder:
   ```bash
   cd "/Users/aumsamel/Documents/Test project"
   jupyter notebook
   ```
   Or to use JupyterLab:
   ```bash
   jupyter lab
   ```

3. **Open the notebook:** In the browser, click **Credit Risk prediction.ipynb**.

4. **Select the correct kernel:**
   - **Conda:** `Kernel` → `Change kernel` → choose **credit_risk** (or the env you created).
   - **venv:** Choose the kernel that points to your `venv` (e.g. **Python 3 (venv)**).

5. **Run the notebook:**
   - **Run all:** `Cell` → `Run All`
   - **Run step by step:** `Shift + Enter` in each cell

---

## 4. Optional: Remove the `pip install` cell

The notebook has a cell that runs `pip install seaborn`. Once your environment is set up with `requirements.txt`, you can delete or skip that cell to avoid reinstalling every time you run the notebook.

---

## Quick reference

| Step              | Command / action                                      |
|-------------------|--------------------------------------------------------|
| Create conda env  | `conda create -n credit_risk python=3.10 -y`          |
| Activate (conda)  | `conda activate credit_risk`                           |
| Install packages  | `pip install -r requirements.txt`                     |
| Start Jupyter     | `jupyter notebook` (from project folder)              |
| Run notebook      | Open **Credit Risk prediction.ipynb** → Run All / run cells |

If something fails (e.g. missing module or wrong CSV path), check that the kernel matches the environment where you ran `pip install -r requirements.txt` and that `UCI_Credit_Card.csv` is in the same directory as the notebook.
