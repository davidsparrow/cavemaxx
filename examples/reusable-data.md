# Example: a reusable tool built from private data

**Prompt**

> Analyse Company A's annual P&L. (a spreadsheet of revenue, cost of sales, payroll,
> marketing, overheads and margins follows)

## `/cave-off`

A written analysis: revenue mix, margin trends, the two or three lines that deserve attention,
and questions to ask the finance team. Company A's figures appear in the text.

## `/cave-default`

Usually the same written analysis, sometimes with a chart of the numbers.

## `/cave-max`

The word *analyse* plus a dataset the user will explore is a strong signal for an
**interactive explorer**. Claude also notices this is the kind of thing the user will want
again next year, or for Company B, so it builds it as a reusable **Annual P&L Explorer**
rather than a *Company A FY25 Dashboard*:

- the interface: margin waterfall, line-by-line variance, a "what if" panel for the two
  biggest cost lines, an at-a-glance summary of the numbers that moved most
- the data: loaded from one clearly marked place at the top of the file, with a paste box
  for a different dataset and a short description of the expected shape (line item, this
  year, last year)
- an empty state that still makes sense, and a "Load sample data" button using obviously
  made-up numbers, so the tool survives with Company A's figures removed

Company A's data is treated as the current input, not as part of the app. If the environment
can save state, it is saved privately to the user, not shared.

In prose: the three findings that matter and the question Claude would put to the finance
team. The explorer carries the detail.

## Why this matters

A dashboard with a company's real payroll figures hard-coded into the source is a liability
the moment it is copied, shared or reused. Separating the interface from the data costs a few
lines and makes the tool worth keeping.
