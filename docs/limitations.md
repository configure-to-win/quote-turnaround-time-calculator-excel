[Back to README](../README.md) · [Open the Excel workbook](../template/quote-turnaround-time-measurement-template.xlsx) · [Use the online calculator](https://configure.win/resources/quote-turnaround-time-calculator)

# Limitations

The Quote Turnaround Time Measurement Template is a practical measurement tool. The following boundaries should be considered when using or reporting its results.

## No industry benchmark

The workbook measures the user’s own quote process. It does not provide:

- an industry average;
- a target turnaround time;
- a recommended performance level;
- a comparison with other companies or industries;
- a recommended approval policy.

Quote complexity, working calendars, approval policies and process definitions can differ substantially between organisations.

## Elapsed time is not business time

The Measurement log calculates elapsed clock time between timestamps. Results can include:

- nights;
- weekends;
- holidays;
- periods in which nobody is actively working.

The workbook does not automatically calculate business hours.

In the Calculator inputs model, one business day equals eight hours. This is a unit convention and not a calendar-aware working-time calculation.

## No automatic unit conversion in Excel

The Calculator inputs worksheet allows Minutes, Hours or Business days to be selected, but it does not convert the values.

Every duration within one row must use the selected unit. Convert values before comparing or aggregating rows that use different units.

## Blank fields produce partial measurements

Unknown duration inputs may be left blank, and only entered values are included in the calculation.

A result based on incomplete fields is not a complete reconstruction of the quote cycle. Record the missing-data context in Notes and avoid presenting the result as complete.

## Timestamp and reconstructed-duration methods are different

The Measurement log and Calculator inputs worksheets do not calculate the same thing in the same way:

- **Measurement log** calculates elapsed clock time between milestones.
- **Calculator inputs** sums manually entered or reconstructed duration components.

Their outputs may differ and are not automatically linked.

## Milestone stage durations may not sum to total turnaround

The Measurement log calculates total turnaround directly from **Quote request received** to **Quote released**.

Its individual calculated durations cover:

- request received to inputs complete;
- inputs complete to commercial calculation complete;
- commercial calculation complete to validation complete;
- approval submitted to approval decided;
- approval decided to customer-ready output complete;
- customer-ready output complete to quote released.

The interval between **Validation complete** and **Approval submitted** is not represented by a separate calculated stage column. The visible stage-duration values can therefore sum to less than total turnaround time.

## Rework duration is not added to elapsed total

The Measurement log records **Rework duration (hours)** separately. It is not added to total turnaround time because rework takes place within the elapsed request-to-release cycle.

Adding it again to the elapsed total would double count that time.

## Largest bottleneck is not a root cause

The Largest bottleneck output returns the label of the highest individual value among the fifteen duration inputs.

It does not determine why that value is high. A long approval wait, for example, is a measured time component; the workbook does not diagnose the policy, routing, information or organisational cause behind it.

When multiple fields share the same maximum value, the Excel formula returns the first matching field from left to right.

## Primary delay reason is a single classification

The Measurement log allows one primary delay reason per quote. A quote may have experienced several material delays, but only one can be selected in that field.

Use Notes to capture additional reasons or context.

## Estimates are not direct observations

Reconstructed durations can be useful when detailed timestamps are unavailable, but they should not be described as directly observed elapsed time.

Distinguish actual timestamps from estimates when reporting results.

## Comparability depends on the sample

Averages are meaningful only when the included quotes follow a sufficiently similar process and complexity profile.

The workbook does not automatically classify quote complexity or verify whether rows are comparable.

## No automatic diagnosis or recommendation

The workbook identifies recorded duration patterns. It does not automatically prescribe a process, control or software change.

Results should be used to identify where further analysis is required.

## Worked example boundary

The worked example uses fictional inputs. It is not:

- customer data;
- benchmark data;
- an industry average;
- a target;
- a recommended policy;
- advice.

## User responsibility

The user remains responsible for:

- input accuracy;
- consistent definitions;
- unit consistency;
- sample comparability;
- interpretation of outputs;
- suitability for the intended purpose.

For the intended measurement rules, see [Methodology](methodology.md) and [Measurement methodology](measurement-methodology.md).
