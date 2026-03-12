# Lab: Monte Carlo π Estimation — Event-Driven Intro with matplotlib

**Context:** You’ve been writing console apps. This lab introduces **event-driven programming** using `matplotlib` widgets (GUI-like controls) to trigger updates to a plot.

---

## Learning Objectives

By the end of this lab, you will:
- Explain how Monte Carlo sampling can estimate π
- Identify **events**, **callbacks**, and the **rendering loop** in a GUI-style app
- Modify a Python script to respond to user input and re-render graphics
- Communicate results and reflect on accuracy vs. sample size

---

## Pre-Lab (read/skim)

- Run the app once (`python pi.py`) to see how the RadioButtons change sample size.
- Read the `draw_plot` function in `pi.py` and find where the plot is updated.
- Find the callback that wires GUI to logic: `radio.on_clicked(...)`.

---

## Tasks

> Work incrementally. Commit often with meaningful messages.

### 1) Understand & Document (10 pts)
- Add **docstrings** to the following functions in `pi.py`: `get_points`, `draw_plot`, `calculate_error`, `random_plot`
- Add **inline comments** explaining:
  - What the event callback does
  - Why `fig.canvas.draw_idle()` is called instead of `plt.show()` repeatedly
- Add your name and date at the top of `pi.py`

### 2) UX Improvement — Add a Slider (10 pts)
- Add a `matplotlib.widgets.Slider` that lets the user select sample sizes continuously (e.g., 10 to 1,000,000 on a log scale or stepped powers of 10)
- Make the slider **update the plot** as it moves (event-driven)
- Keep the RadioButtons OR replace them (explain your choice in `README` or a short `notes.md`)

### 3) Visual Feedback — Legend/Styling (5 pts)
- Change colors/markers so “Inside” vs. “Outside” are clearly distinguishable
- Ensure the legend remains readable

### 4) Reproducibility Control (10 pts)
- Add a **“Reseed” Button** to change the RNG seed and redraw
- Display the current seed in the title or in a corner text annotation

### 5) Accuracy Insight — Show Convergence (10 pts)
- Add an **on-plot text or annotation** that displays:
  - Current estimate of π
  - Absolute error
  - (Optional) Cumulative running average if you implement progressive sampling
- Briefly explain in comments how accuracy tends to improve with more samples (Law of Large Numbers)

### 6) Reflection (5 pts)
- In a short `REFLECTION.md` (3–6 sentences), answer:
  - What is the event-driven part of this program?
  - What did you change and why?
  - How does increasing sample size affect the estimate and runtime?

---

## Deliverables

- Updated `pi.py` (with docstrings, comments, and your enhancements)
- Any additional files you created (e.g., `REFLECTION.md`)
- Your code should run with `python pi.py` after `pip install -r requirements.txt`

**Submission:** Submit your repo or a zip as directed by your instructor.

---

## Optional Extensions (no extra points unless instructor adds extra credit)

- Animate progressive sampling (e.g., using `FuncAnimation`) to show π converging
- Plot error vs. sample size on a second axes
- Add CheckButtons to toggle visibility of inside/outside points
- Vectorize point generation with NumPy to improve performance