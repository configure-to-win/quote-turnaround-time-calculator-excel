[Back to README](../README.md) · [Open the Excel workbook](../template/quote-turnaround-time-measurement-template.xlsx) · [Use the online calculator](https://configure.win/resources/quote-turnaround-time-calculator)

# Measurement methodology

This document describes how to run a consistent quote-turnaround-time measurement exercise using the workbook. It complements [Methodology](methodology.md), which documents the calculation model and formulas.

## 1. Define the measurement objective

Use the workbook to examine either:

- one recent, representative complex quote; or
- a sample of comparable quotes measured with the same definitions.

The workbook is designed to show where recorded time is spent across preparation, commercial calculation, validation, approval and customer-ready release.

It does not provide an external benchmark or target.

## 2. Define the measurement boundary

Use the complete quote cycle:

```text
Initial quote request → Customer-ready release
```

Apply a consistent operational interpretation of the milestone fields throughout the sample.

The Measurement log uses these milestones:

1. Quote request received
2. Inputs complete
3. Commercial calculation complete
4. Validation complete
5. Approval submitted
6. Approval decided
7. Customer-ready output complete
8. Quote released

## 3. Select the measurement method

### Method A: Milestone timestamps

Use the **Measurement log** when timestamps are available.

This method measures elapsed clock time and is suited to recording:

- stage-to-stage elapsed durations;
- total request-to-release elapsed time;
- rework loops and rework duration;
- a primary delay reason;
- contextual notes.

Elapsed time can include nights, weekends and inactive periods.

### Method B: Duration composition

Use **Calculator inputs** when you can estimate or reconstruct time by category.

This method separates:

- active processing time;
- waiting time;
- rework time;
- release lag.

It uses fifteen fields across five stages and identifies the highest individual duration.

### Using both methods

Both methods can be applied to the same quote, but they remain separate measurements. The workbook does not transfer data between the worksheets or reconcile their outputs automatically.

Use the milestone method to understand elapsed flow and the duration-input method to understand composition.

## 4. Use the workbook definitions

Before collecting data, align on the definitions in [Definitions](definitions.md).

In particular:

- active processing means hands-on work;
- waiting means elapsed delay that blocks progress;
- rework means repeated work that would not have been necessary if the quote had been correct and complete the first time;
- release lag means elapsed delay after approval and before actual customer release.

## 5. Use actual data where available

Use actual timestamps when they exist.

Where durations must be reconstructed:

- use the same definitions;
- distinguish estimates from direct observations;
- document relevant assumptions or missing data in Notes;
- leave unknown duration inputs blank rather than replacing them with unsupported values.

Only entered values are included in Calculator inputs totals.

## 6. Keep categories mutually exclusive

Assign each duration to one stage and one category.

Do not count the same time as both:

- active processing and waiting;
- waiting and rework;
- active release preparation and release lag.

Rework duration entered in the Measurement log is not added to the elapsed total because it already occurs within the request-to-release period.

## 7. Keep time units consistent

Within one Calculator inputs row, select one of:

- Minutes
- Hours
- Business days

Enter all fifteen durations in that unit.

One business day equals eight hours. The workbook does not automatically convert units or remove nights, weekends or holidays.

Convert rows to a common unit before comparing or aggregating them.

## 8. Select a representative quote or comparable sample

### One representative quote

Select one recent complex quote and reconstruct the time spent in each stage. Use actual timestamps where available and distinguish hands-on work from elapsed waiting.

### A sample of quotes

Record multiple quotes using the same definitions. Calculate or compare averages only after checking that the quotes follow a sufficiently similar process and complexity profile.

The workbook does not determine comparability automatically.

## 9. Capture context

Use the Measurement log fields for:

- Number of rework loops
- Rework duration
- Primary delay reason
- Notes

Use Notes in Calculator inputs to document:

- incomplete inputs;
- reconstructed estimates;
- unit conversions performed before entry;
- unusual process conditions;
- context needed to interpret a high value.

## 10. Review the outputs in sequence

A consistent review sequence is:

1. Check whether the input set is complete enough for the intended analysis.
2. Review total turnaround time.
3. Review active processing, waiting, rework and release-lag composition.
4. Review the five stage totals.
5. Identify the largest individual bottleneck.
6. Compare the bottleneck with the selected primary delay reason and Notes.
7. Repeat across comparable quotes before drawing broader conclusions.

## 11. Report within the model’s boundaries

When sharing results, state:

- whether the values came from timestamps or reconstructed durations;
- which unit was used;
- whether all fields were known;
- whether the result represents one quote or a sample;
- whether elapsed time includes nights, weekends or holidays;
- that the workbook does not supply an industry benchmark or target.

See [Limitations](limitations.md) for the complete interpretation boundary.
