# Lab 9: Publish and Run a Process with Orchestrator

**Topic:** 5

**Objective:** LO5 — Package, deploy, monitor and optimise a UiPath process

**Alignment:** A7, A8, A9 · K9, K12

**Suggested time:** 80 minutes

## Scenario and outcome

Publish a validated project, create or update an Orchestrator process, start a job or Assistant run, and capture version and execution evidence.

You will produce: **A published package, deployed process, successful job and release evidence record**

## Folder contents

- `Main.xaml` — editable UiPath Studio starter workflow.
- `project.json` — UiPath project manifest.
- `mock-publish-and-run-a-process-with-orchestrator.csv` — portable mock source data.
- `mock-publish-and-run-a-process-with-orchestrator.xlsx` — formatted mock workbook with Data and Rules sheets.
- `CHECKLIST.md` — completion and evidence checklist.


## Preparation

1. Use UiPath Studio Community 2024.10 or later.
2. Extract or clone this entire folder. Keep the data files beside `project.json`.
3. Open `project.json` in Studio and allow package restore. Upgrade dependency versions if Studio requests it.
4. Use mock data only. Do not enter passwords, tokens or real personal data.

## Procedure

1. Open the project and run Analyze File/Project. Resolve blocking validation errors before publishing.
2. Update Project Settings with a meaningful description and increment the package version. Do not reuse an existing version for changed content.
3. Publish to the connected Orchestrator tenant or the instructor-approved custom feed. Record feed, version and time in the release workbook.
4. In Orchestrator, enter the correct modern folder. Confirm the folder has machine/runtime capacity and the learner account has appropriate permissions.
5. Create a Process from the published package or update the existing process to the new version. Verify the selected entry point.
6. Start a Job with safe input arguments, or launch the attended process in UiPath Assistant if the lab environment is configured for attended execution.
7. Monitor the job until it reaches Successful. Open Logs and confirm the release version and transaction summary.
8. Record job ID, start/end time, status and package version. If the run faults, capture the exception and correct the project before republishing a new version.
9. Capture the process version and successful job details as evidence. Do not include credentials or machine keys.

## Expected result

The package version is traceable to a deployed process and a successful execution, with no credential or machine-key exposure in evidence.

## Troubleshooting

If the package is not visible, verify tenant, folder and feed. If a job stays Pending, check machine/runtime allocation and folder assignment rather than repeatedly starting more jobs.

## Evidence and acceptance criteria

Completed release record plus screenshots of the process version and successful job details.

The submission is acceptable when the expected result is visible, output files reconcile to the mock input, and the evidence identifies the tested transaction or process.
