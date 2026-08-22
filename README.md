# Quote Turnaround Time Calculator — Excel Measurement Template

Measure how long complex B2B quotes take from initial request to customer-ready release, and separate active processing time from waiting, rework and post-approval release lag.

This workbook accompanies the [Quote Turnaround Time Calculator by Configure to WIN](https://configure.win/resources/quote-turnaround-time-calculator), where you can enter the same fifteen time inputs online and analyse the composition of a quote cycle in your browser.

## Get the tool

- [Download the latest Excel release](../../releases/latest)
- [Open the Excel workbook](template/quote-turnaround-time-measurement-template.xlsx)
- [Use the online calculator](https://configure.win/resources/quote-turnaround-time-calculator)
- [Read the measurement methodology](docs/methodology.md)

## What this workbook measures

The template helps you distinguish the work required to progress a quote from the delays and repeated effort that extend its total cycle time.

It measures:

- **Total turnaround time** — the complete elapsed time from the initial quote request to customer-ready release.
- **Active processing time** — hands-on work required to prepare, calculate, validate, approve and release the quote.
- **Waiting time** — elapsed delay while the quote cannot progress because information, clarification or an approval decision is still required.
- **Rework time** — repeated work caused by missing inputs, corrections, validation issues or approver feedback.
- **Release lag** — elapsed time between approval and the actual release of the customer-ready quote.
- **Largest bottleneck** — the single calculator input with the highest recorded duration.
- **Stage elapsed time** — milestone-based durations for preparation, commercial calculation, validation, approval waiting, release preparation and release lag.
- **Primary delay reason** — a consistent classification for the main cause of delay across a sample of quotes.

The measurement model covers five stages:

1. Preparation
2. Commercial calculation
3. Validation
4. Approval
5. Customer-ready release

## Workbook contents

| Sheet | Purpose |
| --- | --- |
| **Measurement log** | Records quote milestones, elapsed stage durations, rework loops, rework duration, primary delay reason and notes across up to 100 quotes. Timestamp-based calculations are displayed in hours. |
| **Calculator inputs** | Captures fifteen calculator-aligned inputs for each quote and automatically calculates active processing time, waiting time, rework time, release lag, total turnaround time and the largest individual bottleneck. |
| **Definitions** | Provides the standard definitions, measurement guidance, stage descriptions, validation lists, workbook information and links to the official Configure to WIN resources. |
| **Worked example** | Demonstrates the calculation method with fictional inputs and formula-driven category totals, shares, stage totals and largest-bottleneck output. |

## How to use the workbook

### Option 1: Measure a representative quote with timestamps

Use the **Measurement log** when you have milestone timestamps for one or more completed quotes.

1. Select a recent complex quote that is representative of the process you want to understand.
2. Enter a Quote ID.
3. Record the available timestamps in chronological order, from **Quote request received** through **Quote released**.
4. Enter the number of rework loops and the total rework duration in hours, where applicable.
5. Select the primary delay reason and add contextual notes.
6. Review the calculated elapsed durations and total turnaround time.
7. Repeat the process for comparable quotes when you want to analyse a sample rather than a single case.

The Measurement log calculates elapsed clock time. Elapsed durations can therefore include nights, weekends and other periods in which nobody was actively working.

### Option 2: Separate active work, waiting and rework

Use **Calculator inputs** when you can estimate or reconstruct how time was distributed across the five quote stages.

1. Enter a Quote ID and measurement date.
2. Select one time unit for the row: **Minutes**, **Hours** or **Business days**.
3. Use that same unit for every duration entered in the row.
4. Enter the available values in the fifteen input fields. Leave unknown fields blank.
5. Review the calculated category totals and total turnaround time.
6. Use the **Largest bottleneck** result to identify the single time input that contributed most to the measured cycle.
7. Repeat the measurement with comparable quotes if you need a broader view of the process.

One business day equals eight hours in this measurement model. The workbook does not automatically remove nights, weekends or holidays, and it does not convert values between units for you.

## The fifteen calculator inputs

| Stage | Active processing | Waiting | Rework or release delay |
| --- | --- | --- | --- |
| **Preparation** | Active work time | Waiting for complete inputs | Rework caused by missing inputs |
| **Commercial calculation** | Active calculation time | Waiting for product, price or cost data | Recalculation or correction time |
| **Validation** | Active validation time | Waiting for clarification | Time spent correcting validation issues |
| **Approval** | Approval preparation time | Waiting for an approval decision | Rework after approver feedback |
| **Customer-ready release** | Final document or output preparation; final checks | — | Delay between approval and customer release |

## Calculation methodology

The workbook uses the following aggregate model:

```text
Total turnaround time
= Active processing time
+ Waiting time
+ Rework time
+ Release lag
```

### Active processing time

```text
Preparation active work
+ Commercial calculation active work
+ Validation active work
+ Approval preparation
+ Final output preparation
+ Final checks
```

### Waiting time

```text
Waiting for complete inputs
+ Waiting for product, price or cost data
+ Waiting for clarification
+ Waiting for an approval decision
```

### Rework time

```text
Input-related rework
+ Recalculation or correction
+ Validation corrections
+ Rework after approver feedback
```

### Release lag

```text
Delay between approval and customer release
```

### Largest bottleneck

The **Largest bottleneck** field returns the label of the highest individual value across the fifteen calculator inputs. It identifies the largest recorded time component, not a root cause by itself. Use the process context and notes to interpret why that component is high.

## Interpreting the results

A high total turnaround time does not automatically reveal what should be improved. Review the composition of the cycle:

- High **active processing time** indicates that substantial hands-on effort is required to prepare, calculate, validate, approve or release the quote.
- High **waiting time** indicates that the quote spends a large share of its cycle blocked by missing information, clarification or a pending decision.
- High **rework time** indicates that work is being repeated after incomplete inputs, changed assumptions, validation findings or approver feedback.
- High **release lag** indicates that an approved quote is not reaching the customer immediately.

Use these results to identify where additional process analysis is required. The workbook measures time; it does not determine the underlying organisational, policy, data or software cause automatically.

## Worked example

The included worked example uses fictional data to demonstrate the measurement model. Its calculated result is:

| Metric | Illustrative value |
| --- | ---: |
| Active processing time | 4.00 hours |
| Waiting time | 11.50 hours |
| Rework time | 1.25 hours |
| Release lag | 0.50 hours |
| **Total turnaround time** | **17.25 hours** |

In that example, **Waiting for an approval decision** is the largest individual bottleneck at 7.00 hours. These values are included only to explain how the workbook works. They are not customer data, target values, industry averages or recommended performance levels.

## Measurement guidance

For consistent results:

- **Use stable definitions.** Apply the definitions in the workbook consistently to every quote in the same sample.
- **Compare similar quotes.** Calculate averages only after checking that the quotes follow a sufficiently similar process and complexity profile.
- **Avoid double counting.** Assign each duration to one category and one stage. Do not count the same delay as both waiting and rework.
- **Keep units consistent.** Use one time unit within each Calculator inputs row. Convert values before comparing or aggregating rows that use different units.
- **Use actual timestamps where available.** Reconstructed estimates can still be useful, but should not be presented as directly observed elapsed time.
- **Document context.** Use the notes and delay-reason fields to preserve information needed to interpret the results later.

## Limitations and disclaimer

This workbook is a practical measurement tool. It does **not** provide:

- an industry benchmark;
- a recommended target turnaround time;
- a comparison with other companies or industries;
- a calendar-aware business-hours calculation;
- an automatic diagnosis of the root cause behind a delay;
- legal, financial or commercial advice.

Quote complexity, working calendars, approval policies and process definitions can differ substantially between organisations. The user remains responsible for the accuracy of the inputs, the consistency of the measurement method and the interpretation of the outputs.

The worked example is illustrative only and must not be treated as customer data, benchmark data or a recommended policy.

## License

This repository is licensed under the terms described in [LICENSE.md](LICENSE.md).

When reusing or adapting the workbook or documentation, follow the attribution and modification requirements stated in that file.

## About Configure to WIN

Configure to WIN develops tools and software for B2B quote control, pricing governance, commercial calculation and approval management.

Learn more at [Configure to WIN](https://configure.win/).
