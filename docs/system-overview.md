# System Overview

[Back to README](../README.md)

## Purpose

FaceTap records staff attendance through face recognition at a camera kiosk, and gives authorized staff a web dashboard to manage and report on those records. It is designed for schools and small organizations.

Its design centers on two ideas:

- **Attendance should still be recorded when the network is down.** The kiosk writes to a database on the device first, and copies records to the cloud afterwards.
- **People should stay in control of the records.** Recognition produces a record, but staff can review and correct it, and those corrections are traceable.

## Intended users

| User | What they do | Account role |
|---|---|---|
| Employee or staff member | Stands at the kiosk to record Time-In and Time-Out | None needed to scan |
| HR staff | Manage employees and schedules, correct attendance, review Leave and Official Business, and run reports | HR |
| Administrator | Everything HR does, plus accounts, settings and backups | Admin |
| Kiosk terminal | Runs the attendance screen and nothing else | Kiosk |

The system manages employees. `[TO CONFIRM: whether the project also intends to serve students. The current system has no student records.]`

## Major components

| Component | Role |
|---|---|
| **Kiosk** | A Raspberry Pi with a camera and display, showing a live preview, guidance and results |
| **Face recognition component** | Finds a face in the image, identifies it against enrolled templates and runs a liveness check |
| **Web application** | Applies attendance rules, enforces access control and serves the kiosk screen and dashboard |
| **Local database** | Stores all records on the device |
| **Cloud mirror** (optional) | A PostgreSQL copy of the records, kept up to date in the background |
| **Administrator dashboard** | Browser-based screens for management, monitoring and reports |

## General workflow

### Enrollment

Authorized staff create an employee record and capture face samples, using the kiosk camera or the camera of the device they are signed in on. The system checks that each sample is good enough, and warns if a face appears to belong to another enrolled employee.

### Recording attendance

1. The employee stands in front of the kiosk. No button is needed when hands-free mode is on.
2. If needed, the screen gives one instruction at a time, such as "Move closer" or "Move into better light".
3. Once the person is in position and holding still, the system verifies them across more than one camera frame. This includes the liveness check.
4. If verification succeeds, the first scan of the day records a Time-In, and a later scan records a Time-Out.
5. The screen shows the result. If the employee has an email address on file, they can also be sent a copy.
6. The kiosk waits for that person to leave before starting another scan.

If a scan is refused, nothing is written to the attendance record.

### Evaluating the day

Each day is evaluated against the employee's schedule, the school calendar and any approved Leave or Official Business. The same evaluation feeds the kiosk result, the dashboards and the reports, so they do not disagree with each other.

### Review and correction

Staff can correct times, and can record attendance by hand for a day the kiosk missed. A reason is required, and hand-entered records are marked as such.

## What FaceTap does not do

- It does not guarantee a correct identification. See [Security and Privacy](security-and-privacy.md).
- It does not replace an institution's own attendance policy or appeal process.
