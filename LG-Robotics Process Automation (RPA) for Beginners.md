# Robotics Process Automation (RPA) for Beginners — Learner Guide

**Course Code:** TGS-2026064721  |  **Version:** v15.0 · 23 August 2026  |  **Provider:** Tertiary Infotech Academy Pte Ltd

## Contents

- [Welcome to the Course](#welcome-to-the-course)
  - [Learning Outcomes](#learning-outcomes)
  - [How to Use This Guide](#how-to-use-this-guide)
  - [Environment Preparation](#environment-preparation)
- [Course Concepts and Labs](#course-concepts-and-labs)
  - [Topic 01: Introduction to RPA](#topic-01-introduction-to-rpa)
  - [Lab 1: Assess an RPA Opportunity and Build a First Sequence](#lab-1-assess-an-rpa-opportunity-and-build-a-first-sequence)
  - [Lab 2: Model Attended and Unattended Service Automation](#lab-2-model-attended-and-unattended-service-automation)
  - [Topic 02: RPA Workflows](#topic-02-rpa-workflows)
  - [Lab 3: Route Customer Requests with If and Switch](#lab-3-route-customer-requests-with-if-and-switch)
  - [Lab 4: Process a Customer DataTable with Loops](#lab-4-process-a-customer-datatable-with-loops)
  - [Topic 03: Automations](#topic-03-automations)
  - [Lab 5: Validate and Reconcile Invoices in Excel](#lab-5-validate-and-reconcile-invoices-in-excel)
  - [Lab 6: Extract and Filter a Singapore Schools Table](#lab-6-extract-and-filter-a-singapore-schools-table)
  - [Topic 04: Debug and Exception Handling](#topic-04-debug-and-exception-handling)
  - [Lab 7: Debug a Failing Order Workflow](#lab-7-debug-a-failing-order-workflow)
  - [Lab 8: Build Resilient File Processing with Try Catch](#lab-8-build-resilient-file-processing-with-try-catch)
  - [Topic 05: Manage RPA](#topic-05-manage-rpa)
  - [Lab 9: Publish and Run a Process with Orchestrator](#lab-9-publish-and-run-a-process-with-orchestrator)
  - [Lab 10: Design and Monitor a Multi-Robot Queue](#lab-10-design-and-monitor-a-multi-robot-queue)
- [Assessment Preparation](#assessment-preparation)
  - [Written Assessment](#written-assessment)
  - [Practical Performance](#practical-performance)
  - [Final Readiness Check](#final-readiness-check)
- [Glossary](#glossary)

## Welcome to the Course

This guide is the detailed working companion for the course. The slide deck explains concepts and decision models; this guide contains the click-by-click UiPath procedures, expected results, troubleshooting advice and evidence requirements.

| Course field | Detail |
| --- | --- |
| Title | Robotics Process Automation (RPA) for Beginners |
| Course code | TGS-2026064721 |
| Duration | 2 days · 16 training hours |
| Platform | UiPath Studio Community and Automation Cloud / Orchestrator |
| Assessment | 13-question Written Assessment (60 min) and 5-task Practical Performance (90 min) |
| Lab repository | https://github.com/tertiarycourses/TGS-2026064721-Robotics-Process-Automation-RPA-for-Beginners |


### Learning Outcomes

- LO1: Determine appropriate RPA opportunities and best practices for attended and unattended automation.
- LO2: Plan and construct UiPath workflows using sequences, flowcharts, state machines, variables, arguments and control flow.
- LO3: Design and validate UI, web, data and Excel automation processes with reliable selectors and structured outputs.
- LO4: Test, debug, log and handle exceptions in RPA workflows.
- LO5: Package, deploy, monitor and optimise UiPath processes using Assistant and Orchestrator.


### How to Use This Guide

- Read the concept explanation before starting its lab.
- Keep each lab folder intact so project.json, XAML and mock data stay together.
- Use only the supplied mock data; never place credentials or real personal data in learner evidence.
- Check the expected result and troubleshooting guidance before requesting help.
- Retain the stated evidence because it supports practical assessment readiness.


### Environment Preparation

1. Install UiPath Studio Community or Studio 2024.10 or later. Sign in with the training account provided by the trainer.
2. Open Studio and choose Settings > Licence and Profile. Confirm Studio can create a Process project using Windows compatibility.
3. Download or clone the lab repository. Keep every lab as a separate folder.

   ```text
   https://github.com/tertiarycourses/TGS-2026064721-Robotics-Process-Automation-RPA-for-Beginners
   ```

4. Open a lab by selecting its project.json file. Wait for package restore before opening Main.xaml.
5. If a package version is unavailable, use Manage Packages to select the nearest compatible stable version, then save.
6. Run Main.xaml once. A starter evidence message should appear in the Output panel.

> **Note:** UiPath cloud screens and package versions may change. Follow the named resource and verify the resulting state rather than relying only on button position.


## Course Concepts and Labs


### Topic 01: Introduction to RPA

Opportunity selection · attended and unattended automation · value · governance · intelligent automation.

| Concept | Practical meaning |
| --- | --- |
| RPA operates the interface | A software robot performs rule-based actions through applications much as a user would. |
| Choose stable, repetitive work | Volume, clear rules, structured data and low exception rates make strong candidates. |
| Attended supports people | The user starts or assists the automation at the desktop. |
| Unattended runs centrally | Orchestrator schedules and monitors work without a user at the screen. |
| IPA expands the boundary | OCR, document understanding and AI handle variability beyond simple deterministic rules. |
| Automation needs controls | Ownership, credentials, logging, exception paths and human review make robots sustainable. |


#### Why this topic matters

Selecting the wrong process creates fragile automation and poor returns. Begin with stable rules, digital data, a clear owner and known exceptions.


### Lab 1: Assess an RPA Opportunity and Build a First Sequence

Score a small set of workplace processes, select a strong candidate, then run a starter UiPath sequence that reads the selected process and writes an evidence summary.

| Lab field | Detail |
| --- | --- |
| Objective | LO1 — Determine appropriate RPA opportunities and best practices |
| Alignment | A1, A6 · K1, K2, K10 |
| Suggested time | 55 minutes |
| Tools | UiPath Studio Community, CSV, Excel, Write Line |
| Deliverable | A scored opportunity register, a selected automation candidate and a runnable UiPath sequence |


#### Files

- labs/lab-01-assess-an-rpa-opportunity-and-build-a-first-sequence/project.json
- labs/lab-01-assess-an-rpa-opportunity-and-build-a-first-sequence/Main.xaml
- labs/lab-01-assess-an-rpa-opportunity-and-build-a-first-sequence/mock-assess-an-rpa-opportunity-and-build-a-first-sequence.csv
- labs/lab-01-assess-an-rpa-opportunity-and-build-a-first-sequence/mock-assess-an-rpa-opportunity-and-build-a-first-sequence.xlsx
- labs/lab-01-assess-an-rpa-opportunity-and-build-a-first-sequence/CHECKLIST.md


#### Detailed Procedure

1. Open mock-process-candidates.xlsx and review the five processes. Do not choose by volume alone; consider rule clarity, digital inputs, exception rate and ownership.
2. Add four score columns: VolumeScore, RulesScore, DigitalScore and ExceptionScore. Use a 1–5 scale and document the rule in the Notes sheet.
3. Calculate TotalScore as the sum of the four scores. Sort descending and record the selected ProcessID in the Decision sheet.
4. Open the supplied UiPath project in Studio. If prompted, allow Studio to restore packages or convert the project to the current Windows compatibility.
5. Open Main.xaml and inspect the Sequence variables selectedProcess and decisionMessage.
6. Set selectedProcess to the ProcessName of the highest-scoring candidate. Keep the value configurable rather than embedding it into multiple activities.
7. Run the workflow. Confirm the Output panel prints the process name, why it suits RPA and the next governance action.
8. Change selectedProcess once and run again to prove the value is not coupled to one candidate.
9. Capture the completed scoring table and successful Output panel as evidence.


#### Expected Result

The workbook ranks a rule-based digital process highest, and Main.xaml runs successfully with a clear selected-process message in the Output panel.


#### Troubleshooting

If the project opens with missing dependencies, choose Manage Packages > Restore. If the output is blank, inspect the selectedProcess variable scope and default value.


#### Evidence and Acceptance Criteria

Completed XLSX plus one screenshot showing the successful UiPath Output message.

> **Note:** Before leaving this lab, reconcile input and output record counts, retain the requested evidence, and ensure no credentials or personal data are visible.


### Lab 2: Model Attended and Unattended Service Automation

Classify service requests and design two operating modes: an attended desktop assistant for judgement-heavy cases and an unattended route for complete, low-risk requests.

| Lab field | Detail |
| --- | --- |
| Objective | LO1 — Determine best practices for attended and unattended automation |
| Alignment | A1, A6 · K1, K3, K10 |
| Suggested time | 55 minutes |
| Tools | UiPath Studio Community, CSV, Excel, If, Switch, Write Line |
| Deliverable | A routing matrix and UiPath workflow that labels each request Attended, Unattended or Human Review |


#### Files

- labs/lab-02-model-attended-and-unattended-service-automation/project.json
- labs/lab-02-model-attended-and-unattended-service-automation/Main.xaml
- labs/lab-02-model-attended-and-unattended-service-automation/mock-model-attended-and-unattended-service-automation.csv
- labs/lab-02-model-attended-and-unattended-service-automation/mock-model-attended-and-unattended-service-automation.xlsx
- labs/lab-02-model-attended-and-unattended-service-automation/CHECKLIST.md


#### Detailed Procedure

1. Open mock-service-requests.csv and define the routing rules before opening Studio.
2. Route complete, low-risk and no-judgement requests to Unattended. Route judgement-heavy but complete requests to Attended. Route incomplete requests to Human Review.
3. Record the rules in the workbook Rules sheet and manually classify the first two rows as a check.
4. Open Main.xaml. Inspect the requestType, isComplete, riskLevel and requiresJudgement variables.
5. Use an If activity for completeness, followed by a Switch or nested If for operating mode. Keep a default Human Review path.
6. Add a Write Line message containing RequestID, selected operating mode and reason.
7. Run at least three test cases: one Unattended, one Attended and one Human Review.
8. Compare the workflow results with the manually classified rows and correct any rule mismatch.
9. Capture the three Output messages and the routing matrix as evidence.


#### Expected Result

Three test cases reach three intended routes, every route states a reason, and incomplete requests never continue to unattended processing.


#### Troubleshooting

If all cases take the same branch, check Boolean values and remove surrounding spaces. If Switch misses a case, verify text casing or normalise with Trim.ToLower.


#### Evidence and Acceptance Criteria

Routing matrix and screenshots of the three distinct UiPath outcomes.

> **Note:** Before leaving this lab, reconcile input and output record counts, retain the requested evidence, and ensure no credentials or personal data are visible.


### Topic 02: RPA Workflows

Sequences · flowcharts · state machines · variables · arguments · decisions · loops · data tables.

| Concept | Practical meaning |
| --- | --- |
| Sequence | Best for a short linear path with a clear beginning and end. |
| Flowchart | Makes branching logic and alternate paths easy to inspect. |
| State machine | Models event-driven work that moves between named states. |
| Variables hold local state | Name, type, default value and scope determine what a value can do. |
| Arguments cross boundaries | In, Out and In/Out arguments create explicit contracts between workflows. |
| Control flow expresses rules | If, Switch, For Each, While and Do While turn requirements into executable logic. |


#### Why this topic matters

Maintainable robots start with explicit triggers, decisions, reusable workflow contracts and traceable data movement.


### Lab 3: Route Customer Requests with If and Switch

Translate a routing requirement into a readable UiPath flowchart that validates priority and sends each request to the correct queue.

| Lab field | Detail |
| --- | --- |
| Objective | LO2 — Plan and construct workflows with variables, arguments and control flow |
| Alignment | A2, A3, A4 · K4, K6 |
| Suggested time | 65 minutes |
| Tools | UiPath Studio Community, Flowchart, If, Switch, arguments |
| Deliverable | A flowchart with validation, If and Switch branches plus a reusable routing output argument |


#### Files

- labs/lab-03-route-customer-requests-with-if-and-switch/project.json
- labs/lab-03-route-customer-requests-with-if-and-switch/Main.xaml
- labs/lab-03-route-customer-requests-with-if-and-switch/mock-route-customer-requests-with-if-and-switch.csv
- labs/lab-03-route-customer-requests-with-if-and-switch/mock-route-customer-requests-with-if-and-switch.xlsx
- labs/lab-03-route-customer-requests-with-if-and-switch/CHECKLIST.md


#### Detailed Procedure

1. Read the ExpectedQueue examples and express the routing rules in plain language before building activities.
2. Open Main.xaml and confirm it uses a Flowchart with requestCategory, priority and selectedQueue variables.
3. Add a Flow Decision that checks whether Priority equals High after applying Trim and a consistent case.
4. Add a Switch on Category with Billing, Technical and General cases plus a default Manual-Review case.
5. For high-priority Billing and Technical requests, append -Priority to the queue name.
6. Create or inspect the out_SelectedQueue argument. Assign the final selectedQueue before the workflow ends.
7. Run all six rows one by one or through the supplied test loop. Record the ActualQueue in the workbook.
8. Compare ActualQueue with ExpectedQueue and investigate any mismatch at the decision that produced it.
9. Capture the flowchart and the completed comparison table.


#### Expected Result

All six requests match ExpectedQueue, including Unknown -> Manual-Review and the two priority routes.


#### Troubleshooting

If a category misses its Switch case, normalise the value once before the Switch. If the output argument is empty, ensure the final Assign executes on every path.


#### Evidence and Acceptance Criteria

Completed route-results workbook and one screenshot of the full flowchart.

> **Note:** Before leaving this lab, reconcile input and output record counts, retain the requested evidence, and ensure no credentials or personal data are visible.


### Lab 4: Process a Customer DataTable with Loops

Read customer records, validate fields, calculate a service segment and append a traceable result for every row.

| Lab field | Detail |
| --- | --- |
| Objective | LO2 — Construct a data-driven workflow using loops and structured data |
| Alignment | A2, A4 · K4, K6, K11 |
| Suggested time | 70 minutes |
| Tools | UiPath Studio Community, Read CSV, DataTable, For Each Row, Add Data Row, Write CSV |
| Deliverable | A For Each Row transaction workflow with row-level validation and an output DataTable |


#### Files

- labs/lab-04-process-a-customer-datatable-with-loops/project.json
- labs/lab-04-process-a-customer-datatable-with-loops/Main.xaml
- labs/lab-04-process-a-customer-datatable-with-loops/mock-process-a-customer-datatable-with-loops.csv
- labs/lab-04-process-a-customer-datatable-with-loops/mock-process-a-customer-datatable-with-loops.xlsx
- labs/lab-04-process-a-customer-datatable-with-loops/CHECKLIST.md


#### Detailed Procedure

1. Open mock-customers.csv and confirm the schema. Blank Email is intentional and must be handled as a business exception.
2. Open Main.xaml and inspect the input and output DataTable variables.
3. Use Read CSV to load the file. Log the input Rows.Count before processing.
4. Use For Each Row in Data Table. Inside the loop, read CustomerID, SpendSGD and Email into clearly typed variables.
5. If Email is blank, set Segment to Review. Otherwise set Premium for Spend >= 8000, Growth for Spend >= 1000, and Standard for the remainder.
6. Append CustomerID, Segment and Status to the output DataTable. Preserve the identifier on every row.
7. Write the result to output/customer-segments.csv. Create the output folder if required.
8. Reconcile input row count with output row count and compare Segment with ExpectedSegment.
9. Capture the output file and Output panel count summary.


#### Expected Result

The output contains six traceable rows, every segment matches ExpectedSegment, and the blank-email record is routed to Review without stopping the workflow.


#### Troubleshooting

If numeric conversion fails, use Double.TryParse or Convert.ToDouble only after checking for blanks. If the output file is locked, close it in Excel before rerunning.


#### Evidence and Acceptance Criteria

output/customer-segments.csv and a screenshot showing the 6-in / 6-out reconciliation.

> **Note:** Before leaving this lab, reconcile input and output record counts, retain the requested evidence, and ensure no credentials or personal data are visible.


### Topic 03: Automations

UI automation · selectors · recording · browser work · table extraction · Excel integration.

| Concept | Practical meaning |
| --- | --- |
| UI elements are targets | A selector describes the application and element a robot should operate. |
| Reliable selectors use stable attributes | Prefer durable IDs, names and anchors; avoid volatile indexes and session tokens. |
| Recording accelerates a draft | Recorded actions are a starting point that must be renamed, parameterised and tested. |
| Table extraction creates structure | Browser rows become a DataTable that can be filtered, validated and written to Excel. |
| Excel is both source and destination | Read Range, Write Range and workbook activities connect business data to workflows. |
| Validation closes the loop | Counts, required columns, output files and screenshots provide objective evidence. |


#### Why this topic matters

UI, web and Excel automation must target stable elements, validate outputs and preserve record counts.


### Lab 5: Validate and Reconcile Invoices in Excel

Read an invoice register, validate required values, calculate line totals and write a reconciliation sheet with evidence of exceptions.

| Lab field | Detail |
| --- | --- |
| Objective | LO3 — Design and validate data and Excel automation processes |
| Alignment | A4, A5 · K5, K11 |
| Suggested time | 75 minutes |
| Tools | UiPath Studio Community, Use Excel File, Read Range, For Each Row, Write Range |
| Deliverable | An Excel automation that produces Valid, Review and Rejected outcomes with a reconciliation summary |


#### Files

- labs/lab-05-validate-and-reconcile-invoices-in-excel/project.json
- labs/lab-05-validate-and-reconcile-invoices-in-excel/Main.xaml
- labs/lab-05-validate-and-reconcile-invoices-in-excel/mock-validate-and-reconcile-invoices-in-excel.csv
- labs/lab-05-validate-and-reconcile-invoices-in-excel/mock-validate-and-reconcile-invoices-in-excel.xlsx
- labs/lab-05-validate-and-reconcile-invoices-in-excel/CHECKLIST.md


#### Detailed Procedure

1. Open mock-invoices.xlsx and review the Inputs and Rules sheets. Keep the original input sheet unchanged.
2. Open Main.xaml. Confirm the project uses a relative path based on the project folder, not an absolute user path.
3. Use Use Excel File or Excel Process Scope, then Read Range from Inputs into dtInvoices.
4. For each row, validate Supplier and InvoiceDate. Missing required values produce Review; Quantity <= 0 or UnitPrice <= 0 produces Rejected.
5. For Valid rows calculate Subtotal = Quantity * UnitPrice and Total = Subtotal * (1 + TaxRate). Keep calculations numeric until writing.
6. Build a result table with InvoiceID, Status, Subtotal, Total and Reason.
7. Write results to a new Results sheet and write counts by status to a Summary sheet.
8. Compare actual status with ExpectedStatus and confirm totals for INV4001 and INV4002 manually.
9. Save output/invoice-reconciliation.xlsx and capture the Summary sheet as evidence.


#### Expected Result

All six invoices receive the expected status, Valid totals calculate correctly, and the Summary counts reconcile to six input rows.


#### Troubleshooting

If Excel remains open after a fault, close the application and rerun with the Excel scope configured to save and close. If dates import as text, treat blank checks separately from display format.


#### Evidence and Acceptance Criteria

output/invoice-reconciliation.xlsx with Results and Summary sheets.

> **Note:** Before leaving this lab, reconcile input and output record counts, retain the requested evidence, and ensure no credentials or personal data are visible.


### Lab 6: Extract and Filter a Singapore Schools Table

Use browser table extraction to capture a list of secondary schools, preserve source evidence, filter Ang Mo Kio records and write a validated Excel output.

| Lab field | Detail |
| --- | --- |
| Objective | LO3 — Design and validate web and structured-data automation |
| Alignment | A1, A4, A5 · K5, K7 |
| Suggested time | 85 minutes |
| Tools | UiPath Studio Community, Use Application/Browser, Extract Table Data, DataTable, Excel |
| Deliverable | A table-extraction workflow, schools output workbook and Ang Mo Kio count summary |


#### Files

- labs/lab-06-extract-and-filter-a-singapore-schools-table/project.json
- labs/lab-06-extract-and-filter-a-singapore-schools-table/Main.xaml
- labs/lab-06-extract-and-filter-a-singapore-schools-table/mock-extract-and-filter-a-singapore-schools-table.csv
- labs/lab-06-extract-and-filter-a-singapore-schools-table/mock-extract-and-filter-a-singapore-schools-table.xlsx
- labs/lab-06-extract-and-filter-a-singapore-schools-table/CHECKLIST.md


#### Detailed Procedure

1. Use the supplied mock-schools.xlsx as the deterministic fallback. The live-source exercise must use an authorised public page and follow its terms.
2. Open Main.xaml and set sourceUrl to the course-approved schools page. Keep the URL in one variable or configuration value.
3. Use Application/Browser to open or attach to the browser and verify the page title before extraction.
4. Add Extract Table Data. Indicate the first and second rows so UiPath infers the repeating structure; rename columns meaningfully.
5. Set a reasonable maximum record count and configure pagination only if the source requires it.
6. Validate that SchoolName and PlanningArea columns exist and that Rows.Count is greater than zero. Otherwise throw a BusinessRuleException.
7. Filter rows where PlanningArea.Trim equals Ang Mo Kio, then record the count in a summary variable.
8. Write the full table and filtered table to output/schools-analysis.xlsx, with SourceURL and extraction timestamp on a Summary sheet.
9. Compare the deterministic mock dataset result: Ang Mo Kio count must equal 3. Capture the extraction configuration and Summary sheet.


#### Expected Result

The deterministic dataset produces six total rows and three Ang Mo Kio rows; the output records the source URL, timestamp and both counts.


#### Troubleshooting

If the live table structure changes, use the supplied mock workbook and repair selectors in a separate copy. If the count is zero, trim and normalise PlanningArea before comparing.


#### Evidence and Acceptance Criteria

output/schools-analysis.xlsx plus screenshots of Extract Table Data and the validated Summary sheet.

> **Note:** Before leaving this lab, reconcile input and output record counts, retain the requested evidence, and ensure no credentials or personal data are visible.


### Topic 04: Debug and Exception Handling

Breakpoints · stepping · panels · logs · Try Catch · retry · evidence · recovery.

| Concept | Practical meaning |
| --- | --- |
| Debugging explains behaviour | Breakpoints and stepping reveal values, branches and activity order. |
| Logs explain operation | Structured messages show what ran, with which transaction and result. |
| Exceptions need classification | Business exceptions differ from system failures and lead to different responses. |
| Try Catch contains failure | Catch the specific exception, record evidence and choose retry, skip or stop. |
| Finally restores state | Cleanup actions run whether the Try succeeds or fails. |
| Evidence supports improvement | Screenshots, logs and transaction summaries turn defects into actionable feedback. |


#### Why this topic matters

Production workflows fail safely: they expose context, separate business and system exceptions, and recover only when recovery is safe.


### Lab 7: Debug a Failing Order Workflow

Use breakpoints, stepping, Locals and Watch to find three deliberate defects in an order-classification workflow, then run regression cases.

| Lab field | Detail |
| --- | --- |
| Objective | LO4 — Test, debug and gather evidence about workflow performance |
| Alignment | A5, A7, A8 · K8 |
| Suggested time | 65 minutes |
| Tools | UiPath Studio Community, breakpoints, Step Into/Over, Locals, Watch, logs |
| Deliverable | A repaired workflow, defect log and regression evidence for six orders |


#### Files

- labs/lab-07-debug-a-failing-order-workflow/project.json
- labs/lab-07-debug-a-failing-order-workflow/Main.xaml
- labs/lab-07-debug-a-failing-order-workflow/mock-debug-a-failing-order-workflow.csv
- labs/lab-07-debug-a-failing-order-workflow/mock-debug-a-failing-order-workflow.xlsx
- labs/lab-07-debug-a-failing-order-workflow/CHECKLIST.md


#### Detailed Procedure

1. Open the Defect Log sheet before running the workflow. The starter project contains three deliberate problems; do not rewrite it immediately.
2. Run Main.xaml normally and record the first visible mismatch or exception with OrderID and observed result.
3. Add a breakpoint before the Total calculation. Use Debug File and inspect Quantity, UnitPrice and Total in Locals.
4. Add Total and orderBand to Watch. Step Over the Assign and compare actual values with ExpectedTotal.
5. Repair only the calculation defect, rerun the affected case and record the evidence before moving to the next defect.
6. Use a breakpoint at the band decision. Confirm the boundary for Priority is Total >= 1000, including O5005 exactly at 1000.
7. Add validation for UnitPrice <= 0 so O5006 becomes Review instead of a normal order.
8. Run all six regression cases and complete ActualBand, ActualTotal and Pass/Fail columns.
9. Export or save the defect log and capture Locals/Watch evidence for one repaired case.


#### Expected Result

All six cases pass, O5005 is Priority at the boundary, O5006 is Review, and the defect log records symptom, root cause, change and retest evidence.


#### Troubleshooting

If the workflow still uses old values, stop Debug rather than rerunning from a paused state. If a Watch expression errors, check variable scope at the paused activity.


#### Evidence and Acceptance Criteria

Completed defect log and screenshot of a breakpoint with Locals/Watch values.

> **Note:** Before leaving this lab, reconcile input and output record counts, retain the requested evidence, and ensure no credentials or personal data are visible.


### Lab 8: Build Resilient File Processing with Try Catch

Process a file manifest, classify missing or invalid files, retry transient access failures and produce a clean exception summary without exposing sensitive data.

| Lab field | Detail |
| --- | --- |
| Objective | LO4 — Handle business and system exceptions with controlled recovery |
| Alignment | A5, A7, A8 · K8, K13 |
| Suggested time | 70 minutes |
| Tools | UiPath Studio Community, Try Catch, Retry Scope, Log Message, file activities |
| Deliverable | A Try Catch workflow with bounded retry, Finally cleanup and a structured exception report |


#### Files

- labs/lab-08-build-resilient-file-processing-with-try-catch/project.json
- labs/lab-08-build-resilient-file-processing-with-try-catch/Main.xaml
- labs/lab-08-build-resilient-file-processing-with-try-catch/mock-build-resilient-file-processing-with-try-catch.csv
- labs/lab-08-build-resilient-file-processing-with-try-catch/mock-build-resilient-file-processing-with-try-catch.xlsx
- labs/lab-08-build-resilient-file-processing-with-try-catch/CHECKLIST.md


#### Detailed Procedure

1. Open the manifest and define which outcomes are business exceptions versus system exceptions.
2. Open Main.xaml. Inside the For Each Row, place normal file processing in a Try block.
3. If Exists is No or ContentValid is No, throw or create a BusinessRuleException with TransactionID and a safe reason.
4. For Locked = Yes, use Retry Scope or a bounded loop with at most three attempts and a short delay. Log each attempt.
5. Catch BusinessRuleException separately from System.Exception. Route business exceptions to Review; route unresolved system failures to Technical Support.
6. In Finally, release any file/application resource and append a transaction result regardless of outcome.
7. Write TransactionID, Outcome, Attempts and SafeMessage to output/exception-summary.csv. Do not write passwords, tokens or full confidential content.
8. Run all six manifest rows and compare outcome with ExpectedOutcome. Explain why TX6006 must not be reported as successful.
9. Capture the Try Catch design and the final exception summary.


#### Expected Result

All six rows produce one final result, retries never exceed three, business and system exceptions are distinct, and no sensitive value appears in logs.


#### Troubleshooting

If the workflow continues after a critical system failure, check ContinueOnError and the Catch recovery path. If results duplicate, append only once in Finally.


#### Evidence and Acceptance Criteria

output/exception-summary.csv and screenshots of Try Catch plus one retry log sequence.

> **Note:** Before leaving this lab, reconcile input and output record counts, retain the requested evidence, and ensure no credentials or personal data are visible.


### Topic 05: Manage RPA

Packages · processes · machines · runtimes · jobs · triggers · Assistant · monitoring · optimisation.

| Concept | Practical meaning |
| --- | --- |
| Studio creates packages | Publishing turns a tested project into a versioned automation package. |
| Orchestrator creates processes | A process associates a package version with a folder and runtime context. |
| Machines provide execution capacity | Machine templates and runtimes connect infrastructure to folders. |
| Jobs are executions | Start now, schedule with triggers, or launch an attended process through Assistant. |
| Monitoring reveals health | Statuses, logs, queues and alerts expose throughput, exceptions and bottlenecks. |
| Optimisation is evidence-led | Measure cycle time, success rate and exception causes before changing the robot. |


#### Why this topic matters

A successful Studio project becomes a controlled service only after packaging, deployment, runtime assignment, monitoring and evidence-led optimisation.


### Lab 9: Publish and Run a Process with Orchestrator

Publish a validated project, create or update an Orchestrator process, start a job or Assistant run, and capture version and execution evidence.

| Lab field | Detail |
| --- | --- |
| Objective | LO5 — Package, deploy, monitor and optimise a UiPath process |
| Alignment | A7, A8, A9 · K9, K12 |
| Suggested time | 80 minutes |
| Tools | UiPath Studio Community, Automation Cloud Orchestrator, UiPath Assistant |
| Deliverable | A published package, deployed process, successful job and release evidence record |


#### Files

- labs/lab-09-publish-and-run-a-process-with-orchestrator/project.json
- labs/lab-09-publish-and-run-a-process-with-orchestrator/Main.xaml
- labs/lab-09-publish-and-run-a-process-with-orchestrator/mock-publish-and-run-a-process-with-orchestrator.csv
- labs/lab-09-publish-and-run-a-process-with-orchestrator/mock-publish-and-run-a-process-with-orchestrator.xlsx
- labs/lab-09-publish-and-run-a-process-with-orchestrator/CHECKLIST.md


#### Detailed Procedure

1. Open the project and run Analyze File/Project. Resolve blocking validation errors before publishing.
2. Update Project Settings with a meaningful description and increment the package version. Do not reuse an existing version for changed content.
3. Publish to the connected Orchestrator tenant or the instructor-approved custom feed. Record feed, version and time in the release workbook.
4. In Orchestrator, enter the correct modern folder. Confirm the folder has machine/runtime capacity and the learner account has appropriate permissions.
5. Create a Process from the published package or update the existing process to the new version. Verify the selected entry point.
6. Start a Job with safe input arguments, or launch the attended process in UiPath Assistant if the lab environment is configured for attended execution.
7. Monitor the job until it reaches Successful. Open Logs and confirm the release version and transaction summary.
8. Record job ID, start/end time, status and package version. If the run faults, capture the exception and correct the project before republishing a new version.
9. Capture the process version and successful job details as evidence. Do not include credentials or machine keys.


#### Expected Result

The package version is traceable to a deployed process and a successful execution, with no credential or machine-key exposure in evidence.


#### Troubleshooting

If the package is not visible, verify tenant, folder and feed. If a job stays Pending, check machine/runtime allocation and folder assignment rather than repeatedly starting more jobs.


#### Evidence and Acceptance Criteria

Completed release record plus screenshots of the process version and successful job details.

> **Note:** Before leaving this lab, reconcile input and output record counts, retain the requested evidence, and ensure no credentials or personal data are visible.


### Lab 10: Design and Monitor a Multi-Robot Queue

Model a dispatcher-worker pattern, calculate queue metrics and decide when to scale, retry or route work for human review.

| Lab field | Detail |
| --- | --- |
| Objective | LO5 — Optimise robot performance using queues, monitoring and feedback |
| Alignment | A1, A2, A3, A4, A5, A7, A8, A9 · K3, K9, K13 |
| Suggested time | 80 minutes |
| Tools | UiPath Studio Community, Orchestrator queues, dispatcher/worker pattern, monitoring |
| Deliverable | A dispatcher-worker UiPath design, queue simulation workbook and evidence-led optimisation recommendation |


#### Files

- labs/lab-10-design-and-monitor-a-multi-robot-queue/project.json
- labs/lab-10-design-and-monitor-a-multi-robot-queue/Main.xaml
- labs/lab-10-design-and-monitor-a-multi-robot-queue/mock-design-and-monitor-a-multi-robot-queue.csv
- labs/lab-10-design-and-monitor-a-multi-robot-queue/mock-design-and-monitor-a-multi-robot-queue.xlsx
- labs/lab-10-design-and-monitor-a-multi-robot-queue/CHECKLIST.md
- labs/lab-10-design-and-monitor-a-multi-robot-queue/ProcessItem.xaml


#### Detailed Procedure

1. Open the queue simulation workbook and identify throughput, success rate, average handling time and retry count.
2. Open Main.xaml and ProcessItem.xaml. Main represents the dispatcher/worker coordinator; ProcessItem has one transaction responsibility.
3. Define queue item data: TransactionID, Priority and input fields. Keep credentials out of item-specific content.
4. In the dispatcher path, read input rows and add one transaction per row with a reference based on TransactionID.
5. In the worker path, get one transaction, invoke ProcessItem.xaml and set Successful, Failed or Business Exception explicitly.
6. Retry only system exceptions and cap attempts. Business exceptions go to human review without blind retry.
7. Calculate metrics from the mock data. Confirm six successful attempts out of eight records, with one business and two distinct system-failure transactions represented.
8. Recommend scale-out only when queue age or throughput evidence supports it. Separate capacity problems from data-quality failures.
9. Capture the dispatcher-worker diagram, metric summary and one optimisation recommendation.


#### Expected Result

Every transaction has a unique reference and final state, retries are bounded, business exceptions are not retried, and the optimisation recommendation cites measured queue evidence.


#### Troubleshooting

If workers duplicate items, verify unique references and transaction-state updates. If queue age grows while success rate falls, fix the dominant exception before adding capacity.


#### Evidence and Acceptance Criteria

Queue metrics workbook, workflow screenshots and a written scale/retry/review recommendation.

> **Note:** Before leaving this lab, reconcile input and output record counts, retain the requested evidence, and ensure no credentials or personal data are visible.


## Assessment Preparation


### Written Assessment

Written Assessment (WA / SAQ) — 13 open-ended questions, 60 minutes, open book.

- K1: Autonomy, agency, and attended versus unattended operation
- K2: Automating repetitive tasks and intelligent process automation
- K3: Single-agent and multiple-agent robot patterns
- K4: Sequences, flowcharts, and state-machine workflows
- K5: User-interface automation and recording
- K6: System activities, user events, and loop selection
- K7: Recording and extracting structured data from websites
- K8: Testing, debugging, logging, and exception handling
- K9: Multi-robot management and Orchestrator
- K10: Industry best practices for software robots
- K11: Application and data integration
- K12: Packaging, embedding, deploying, and running robots
- K13: Validation, verification, and resilient exception handling


### Practical Performance

Practical Performance (PP) — 5 connected UiPath tasks, 90 minutes, open book.

| Task | Ability mapping | Related labs |
| --- | --- | --- |
| 1 | A1, A4 | Labs 1–2 |
| 2 | A2, A5 | Labs 3–4 |
| 3 | A3, A6 | Labs 5–6 |
| 4 | A7 | Labs 7–8 |
| 5 | A8, A9 | Labs 9–10 |


### Final Readiness Check

- Explain attended and unattended RPA and select an appropriate candidate.
- Build and explain sequence, flowchart, argument, decision and loop patterns.
- Automate structured data and verify output completeness.
- Use debugging, logging and Try Catch without hiding failures.
- Explain the package-process-job lifecycle and interpret operational measures.


## Glossary

| Term | Meaning |
| --- | --- |
| RPA | Software automation that performs rule-based actions across digital applications. |
| Attended automation | A user starts or collaborates with the robot in an interactive session. |
| Unattended automation | A centrally managed robot runs from a trigger or schedule without a user at the screen. |
| Selector | A structured description used to identify an application or UI element. |
| DataTable | An in-memory table with named columns and rows used by UiPath data activities. |
| Argument | A typed input, output or in/out contract between workflows. |
| Business exception | A rule or data condition that prevents normal processing. |
| System exception | A technical failure such as a timeout, file lock or unavailable application. |
| Package | A versioned published output from a UiPath Studio project. |
| Process | An Orchestrator deployment that selects a package version and execution context. |
| Job | One execution of a process. |
| Queue | A centrally managed collection of transaction items for scalable processing. |
