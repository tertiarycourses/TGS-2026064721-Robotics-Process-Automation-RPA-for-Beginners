# Lab 4: Process a Customer DataTable with Loops

**Topic:** 2

**Objective:** LO2 — Construct a data-driven workflow using loops and structured data

**Alignment:** A2, A4 · K4, K6, K11

**Suggested time:** 70 minutes

## Scenario and outcome

Read customer records, validate fields, calculate a service segment and append a traceable result for every row.

You will produce: **A For Each Row transaction workflow with row-level validation and an output DataTable**

## Folder contents

- `Main.xaml` — editable UiPath Studio starter workflow.
- `project.json` — UiPath project manifest.
- `mock-process-a-customer-datatable-with-loops.csv` — portable mock source data.
- `mock-process-a-customer-datatable-with-loops.xlsx` — formatted mock workbook with Data and Rules sheets.
- `CHECKLIST.md` — completion and evidence checklist.


## Preparation

1. Use UiPath Studio Community 2024.10 or later.
2. Extract or clone this entire folder. Keep the data files beside `project.json`.
3. Open `project.json` in Studio and allow package restore. Upgrade dependency versions if Studio requests it.
4. Use mock data only. Do not enter passwords, tokens or real personal data.

## Procedure

1. Open mock-customers.csv and confirm the schema. Blank Email is intentional and must be handled as a business exception.
2. Open Main.xaml and inspect the input and output DataTable variables.
3. Use Read CSV to load the file. Log the input Rows.Count before processing.
4. Use For Each Row in Data Table. Inside the loop, read CustomerID, SpendSGD and Email into clearly typed variables.
5. If Email is blank, set Segment to Review. Otherwise set Premium for Spend >= 8000, Growth for Spend >= 1000, and Standard for the remainder.
6. Append CustomerID, Segment and Status to the output DataTable. Preserve the identifier on every row.
7. Write the result to output/customer-segments.csv. Create the output folder if required.
8. Reconcile input row count with output row count and compare Segment with ExpectedSegment.
9. Capture the output file and Output panel count summary.

## Expected result

The output contains six traceable rows, every segment matches ExpectedSegment, and the blank-email record is routed to Review without stopping the workflow.

## Troubleshooting

If numeric conversion fails, use Double.TryParse or Convert.ToDouble only after checking for blanks. If the output file is locked, close it in Excel before rerunning.

## Evidence and acceptance criteria

output/customer-segments.csv and a screenshot showing the 6-in / 6-out reconciliation.

The submission is acceptable when the expected result is visible, output files reconcile to the mock input, and the evidence identifies the tested transaction or process.
