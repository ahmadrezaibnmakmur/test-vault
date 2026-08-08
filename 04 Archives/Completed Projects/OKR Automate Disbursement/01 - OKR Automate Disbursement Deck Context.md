---
type: source-deck-context
created: 2026-06-19
project: OKR Automate Disbursement
source:
  - /Users/ahmadreza/Downloads/OKR Automate- Disbursement.pptx
tags:
  - anyflo
  - disbursement
  - okr
  - operations
  - process-improvement
  - dmaic
  - source-deck
---

# OKR Automate Disbursement Deck Context

## Source

File: `/Users/ahmadreza/Downloads/OKR Automate- Disbursement.pptx`

Extraction workspace:

`/Users/ahmadreza/Documents/Personal Branding Agent/Projects/OKR Automate Disbursement/source_decks/okr_disbursement_extraction`

## Extraction Status

- Slide count: 52
- Media/image files: 36
- Native table objects detected: 5
- Native chart objects detected: 0
- Rendered slide PNGs: 52
- Contact sheets: 5

Important note:

> Many charts, process maps, issue recap tables, and possible-solution tables are embedded as images/screenshots, not native PowerPoint chart objects. Full context therefore requires both extracted text and rendered visual inspection.

## Deck Structure

The deck follows a DMAIC-style project structure:

1. Define Phase
2. Measure Phase
3. Analyze Phase
4. Improve Phase
5. Control Phase

## Project Topic

The project is about automating or improving the disbursement process at ESB.

Core problem:

- Disbursement process is still semi-automated.
- Transfer can only happen at earliest H+1 from transaction date, usually in the afternoon.
- Monday disbursements can extend into evening.
- Finance team must manually check before transfer.
- Disbursement can only be processed on business days.
- Data reconciliation is required due to transaction data issues, increasing lead time.

## As-Is Process

Main flow:

1. System initiates disbursement process.
2. System calculates transaction details automatically.
3. AP Staff compiles transaction data.
4. AP Staff reviews and reconciles data.
5. Data Analyst adjusts data if discrepancies exist.
6. AP Staff processes fund transfer.
7. Disbursement process completes.

Sub-processes:

- Compiling data.
- Reconciling data.
- Adjusting data.
- Transferring fund.

## Measure Phase

Key metrics:

| Metric | Unit | Baseline | Target |
|---|---:|---:|---:|
| Disburse Lead Time Average | Time in hrs | 16.2 | 12 |
| Error Rate Jul-Dec 2024 | Percent | 3.4% | 0.5% |
| Disburse Delayed Due to Holiday Q1-Q3 2024 | Days | 13 | 0 |

Observed measurement insights:

- Majority of disbursements occur between 3 PM and 5 PM.
- Peak frequency is 4 PM.
- Disbursements before 1 PM are rare.
- Distribution is right-skewed.
- Error rate tracking began after ticketing system implementation in July 2024.

## Analyze Phase

Main lead-time issue categories:

1. Data calculation takes 6 hours on average.
2. Data compiling takes 1.5 hours on average.
3. Reconcile process takes 3 hours on average.
4. Data adjustment process takes 90 minutes on average.
5. Manual email drafting takes 90 minutes on average.

Technical issue categories captured in the deck:

- Rounding discrepancies.
- Max cap calculation per outlet is incorrect.
- Manual push required for client morning transfer request.
- Discount does not match contract.
- MDR ESO rate does not match contract.
- Double disbursement data.
- Incorrect disbursement amount.
- MDR ESB still counted for clients with auto-debit = No.
- Refunded transactions still included in disbursement data.
- Client complaint because transaction not disbursed.
- Client performed ESO transactions without PG registration.
- Incorrect delivery cost deduction.
- Negative disbursement value.
- Non-PG ESB client transactions included in disbursement data.
- Incorrect client bank account information.
- Other issues: finance/data team dependency and end-of-month transfer requests.

## Waste and Variance

Operational and lead-time waste:

- Manual per-file report download for reconciliation.
- Manual delivery cost updates in daily disbursement report.
- Manual reconciliation using Excel and macros.
- Manual discount and max cap recording after daily disbursement.
- Manual drafting and sending of daily disbursement report emails.
- Manual bank account validation through m-banking/online payment.
- Double-checking client bank account recap in admin Google Sheet.

## Improve Phase

Implementation plan contains 22 projects.

Completed examples:

- Price, Disc & ESO Scheme Setting Standard for Special Case Contract.
- Disbursement Report Bulk Download.
- Disbursement Report Table Formatting.
- Limit User Role Access to Price & Discount.
- Enhancement Contract Mapping - CMS.
- Limit Bank Account Change Request to H+1.
- Cleaning Data & SOP Master Disbursement.
- PG Request Data Validation Flow.

In-progress examples:

- Adjustment Feature [New Engine].
- Auto Email Feature [New Engine].
- Update Disbursement Push Manual Status [New Engine].
- Schedule & QRIS Transaction Setting Enhancement [New Engine].
- PG Registration for DB Migration.
- Negative Disbursement Value Management.
- Streamline Pending Transaction Issue Handling in CMS.
- Disbursement Calculations Revamp.
- PG Tagging by Transaction.
- Refund and delivery-cost issue handling in CMS.
- Enable Auto Transfer Flow [New Engine].

Selected before-after improvements:

- Data compiling reduced from 1.5 hours to less than 10 minutes.
- Price/discount setting standardized for special-case contracts.
- User role access to price and discount limited to reduce accidental edits.
- Contract mapping enhanced to prevent duplicate disbursement data.
- Bank account change request limited to H+1 to reduce manual adjustment.
- Master disbursement data cleaned and SOP created.

## Control Phase

Control phase includes:

- Process Control Plan.
- Control Chart.
- Benefit of The Project.
- Project Closing Documentation.

Visual inspection note:

> Slides 44-46 and 48-50 appear mostly blank/placeholders except title/chrome in the rendered deck. Slide 51 contains a project closing documentation template. Slide 52 is the thank-you closing slide.

## Extracted Artifacts

Workspace artifacts:

- `deck_extraction.md`: full slide-by-slide text, native tables, and picture references.
- `media_inventory.md`: media file dimensions and slide usage.
- `deck_extraction.json`: structured extraction.
- `rendered_slides/`: 52 rendered slide PNGs.
- `contact_sheet_1.png` to `contact_sheet_5.png`: visual overview of all slides.
- `media/`: extracted image assets from the PPTX.

Obsidian artifacts:

- `Sources/OKR Automate Disbursement/deck_extraction.md`
- `Sources/OKR Automate Disbursement/media_inventory.md`
- `Sources/OKR Automate Disbursement/contact_sheet_1.png`
- `Sources/OKR Automate Disbursement/contact_sheet_2.png`
- `Sources/OKR Automate Disbursement/contact_sheet_3.png`
- `Sources/OKR Automate Disbursement/contact_sheet_4.png`
- `Sources/OKR Automate Disbursement/contact_sheet_5.png`

## Relationship To AnyFlo

This deck is highly relevant to AnyFlo.id because it documents a real operational workflow transformation:

- Process mapping before system change.
- Manual reconciliation and data fixing as bottlenecks.
- Approval/access-control issues.
- Need for data standardization.
- Need for clear ownership between Finance, Data, Operations, and System.
- Workflow automation opportunities around adjustment, email, transfer status, and issue handling.

Reusable AnyFlo themes:

- Workflow before software.
- Manual checking creates lead-time waste.
- Data quality issues create operational dependency.
- Role access control is part of workflow design.
- Automation should reduce waste, not just digitize existing manual work.

## Related Notes

- [[02 Areas/Personal Branding Agent/03 - AnyFlo ID Strategy|AnyFlo ID Strategy]]
- [[02 Areas/Personal Branding Agent/05 - AnyFlo Problem and Use Case Map|AnyFlo Problem and Use Case Map]]
- [[02 Areas/Personal Branding Agent/11 - Ahmad Reza Career Profile|Ahmad Reza Career Profile]]
- [[00 - PARA Home|PARA Home]]
