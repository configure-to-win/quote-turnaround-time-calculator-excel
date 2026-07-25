[Back to README](../README.md) · [Open the Excel workbook](../template/quote-turnaround-time-measurement-template.xlsx) · [Use the online calculator](https://configure.win/resources/quote-turnaround-time-calculator)

# Milestone measurement guide

Use the **Measurement log** to record quote milestones and calculate elapsed clock time across up to 100 quotes.

## What the sheet measures

Each row represents one quote. The worksheet calculates elapsed hours between selected milestones and total elapsed time from the initial request to release.

## Input fields

| Column | Field | Entry guidance |
| --- | --- | --- |
| A | Quote ID | Enter a unique internal reference suitable for the measurement exercise. |
| B | Quote request received | Enter the timestamp at which the initial quote request was received. |
| C | Inputs complete | Enter the timestamp at which the inputs required to progress the quote were complete. |
| D | Commercial calculation complete | Enter the completion timestamp for the commercial calculation. |
| E | Validation complete | Enter the completion timestamp for validation. |
| F | Approval submitted | Enter the timestamp at which the quote was submitted for approval. |
| G | Approval decided | Enter the timestamp at which the required approval decision was received. |
| H | Customer-ready output complete | Enter the timestamp at which the customer-ready output was complete. |
| I | Quote released | Enter the timestamp at which the quote was released to the customer. |
| J | Number of rework loops | Enter a whole number of zero or greater. |
| K | Rework duration (hours) | Enter the total rework duration as a non-negative number of hours. |
| L | Primary delay reason | Select one value from the validation list. |
| M | Notes | Add context needed to understand the recorded values. |

Enter timestamps in chronological order.

## Primary delay reason

Choose one:

- Missing inputs
- Product, price or cost data
- Validation clarification
- Approval waiting
- Rework
- Release lag
- Other

Use Notes when several delay reasons were material or when the selected label requires explanation.

## Calculated durations

| Output | Formula boundary |
| --- | --- |
| **Preparation elapsed hours** | Inputs complete minus Quote request received |
| **Calculation elapsed hours** | Commercial calculation complete minus Inputs complete |
| **Validation elapsed hours** | Validation complete minus Commercial calculation complete |
| **Approval waiting hours** | Approval decided minus Approval submitted |
| **Release preparation hours** | Customer-ready output complete minus Approval decided |
| **Release lag hours** | Quote released minus Customer-ready output complete |
| **Total turnaround hours** | Quote released minus Quote request received |

Excel stores timestamps as days, so the workbook multiplies each difference by 24 to display hours.

A calculated duration remains blank when either required timestamp is missing. The formulas apply a minimum of zero, so a reverse timestamp does not create a negative duration. A zero result should not be treated as confirmation that the timestamps were entered correctly; review chronological order directly.

## Important reconciliation note

The calculated stage durations do not necessarily add up to total turnaround hours.

The interval between **Validation complete** and **Approval submitted** is not represented by a separate calculated duration. Total turnaround is calculated directly from **Quote request received** to **Quote released**, so it can include time that is not visible in the stage-duration columns.

Do not replace total turnaround with the sum of the visible stage columns.

## Rework treatment

Record:

- the number of rework loops; and
- total rework duration in hours.

These fields provide context. Rework duration is not added to total turnaround time because rework occurs within the elapsed request-to-release cycle.

Adding it to the elapsed total would count that time twice.

## Elapsed time boundary

The sheet measures complete clock time. It may include:

- nights;
- weekends;
- holidays;
- inactive periods.

It does not calculate business hours or remove non-working periods.

## Recommended measurement procedure

1. Select one completed quote.
2. Enter its Quote ID.
3. Enter every available timestamp in chronological order.
4. Record rework information.
5. Select the primary delay reason.
6. Document missing timestamps, unusual events or interpretive context in Notes.
7. Review total turnaround hours.
8. Review the individual elapsed intervals.
9. Repeat for comparable quotes using the same milestone definitions.

## Data-quality checks

Before using a row in analysis, confirm:

- the Quote ID is present;
- timestamps use the same time basis;
- timestamps are chronological;
- the start and release timestamps are present when total turnaround is required;
- rework loops are whole numbers;
- rework duration is expressed in hours;
- one primary delay reason has been selected where known;
- Notes explain missing or unusual values.

## When to use Calculator inputs as well

The Measurement log shows elapsed flow but does not separate each elapsed interval into active work, waiting and rework.

Use [Duration input guide](duration-input-guide.md) when that composition is needed.
