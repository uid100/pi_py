# Monte Carlo pi(π) Estimator (Python + matplotlib)

A visual Monte Carlo simulation that estimates π by randomly sampling points in a unit square and checking whether they fall inside a unit quarter-circle.

Includes a simple GUI using `matplotlib` **RadioButtons** to change the number of samples interactively as an **event-driven programming** demostration.


## Quick Start

```bash
# (Recommended) create and activate a virtual environment
python -m venv .venv

# Windows PowerShell
. .venv\Scripts\Activate.ps1

# macOS/Linux
source .venv/bin/activate

# Install requirements
pip install -r requirements.txt

# Run the demo
python pi.py