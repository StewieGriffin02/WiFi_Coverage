Campus Wi-Fi Coding Lab — User Guide

1. Requirements and launch
Use Python 3.10+ with Tkinter. Only the Python standard library is required. Extract the entire project folder before running.
Windows: double-click Start_WiFi_Lab.bat or run py -3 main.py from WiFi_Lab.
macOS: run python3 main.py from WiFi_Lab (a .command shortcut is also supplied).
Run python3 -m tkinter to check Tkinter availability if necessary.
Basic lab is TODO 1–2; Optimization lab is TODO 3–6. Launch directly via python3 main.py --basic or --advanced. Do not use the older root gui.py for class.

2. Optimization lab workflow
Expressions: enter TODO 3 (cost), TODO 4 (weighted score), TODO 5 (comparison); click Run 49 expression tests.
Algorithm: in Guided blocks complete A (union), B (score), C (update); A/B use 35 cases each, C uses six. Run each block and then Run & record my algorithm. Preview assembled algorithm shows the result. Free coding is an alternative.
Change weights at the top: 100/0, 70/30, 30/70. Code and history remain, but new block tests and algorithm execution are required.
Debug: predict → run seeded bug → repair → retest → explain and record. Two exercises: Overlap and Comparison.
Evidence: compare solutions, record recommendation, copy data or export TXT before closing. Session history is not persistent and code drafts are not auto-saved.

3. Student and teacher separation
Default unfinished TODO fields are intentional. teacher/reference_answers.py has EXPRESSIONS, BLOCKS, FREE_ALGORITHM and DEBUG_REPAIRS for verification. Do not distribute teacher files and engineering test cases as student assignments.
GUI editors request expression text or a function body; do not add def/import declarations. MAX_COST, coverage_weight, cost_weight and model data dictionaries are provided by the GUI. Helpers student_cost, student_score, student_better reuse TODO 3–5. The standalone stage3/student_algorithm.py file and GUI editors do not synchronize.

4. Model
12 classroom detection points; seven possible sites A–G; exactly three distinct routers; ideal radius 3 with boundary included. Union coverage is deduplicated. Cost differs by location, not router capacity. Score F=coverage_weight*(covered/12)+cost_weight*(1−total_cost/1100). MAX_COST=1100 is a normalization reference, not a budget. Coverage ratio is 0–1 internally. Tied globally optimal legal plans should all count as optimal. Compare cost and coverage across scenarios, not composite scores under different weights. No walls, attenuation, population, capacities or 3D in the main GUI.

5. Test commands and historical record
python3 run_tests.py  (54 automated tests recorded as passing)
python3 -m unittest -v test_demand_extension (seven optional tests recorded as passing)
teacher/TEST_RESULTS.txt contains main test output. No actual desktop click, window layout or projector test was recorded. Before teaching, verify both labs, all expressions, all blocks, all three weights, Debug exercises, Evidence export and legibility on the actual display.

6. Optional population/budget extension
python3 demand_extension.py --budget 750
Add --csv results.csv to export all 35 plans. This is command-line-only, fixed to exactly three sites, using synthetic population (410 people). It does not add budget or population controls to the main GUI.
