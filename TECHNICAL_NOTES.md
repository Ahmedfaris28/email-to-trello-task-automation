# Technical Notes (Public, Sanitized)

## Pattern

Trigger → HTML conversion → normalization → extraction scope → create a templated task.

- **Normalization:** remove invisible characters that can interfere with matching.
- **Extraction:** use a known starting label and the next field boundary; check a label exists before reading its value.
- **Optional fields:** return a blank value when a label is absent instead of raising a parsing exception.
- **Formatting:** combine field values into a structured Markdown-style task description.
- **Card consistency:** copy relevant properties from an existing reference card.

## Design boundaries

This example is a *portfolio case study*, not an installable automation. Specific organization labels, resource IDs, exact production rules, destination names, mailbox settings, and expressions are not distributed.

## Open improvements at the time documented

- Expand routing for additional record statuses.
- Verify less-frequent populated optional fields.
- Improve empty-line suppression and uncommon trailing-field boundaries.
- Explore AI-based classification separately if the value justifies approval, cost, and risk.
