# Example: comparing competitors

**Prompt**

> Compare these six competitors across pricing, features, target market and strengths.
> (six names and a paragraph of notes on each follow)

## `/cave-off`

A large Markdown table, six rows by four columns, plus a paragraph of commentary. Accurate,
dense, hard to scan on a phone, and every "what if I only care about X" is another message.

## `/cave-default`

Usually the same Markdown table. Sometimes an artifact if the data is very large.

## `/cave-max`

Six things compared on four-plus dimensions is a clear signal, so Claude builds an
**interactive comparison matrix**:

- one row per competitor, one column per dimension, with the user's notes loaded
- filter by capability, sort by price, show or hide competitors
- optional weighting of the criteria, with a weighted score that updates live
- tap a cell to expand the supporting notes

In prose: one paragraph naming the two or three that stand out and why. The matrix does the
rest.

The interface opens with the six competitors already loaded, because an empty matrix is not
useful. The competitor data sits in one place at the top of the file, so it can be swapped for
a different set later.
