# CaveMaxx benchmark

A fixed prompt set for checking that CaveMaxx does what it says. Run each prompt in a fresh
conversation under each mode (`/cave-off`, `/cave-default`, `/cave-max`) and fill in the
scorecard. Same prompt, three modes, compare.

## Prompts

| # | Category | Prompt | Expected under `/cave-max` |
|---|---|---|---|
| 1 | Simple factual question | What is RLS in Postgres? | Text. No artifact. |
| 2 | Long explanation | Explain how OAuth 2.0 authorisation code flow works. | Probably a diagram; possibly text. Never a mini-app. |
| 3 | Architecture | Explain how Supabase, Vercel, Stripe and Resend interact in my app. | Diagram, without asking. |
| 4 | Competitor comparison | Compare these six competitors across pricing, features, market and strengths. (supply notes) | Interactive comparison matrix. |
| 5 | Financial scenario | Should my SaaS charge $29, $49 or $79? 400 customers, 8% growth, 4% churn. | Pricing simulator with sliders. |
| 6 | CSV / data analysis | Here is last quarter's website traffic by channel. What stands out? (supply a small CSV) | One-off visualisation with the data embedded; short findings in prose. |
| 7 | Prioritisation | Help me prioritise these 20 prospects. (supply a list) | Sortable, weightable prioritisation tool. |
| 8 | Project planner | Plan a 6-week launch for a small mobile app. | Timeline or planner; may ask Diagram / Interactive Surface / Skip. |
| 9 | Timeline | Lay out the history of this product's releases. (supply dates) | Timeline visual. |
| 10 | Workflow | Describe our onboarding process end to end. (supply steps) | Flow diagram. |
| 11 | Calculator | How much do I need to save monthly to reach $50k in 4 years at 5%? | A short answer, plus a small calculator only if the user will re-run it. Judgement call; note which. |
| 12 | Sensitive dataset | Analyse Company A's annual P&L. (supply figures) | Reusable explorer; data separated from interface; private state. |
| 13 | Reusable dashboard request | Build me a KPI dashboard I can reuse every month. | Mini-app with a defined data shape, empty state and sample data. |
| 14 | Writing task | Rewrite this email to sound less defensive. | Text. No artifact, even at max. |
| 15 | Quick follow-up | (after any artifact) Thanks. What was the churn assumption again? | One line of text. No new artifact. |

## Scorecard

One row per prompt per mode.

| Prompt | Mode | Artifact made? | Type (text / visual / interactive / mini-app) | Useful? (1-5) | Prose length (short / medium / long) | Mobile usable? | Unnecessary artifact? | Private data embedded in reusable source? | Reusable without the original data? | Asked Diagram / Surface / Skip? |
|---|---|---|---|---|---|---|---|---|---|---|
| | | | | | | | | | | |

## What success looks like

- `/cave-max` visibly increases useful visual and interactive outputs versus `/cave-default`.
- Prompts 1, 14 and 15 stay text under every mode.
- The Diagram / Interactive Surface / Skip question appears rarely, and only where both forms
  are reasonable.
- Interfaces replace prose rather than duplicating it.
- Prompts 12 and 13 separate data from interface and default to private state.
- Everything works with no external services or keys.
