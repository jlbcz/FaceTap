# Software Requirements

[Back to README](../README.md)

## Confirmed stack

This was checked against the private codebase on 6 November 2026.

| Category | Software | Purpose |
|---|---|---|
| Language | Python 3.11 or newer | Application and face-recognition pipeline |
| Web framework | Flask | Web application, with Jinja templates |
| Front end | HTML, CSS, JavaScript | Kiosk screen and dashboard |
| Application server | Gunicorn | Running the application in production |
| Local database | SQLite | The primary store on the device |
| Cloud database | PostgreSQL (Neon) | Optional background mirror |
| Database access | SQLAlchemy, psycopg2 | Connections and database drivers |
| Computer vision | OpenCV | Runs the detection, recognition and liveness models |
| Face models | YuNet, SFace, MiniFASNetV2 | Detection, recognition and liveness |
| Camera | Picamera2, OpenCV | Raspberry Pi camera modules, and USB cameras |
| Security | Argon2 (argon2-cffi), Flask-WTF | Password hashing, and protection against cross-site request forgery |
| Documents | ReportLab, lxml, openpyxl, Pillow | PDFs, Word templates, reading spreadsheets, images |

Exact versions are kept in the private repository.

## Runtime environment

| Requirement | Notes |
|---|---|
| Operating system | Raspberry Pi OS for the kiosk. Linux and macOS have been used for development. `[TO CONFIRM: the exact Raspberry Pi OS release you support]` |
| Browser | A current Chromium-based browser on the kiosk. `[TO CONFIRM: the browsers you have tested for the dashboard]` |
| HTTPS | Needed in front of the application when it is reached over a network |

## Optional services

| Service | Purpose | If it is absent |
|---|---|---|
| Neon PostgreSQL | Off-device copy of records | Data stays on the device |
| Email delivery | Attendance copies and notices | No emails are sent |

## Third-party licenses

The libraries and models above are third-party work under their own licenses. `[TO CONFIRM: add a full list of third-party notices if you distribute FaceTap]`
