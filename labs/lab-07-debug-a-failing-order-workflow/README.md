# Lab 7: Debug a Failing Order Workflow

**Topic:** 4

**Objective:** LO4 — Test, debug and gather evidence about workflow performance

**Alignment:** A5, A7, A8 · K8

**Suggested time:** 65 minutes

## Scenario and outcome

Use breakpoints, stepping, Locals and Watch to find three deliberate defects in an order-classification workflow, then run regression cases.

You will produce: **A repaired workflow, defect log and regression evidence for six orders**

## Folder contents

- `Main.xaml` — editable UiPath Studio starter workflow.
- `project.json` — UiPath project manifest.
- `mock-debug-a-failing-order-workflow.csv` — portable mock source data.
- `mock-debug-a-failing-order-workflow.xlsx` — formatted mock workbook with Data and Rules sheets.
- `CHECKLIST.md` — completion and evidence checklist.


## Preparation

1. Use UiPath Studio Community 2024.10 or later.
2. Extract or clone this entire folder. Keep the data files beside `project.json`.
3. Open `project.json` in Studio and allow package restore. Upgrade dependency versions if Studio requests it.
4. Use mock data only. Do not enter passwords, tokens or real personal data.

## Procedure

1. Open the Defect Log sheet before running the workflow. The starter project contains three deliberate problems; do not rewrite it immediately.
2. Run Main.xaml normally and record the first visible mismatch or exception with OrderID and observed result.
3. Add a breakpoint before the Total calculation. Use Debug File and inspect Quantity, UnitPrice and Total in Locals.
4. Add Total and orderBand to Watch. Step Over the Assign and compare actual values with ExpectedTotal.
5. Repair only the calculation defect, rerun the affected case and record the evidence before moving to the next defect.
6. Use a breakpoint at the band decision. Confirm the boundary for Priority is Total >= 1000, including O5005 exactly at 1000.
7. Add validation for UnitPrice <= 0 so O5006 becomes Review instead of a normal order.
8. Run all six regression cases and complete ActualBand, ActualTotal and Pass/Fail columns.
9. Export or save the defect log and capture Locals/Watch evidence for one repaired case.

## Expected result

All six cases pass, O5005 is Priority at the boundary, O5006 is Review, and the defect log records symptom, root cause, change and retest evidence.

## Troubleshooting

If the workflow still uses old values, stop Debug rather than rerunning from a paused state. If a Watch expression errors, check variable scope at the paused activity.

## Evidence and acceptance criteria

Completed defect log and screenshot of a breakpoint with Locals/Watch values.

The submission is acceptable when the expected result is visible, output files reconcile to the mock input, and the evidence identifies the tested transaction or process.
