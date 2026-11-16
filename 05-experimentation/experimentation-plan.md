# Experimentation Plan (Module 5)

## Get your documents ready
- **From M3, your hypothesis sentence:** I believe that one combined plan sized to a typical month’s income, for multi-claim consumers like Mara, will result in more plans agreed and kept online, as measured by a 5-point rise (27.4% → 32.4%) in kept plans per multi-claim starter. I will protect the 60-day missed-payment rate (≤19%).
- **From M3, your primary success metric & guardrail metric:** Primary: kept plans per multi-claim starter (27.4%). Guardrail: 60-day missed-payment rate (≤19.0%).
- **From M4, the feature you scoped in your PRD this is what you're testing:** B2, the plain explainer for why income is asked and how it’s used (the clear income question).

## Define your experiment parameters
- **Feature under test pull from your M4 PRD:** B2, the clear income question: which figure to give, why it’s asked, and who sees it and for how long, all next to the field (PRD screen 2, FR1–FR5).
- **Persona pull your M2 persona:** Mara, a shift worker with two open claims who uses the portal on her phone during short breaks.
- **Expected outcome the behaviour change you expect, from your M3 hypothesis:** more multi-claim starters answer the income question and move on, instead of closing the portal (N-01) or calling to ask why (16.2% of contacts).
- **Primary success metric the one number that defines success, from M3:** income-step completion: the share of multi-claim starters who reach the affordability questions and go on to the next step.
- **Baseline rate today's rate of your primary metric, from your M3 data:** 80.7% (5,943 of 7,364 in the sample month). This is the all-starter figure; the data pack has no funnel split by number of claims. Metric to ask for: this step’s completion rate for multi-claim consumers only.
- **Guardrail metric & boundary what must not break, and how far it can move before you investigate:** 60-day missed-payment rate, baseline 19.0%. Investigate if the variant is 1 point or more above control. Stop if it goes above 20%.
- **Minimum Detectable Effect (MDE) the smallest improvement worth shipping, your floor:** +5 points (80.7% → 85.7%). That’s about a quarter of the drop-off, in line with the PRD target of a drop of 14% or less.
- **Sample size per arm use the calculator in the builder, baseline + MDE:** 1059
- **Traffic split & test duration 50/50 standard · cover ≥ 2 weekly cycles:** 50/50, 4 weeks
- **Significance threshold p < 0.05 is standard, explain any deviation:** p < 0.05

## Define your control and variant
- **Control (A) the current experience, reference your M2 moment of misery and M3 funnel/workflow data:** today’s income step. It asks for “income” with no period, no reason and no retention line (T-206). Shift workers can’t tell “this month or a normal month?” (N-01), and 19.3% drop at this step (1,421 a month).
- **Variant (B) your single change, copy the relevant screens & functional requirements from your M4 PRD:** The label reads “Your usual monthly income after tax”.
An always-visible variable-pay hint.
A why line (≤20 words) and a retention line (≤25 words), both from approved text by ID and version.
All of it fits in one 375×667 view.
- **Isolation check, what has NOT changed? list everything identical between arms (app version, eligibility rules, notifications, onboarding). If something changed inadvertently, your test is compromised.:** App version and release, and eligibility (Germany, 2+ open claims).
Reminders and their timing, including the T-207 bug.
The document step (T-201 unchanged).
The plan options screen, including the current 6-month-first default.
Chat availability, agent scripts and the support phone line.
Field validation rules, and the claim amounts and letters.

## Formalize your hypothesis & shipping criteria
- **Your hypothesis (filled in):** I believe that a clear income question (which figure, why we ask, who sees it) for multi-claim consumers like Mara will result in more of them finishing the income step instead of closing the portal or calling, as measured by a +5-point (80.7% → 85.7%) change in income-step completion within 4 weeks. We will protect the 60-day missed-payment rate (≤19%) and agent contacts within 7 days throughout the test.
- **Your shipping criteria (filled in):** We will ship if income-step completion improves by ≥ 5 points at p < 0.05, and the 60-day missed-payment rate does not reach control + 1 point (or 20%) after 60 days of follow-up.
We will iterate if the direction is positive but the lift is below the MDE.
We will kill if the primary metric shows no improvement or moves negatively.
The read date is fixed at the end of week 4 for the primary metric, and day 60 after the last sign-up for the guardrail. No results are reviewed before these dates.
- **Hardest parameter to define, and did it change your hypothesis? quick debrief:** The primary metric. My M3 metric (kept plans per starter) is the right measure for the initiative but wrong for a test of one copy change: it’s 60 days away and affected by later screens. I narrowed the hypothesis from “a combined, affordable plan” to “a clear income question”, measured at the step where Mara gives up. Kept plans and missed payments now protect the result instead of defining it.
