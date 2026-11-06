# Screenshots

This folder holds screenshots for the public documentation.

## Before adding a screenshot

This repository is public, and removing a file later does not remove it from Git history. Check every image first:

- [ ] It uses test accounts and made-up data only.
- [ ] It shows no real person's face, name, employee ID, email or attendance record, unless that person has agreed in writing.
- [ ] It shows no internal web addresses, IP addresses or device names.
- [ ] It shows no passwords, tokens, keys or connection strings, including in browser tabs or autofill.
- [ ] Nothing sensitive is merely blurred. Cover it fully, or better, retake the screenshot with test data.

If a camera view is needed, use a person who has agreed to appear, or show the screen with the camera area covered.

## Recommended filenames

| Filename | What it should show |
|---|---|
| `login-page.png` | The sign-in page |
| `admin-dashboard.png` | The administrator dashboard |
| `attendance-monitoring.png` | The attendance overview, or the kiosk screen |
| `employee-management.png` | The employee list |
| `attendance-report.png` | A report or its PDF |

FaceTap currently manages employees, so `employee-management.png` is the name to use. `student-management.png` would apply only if student records are added to the system later.

## Format

- Use PNG, with lowercase filenames and hyphens.
- A width of about 1280 pixels is enough for pages. Kiosk screens can stay at their real size.
- Keep each file under about 1 MB where possible.

## Adding them to the main README

The main `README.md` has a commented-out image table in its Screenshots section. Once the files exist, remove the comment markers (`<!--` and `-->`) around it. Remove the rows for any images you have not added, because a missing file shows as a broken image.
