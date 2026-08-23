# Lab 6: Extract and Filter a Singapore Schools Table

**Topic:** 3

**Objective:** LO3 — Design and validate web and structured-data automation

**Alignment:** A1, A4, A5 · K5, K7

**Suggested time:** 85 minutes

## Scenario and outcome

Use browser table extraction to capture a list of secondary schools, preserve source evidence, filter Ang Mo Kio records and write a validated Excel output.

You will produce: **A table-extraction workflow, schools output workbook and Ang Mo Kio count summary**

## Folder contents

- `Main.xaml` — editable UiPath Studio starter workflow.
- `project.json` — UiPath project manifest.
- `mock-extract-and-filter-a-singapore-schools-table.csv` — portable mock source data.
- `mock-extract-and-filter-a-singapore-schools-table.xlsx` — formatted mock workbook with Data and Rules sheets.
- `CHECKLIST.md` — completion and evidence checklist.


## Preparation

1. Use UiPath Studio Community 2024.10 or later.
2. Extract or clone this entire folder. Keep the data files beside `project.json`.
3. Open `project.json` in Studio and allow package restore. Upgrade dependency versions if Studio requests it.
4. Use mock data only. Do not enter passwords, tokens or real personal data.

## Procedure

1. Use the supplied mock-schools.xlsx as the deterministic fallback. The live-source exercise must use an authorised public page and follow its terms.
2. Open Main.xaml and set sourceUrl to the course-approved schools page. Keep the URL in one variable or configuration value.
3. Use Application/Browser to open or attach to the browser and verify the page title before extraction.
4. Add Extract Table Data. Indicate the first and second rows so UiPath infers the repeating structure; rename columns meaningfully.
5. Set a reasonable maximum record count and configure pagination only if the source requires it.
6. Validate that SchoolName and PlanningArea columns exist and that Rows.Count is greater than zero. Otherwise throw a BusinessRuleException.
7. Filter rows where PlanningArea.Trim equals Ang Mo Kio, then record the count in a summary variable.
8. Write the full table and filtered table to output/schools-analysis.xlsx, with SourceURL and extraction timestamp on a Summary sheet.
9. Compare the deterministic mock dataset result: Ang Mo Kio count must equal 3. Capture the extraction configuration and Summary sheet.

## Expected result

The deterministic dataset produces six total rows and three Ang Mo Kio rows; the output records the source URL, timestamp and both counts.

## Troubleshooting

If the live table structure changes, use the supplied mock workbook and repair selectors in a separate copy. If the count is zero, trim and normalise PlanningArea before comparing.

## Evidence and acceptance criteria

output/schools-analysis.xlsx plus screenshots of Extract Table Data and the validated Summary sheet.

The submission is acceptable when the expected result is visible, output files reconcile to the mock input, and the evidence identifies the tested transaction or process.
