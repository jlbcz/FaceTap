# Security and Privacy

[Back to README](../README.md)

FaceTap handles biometric and personal data. This page explains how that data is protected, and what remains the responsibility of whoever deploys the system.

> This project makes no claim of compliance with any specific law, regulation or standard. No system is completely secure, and this page does not claim otherwise.

## Protection of biometric data

- Face templates and samples are stored on the kiosk device, outside the public web folder.
- They are not sent to the cloud database. They are included in backups so the system can be restored.
- Match scores and details of how the liveness decision was reached are not shown on the kiosk screen.
- Authorized staff can remove an employee's face data, and this is recorded in the activity log.

A face cannot be changed the way a password can, so a leak of biometric data is more serious than most leaks. Treat the device and its backups accordingly.

## Access control

- There are three account roles: Admin, HR and Kiosk.
- Each route checks permissions on the server. Hiding a menu item is not relied on as a control.
- The Kiosk role can reach the attendance terminal and nothing else.
- Requests that change data need a token that protects against cross-site request forgery.
- Repeated failed sign-ins are limited.
- The activity log records sign-ins and administrative actions.

## Password security

- Passwords are stored as Argon2id hashes, never as plain text.
- The system has no default accounts.
- `[TO CONFIRM: your institution's own password and account review rules]`

## Database protection

- The local database and private files are kept outside the public web folder.
- Secrets come from private configuration, not from source code.
- Backups on the device are kept in owner-only folders and are not themselves encrypted. If a public key is configured, an encrypted copy is also produced for off-device storage. Unencrypted copies should not leave the device.
- The cloud mirror holds personal records, including password hashes by default. Its credentials should be treated as highly sensitive.

## Secure transmission

- HTTPS is expected in front of the application whenever it is reached over a network.
- The connection to the cloud database is encrypted.
- Deployers should confirm this for their own network before going live.

## Privacy considerations

**Suggested** practice for any institution using FaceTap:

- Tell people what is collected, why, who can see it and how long it is kept.
- Obtain consent or another valid basis, as local rules and institutional policy require.
- Offer an alternative for people who cannot or do not wish to use face recognition.
- Limit dashboard accounts to the people who need them.
- Use test data in demonstrations and screenshots.

## Responsible use of facial recognition

- **It can be wrong.** It can fail to recognize someone, or match the wrong person. Lighting, camera position, masks, glasses and changes in appearance can all affect it.
- **Accuracy may vary between people.** Face recognition systems in general have been shown to perform differently across demographic groups. FaceTap has not been evaluated for this.
- **It can be deceived.** The liveness check is intended to reject photos and screens, but it is not foolproof, and testing so far has been limited.
- **People should be able to challenge a result.** A wrong record should be correctable by a person, without penalty for the error.
- **Keep it to its purpose.** FaceTap is for attendance at a kiosk that people deliberately stand in front of. Using it for general surveillance is outside its intended purpose.

## Retention of attendance and biometric information

| Data | Current behavior | Policy |
|---|---|---|
| Activity log | Rotated daily, with 90 days kept | `[TO CONFIRM: is this period suitable?]` |
| Attendance records | No automatic deletion was found | `[TO CONFIRM: retention period]` |
| Face data | Kept until removed by staff | `[TO CONFIRM: when it must be removed, such as when employment ends]` |
| Backups | Kept until removed | `[TO CONFIRM: retention period and storage location]` |

**Suggested:** remove face data once someone no longer needs to use the kiosk, and remember that backups may still contain it until they expire.

## Institutional policy compliance

Each institution is responsible for checking its use of FaceTap against the data privacy laws and internal policies that apply to it, and should seek its own legal advice.

`[TO CONFIRM: the institution's data privacy office or officer, and any approval obtained]`

## Reporting a security issue

`[TO CONFIRM: a private contact for reporting security issues]`

Please do not publish details of a suspected vulnerability in a public issue.
