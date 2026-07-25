[Back to README](../README.md) · [Open the Excel workbook](../template/quote-turnaround-time-measurement-template.xlsx) · [Use the online calculator](https://configure.win/resources/quote-turnaround-time-calculator)

# Bottleneck interpretation

The workbook helps identify where recorded time is concentrated. It does not automatically diagnose why a delay occurred or prescribe a solution.

## Start with data completeness

Before interpreting a result, check:

- whether the row represents one quote or an average;
- which time unit was used;
- whether unknown inputs were left blank;
- whether all relevant stages were measured;
- whether values are actual observations or reconstructed estimates;
- whether Notes preserve important context.

A result based on incomplete fields is a partial measurement.

## Review total turnaround time

Total turnaround time represents:

```text
Active processing time
+ Waiting time
+ Rework time
+ Release lag
```

A high total alone does not indicate which part of the process requires further analysis. Review its composition.

## Interpret category composition

### High active processing time

A high active-processing value indicates that substantial hands-on effort is required to prepare, calculate, validate, prepare approval context or create and check the final output.

Review which active field and stage account for the largest share.

### High waiting time

A high waiting value indicates that the quote spends a large share of its measured cycle blocked by:

- incomplete inputs;
- missing product, price or cost data;
- clarification;
- an approval decision.

Identify the specific waiting input rather than treating all waiting as one issue.

### High rework time

A high rework value indicates that work is being repeated after:

- incomplete, incorrect or changed inputs;
- changed data, assumptions or commercial inputs;
- a validation issue;
- approver feedback.

Rework time measures repeated effort. It does not identify the underlying cause automatically.

### High release lag

A high release-lag value indicates that an approved quote is not being released to the customer immediately.

Keep release lag separate from active output preparation and final checks.

## Review stage totals

The five stages are:

1. Preparation
2. Commercial calculation
3. Validation
4. Approval
5. Customer-ready release

A high stage total shows where time is concentrated across the combined active, waiting and rework inputs for that stage.

A stage total and a category total answer different questions:

- **Stage:** Where in the process is time concentrated?
- **Category:** What type of time is being recorded?

Review both before drawing a conclusion.

## Interpret the Largest bottleneck output

The **Largest bottleneck** is the highest single duration among the fifteen calculator inputs.

Use it as a pointer to the first field requiring further review.

It is not:

- proof of the underlying root cause;
- an industry comparison;
- a performance target;
- a recommended process change.

When multiple input fields share the same maximum value, the Excel workbook returns the first matching field from left to right.

## Compare the bottleneck with the primary delay reason

The Measurement log contains one **Primary delay reason** per quote:

- Missing inputs
- Product, price or cost data
- Validation clarification
- Approval waiting
- Rework
- Release lag
- Other

The Calculator inputs worksheet identifies the largest duration automatically, while the Measurement log records a selected classification.

These two signals may not be identical:

- the largest measured duration may not have been selected as the primary perceived reason;
- one selected reason may summarise several smaller duration components;
- the primary reason may require context that is only captured in Notes.

Use them together rather than treating either as a complete diagnosis.

## Interpret a sample, not just one row

For broader process conclusions:

1. Use the same definitions.
2. Compare quotes with sufficiently similar process and complexity profiles.
3. Convert values to a common unit.
4. Review whether the same category, stage or individual field is repeatedly high.
5. Preserve exceptions and missing-data context.

The workbook does not automatically verify whether quotes are comparable.

## Move from measurement to further analysis

Use the result to identify where additional review is required.

The published calculator guidance recommends moving from measurement to a review of the process, controls and software capabilities behind the largest delay.

The workbook itself does not determine which organisational, policy, data or software factor is responsible.

## Reporting language

Prefer precise statements such as:

> Waiting for an approval decision was the largest recorded input for this quote.

Avoid unsupported statements such as:

> The approval policy is the root cause.

The first statement is supported by the measurement. The second requires separate evidence.

## Related documentation

- [Methodology](methodology.md)
- [Measurement methodology](measurement-methodology.md)
- [Definitions](definitions.md)
- [Limitations](limitations.md)
