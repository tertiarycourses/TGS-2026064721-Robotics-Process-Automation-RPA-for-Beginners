# Lab 3: Route Customer Requests with If and Switch

**Topic:** 2

**Objective:** LO2 — Plan and construct workflows with variables, arguments and control flow

**Alignment:** A2, A3, A4 · K4, K6

**Suggested time:** 65 minutes

## Scenario and outcome

Translate a routing requirement into a readable UiPath flowchart that validates priority and sends each request to the correct queue.

You will produce: **A flowchart with validation, If and Switch branches plus a reusable routing output argument**

## Folder contents

- `Main.xaml` — editable UiPath Studio starter workflow.
- `project.json` — UiPath project manifest.
- `mock-route-customer-requests-with-if-and-switch.csv` — portable mock source data.
- `mock-route-customer-requests-with-if-and-switch.xlsx` — formatted mock workbook with Data and Rules sheets.
- `CHECKLIST.md` — completion and evidence checklist.


## Preparation

1. Use UiPath Studio Community 2024.10 or later.
2. Extract or clone this entire folder. Keep the data files beside `project.json`.
3. Open `project.json` in Studio and allow package restore. Upgrade dependency versions if Studio requests it.
4. Use mock data only. Do not enter passwords, tokens or real personal data.

## Procedure

1. Read the ExpectedQueue examples and express the routing rules in plain language before building activities.
2. Open Main.xaml and confirm it uses a Flowchart with requestCategory, priority and selectedQueue variables.
3. Add a Flow Decision that checks whether Priority equals High after applying Trim and a consistent case.
4. Add a Switch on Category with Billing, Technical and General cases plus a default Manual-Review case.
5. For high-priority Billing and Technical requests, append -Priority to the queue name.
6. Create or inspect the out_SelectedQueue argument. Assign the final selectedQueue before the workflow ends.
7. Run all six rows one by one or through the supplied test loop. Record the ActualQueue in the workbook.
8. Compare ActualQueue with ExpectedQueue and investigate any mismatch at the decision that produced it.
9. Capture the flowchart and the completed comparison table.

## Expected result

All six requests match ExpectedQueue, including Unknown -> Manual-Review and the two priority routes.

## Troubleshooting

If a category misses its Switch case, normalise the value once before the Switch. If the output argument is empty, ensure the final Assign executes on every path.

## Evidence and acceptance criteria

Completed route-results workbook and one screenshot of the full flowchart.

The submission is acceptable when the expected result is visible, output files reconcile to the mock input, and the evidence identifies the tested transaction or process.
