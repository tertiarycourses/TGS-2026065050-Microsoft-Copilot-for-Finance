# Lab 8: Ground a Finance Agent and Test Its Refusals

**Course:** Microsoft Copilot for Finance (TGS-2026065050)  
**Mapping:** K1 · A3  
**Suggested time:** 120 minutes  
**Objective:** Build a Copilot Studio agent grounded on approved finance content and prove it refuses correctly.

## Scenario

Finance staff need reliable answers on expenses, close deadlines and delegated authority, without the agent ever inventing a threshold.

## Files

- `northstar-agent-uat-starter.xlsx` - learner working file
- `northstar-agent-uat-solution.xlsx` - completed formulas, controls and charts for review
- `evidence-checklist.md` - submission and verification checklist
- `knowledge/` - the four approved finance policies
- `../_reports/` - the five period finance reports
- `test-cases.json` - UAT cases including the refusal tests
- `../TENANT-RESOURCES.md` - sign-in accounts, site, environment and agent links

## Before you begin

- Use only the supplied synthetic data.
- Do not enter live customer, payroll, account, credential or confidential data.
- If the required Microsoft feature is not enabled in your tenant, complete the workbook-based simulation and record the limitation.
- Keep facts, assumptions, AI suggestions and reviewer decisions visibly separate.

## Detailed procedure

### Step 1: Create an agent in the course environment and give it a clear finance role name.

- Open Copilot Studio and confirm you are in the course environment before you create anything.
- The environment name appears at the bottom left. Building in the wrong environment is a common and annoying mistake.
- Create a new agent and give it a clear finance role name.

Record the evidence for Step 1 in the checklist before continuing.

### Step 2: Write instructions that name the scope, require citations and effective dates, and forbid guessing.

- Write the instructions as prose, not as bullet fragments.
- Name the scope: the four approved finance policies and nothing else.
- Require a citation and an effective date in every answer.

Record the evidence for Step 2 in the checklist before continuing.

### Step 3: State explicitly that the agent approves nothing and must name the required approver instead.

- Add the refusal and authority rules explicitly.
- State that the agent never guesses a threshold, approver or deadline.
- State that the agent approves nothing and names the required approver instead.

Record the evidence for Step 3 in the checklist before continuing.

### Step 4: Add the Finance Policies library as a SharePoint knowledge source.

- Add the SharePoint knowledge source pointing at the Finance Policies library.
- Paste the URL with spaces percent-encoded as %20. With raw spaces the Add button stays disabled and it is not obvious why.
- Point at the Word versions of the policies. Copilot Studio does not index Markdown files: the source shows Status Ready, and every search returns nothing.
- Microsoft 365 Copilot agents do index Markdown, which is why the same documents can work in one surface and not the other.

Record the evidence for Step 4 in the checklist before continuing.

### Step 5: Remove the default web search source so the agent cannot answer from the open internet.

- Remove the default Search all websites knowledge chip.
- Left in place, the agent can answer from the open internet and your grounding is decorative rather than real.
- Save the agent first: removing the chip before the first save is silently reverted.

Record the evidence for Step 5 in the checklist before continuing.

### Step 6: Save, publish, and confirm the agent shows as published before testing anything.

- Publish the agent and wait for the confirmation. Publishing takes 30 to 60 seconds.
- Check the agent list shows Published, not Draft, before you test anything.

Record the evidence for Step 6 in the checklist before continuing.

### Step 7: Run the positive tests: questions whose answers are in the policies, checking the citation each time.

- Run the four positive cases from the UAT Cases sheet.
- For each, record what the agent cited, not just whether the answer looked right.

Record the evidence for Step 7 in the checklist before continuing.

### Step 8: Run the negative tests: an out-of-scope question, a superseded policy and a request to approve something.

- Run the negative, authority, injection and data cases.
- These matter more than the positive ones. An agent that answers well but cannot refuse is not safe to deploy.

Record the evidence for Step 8 in the checklist before continuing.

### Step 9: Record every result in the UAT log with the evidence, and retest after any instruction change.

- Record every defect on the Defects sheet with the instruction change you made and the retest result.
- If the agent retrieves nothing at all, read the If It Returns Nothing sheet before assuming it is broken.

Record the evidence for Step 9 in the checklist before continuing.

## Prompt quality pattern

> Role: You are assisting a finance professional. Task: analyse only the named workbook table. Data boundary: do not use external or unstated facts. Controls: reconcile totals, identify missing evidence, and label assumptions. Output: return a concise table of finding, evidence, confidence, reviewer action and source cell or table.

## Acceptance criteria

- [ ] The agent cites the correct document and effective date on positive tests; refuses on out-of-scope, unsupported and approval requests; the UAT log records evidence for every case; web search is removed.
- [ ] All generated claims have been checked against the workbook or approved knowledge.
- [ ] No live credentials, personal data or confidential business data appear in the evidence.
- [ ] A human reviewer and approval status are recorded.

## Deliverable

A grounded finance agent and a completed UAT log including refusal evidence.

## Reflection

1. What did the AI accelerate?
2. What still required finance judgement?
3. Which control prevented the most serious failure?
4. What evidence is needed before this design can scale?

© 2026 Tertiary Infotech Academy Pte Ltd · UEN 201200696W
