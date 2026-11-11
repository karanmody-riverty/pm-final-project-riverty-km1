# Roadmap, PRD & Prototype (Module 4)

## Your strategic anchors
- **Persona (M2), who are you solving for?:** Mara, a shift worker with two open claims who uses the portal on her phone in short breaks. She wants one plan for all her claims that she can keep, without calling anyone.
- **Primary success metric (M3), your leading indicator:** Kept plans per multi-claim starter (no missed payment within 60 days). Baseline 27.4%, target 32.4%. The early read is the first instalment paid on time, around day 30.
- **Moment of misery (M2), the specific friction blocking the goal:** On her phone during a break, she can’t tell which income figure to give and can only see one claim at a time. She either closes the portal and calls, or picks the shortest plan and misses the second payment (N-01, N-02, N-03).
- **Guardrail metric (M3), what must not drop or break:** The 60-day missed-payment rate must stay at or below 19.0%.

## Scan the backlog & set a human baseline
- **My instinctive “quick wins” before touching the AI (2 to 3 feature IDs + why):** B2 and B4. So the plain explainer for the income question, it is a static question which can be plugged in directly via the database, and the handoff summary to agent, as this is information which is already collected and just needs to be transferred.

## Audit, override & decide
- **Where did you override the AI? (feature + old vs. new score + why):** B2, Value 3 → 4. The income steps cause 61% of drop-outs, and finishing counts toward kept plans per starter.
B5, Value 3 → 4, Effort 2 → 1. The document step is the biggest single drop (22.1%), and 853 documents never arrived (T-201).
B1, Effort 4 → 5, and B3, Effort 3 → 4. Combining claims and making recommendations explainable (N-12) are heavier than the AI assumed
- **Did the AI over-value a Sales/Eng request your M2 interviews don’t support?:** No. It already scored the “raise recovery” feature (B7) and the tech showcase (B8) lowest. M2 backs that: N-02 shows the shortest plan breaks, and N-05 shows the chat’s quick yes leaves consumers unsure about late payments.
- **Did it underweight something your M3 cohort/funnel data strongly supports?:** Yes, B5. The AI treated it as medium, but the funnel shows the document step as the largest single drop (1,313 starters), and 78% of starters are on mobile, where uploads fail.

## Generate your interactive roadmap
- **My “Now” lane (this sprint), the 2 to 3 quick wins I’ll build first:** B2, B4, B6
- **What I cut, and the “no” I’m protecting the scope from:** B7
- **Prototype/roadmap screenshot link (paste into your deliverables):** roadmap.html
