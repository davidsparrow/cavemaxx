# Example: a pricing decision

**Prompt**

> Help me figure out whether my SaaS should cost $29, $49 or $79 a month. I have about 400
> customers today, growing maybe 8% a month, and churn is around 4%.

## `/cave-off`

Ordinary analysis in Markdown. What each price signals, how conversion typically responds,
the retention argument, a recommendation with caveats. Perhaps a small table of the three
tiers at today's customer count. Nothing interactive. Fine if you want to paste it into a memo.

## `/cave-default`

Whatever stock Claude would do: usually the same analysis, occasionally a table or chart if
Claude happens to think of it.

## `/cave-max`

The best form is obvious (numbers the user will want to change, three scenarios to compare,
a decision to make), so Claude does not ask. It builds a **pricing simulator**:

- sliders for price, starting customers, monthly growth, monthly churn, and how much
  conversion drops at each higher tier
- the three tiers side by side: monthly revenue now, revenue in 12 months, customers in 12
  months
- a small chart of revenue over 12 months per tier
- the assumptions written out where the user can see them, so the model is checkable

Underneath, two or three sentences: which tier the numbers favour given the stated
assumptions, and the one assumption that would flip it. That is the whole answer. No
recap of the dashboard in prose.

If the request had been *"which price would you pick and why?"* with no numbers, the choice
would be less obvious and Claude might ask: *This could work better visually. Diagram ·
Interactive Surface · Skip.*
