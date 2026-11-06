# Features

[Back to README](../README.md)

These features were confirmed against the private codebase on 6 November 2026. Being implemented does not mean a feature has been formally evaluated. See [Project Status](project-status.md).

## Attendance management

- Time-In and Time-Out recorded at the kiosk
- One attendance record per employee per day
- Weekly schedules for each employee, set on screen or imported from a spreadsheet
- School calendar, including holidays and make-up days
- Daily status worked out from the schedule, with a configurable grace period
- Corrections and manual entries, each with a required reason

## Facial recognition

- Face detection and identification from the kiosk camera
- Hands-free scanning, with an on/off setting
- On-screen guidance based on the detected face, such as distance and lighting
- A liveness check required for attendance and for enrollment
- Verification across more than one camera frame
- One scan per presentation: the kiosk waits for the person to leave before scanning again

Face recognition can make mistakes, and the liveness check is not a guarantee against spoofing. See [Security and Privacy](security-and-privacy.md).

## User management

- Employee records, including activation and deactivation
- Face enrollment by authorized staff, from the kiosk camera or a signed-in device's camera
- Removal of an employee's face data
- Staff accounts with three roles: Admin, HR and Kiosk

## Administration

- Web-based dashboard
- System settings, including features and terminology that can be customized
- Organization branding, such as name, colors and logos
- Backup and recovery tools
- Activity log of sign-ins and administrative actions
- System status and health information

## Reports and records

- Attendance reports filtered by date and employee
- PDF exports
- Attendance summary, which can be exported for payroll use
- Attendance statistics
- Leave and Official Business forms, approvals and printable copies
- Optional email copies of attendance events to employees

## Monitoring

- Attendance overview on the dashboard
- Today's activity on the kiosk screen
- Live camera preview at the kiosk
- Status of the camera and of cloud mirroring

## Optional features

- Temperature reading from an attached thermal sensor. `[TO CONFIRM: whether this has been tested with real hardware]`
- Mirroring to a Neon PostgreSQL database. Without it, data stays on the device.
