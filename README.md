# Absence Modal Prototype

Interactive prototype for the absence request and review feature, targeting the German Kita market.

## What this covers

- **Staff → Current** — The existing absence request modal as it is in the product today. Flat summary in the footer.
- **Staff → Alternative** — Proposed redesign. Dates first, "How absence works" link in the header, notice with "See request details" button, and the absence details modal with shift-level breakdowns.
- **Manager → Current** — Two-column review modal. Left: request form with flat summary. Right: flat shift list grouped by date.
- **Manager → Alternative** — Two-column review modal. Left: form with summary accordion. Right: staff away panel + shift accordions with expand/collapse.

## Scenarios

Switch between 7 scenarios using the control bar at the top:

| Scenario | What it tests |
|---|---|
| Holiday · Annual leave | Baseline — standard paid holiday |
| Holiday · Closure day | Range includes a Betriebsausflug (Paid closure day) |
| Holiday · Unpaid | Unpaid leave, no holiday deduction |
| Sick leave | Paid sickness, no balance impact |
| Child sick (§45 SGB V) | Statutory child sick leave |
| Holiday · Over entitlement | Request exceeds available balance |
| Holiday · No shifts published | No rota published for the period |

## Key behaviours

- Hours are calculated from shift data with break deductions applied (§4 ArbZG)
- Closure days and weekends show a diagonal stripe pattern in the skipped days list
- Summary totals are consistent across the main modal and the absence details modal
- All accordions start closed by default
- Hover states on all buttons and accordion triggers

## Technical notes

Self-contained single HTML file. No build step, no dependencies, no server required.
Built with React 18 via CDN and Babel standalone. Famly design tokens applied via inline styles.

---

*Part of [famly-design-prototypes](../)*
