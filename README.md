# Update Job Tracker

A manually launched macOS job-application tracker, opened through Apple Shortcuts. This repository contains a high-level overview only.

## How it works

1. Choose how many days of application correspondence to check.
2. Read relevant application messages from configured Apple Mail accounts.
3. Interpret selected application evidence using a signed-in Codex account.
4. Match existing applications to avoid duplicate rows and fill verified blank fields.
5. Optionally check published LinkedIn job-poster contact information when neither recruiter email nor phone is available in application correspondence.
6. Create a dated backup and safely save verified updates to an Excel tracker.

## Components

- Apple Shortcuts launches the updater manually.
- Swift provides the Mac interface and days-to-check prompt.
- Apple Mail automation selects application correspondence.
- Python processes evidence, validates contacts and updates the workbook safely.
- A spreadsheet-authoring stage prepares changes, followed by preservation checks.

## Data handling

Workbook editing and backups happen locally. Selected application-email text is sent to OpenAI through Codex for interpretation. Optional contact lookup uses online searches for published professional contact information. This is not an entirely offline tool.

The implementation filters tracking links and recognised sensitive fields before analysis. This filtering does not guarantee removal of every possible sensitive item. Local evidence and caches must be treated as private.

Existing values are preserved; missing or unverified contact details remain blank. The updater does not send messages, submit applications or run on a schedule.

## Validation approach

Workbook-copy and synthetic-evidence tests check duplicate handling, blank-field updates, contact matching, backups and preservation of unrelated workbook content.

## Repository scope

Only this general description is included. No implementation files, email messages, workbooks, contact records, account addresses, credentials, tokens, caches, run logs, binaries or machine-specific paths are published here.
