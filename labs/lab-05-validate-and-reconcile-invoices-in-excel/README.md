# Lab 5: Validate and Reconcile Invoices in Excel

**Topic:** 3

**Objective:** LO3 — Design and validate data and Excel automation processes

**Alignment:** A4, A5 · K5, K11

**Suggested time:** 75 minutes

## Scenario and outcome

Read an invoice register, validate required values, calculate line totals and write a reconciliation sheet with evidence of exceptions.

You will produce: **An Excel automation that produces Valid, Review and Rejected outcomes with a reconciliation summary**

## Folder contents

- `Main.xaml` — editable UiPath Studio starter workflow.
- `project.json` — UiPath project manifest.
- `mock-validate-and-reconcile-invoices-in-excel.csv` — portable mock source data.
- `mock-validate-and-reconcile-invoices-in-excel.xlsx` — formatted mock workbook with Data and Rules sheets.
- `CHECKLIST.md` — completion and evidence checklist.


## Preparation

1. Use UiPath Studio Community 2024.10 or later.
2. Extract or clone this entire folder. Keep the data files beside `project.json`.
3. Open `project.json` in Studio and allow package restore. Upgrade dependency versions if Studio requests it.
4. Use mock data only. Do not enter passwords, tokens or real personal data.

## Procedure

1. Open mock-invoices.xlsx and review the Inputs and Rules sheets. Keep the original input sheet unchanged.
2. Open Main.xaml. Confirm the project uses a relative path based on the project folder, not an absolute user path.
3. Use Use Excel File or Excel Process Scope, then Read Range from Inputs into dtInvoices.
4. For each row, validate Supplier and InvoiceDate. Missing required values produce Review; Quantity <= 0 or UnitPrice <= 0 produces Rejected.
5. For Valid rows calculate Subtotal = Quantity * UnitPrice and Total = Subtotal * (1 + TaxRate). Keep calculations numeric until writing.
6. Build a result table with InvoiceID, Status, Subtotal, Total and Reason.
7. Write results to a new Results sheet and write counts by status to a Summary sheet.
8. Compare actual status with ExpectedStatus and confirm totals for INV4001 and INV4002 manually.
9. Save output/invoice-reconciliation.xlsx and capture the Summary sheet as evidence.

## Expected result

All six invoices receive the expected status, Valid totals calculate correctly, and the Summary counts reconcile to six input rows.

## Troubleshooting

If Excel remains open after a fault, close the application and rerun with the Excel scope configured to save and close. If dates import as text, treat blank checks separately from display format.

## Evidence and acceptance criteria

output/invoice-reconciliation.xlsx with Results and Summary sheets.

The submission is acceptable when the expected result is visible, output files reconcile to the mock input, and the evidence identifies the tested transaction or process.
