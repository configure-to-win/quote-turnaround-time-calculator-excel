[Back to README](../README.md) · [Open the Excel workbook](../template/quote-turnaround-time-measurement-template.xlsx) · [Use the online calculator](https://configure.win/resources/quote-turnaround-time-calculator)

# Methodology

The Quote Turnaround Time Calculator uses a stage-based measurement model that separates hands-on processing from elapsed waiting, repeated work and post-approval release delay.

## Measurement boundary

The overall measurement boundary runs from the **initial quote request** to **customer-ready release**.

The model covers five stages:

1. Preparation
2. Commercial calculation
3. Validation
4. Approval
5. Customer-ready release

## Core measurement categories

### Active processing time

Hands-on work required to prepare, calculate, validate, approve and release the quote.

```text
Active processing time
= Preparation active work
+ Commercial calculation active work
+ Validation active work
+ Approval preparation
+ Final document or output preparation
+ Final checks
```

### Waiting time

Elapsed delay while the quote cannot progress because information, clarification or an approval decision is still required.

```text
Waiting time
= Waiting for complete inputs
+ Waiting for product, price or cost data
+ Waiting for clarification
+ Waiting for an approval decision
```

### Rework time

Repeated work caused by missing inputs, corrections, validation issues or approver feedback.

```text
Rework time
= Rework caused by missing inputs
+ Recalculation or correction time
+ Time spent correcting validation issues
+ Rework after approver feedback
```

### Release lag

Elapsed time between approval and the actual customer-ready release of the quote.

```text
Release lag
= Delay between approval and customer release
```

### Total turnaround time

```text
Total turnaround time
= Active processing time
+ Waiting time
+ Rework time
+ Release lag
```

This aggregate formula is used by the **Calculator inputs** worksheet and the online calculator.

## Stage totals

The fifteen inputs can also be grouped by stage.

### Preparation

```text
Preparation
= Active work time
+ Waiting for complete inputs
+ Rework caused by missing inputs
```

### Commercial calculation

```text
Commercial calculation
= Active calculation time
+ Waiting for product, price or cost data
+ Recalculation or correction time
```

### Validation

```text
Validation
= Active validation time
+ Waiting for clarification
+ Time spent correcting validation issues
```

### Approval

```text
Approval
= Approval preparation time
+ Waiting for an approval decision
+ Rework after approver feedback
```

### Customer-ready release

```text
Customer-ready release
= Final document or output preparation
+ Final checks
+ Delay between approval and customer release
```

## Largest bottleneck

The **Largest bottleneck** is the highest individual duration across the fifteen inputs.

It identifies the largest recorded time component. It does not establish why that component is high and should not be treated as a root-cause diagnosis.

In the Excel workbook, when multiple fields share the same maximum value, the formula returns the first matching field from left to right.

## Units

The Calculator inputs worksheet and online calculator support:

- Minutes
- Hours
- Business days

One business day equals eight hours in the Configure to WIN measurement model.

Use one unit consistently for every duration in a single row. The Excel workbook does not convert values between units. Convert rows to a common unit before comparing or aggregating rows that use different units.

The model is not calendar-aware. It does not automatically remove nights, weekends or holidays.

## Blank and unknown inputs

Unknown duration fields may be left blank. Only entered values are included in the result.

A total based on incomplete inputs is therefore a partial measurement. Preserve that context in the notes and do not present a partial result as a complete reconstruction of the quote cycle.

## Milestone-based elapsed measurement

The **Measurement log** uses timestamps and calculates elapsed clock time in hours.

| Calculated duration | Start milestone | End milestone |
| --- | --- | --- |
| Preparation elapsed hours | Quote request received | Inputs complete |
| Calculation elapsed hours | Inputs complete | Commercial calculation complete |
| Validation elapsed hours | Commercial calculation complete | Validation complete |
| Approval waiting hours | Approval submitted | Approval decided |
| Release preparation hours | Approval decided | Customer-ready output complete |
| Release lag hours | Customer-ready output complete | Quote released |
| Total turnaround hours | Quote request received | Quote released |

Each calculated stage value is returned only when both required milestones are present. Negative durations are prevented by applying a minimum of zero.

The stage-duration columns do not necessarily add up to total turnaround time. In particular, the interval between **Validation complete** and **Approval submitted** is not represented by a separate calculated stage column. Total turnaround is calculated directly from the first to the last milestone.

Rework duration is entered separately for analysis and is not added to total turnaround time, because it occurs within the elapsed cycle.

## Worked example

The workbook includes a fictional worked example:

| Metric | Illustrative value | Share of total |
| --- | ---: | ---: |
| Active processing time | 4.00 hours | 23.19% |
| Waiting time | 11.50 hours | 66.67% |
| Rework time | 1.25 hours | 7.25% |
| Release lag | 0.50 hours | 2.90% |
| **Total turnaround time** | **17.25 hours** | **100.00%** |

The largest individual value is **Waiting for an approval decision** at 7.00 hours.

The example explains the formulas only. It is not a benchmark, target or recommended policy.

## Interpretation boundary

The model measures where time is recorded. It does not automatically determine the organisational, data, policy or software cause behind a value.

For interpretation guidance, see [Bottleneck interpretation](bottleneck-interpretation.md). For measurement constraints, see [Limitations](limitations.md).
