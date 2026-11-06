# Installation Overview

[Back to README](../README.md)

> This page is a high-level overview. It cannot be used to install FaceTap by itself, because the source code is private. Full installation instructions are maintained internally.

## Stages

```mermaid
flowchart LR
    A[Prepare hardware] --> B[Install the operating system]
    B --> C[Install the application]
    C --> D[Add model files]
    D --> E[Configure privately]
    E --> F[Create an administrator]
    F --> G[Start and verify]
    G --> H[Enroll employees]
```

## 1. Prepare the hardware

Assemble the Raspberry Pi, camera, display and power supply. See [Hardware Requirements](hardware-requirements.md).

## 2. Install the operating system

Install and update the operating system, then enable the camera if your setup needs it.

## 3. Install the application

Authorized people obtain the application from the private repository, and install it and its dependencies in an isolated Python environment.

## 4. Add the model files

The face-recognition models are not part of the application's source code, and are installed separately. Each is checked for integrity before use.

## 5. Configure privately

Each deployment has its own private configuration, kept out of version control and readable only by the account running the application. This covers items such as:

- Application secret key
- Database connection, if a cloud mirror is used
- Email settings, if email is used

No values belong in this repository.

## 6. Create an administrator

The first administrator account is created during setup. The system has no default accounts.

## 7. Start and verify

Run the application under a production server, with HTTPS in front of it when it is reached over a network. Check that the camera, the models and the database all work, and that it is not reachable from anywhere it should not be.

## 8. Enroll employees and go live

Add employees and schedules, enroll faces, and run trial scans in the real location and lighting before relying on it.

## After installation

**Suggested** ongoing practice:

- Schedule backups, and test restoring one.
- Keep the system and its dependencies updated.
- Review the activity log from time to time.
- Agree on who may correct records, and how a person can dispute one.
