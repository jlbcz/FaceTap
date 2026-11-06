# Hardware Requirements

[Back to README](../README.md)

This is a practical list for one kiosk. No minimum specification has been formally established. Where a specific model is named below, it describes the equipment used during development, not a requirement.

## Required

| Item | Notes |
|---|---|
| **Raspberry Pi** | Runs the application and face recognition. Development and testing have used a Raspberry Pi 4. `[TO CONFIRM: the recommended model and memory for your deployment]` |
| **Compatible camera** | A Raspberry Pi camera module, or a USB webcam. Development and testing have used a Raspberry Pi Camera Module 3. |
| **Storage** | A microSD card or other storage for the operating system, database and face data. `[TO CONFIRM: recommended capacity]` |
| **Power supply** | Use a supply rated for your Raspberry Pi model. An inadequate supply can cause instability. |

## Required where applicable

| Item | When it is needed |
|---|---|
| **Display** | For a kiosk people stand in front of, so they can see guidance and results. The kiosk interface has a layout for small panels. |
| **Network connection** | For cloud mirroring, email and remote access to the dashboard. Recording attendance itself does not need it. |
| **Admin computer** | Any device with a modern browser, for staff using the dashboard. |

## Optional accessories

- Case and cooling, because face recognition is demanding work for a small computer running all day
- Mount or stand, to hold the camera steady at about face height
- Consistent front lighting, which helps recognition. Dim or strongly backlit positions make it harder.
- Uninterruptible power supply, to reduce the risk of data damage from a sudden power loss
- Thermal sensor (MLX90614 or MLX90640), for the optional temperature reading. `[TO CONFIRM: tested with real hardware]`

## Placement advice

**Suggested**, based on what generally helps camera-based recognition:

- Put the kiosk where light falls on people's faces, not behind them.
- Avoid pointing the camera at a busy walkway or a poster with faces, since other faces in view can get in the way of a scan.
- Allow room for one person at a time to stand in front of it.
