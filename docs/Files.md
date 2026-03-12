### content
```
pi_py/
├─ pi.py                      # The main demo script (your Monte Carlo π visualization)
├─ README.md                  # Project overview + quick start + links
├─ requirements.txt           # Minimal dependencies
├─ .gitignore                 # Python ignores
├─ docs/
│  └─ setup-troubleshooting.md  # Student handout for setup + troubleshooting
└─ lab/
   ├─ assignment.md           # The lab brief (objectives, tasks, deliverables)
   └─ rubric.md               # 50-point grading rubric
```

## Files
- pi.py — the Monte Carlo π estimator with an interactive control (RadioButtons)
- docs/setup-troubleshooting.md — step-by-step setup and OS-specific fixes
- lab/assignment.md — student lab with tasks and deliverables
- lab/rubric.md — 50-point grading rubric
- requirements.txt — pinned/core dependencies
- .gitignore — ignore caches and virtual envs


## Description
- Random points (x, y) are generated in [0,1] × [0,1]
- A point is inside the quarter-circle if x**2 + y**2 <= 1
- Estimate is π ≈ 4 × (inside / total)
- Changing the sample size triggers a callback (event-driven) that re-draws the plot

This is intentionally simple to focus on:

- Event callbacks (radio button on_clicked)
- Redrawing the canvas (fig.canvas.draw_idle())
- Connecting GUI controls to computation


