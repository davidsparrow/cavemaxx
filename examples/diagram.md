# Example: explaining an architecture

**Prompt**

> Explain how Supabase, Vercel, Stripe and Resend interact in my app.

## `/cave-off`

A prose walkthrough: the browser talks to Vercel, Vercel calls Supabase for data and auth,
Stripe webhooks hit an API route, Resend sends the emails. Four paragraphs, correct, and the
reader has to draw the picture in their head.

## `/cave-default`

Usually prose. Sometimes a Mermaid or ASCII sketch.

## `/cave-max`

The primary task is understanding relationships, so this is a **diagram**, and the best form
is obvious enough that Claude does not ask. It draws the four services as boxes with labelled
arrows for every interaction the user described: request flow, auth, database reads and
writes, checkout, webhooks, transactional email.

Where a diagram helps, a little interaction can help more: hovering or tapping an arrow shows
what data crosses it, and a toggle switches between "sign-up flow" and "payment flow". No more
than that. This is a diagram for understanding, not an app.

In prose: a short note on the one interaction people usually get wrong (for example, that
Stripe's webhook must be verified server-side, not in the browser). Everything else is in the
picture.
