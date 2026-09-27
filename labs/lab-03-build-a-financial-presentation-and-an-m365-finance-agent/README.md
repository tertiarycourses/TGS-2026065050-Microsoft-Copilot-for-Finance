# Lab 3: Build a Financial Presentation and an M365 Finance Agent

**Course:** Microsoft Copilot for Finance (TGS-2026065050)  
**Mapping:** K2 · A1  
**Suggested time:** 90 minutes  
**Objective:** Generate a board deck from the approved report, then build a no-code M365 agent grounded on the finance site.

## Scenario

The approved report exists. The CFO needs a short board deck from it, and finance staff keep asking the same policy questions that an agent could answer.

## Files

- `northstar-deck-checklist-starter.xlsx` - learner working file
- `northstar-deck-checklist-solution.xlsx` - completed formulas, controls and charts for review
- `evidence-checklist.md` - submission and verification checklist
- `../_data/` - the shared Northstar finance dataset (CSV)
- `../TENANT-RESOURCES.md` - sign-in accounts, site, environment and agent links

## Before you begin

- Use only the supplied synthetic data.
- Do not enter live customer, payroll, account, credential or confidential data.
- If the required Microsoft feature is not enabled in your tenant, complete the workbook-based simulation and record the limitation.
- Keep facts, assumptions, AI suggestions and reviewer decisions visibly separate.

## Detailed procedure

### Step 1: Open PowerPoint and use Copilot to create a presentation from the approved Word report.

- Open PowerPoint with the same Microsoft 365 Premium account and start a new presentation.
- Use Copilot to create a presentation from the Word report you approved in the previous lab.
- Point it at the file. Do not describe the report from memory.

Record the evidence for Step 1 in the checklist before continuing.

### Step 2: Correct the story: lead with the decision, not the chronology, and cut slides that repeat the report.

- Compare what Copilot produced against the Deck Story sheet.
- Copilot orders slides the way the document runs. A board deck leads with the decision, not the chronology.
- Move the ask to slide one, and delete slides that only repeat the report.

Record the evidence for Step 2 in the checklist before continuing.

### Step 3: Cross-check every repeated figure against the report and the source workbook.

- Fill in the Deck Checklist sheet: every figure that appears on a slide, and its value in the report.
- Numbers drift between a document and a generated deck. This is exactly where it happens.

Record the evidence for Step 3 in the checklist before continuing.

### Step 4: Go to the SharePoint Build page and create an agent, naming it and stating its purpose.

- Go to the SharePoint start page and open the Build tab, then choose Agent.
- Give the agent a clear name and write a purpose that states what it answers and for whom.

Record the evidence for Step 4 in the checklist before continuing.

### Step 5: Add the Northstar Finance site as the source, so the agent answers only from approved content.

- On the Sources tab, search for the Northstar Finance site by name and add the entire site.
- If the site does not appear, it is not yet in the search index. A newly created site takes 30 to 60 minutes.
- Adding the whole site is right here because the agent needs both the policies and the reports.

Record the evidence for Step 5 in the checklist before continuing.

### Step 6: Write instructions that require citations, forbid guessing and state that the agent approves nothing.

- On the Behavior tab, write the agent instructions.
- Require it to name the source document and its effective date in every answer.
- Require it to refuse when the approved documents do not cover the question, and to point to Finance Operations.
- State that the agent approves nothing and must name the approver required instead.

Record the evidence for Step 6 in the checklist before continuing.

### Step 7: Add three starter prompts, create the agent, and test a policy question with a known answer.

- Add three starter prompts so a new user can see what the agent is for.
- Create the agent, then open it and ask a question whose answer you already know.
- Check the citation, not just the answer. An answer without a source is not usable finance evidence.

Record the evidence for Step 7 in the checklist before continuing.

### Step 8: Test a question the documents cannot answer and confirm the agent refuses rather than inventing.

- Now ask something the documents cannot answer, such as a cryptocurrency treasury policy.
- A correct agent says it cannot find that in the approved documents and directs you elsewhere.
- An agent that invents a plausible answer has failed the test, however good the answer sounds.

Record the evidence for Step 8 in the checklist before continuing.

## Prompt quality pattern

> Role: You are assisting a finance professional. Task: analyse only the named workbook table. Data boundary: do not use external or unstated facts. Controls: reconcile totals, identify missing evidence, and label assumptions. Output: return a concise table of finding, evidence, confidence, reviewer action and source cell or table.

## Acceptance criteria

- [ ] Repeated figures reconcile across workbook, report and deck; the agent cites a source document and its effective date, and refuses an out-of-scope question instead of guessing.
- [ ] All generated claims have been checked against the workbook or approved knowledge.
- [ ] No live credentials, personal data or confidential business data appear in the evidence.
- [ ] A human reviewer and approval status are recorded.

## Deliverable

A board deck generated from the approved report and a working M365 Copilot agent.

## Reflection

1. What did the AI accelerate?
2. What still required finance judgement?
3. Which control prevented the most serious failure?
4. What evidence is needed before this design can scale?

© 2026 Tertiary Infotech Academy Pte Ltd · UEN 201200696W
