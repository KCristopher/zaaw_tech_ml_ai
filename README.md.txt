## Environment setup and Python version check (end-to-end)

This notebook requires Python **Python 3.8 or newer (3.9+ recommended)** and the libraries listed in `requirements.txt`.

---


### Option A: PyCharm

1. Open the project in **PyCharm**.
2. Go to **File → Settings → Python Interpreter**.
3. Click **Add Interpreter → Virtualenv Environment**.
4. Select Python **3.9+** and create a virtual environment in `.venv`.
5. Open the PyCharm terminal and install dependencies:

    ```bash
    pip install -r requirements.txt
    ```

6. Make sure PyCharm is using:

    ```
    project/.venv/Scripts/python.exe
    ```

---

### Option B: Anaconda + Jupyter Notebook

1. Open **Anaconda Prompt**.
2. Create and activate a new environment:

    ```bash
    conda create -n myenv python=3.9
    conda activate myenv
    ```

3. Go to the project directory and install required packages:

    ```bash
    cd path/to/project
    pip install -r requirements.txt
    ```

4. Make the environment available in Jupyter:

    ```bash
    pip install ipykernel
    python -m ipykernel install --user --name myenv --display-name "Python (myenv)"
    ```

5. Start Jupyter Notebook:

    ```bash
    jupyter notebook
    ```

6. In Jupyter, select the kernel:  
   **Kernel → Change Kernel → Python (myenv)**

---


### Option C: Plain Python (terminal)

```bash
python -m venv .venv
.venv\Scripts\activate
pip install -r requirements.txt
