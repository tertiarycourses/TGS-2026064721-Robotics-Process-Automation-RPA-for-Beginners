# Lab 1: Assess an RPA Opportunity and Build a First Sequence

**Topic:** 1

**Objective:** LO1 — Determine appropriate RPA opportunities and best practices

**Alignment:** A1, A6 · K1, K2, K10

**Suggested time:** 55 minutes

## Scenario and outcome

Score a small set of workplace processes, select a strong candidate, then run a starter UiPath sequence that reads the selected process and writes an evidence summary.

You will produce: **A scored opportunity register, a selected automation candidate and a runnable UiPath sequence**

## Folder contents

- `Main.xaml` — editable UiPath Studio starter workflow.
- `project.json` — UiPath project manifest.
- `mock-assess-an-rpa-opportunity-and-build-a-first-sequence.csv` — portable mock source data.
- `mock-assess-an-rpa-opportunity-and-build-a-first-sequence.xlsx` — formatted mock workbook with Data and Rules sheets.
- `CHECKLIST.md` — completion and evidence checklist.


## Preparation

1. Use UiPath Studio Community 2024.10 or later.
2. Extract or clone this entire folder. Keep the data files beside `project.json`.
3. Open `project.json` in Studio and allow package restore. Upgrade dependency versions if Studio requests it.
4. Use mock data only. Do not enter passwords, tokens or real personal data.

## Procedure

1. Open mock-process-candidates.xlsx and review the five processes. Do not choose by volume alone; consider rule clarity, digital inputs, exception rate and ownership.
2. Add four score columns: VolumeScore, RulesScore, DigitalScore and ExceptionScore. Use a 1–5 scale and document the rule in the Notes sheet.
3. Calculate TotalScore as the sum of the four scores. Sort descending and record the selected ProcessID in the Decision sheet.
4. Open the supplied UiPath project in Studio. If prompted, allow Studio to restore packages or convert the project to the current Windows compatibility.
5. Open Main.xaml and inspect the Sequence variables selectedProcess and decisionMessage.
6. Set selectedProcess to the ProcessName of the highest-scoring candidate. Keep the value configurable rather than embedding it into multiple activities.
7. Run the workflow. Confirm the Output panel prints the process name, why it suits RPA and the next governance action.
8. Change selectedProcess once and run again to prove the value is not coupled to one candidate.
9. Capture the completed scoring table and successful Output panel as evidence.

## Expected result

The workbook ranks a rule-based digital process highest, and Main.xaml runs successfully with a clear selected-process message in the Output panel.

## Troubleshooting

If the project opens with missing dependencies, choose Manage Packages > Restore. If the output is blank, inspect the selectedProcess variable scope and default value.

## Evidence and acceptance criteria

Completed XLSX plus one screenshot showing the successful UiPath Output message.

The submission is acceptable when the expected result is visible, output files reconcile to the mock input, and the evidence identifies the tested transaction or process.
