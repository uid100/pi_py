This guide helps you install Python, set up your environment, and run the Monte Carlo π estimator with a small GUI built using `matplotlib`.

---

## 1) Install Python 3

### Windows
1. Download from https://www.python.org/downloads/windows/
2. Run installer and **check**: “Add Python to PATH”
3. Finish install. Open **PowerShell** and check:
   ```powershell
   python --version

macOS

Download from https://www.python.org/downloads/macos/
Install the .pkg
Check:
Shellpython3 --versionShow more lines


Ubuntu/Debian Linux
Shellsudo apt updatesudo apt install -y python3 python3-pip python3-venv python3-tkpython3 --versionShow more lines

python3-tk provides the Tk GUI bindings that matplotlib often uses for interactive windows.


2) Create a Virtual Environment (Recommended)
Shell# In the project folderpython -m venv .venv# Activate it# Windows PowerShell. .venv\Scripts\Activate.ps1# macOS/Linuxsource .venv/bin/activateShow more lines
If activation succeeds, your prompt will start with (.venv).

3) Install Dependencies
Shellpip install -r requirements.txtShow more lines
Verify:
Shellpython -c "import matplotlib; print(matplotlib.__version__)"Show more lines

4) Run the App
From the project root:
Shellpython pi.pyShow more lines
A window should open showing random points and a set of RadioButtons to change sample sizes.

5) Troubleshooting
“ModuleNotFoundError: No module named 'matplotlib'”
Install via:
Shellpip install matplotlibShow more lines
No window appears (Mac)
Try forcing a Tk backend:
Python# add near the top of pi.py, before importing pyplotimport matplotlibmatplotlib.use("TkAgg")Show more lines
Then reinstall tkinter if needed (macOS):

Install Python via official installer (includes Tk), or
For Homebrew Python: brew install python-tk@3.12 (version may vary)

No window appears (Linux)
Make sure Tk is installed:
Shellsudo apt install -y python3-tkShow more lines
Using python vs python3

On Windows, python is usually correct.
On macOS/Linux, try python3 if python fails.

Virtual environment issues
If pip installs to the global site-packages instead of your venv:

Confirm you activated the venv (prompt should show (.venv))
Run python -m pip install -r requirements.txt to bind pip to the active Python.


6) Next Steps

Finished? Open lab/assignment.md for the lab tasks.
Want to explore? Try changing point colors, adding sliders, or animating the sampling.