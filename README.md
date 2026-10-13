# Time-Entry and Billing Validation (Practice Project)

> **Self-directed practice project. Employees, clients, rates, hours and billing data are fictional.** This is not professional payroll or billing experience and uses no employer data.

An Excel workbook that validates a high-volume set of time records and reconciles them to a billing export.

## Scenario
30 fictional employees record time to 4 fictional client projects and one internal code over two working weeks (2026-09-14 to 2026-09-25). 328 time rows and 315 billing lines are checked.

## What is inside
| Sheet | Contents |
| --- | --- |
| `Time_Entries` | Data plus check columns: duplicate, hours range, weekend, project code, rate vs contract, billing check |
| `Billing_Data` | Billing export with reconciliation to time, rate and amount |
| `Coverage` | 30 x 10 grid showing MISSING, LEAVE or hours for every employee-day |
| `Discrepancy_Log` | 33 logged exceptions with expected vs found, possible $ impact, proposed action and owner |
| `Summary_Checks` | One-page summary of the 10 checks, with a reconciliation of checks to log |
| `Lists` | Employees, projects, rate card, approved leave |

## Excel features used
Data validation (drop-downs, hour limits, weekday date rule), filters, freeze panes, SUMIFS, COUNTIFS, INDEX/MATCH lookups, SUMPRODUCT, conditional formatting.

## Results
The data was seeded with known problems. Every check matches its expected count and the discrepancy log agrees: 7 missing days, 5 duplicates, 4 wrong rates, 2 out-of-range hours, 1 weekend entry, 1 invalid project code, 5 billed-hours mismatches, 3 billed-rate mismatches, 3 billed lines with no time entry, 2 billable entries not billed. Duplicate rows would have added 36 hours.

## Limits
One rate per role per project, no overtime or premium rates, no approval workflow. Data validation blocks bad typing but not pasted data, which is why the check columns exist.
