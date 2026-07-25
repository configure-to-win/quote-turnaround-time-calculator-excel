[Back to README](../README.md) · [Open the Excel workbook](../template/quote-turnaround-time-measurement-template.xlsx) · [Use the online calculator](https://configure.win/resources/quote-turnaround-time-calculator)

# Definitions

Use these definitions consistently for every quote included in the same measurement exercise.

## Core metrics

| Term | Definition | Measurement guidance |
| --- | --- | --- |
| **Total turnaround time** | The complete elapsed time required to move a quote from the initial request to customer-ready release. | Measure the full duration, including active work, waiting, rework and release lag. |
| **Active processing time** | Hands-on work required to prepare, calculate, validate, approve and release the quote. | Include only time during which someone is actively progressing the quote. |
| **Waiting time** | Elapsed delay while the quote cannot progress because information, clarification or an approval decision is still required. | Include internal and external waiting that blocks the next stage. |
| **Rework time** | Repeated work caused by missing inputs, corrections, validation issues or approver feedback. | Record work that would not have been necessary if the quote had been correct and complete the first time. |
| **Release lag** | Elapsed time between approval and the actual customer-ready release of the quote. | Keep this separate from active document preparation and final checks. |
| **Elapsed time** | The complete clock time between two milestones. | Elapsed time can include nights, weekends and periods in which nobody is actively working. |
| **Business hours** | Time measured only during the organisation’s selected working schedule. | The template does not automatically remove nights, weekends or holidays. |
| **Business day** | A measurement unit equal to eight hours in the Configure to WIN calculator. | It is a unit conversion, not a calendar-aware scheduling calculation. |
| **Largest bottleneck** | The individual calculator input with the highest entered duration. | Treat it as the largest recorded time component, not as an automatic root-cause diagnosis. |
| **Primary delay reason** | A selected classification for the main reason a measured quote was delayed. | Use one consistent classification and preserve additional context in Notes. |

## Process stages

| Stage | Definition | Typical measurements |
| --- | --- | --- |
| **Preparation** | Time spent gathering and completing the inputs required to start the quote. | Active preparation, waiting for complete inputs and input-related rework. |
| **Commercial calculation** | Time spent finding product, price and cost data and calculating the commercial outcome. | Active calculation, waiting for data and recalculation or correction. |
| **Validation** | Time spent checking completeness, commercial rules and exceptions. | Active validation, waiting for clarification and correction of validation issues. |
| **Approval** | Time spent preparing approval context, waiting for a decision and correcting issues raised during review. | Approval preparation, approval waiting and rework after approver feedback. |
| **Customer-ready release** | Time spent creating the final output, completing final checks and releasing the approved quote. | Output preparation, final checks and delay between approval and release. |

## Calculator input definitions

### Preparation

| Input | Definition |
| --- | --- |
| **Active work time** | Hands-on work used to gather products, requirements, customer context and other quote inputs. |
| **Waiting for complete inputs** | Time in which the quote cannot progress because required information is missing. |
| **Rework caused by missing inputs** | Repeated work required because inputs were incomplete, incorrect or changed. |

### Commercial calculation

| Input | Definition |
| --- | --- |
| **Active calculation time** | Hands-on work used to calculate pricing, cost, margin and other commercial outcomes. |
| **Waiting for product, price or cost data** | Delay caused by unavailable or incomplete product, pricing, supplier or cost information. |
| **Recalculation or correction time** | Time spent repeating calculations after data, assumptions or commercial inputs change. |

### Validation

| Input | Definition |
| --- | --- |
| **Active validation time** | Hands-on time used to validate quote data, calculations, rules and exceptions. |
| **Waiting for clarification** | Delay while sales, pricing, finance or another stakeholder supplies clarification. |
| **Time spent correcting validation issues** | Rework required after an incomplete input, rule exception or calculation issue is identified. |

### Approval

| Input | Definition |
| --- | --- |
| **Approval preparation time** | Hands-on time used to prepare the commercial context required by approvers. |
| **Waiting for an approval decision** | Elapsed delay between submitting the quote for review and receiving the required decision. |
| **Rework after approver feedback** | Time spent changing the quote after an approver requests corrections or additional context. |

### Customer-ready release

| Input | Definition |
| --- | --- |
| **Final document or output preparation** | Hands-on work required to create the customer-ready output after approval. |
| **Final checks** | Time spent confirming the approved data and output are ready for the customer. |
| **Delay between approval and customer release** | Post-approval elapsed time before the quote is actually released to the customer. |

## Milestone fields

The Measurement log records these milestones in chronological order:

1. Quote request received
2. Inputs complete
3. Commercial calculation complete
4. Validation complete
5. Approval submitted
6. Approval decided
7. Customer-ready output complete
8. Quote released

The workbook does not add separate definitions beyond the milestone labels. Apply one agreed operational interpretation of each milestone throughout the measurement sample.

## Primary delay reason values

The Measurement log provides the following values:

- **Missing inputs**
- **Product, price or cost data**
- **Validation clarification**
- **Approval waiting**
- **Rework**
- **Release lag**
- **Other**

The selected value should represent the primary delay reason for the quote. Use **Notes** to preserve detail that the classification alone does not capture.

## Time unit values

The Calculator inputs worksheet provides:

- **Minutes**
- **Hours**
- **Business days**

One business day equals eight hours. The Excel workbook does not convert values between units automatically.

## Related documentation

- [Methodology](methodology.md)
- [Milestone measurement guide](milestone-measurement-guide.md)
- [Duration input guide](duration-input-guide.md)
- [Limitations](limitations.md)
