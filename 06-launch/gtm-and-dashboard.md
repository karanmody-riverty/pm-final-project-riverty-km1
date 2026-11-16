# GTM Launch Plan, Riverty BU Collection, A Fair Way Forward

| Field | Value |
|---|---|
| Feature | B2: the clear income question (which figure, why it’s asked, who sees it and how long it’s kept) |
| Goal | Conversion |
| Launch tier | S, Minimal |

## Goal & Audience
- **Goal:** Conversion, The goal is to get more of the people who are already in the journey through one step: from seeing the income question to submitting it and moving on, 80.7% → 85.7%. That’s a conversion goal.
- **Target audience:** Primary: German portal users with 2+ open claims who start an instalment plan, about 2,968 a month (35.5% of starters), 78% of them on mobile.
Internal: collection agents, client account managers and compliance.

## Launch Tier
- **S, Minimal**, Quiet launch inside the product. It’s a copy change on one step, so consumers don’t need to be told; they just meet a clearer question. Promoting a debt-collection journey would feel pushy and could get between the customer and paying. The work goes into internal readiness and the A/B gate, not into announcements.

## Channels
1. **Owned: The portal’s income step itself, plus the Help/FAQ page carrying the same approved text IDs, so the answer is identical wherever Mara looks. Reminders stay unchanged during the test (isolation). After rollout, there’s an option to mention “a clearer way to set up a plan” in the email reminder.**
2. **Earned: Client account managers include the result in client reporting (“fewer broken plans and complaints”, N-10). An internal showcase for collections and product teams, so other markets reuse the pattern.**
3. **Paid: none, on purpose. Paid media aimed at people in debt isn’t appropriate, and the audience already arrives through reminders.**

## Enablement & Assets
Agent briefing for Daniel: what changed, the exact approved texts, and how to answer “why do you need my income?” and “how long do you keep it?” in the same words. One page plus a 10-minute team huddle before launch.
Approved text entries: TXT-INCOME-LABEL, -HINT, -WHY and -RETENTION (v1), signed off by Data Protection and Compliance for Germany. The retention period is filled in by Data Protection, never by the team.
Help/FAQ update using the same text IDs.
Client account manager one-pager: what changed, why, and what to expect in reporting.
Experiment dashboard:
income-step completion by arm
contact reasons
7-day contacts
the 60-day missed-payment tripwire
the 50/50 split check
Launch checklist: all four text IDs load in production, tracking events fire, randomisation is sticky per consumer.

## Ownership, Budget & Timeline
- **Ownership & budget:** Karan (PM) owns the launch and the go/no-go decision.
Data Protection owns the retention text, and Compliance signs off the wording.
The Collections Ops lead runs the agent briefing.
The client account management lead handles client messaging.
Analytics owns the dashboard and the split check.

Budget: no media spend. Roughly 1 sprint of 2 front-end developers, plus copy and legal review time (an estimate).
- **Timeline:** Week 0: text sign-off, agent briefing, launch checklist passed.
Weeks 1–4: 50/50 A/B test, no peeking.
End of week 4: read the primary metric, go/no-go.
Week 5: roll out to 100% of German multi-claim starters if it passes.
Day 60 after the last sign-up: missed-payment tripwire review.
After that: other markets only once each has its own approved texts (for example de-AT). A missing text blocks the step; it’s never translated.

## Success Metrics
- **Metrics:** Primary: income-step completion +5 points (p < 0.05).
Supporting: the share of “why is income asked?” contacts falls below 16.2%.
Guardrail: agent contacts within 7 days don’t rise by more than 2 points.
Tripwire: the 60-day missed-payment rate stays within control + 3 points and at or below 22%.
- **Bad signal to watch for:** Completion rises, but so do re-entered figures, entries of €0, or calls asking “how long do you keep my data?”. That would mean the retention line created a new worry. Or missed payments climb because people who are less sure of their figure now get through.
- **Likely post-launch decision:** ship it to all German starters, single-claim too, because the copy isn’t segment-specific. Then reuse the clear income figure as the input for B3 (affordability-based plan sizing), the next “Major Project”. If the lift lands below 5 points, test copy variants of the why and retention lines first.
