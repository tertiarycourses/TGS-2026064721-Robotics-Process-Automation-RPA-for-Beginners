<div align="center">

# Robotics Process Automation (RPA) for Beginners

[![WSQ](https://img.shields.io/badge/WSQ-TGS--2026064721-1f6feb)](https://www.tertiarycourses.com.sg/casl-robotics-process-automation-rpa-for-beginners.html)
[![UiPath](https://img.shields.io/badge/UiPath-Studio%202024.10-orange)](https://www.uipath.com/)
[![Labs](https://img.shields.io/badge/Labs-10-10b981)](#hands-on-labs)

**UiPath starter projects and mock data for a two-day, beginner-level RPA course.**

</div>

| Course detail | Information |
|---|---|
| Course code | `TGS-2026064721` |
| Programme | WSQ (CASL) |
| TSC | Self-Learning Systems (`ICT-DIT-4028-1.1`) |
| Duration | 2 days / 16 hours (including a 2-hour assessment) |
| Level | Beginner |
| Current courseware | v15.0 |
| Registration | [View course details and register](https://www.tertiarycourses.com.sg/casl-robotics-process-automation-rpa-for-beginners.html) |
| Funding | Up to 70% course-fee funding for eligible learners (SME employees or the Mid-Career Enhanced Subsidy; up to 50% baseline). The course page lists funding validity from 20 Jul 2026 to 19 Jul 2028. Eligibility, attendance and assessment terms apply. |

## About the course

This learner repository supports **TGS-2026064721**. It progresses from RPA opportunity selection and workflow design through UI/data automation, debugging, exception handling, deployment, monitoring and optimisation.

Every lab is self-contained with:

- an editable UiPath `project.json` and `Main.xaml`;
- realistic mock data in both CSV and formatted Excel formats;
- a detailed `README.md` with expected results and troubleshooting;
- a completion/evidence checklist and PDF mirrors.

## Learning outcomes

- **LO1:** Determine appropriate RPA opportunities and best practices for attended and unattended automation.
- **LO2:** Plan and construct UiPath workflows using sequences, flowcharts, state machines, variables, arguments and control flow.
- **LO3:** Design and validate UI, web, data and Excel automation processes with reliable selectors and structured outputs.
- **LO4:** Test, debug, log and handle exceptions in RPA workflows.
- **LO5:** Package, deploy, monitor and optimise UiPath processes using Assistant and Orchestrator.

## Topics covered (learning journey)

```text
Opportunity → Workflow design → UI and data automation → Resilience → Managed deployment
     │               │                    │                   │              │
  Labs 1–2       Labs 3–4             Labs 5–6           Labs 7–8       Labs 9–10
```

## Hands-On Labs

| Lab | Outcome |
|---:|---|
| 1 | [Assess RPA opportunities and run a first Sequence](labs/lab-01-assess-an-rpa-opportunity-and-build-a-first-sequence/README.md) |
| 2 | [Model attended, unattended and human-review routes](labs/lab-02-model-attended-and-unattended-service-automation/README.md) |
| 3 | [Route customer requests with `If` and `Switch`](labs/lab-03-route-customer-requests-with-if-and-switch/README.md) |
| 4 | [Process a customer `DataTable` with loops](labs/lab-04-process-a-customer-datatable-with-loops/README.md) |
| 5 | [Validate and reconcile invoice data in Excel](labs/lab-05-validate-and-reconcile-invoices-in-excel/README.md) |
| 6 | [Extract and filter a Singapore schools table](labs/lab-06-extract-and-filter-a-singapore-schools-table/README.md) |
| 7 | [Debug a failing order workflow](labs/lab-07-debug-a-failing-order-workflow/README.md) |
| 8 | [Build resilient file processing with `Try Catch`](labs/lab-08-build-resilient-file-processing-with-try-catch/README.md) |
| 9 | [Publish and run a process with Orchestrator](labs/lab-09-publish-and-run-a-process-with-orchestrator/README.md) |
| 10 | [Design and monitor a multi-robot queue](labs/lab-10-design-and-monitor-a-multi-robot-queue/README.md) |

Open [labs/README.md](labs/README.md) for direct links to every lab.

## Getting Started

### Prerequisites

- UiPath Studio Community or Studio 2024.10 or later
- Microsoft Excel or a compatible workbook viewer
- A training UiPath Automation Cloud account for the Orchestrator labs

### Use a lab

1. Clone or download this repository.
2. Open one folder under `labs/` and keep all its files together.
3. Open `project.json` in UiPath Studio and allow dependency restoration.
4. Read the lab `README.md`, inspect the CSV/XLSX mock data, then complete the workflow.
5. Verify the expected result and retain the evidence listed in `CHECKLIST.md`.

> Use only the supplied mock data. Never place passwords, access tokens or real personal data in source files, XAML or screenshots.

## Courseware package

| Item | Files |
|---|---|
| Trainer slide deck (v15.0) | [PPTX](<courseware/Robotics Process Automation (RPA) for Beginners-v15.0.pptx>) · [PDF](<courseware/Robotics Process Automation (RPA) for Beginners-v15.0.pdf>) |
| Learner Guide | [DOCX](<courseware/LG-Robotics Process Automation (RPA) for Beginners.docx>) · [PDF](<courseware/LG-Robotics Process Automation (RPA) for Beginners.pdf>) · [Markdown](<LG-Robotics Process Automation (RPA) for Beginners.md>) |
| Lesson Plan | [DOCX](<courseware/LP-Robotics Process Automation (RPA) for Beginners.docx>) · [PDF](<courseware/LP-Robotics Process Automation (RPA) for Beginners.pdf>) |
| Labs | [labs/](labs/README.md) |

The deck includes the "Login to LMS and Download Course Material" slide showing the current [LMS-TMS](https://lms-tms.tertiaryinfotech.com) sign-in page.

## Repository Structure

```text
.
├── README.md
├── LG-Robotics Process Automation (RPA) for Beginners.md
├── courseware/          slide deck (PPTX + PDF), Learner Guide, Lesson Plan
└── labs/
    ├── README.md
    ├── README.pdf
    ├── lab-01-.../
    │   ├── README.md / README.pdf
    │   ├── CHECKLIST.md / CHECKLIST.pdf
    │   ├── project.json
    │   ├── Main.xaml
    │   └── mock-*.csv / mock-*.xlsx
    └── lab-10-.../
        └── ProcessItem.xaml
```

## Public/private distribution boundary

Assessment papers, answer keys, the Facilitator Guide, the Assessment Plan, trainer reference materials, release tooling and credentials are intentionally excluded from this public repository. Answer keys are trainer-only and are never linked from the LMS.

## Support

- Email: enquiry@tertiaryinfotech.com
- Telephone: +65 6100 0613
- Website: [Tertiary Courses](https://www.tertiarycourses.com.sg/)

## Developed By

Tertiary Infotech Academy Pte Ltd · UEN 201200696W
