# AI Synthesis, Product Health & Insights Summary (Module 2)

## Responses
- **Assumption to validate #1:** There is no clarity provided by the chat for the installment planning tool in the portal
- **Assumption to validate #2:** Agents and consumers end up putting double effort for one case
- **Assumption to validate #3:** Consumers find agents to be more empathetic than the bot
- **Moment of misery / red flag #1 (e.g., “user gave up after 3 tries”):** Amount was too high for installment and missed payment 2
- **Moment of misery / red flag #2:** No clarity on what the amount meant and also asked for information without giving context
- **Moment of misery / red flag #3:** Agents has to ask the user questions they have already answered creating friction
- **Product Health & Insights Summary (Claude's output):** Product Health & Insights Summary

Repayment Plan Portal, Chat Assistant & Agent Tooling, based on 12 interview notes and 8 tickets/bugs (illustrative sample data)

Executive Summary

The plan set-up journey is fast once a consumer reaches the end, but it is undermined by two critical stability failures: mobile document uploads that time out, and portal amounts that don’t match letters. Together these affected 1,384 journeys in the sample month. Beyond those defects, the larger risk is experiential: consumers in financial strain meet ambiguous questions, unexplained data requests and plan options that nudge them toward unaffordable commitments, while agents and compliance lack visibility into how any plan was reached. As a result, technically completed plans aren’t reliably sustainable, and broken plans move downstream into repeat calls, complaints and client-facing reporting.

Thematic Synthesis
1. Technical Stability & Data Integrity

The two highest-volume defects both block consumers from moving forward. The upload failure stops journeys outright. The amount mismatch is less visible but arguably more damaging, because it makes the consumer doubt the whole process just as they are being asked to commit. The mismatch is concentrated in purchased portfolios (343 of 531 affected journeys, about 65%). That matches the analyst’s report that acquired portfolios carry inconsistent source data, so this looks like an upstream data-quality issue rather than an isolated display bug.

Critical: Income document upload times out on mobile for large photos. 853 journeys requested a document that never arrived (T-201).
Critical: Portal amount differs from the letter, mostly in purchased portfolio cases (531 journeys, 343 purchased). Consumers decline to commit until someone explains it (T-203, N-07).
High: The pre-instalment reminder sometimes arrives after the due date, which removes the main safeguard against early plan failure (T-207).
Medium: Acquired portfolios lack consistent data, including reliable phone and address history. This limits both the accuracy of amounts and the ability to reach consumers (N-11).
2. Onboarding, UX & Plan Selection

The affordability flow assumes a stable, single-claim, unhurried consumer. Shift workers completing it on a break, consumers with several claims, and those with irregular income find the questions ambiguous and the structure mismatched to their situation. The plan selection screen also seems to create a bias: the shortest plan reads as the “correct” answer, which pushes consumers toward instalments they can’t sustain.

High: Plan options suggest the shortest duration is the right choice, leading consumers to pick unaffordable instalments and miss early payments (N-02).
High: Claims appear separately, with no way to set up one plan across multiple claims. Consumers can’t tell whether paying one claim stops collection on another (T-202, N-03).
High: The income question doesn’t say which reference period it means (current month or typical month), which causes abandonment among irregular earners (N-01).
3. Trust, Clarity & Explainability

The most consistent signal from consumer interviews is anxiety, not confusion. Consumers fear that the information they enter will be used against them, and they can’t see the consequences of the commitments they make. The chat assistant shows this tension clearly: it is valued for its speed, but it confirms plans without disclosing what happens after a missed payment. Compliance sets an explicit requirement that recommendations must be explainable to both consumers and agents, and the current experience doesn’t support that.

High: No help text explains why income is requested or how long it is kept, which heightens fear of misuse among financially stretched consumers (T-206, N-06).
High: The chat assistant and plan flow confirm agreements without showing what happens after a late or missed payment (T-208, N-05).
High: Plan decisions lack traceable reasoning, which conflicts with the compliance requirement that decisions be explainable on request (N-12).
Medium: Some consumers still prefer human contact for reassurance about cost implications. This reflects a trust gap in self-service rather than a channel preference alone (N-04).
4. Agent Experience & Support Load

Digital journeys don’t pass context to the assisted channel. When a consumer abandons online or a plan fails, agents start from scratch: they re-collect information the consumer has already entered and can’t diagnose why a failed plan was offered. This turns self-service friction directly into longer handling times, and it repeats the consumer’s frustration at the point where they most need resolution.

High: The agent screen doesn’t show consumer-entered data or the rationale behind an offered plan. By one agent’s estimate, about half of calls begin with re-collecting known details (T-205, N-08).
High: Agents can’t diagnose plan failures because only the plan amount is visible, not the inputs or logic behind it (N-09).
5. Client & Commercial Exposure

Client account management notes that complaints matter to clients as much as recovery rates, and that spikes in broken plans show up in client reporting. The issues above therefore add up to a commercial exposure: unaffordable plan selection, late reminders, unexplained amounts and missing consequence disclosure each raise the rate of broken plans, which then shows up as a client-visible metric.

High: Broken plans and complaints are reported to clients and directly affect relationship health, which magnifies the effect of every upstream defect (N-10).
Minor Technical Debt

Low: The back button on the plan review screen clears affordability answers, adding re-entry friction to an already time-pressured flow (T-204).
- **Did the AI catch the specific moment of misery / pain point you found in Step 1?:** Yes, and more. It pointed out things I generalised
- **Did it smooth over a critical frustration into a generic bullet point?:** Not exactly, it gave me proper insights
- **Did the AI try to suggest features or a roadmap despite the constraints?:** No
- **Logic leak / hallucination #1 (e.g., “AI suggested a new search bar feature, roadmap leak”):** _(not filled in)_
- **Logic leak / hallucination #2:** _(not filled in)_
