[Back to README](../README.md) · [Open the Excel workbook](../template/quote-turnaround-time-measurement-template.xlsx) · [Use the online calculator](https://configure.win/resources/quote-turnaround-time-calculator)

# Workbook guide

This guide explains how to use the four worksheets in the **Quote Turnaround Time Measurement Template** and how the two measurement approaches relate to each other.

## Choose the appropriate measurement approach

The workbook supports two different ways to examine quote turnaround time.

| Use | Worksheet | What you record | What the worksheet calculates |
| --- | --- | --- | --- |
| Measure elapsed time from process milestones | **Measurement log** | Timestamps, rework information, a primary delay reason and notes | Elapsed stage durations and total turnaround time in hours |
| Separate the cycle into active work, waiting, rework and release lag | **Calculator inputs** | Fifteen duration inputs using one selected unit per quote | Category totals, total turnaround time and the largest individual bottleneck |

Use the **Measurement log** when milestone timestamps are available. Use **Calculator inputs** when you can estimate or reconstruct how the total cycle was distributed across the five stages.

The two worksheets answer related but different questions:

- **Measurement log:** How much elapsed clock time passed between defined milestones?
- **Calculator inputs:** How was the measured or reconstructed duration composed?

Do not assume that the outputs from both worksheets will reconcile automatically. They use different input structures and do not exchange data.

## Worksheet 1: Measurement log

The **Measurement log** supports up to 100 quote records. Each row represents one quote.

### Input columns

Enter the following information where available:

1. **Quote ID**
2. **Quote request received**
3. **Inputs complete**
4. **Commercial calculation complete**
5. **Validation complete**
6. **Approval submitted**
7. **Approval decided**
8. **Customer-ready output complete**
9. **Quote released**
10. **Number of rework loops**
11. **Rework duration (hours)**
12. **Primary delay reason**
13. **Notes**

Enter timestamps in chronological order. The calculated durations use elapsed clock time and are displayed in hours.

The permitted primary delay reasons are:

- Missing inputs
- Product, price or cost data
- Validation clarification
- Approval waiting
- Rework
- Release lag
- Other

### Calculated columns

The worksheet calculates:

- Preparation elapsed hours
- Calculation elapsed hours
- Validation elapsed hours
- Approval waiting hours
- Release preparation hours
- Release lag hours
- Total turnaround hours

The total turnaround value is calculated directly from **Quote request received** to **Quote released**. The rework-duration field is contextual information and is not added separately to total turnaround time.

For the exact milestone formulas and reconciliation boundaries, see [Milestone measurement guide](milestone-measurement-guide.md).

## Worksheet 2: Calculator inputs

The **Calculator inputs** worksheet also supports up to 100 quote records. Each row represents one quote or one set of averaged inputs.

### Row identification

Enter:

- **Quote ID**
- **Measurement date**
- **Time unit**
- **Notes**

The available units are:

- Minutes
- Hours
- Business days

Use the same unit for all fifteen duration fields in a row. The worksheet does not convert units automatically.

### Duration inputs

The worksheet contains fifteen inputs across five stages:

| Stage | Inputs |
| --- | --- |
| **Preparation** | Active work time; Waiting for complete inputs; Rework caused by missing inputs |
| **Commercial calculation** | Active calculation time; Waiting for product, price or cost data; Recalculation or correction time |
| **Validation** | Active validation time; Waiting for clarification; Time spent correcting validation issues |
| **Approval** | Approval preparation time; Waiting for an approval decision; Rework after approver feedback |
| **Customer-ready release** | Final document or output preparation; Final checks; Delay between approval and customer release |

Leave unknown fields blank. Only entered values are included in the calculation.

### Calculated outputs

For each row, the worksheet calculates:

- Active processing time
- Waiting time
- Rework time
- Release lag
- Total turnaround time
- Largest bottleneck

The **Largest bottleneck** output identifies the label of the highest individual value among the fifteen inputs. It does not diagnose the underlying root cause.

For field-by-field guidance, see [Duration input guide](duration-input-guide.md).

## Worksheet 3: Definitions

The **Definitions** worksheet is the reference point for consistent measurement. It contains:

- definitions of the core metrics;
- descriptions of the five process stages;
- measurement guidance;
- validation lists;
- workbook version and publisher information;
- links to the official Configure to WIN resources.

Use the same definitions for every quote included in one sample. Changing a definition during measurement can make rows difficult to compare.

See [Definitions](definitions.md) for the repository version of this reference material.

## Worksheet 4: Worked example

The **Worked example** contains fictional values that demonstrate:

- the fifteen inputs;
- category totals;
- category shares of total turnaround time;
- stage totals;
- the largest individual bottleneck.

The illustrative result is:

| Metric | Value |
| --- | ---: |
| Active processing time | 4.00 hours |
| Waiting time | 11.50 hours |
| Rework time | 1.25 hours |
| Release lag | 0.50 hours |
| **Total turnaround time** | **17.25 hours** |

The largest individual bottleneck is **Waiting for an approval decision** at 7.00 hours.

These values are not customer data, benchmark data, target values or a recommended policy.

## Recommended operating sequence

1. Decide whether you are measuring one representative quote or a sample of comparable quotes.
2. Select the **Measurement log**, **Calculator inputs**, or both.
3. Apply the definitions consistently.
4. Record actual timestamps where available.
5. Distinguish observed data from reconstructed estimates.
6. Keep units consistent.
7. Add notes needed to interpret unusual values.
8. Review category composition, stage values and the largest individual bottleneck.
9. Treat the results as a starting point for further process analysis, not as an automatic diagnosis.

## Related documentation

- [Methodology](methodology.md)
- [Measurement methodology](measurement-methodology.md)
- [Definitions](definitions.md)
- [Milestone measurement guide](milestone-measurement-guide.md)
- [Duration input guide](duration-input-guide.md)
- [Bottleneck interpretation](bottleneck-interpretation.md)
- [Limitations](limitations.md)
