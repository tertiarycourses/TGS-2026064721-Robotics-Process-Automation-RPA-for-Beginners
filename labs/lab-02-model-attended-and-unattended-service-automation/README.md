# Lab 2: Model Attended and Unattended Service Automation

**Topic:** 1

**Objective:** LO1 — Determine best practices for attended and unattended automation

**Alignment:** A1, A6 · K1, K3, K10

**Suggested time:** 55 minutes

## Scenario and outcome

Classify service requests and design two operating modes: an attended desktop assistant for judgement-heavy cases and an unattended route for complete, low-risk requests.

You will produce: **A routing matrix and UiPath workflow that labels each request Attended, Unattended or Human Review**

## Folder contents

- `Main.xaml` — editable UiPath Studio starter workflow.
- `project.json` — UiPath project manifest.
- `mock-model-attended-and-unattended-service-automation.csv` — portable mock source data.
- `mock-model-attended-and-unattended-service-automation.xlsx` — formatted mock workbook with Data and Rules sheets.
- `CHECKLIST.md` — completion and evidence checklist.


## Preparation

1. Use UiPath Studio Community 2024.10 or later.
2. Extract or clone this entire folder. Keep the data files beside `project.json`.
3. Open `project.json` in Studio and allow package restore. Upgrade dependency versions if Studio requests it.
4. Use mock data only. Do not enter passwords, tokens or real personal data.

## Procedure

1. Open mock-service-requests.csv and define the routing rules before opening Studio.
2. Route complete, low-risk and no-judgement requests to Unattended. Route judgement-heavy but complete requests to Attended. Route incomplete requests to Human Review.
3. Record the rules in the workbook Rules sheet and manually classify the first two rows as a check.
4. Open Main.xaml. Inspect the requestType, isComplete, riskLevel and requiresJudgement variables.
5. Use an If activity for completeness, followed by a Switch or nested If for operating mode. Keep a default Human Review path.
6. Add a Write Line message containing RequestID, selected operating mode and reason.
7. Run at least three test cases: one Unattended, one Attended and one Human Review.
8. Compare the workflow results with the manually classified rows and correct any rule mismatch.
9. Capture the three Output messages and the routing matrix as evidence.

## Expected result

Three test cases reach three intended routes, every route states a reason, and incomplete requests never continue to unattended processing.

## Troubleshooting

If all cases take the same branch, check Boolean values and remove surrounding spaces. If Switch misses a case, verify text casing or normalise with Trim.ToLower.

## Evidence and acceptance criteria

Routing matrix and screenshots of the three distinct UiPath outcomes.

The submission is acceptable when the expected result is visible, output files reconcile to the mock input, and the evidence identifies the tested transaction or process.
