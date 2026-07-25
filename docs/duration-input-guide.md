[Back to README](../README.md) · [Open the Excel workbook](../template/quote-turnaround-time-measurement-template.xlsx) · [Use the online calculator](https://configure.win/resources/quote-turnaround-time-calculator)

# Duration input guide

Use the **Calculator inputs** worksheet to separate quote turnaround time into active processing, waiting, rework and release lag.

Each row represents one quote or one set of averaged inputs.

## Row setup

Enter:

- **Quote ID**
- **Measurement date**
- **Time unit**
- **Notes**

Select one time unit:

- Minutes
- Hours
- Business days

Use the selected unit for every duration in the row. The Excel workbook does not convert values automatically.

One business day equals eight hours in the Configure to WIN model.

## Input rules

- Enter non-negative durations.
- Leave unknown fields blank.
- Only entered values are included in the totals.
- Do not count the same time in multiple fields.
- Distinguish hands-on work from elapsed waiting.
- Keep release lag separate from final output preparation and final checks.

## The fifteen inputs

### 1. Preparation

Time spent gathering and completing the inputs required to start the quote.

| Input | Include |
| --- | --- |
| **Active work time** | Hands-on work used to gather products, requirements, customer context and other quote inputs. |
| **Waiting for complete inputs** | Time in which the quote cannot progress because required information is missing. |
| **Rework caused by missing inputs** | Repeated work required because inputs were incomplete, incorrect or changed. |

### 2. Commercial calculation

Time spent finding product, price and cost data and calculating the commercial outcome.

| Input | Include |
| --- | --- |
| **Active calculation time** | Hands-on work used to calculate pricing, cost, margin and other commercial outcomes. |
| **Waiting for product, price or cost data** | Delay caused by unavailable or incomplete product, pricing, supplier or cost information. |
| **Recalculation or correction time** | Time spent repeating calculations after data, assumptions or commercial inputs change. |

### 3. Validation

Time spent checking completeness, commercial rules and exceptions.

| Input | Include |
| --- | --- |
| **Active validation time** | Hands-on time used to validate quote data, calculations, rules and exceptions. |
| **Waiting for clarification** | Delay while sales, pricing, finance or another stakeholder supplies clarification. |
| **Time spent correcting validation issues** | Rework required after an incomplete input, rule exception or calculation issue is identified. |

### 4. Approval

Time spent preparing approval context, waiting for a decision and correcting issues raised during review.

| Input | Include |
| --- | --- |
| **Approval preparation time** | Hands-on time used to prepare the commercial context required by approvers. |
| **Waiting for an approval decision** | Elapsed delay between submitting the quote for review and receiving the required decision. |
| **Rework after approver feedback** | Time spent changing the quote after an approver requests corrections or additional context. |

### 5. Customer-ready release

Time spent creating the final output, completing final checks and releasing the approved quote.

| Input | Include |
| --- | --- |
| **Final document or output preparation** | Hands-on work required to create the customer-ready output after approval. |
| **Final checks** | Time spent confirming the approved data and output are ready for the customer. |
| **Delay between approval and customer release** | Post-approval elapsed time before the quote is actually released to the customer. |

## Calculated category totals

### Active processing time

The worksheet sums:

- Preparation — Active work time
- Commercial calculation — Active calculation time
- Validation — Active validation time
- Approval — Approval preparation time
- Customer-ready release — Final document or output preparation
- Customer-ready release — Final checks

### Waiting time

The worksheet sums:

- Preparation — Waiting for complete inputs
- Commercial calculation — Waiting for product, price or cost data
- Validation — Waiting for clarification
- Approval — Waiting for an approval decision

### Rework time

The worksheet sums:

- Preparation — Rework caused by missing inputs
- Commercial calculation — Recalculation or correction time
- Validation — Time spent correcting validation issues
- Approval — Rework after approver feedback

### Release lag

The worksheet uses:

- Customer-ready release — Delay between approval and customer release

### Total turnaround time

```text
Total turnaround time
= Active processing time
+ Waiting time
+ Rework time
+ Release lag
```

## Largest bottleneck

The worksheet returns the label of the highest individual value among the fifteen duration inputs.

This is the largest recorded time component, not a root-cause diagnosis.

When two or more fields share the same maximum value, the Excel formula returns the first matching field from left to right.

## Using averages

The online calculator and workbook can be used with one representative quote or with averages from a sample.

Before entering averages:

1. Apply the same definitions to every quote.
2. Check that the quotes follow a sufficiently similar process and complexity profile.
3. Convert all values to one common unit.
4. Preserve the fact that the row contains averages in the Quote ID or Notes field.
5. Do not combine unknown values with zero unless zero is the correct measured value.

## Worked example

The workbook’s fictional example produces:

| Output | Value |
| --- | ---: |
| Active processing time | 4.00 hours |
| Waiting time | 11.50 hours |
| Rework time | 1.25 hours |
| Release lag | 0.50 hours |
| **Total turnaround time** | **17.25 hours** |
| Largest bottleneck | Waiting for an approval decision — 7.00 hours |

These values demonstrate the formulas only and are not a benchmark or target.

## Related documentation

- [Definitions](definitions.md)
- [Methodology](methodology.md)
- [Bottleneck interpretation](bottleneck-interpretation.md)
- [Limitations](limitations.md)
