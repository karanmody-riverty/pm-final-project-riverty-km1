# PRD & Prototype Sprint (Module 4)

## Pick & scope with MoSCoW
- **The “Now” feature I’m scoping (name + one-line core description):** B2, a plain explainer for why income is asked and how it’s used. It should include the one change that matters most: saying which income figure is meant (“a typical month; if your pay varies, use a lower month”).
- **My finalized Must-Haves (after overriding the AI):** 1. Say which period is meant. The question reads “Your usual monthly income after tax”, with one line for variable pay: “If your pay changes, use a lower month.” This is the exact cause of N-01.
2. One line on why it’s asked, next to the question. For example: “We use this only to suggest a plan you can afford.” It sits beside the field, not behind a link. It answers the fear in N-06 that the figure “will be used against” her.
3. One line on who sees it and how long it’s kept. This fills the missing text in T-206. The wording must come from data protection as approved, versioned text, never written ad hoc.
4. It works on a phone during a break. All three lines are readable at 375px without scrolling past the field or opening a PDF or a new page. 78% of starters are on mobile.
- **What I demoted from Must → Should/Won’t, and why:** A sample figure in the field (“e.g. 1,850 €”), clearly marked as an example.

Not needed

## Generate your Simplified PRD
- **One thing my PRD makes explicit that a vague brief would have missed:** A vague brief like “add an explainer for why we ask for income” would let a developer, or an AI, write the wording itself, including how long the data is kept. That’s a legal statement about personal data, and if it’s wrong, Riverty has made a false promise to a consumer who is already scared it will be “used against” her (N-06).

## Prompt-to-prototype sprint
- **Where did the prototype reveal a gap in my PRD logic? (what I had to update):** I'd say it scoped out a smaller feature from the planning functionality which should have been part of the prototype
- **My prototype: save Claude's HTML as prototype.html in 04-roadmap/, open it in your browser, and add a screenshot:** prototype.html
