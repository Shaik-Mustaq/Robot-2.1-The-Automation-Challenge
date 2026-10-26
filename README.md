# Robot 2.1 — The Automation Challenge

An RPA project built with **UiPath Studio** to complete [The Automation Challenge](https://www.theautomationchallenge.com/).

The goal is to read records from a spreadsheet, enter the data into dynamic web form fields, and submit each record efficiently. The form fields can change position and size after each submission, so the automation must identify the correct fields reliably rather than depend on fixed screen coordinates.

## Table of Contents

- [Overview](#overview)
- [Objectives](#objectives)
- [Technology Stack](#technology-stack)
- [Project Files](#project-files)
- [Prerequisites](#prerequisites)
- [Getting Started](#getting-started)
- [Run the Automation](#run-the-automation)
- [Expected Workflow](#expected-workflow)
- [Troubleshooting](#troubleshooting)
- [Future Improvements](#future-improvements)
- [Author](#author)

## Overview

This project automates a repetitive data-entry challenge using UiPath. It reads the challenge data from an Excel workbook and enters each record into the corresponding fields on the website.

A key challenge is that the form layout changes after each submission. The workflow therefore needs to identify fields reliably and process records without relying on their fixed positions.

## Objectives

- Read input records from an Excel spreadsheet.
- Identify dynamic form fields reliably.
- Enter each record into its corresponding fields.
- Submit records through the challenge workflow.
- Improve execution speed while maintaining accuracy.
- Reduce repetitive manual data entry.

## Technology Stack

- **RPA platform:** UiPath Studio
- **Input data:** Microsoft Excel workbook (`challenge.xlsx`)
- **Target application:** The Automation Challenge website
- **Workflow:** UiPath XAML (`Main.xaml`)

## Project Files

| File | Purpose |
|---|---|
| `Main.xaml` | Main UiPath automation workflow |
| `challenge.xlsx` | Spreadsheet containing challenge input data |
| `project.json` | UiPath project configuration |
| `project.uiproj` | UiPath Studio project file |
| `AGENTS.md` / `CLAUDE.md` | Project-specific guidance files |

Other configuration and support files are included in the repository.

## Prerequisites

Before running the project, make sure you have:

- A Windows computer.
- UiPath Studio installed.
- Access to [The Automation Challenge](https://www.theautomationchallenge.com/).
- Create a account by sign-up.
- The repository files downloaded to your computer.
- The required UiPath activity packages restored in Studio.

## Getting Started

### 1. Clone the repository

Open Command Prompt or a terminal and run:

```bash
git clone https://github.com/Shaik-Mustaq/Robot-2.1-The-Automation-Challenge.git
cd Robot-2.1-The-Automation-Challenge
```

### 2. Open the project in UiPath Studio

1. Launch UiPath Studio.
2. Open the cloned project folder.
3. Open `project.json` or the project file in Studio.
4. Allow Studio to restore the project's dependencies.
5. Confirm that `Main.xaml` and `challenge.xlsx` are available.

### 3. Verify the input workbook

Check that `challenge.xlsx` is present and contains the expected challenge data. If the workflow uses a configured file path, update it to match the location on your computer.

## Run the Automation

1. Open `Main.xaml` in UiPath Studio.
2. Confirm the target browser and input workbook settings.
3. Open [The Automation Challenge](https://www.theautomationchallenge.com/) if the workflow requires the website to be available in advance.
4. Make sure you already signed in.
5. Run the workflow from Studio.
6. Review the execution output and the result displayed by the challenge website.

> **Tip:** Test the workflow with a small or non-critical run first, if the challenge environment permits it. Confirm that each value is entered into the correct field before focusing on speed improvements.

## Expected Workflow

1. Load the challenge data from the Excel workbook.
2. Open or attach to the challenge website.
3. Locate the appropriate form fields despite layout changes.
4. Enter the current record's values.
5. Submit the record.
6. Continue until all records have been processed.
7. Review the final challenge result and any execution errors.

## Troubleshooting

- **Workbook not found:** Verify that `challenge.xlsx` exists and update any file path configured in the workflow.
- **Dependencies fail to restore:** Check the project dependencies in UiPath Studio and restore or update packages as appropriate.
- **Fields are not populated correctly:** Recheck selectors or field-identification logic; avoid relying on fixed coordinates when the layout changes.
- **Website interaction fails:** Confirm that the website is reachable and that the browser/session matches the workflow's configuration.
- **Automation is slow:** Review unnecessary waits and repeated lookups, then optimize only after confirming that the workflow remains accurate.

## Future Improvements

- Add structured logging for processed records and failures.
- Improve exception handling and recovery for transient UI issues.
- Measure completion time and accuracy across repeated runs.
- Document the exact selectors, activities, and package versions used by the final workflow.
- Capture a screenshot or short demo of a successful run.

## Author

**Shaik Mustaq**

- GitHub: [Shaik-Mustaq](https://github.com/Shaik-Mustaq)
- Repository: [Robot 2.1 — The Automation Challenge](https://github.com/Shaik-Mustaq/Robot-2.1-The-Automation-Challenge)

---

If you find this project useful, feel free to explore the repository and share feedback.
