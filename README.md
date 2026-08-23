<div align="center">

# Robotics Process Automation (RPA) for Beginners

[![WSQ](https://img.shields.io/badge/WSQ-TGS--2026064721-1f6feb)](https://www.tertiarycourses.com.sg/casl-robotics-process-automation-rpa-for-beginners.html)
[![UiPath](https://img.shields.io/badge/UiPath-Studio%202024.10-orange)](https://www.uipath.com/)
[![Labs](https://img.shields.io/badge/Labs-10-10b981)](#hands-on-labs)

**UiPath starter projects and mock data for a two-day, beginner-level RPA course.**

[Course page](https://www.tertiarycourses.com.sg/casl-robotics-process-automation-rpa-for-beginners.html) · [Report an issue](https://github.com/tertiarycourses/TGS-2026064721-Robotics-Process-Automation-RPA-for-Beginners/issues)

</div>

## About

This learner repository supports **TGS-2026064721**. It progresses from RPA opportunity selection and workflow design through UI/data automation, debugging, exception handling, deployment, monitoring and optimisation.

Every lab is self-contained with:

- an editable UiPath `project.json` and `Main.xaml`;
- realistic mock data in both CSV and formatted Excel formats;
- a detailed `README.md` with expected results and troubleshooting;
- a completion/evidence checklist and PDF mirrors.

## Learning Journey

```text
Opportunity → Workflow design → UI and data automation → Resilience → Managed deployment
     │               │                    │                   │              │
  Labs 1–2       Labs 3–4             Labs 5–6           Labs 7–8       Labs 9–10
```

## Hands-On Labs

| Lab | Outcome |
|---:|---|
| 1 | Assess RPA opportunities and run a first Sequence |
| 2 | Model attended, unattended and human-review routes |
| 3 | Route customer requests with `If` and `Switch` |
| 4 | Process a customer `DataTable` with loops |
| 5 | Validate and reconcile invoice data in Excel |
| 6 | Extract and filter a Singapore schools table |
| 7 | Debug a failing order workflow |
| 8 | Build resilient file processing with `Try Catch` |
| 9 | Publish and run a process with Orchestrator |
| 10 | Design and monitor a multi-robot queue |

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

## Repository Structure

```text
.
├── README.md
├── LG-Robotics Process Automation (RPA) for Beginners.md
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

Assessment papers, answer keys, trainer materials, release tooling and credentials are intentionally excluded from this public repository.

## Support

- Email: enquiry@tertiaryinfotech.com
- Telephone: +65 6100 0613
- Website: [Tertiary Courses](https://www.tertiarycourses.com.sg/)

## Developed By

Tertiary Infotech Academy Pte Ltd · UEN 201200696W
