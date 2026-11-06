# Project Status

[Back to README](../README.md)

Last reviewed: 6 November 2026.

## Summary

| Item | Status |
|---|---|
| Current version | `[TO CONFIRM: version number]` |
| Development status | `[TO CONFIRM: for example, capstone prototype, pilot or in use]` |
| Deployment | `[TO CONFIRM: where it runs, in general terms, and since when]` |
| Last updated | `[TO CONFIRM: update whenever this page changes]` |

## Completed modules

These are implemented in the private codebase. Implemented does not mean formally evaluated.

| Module | Implemented | Field-tested or evaluated |
|---|---|---|
| Kiosk attendance and face recognition | Yes | `[TO CONFIRM]` |
| Liveness check | Yes | `[TO CONFIRM]` |
| Employee management and face enrollment | Yes | `[TO CONFIRM]` |
| Schedules and school calendar | Yes | `[TO CONFIRM]` |
| Leave and Official Business | Yes | `[TO CONFIRM]` |
| Reports, statistics and PDF exports | Yes | `[TO CONFIRM]` |
| Accounts, roles and activity log | Yes | `[TO CONFIRM]` |
| Local storage with cloud mirror | Yes | `[TO CONFIRM]` |
| Backup and recovery tools | Yes | `[TO CONFIRM]` |

## Modules under development

- `[TO CONFIRM: list current work]`

## Planned improvements

`[TO CONFIRM: replace these with the team's actual plan]`

**Suggested** items:

- Formal evaluation of recognition accuracy
- Wider liveness testing, including printed photos and replayed video
- A documented data retention schedule
- Further Leave and Official Business workflow improvements

## Known limitations

- **No published accuracy figures.** Recognition has not been formally evaluated, so this documentation gives no accuracy numbers.
- **Limited liveness testing.** Testing so far has involved few people and few types of attack. Printed photos and replayed video have not been evaluated.
- **Sensitive to conditions.** Lighting and camera position affect recognition.
- **One camera per application instance.** The supported deployment is a single kiosk.
- **One person at a time.** The kiosk does not scan several people at once.
- **Automatic retention is limited.** Attendance and face data are kept until someone removes them.
- `[TO CONFIRM: add any others you know about]`

## Evaluation results

No results have been published yet. Once an evaluation has been done, record its method, sample size, conditions and limitations here.

`[TO CONFIRM: evaluation results, only if they were actually measured]`
