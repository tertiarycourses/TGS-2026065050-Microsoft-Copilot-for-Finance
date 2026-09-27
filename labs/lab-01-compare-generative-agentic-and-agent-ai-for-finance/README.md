# Lab 1: Compare Generative, Agentic and Agent AI for Finance

**Course:** Microsoft Copilot for Finance (TGS-2026065050)  
**Mapping:** K2 · A1  
**Suggested time:** 60 minutes  
**Objective:** Classify finance and fintech use cases by AI type and match each to the control it needs.

## Scenario

Northstar Finance is deciding where to start with AI. The CFO wants to know which of the three AI types each candidate use case actually needs, because the controls differ.

## Files

- `ai-type-use-case-map-starter.xlsx` - learner working file
- `ai-type-use-case-map-solution.xlsx` - completed formulas, controls and charts for review
- `evidence-checklist.md` - submission and verification checklist
- `../TENANT-RESOURCES.md` - sign-in accounts, site, environment and agent links

## Before you begin

- Use only the supplied synthetic data.
- Do not enter live customer, payroll, account, credential or confidential data.
- If the required Microsoft feature is not enabled in your tenant, complete the workbook-based simulation and record the limitation.
- Keep facts, assumptions, AI suggestions and reviewer decisions visibly separate.

## Detailed procedure

### Step 1: Review the twenty candidate use cases in the workbook and the definitions sheet.

- Open the starter workbook and read the Definitions sheet before you classify anything.
- The three definitions are not interchangeable labels. Generative produces content, Agentic pursues a goal across steps, and an Agent is the deployed unit with an identity and permissions.
- Note the third column: what the control must address changes with each type.

Record the evidence for Step 1 in the checklist before continuing.

### Step 2: Classify each as Generative, Agentic or Agent, and record why.

- Work down the Use Case Map sheet one row at a time.
- Ask: does this only produce content (Generative), does it take several steps toward a goal (Agentic), or is it a named deployment with its own permissions (Agent)?
- Record your reason in the same row. A classification without a reason cannot be challenged later.

Record the evidence for Step 2 in the checklist before continuing.

### Step 3: For each, state the highest-impact action the AI could take without a person.

- For each row, write the worst thing the AI could do if no person intervened.
- Be specific. 'Make a mistake' is not an answer; 'post a journal that misstates the accounts' is.
- This column is what drives the control, so do not skip it.

Record the evidence for Step 3 in the checklist before continuing.

### Step 4: Assign the control that must exist before the use case may run.

- Name the control that must exist before the use case may run.
- Prefer structural controls (an approval gate, a permission boundary) over procedural ones (an instruction in a prompt).
- Seven of the twenty rows are decisions that must never be delegated to AI at all. Find them.

Record the evidence for Step 4 in the checklist before continuing.

### Step 5: Name an accountable human owner for each use case.

- Give every row a named accountable human owner, by role.
- If you cannot name an owner, the use case is not ready to start.

Record the evidence for Step 5 in the checklist before continuing.

### Step 6: Select three to sequence first and justify the order on control readiness, not enthusiasm.

- On the Sequencing sheet, choose three to start.
- Rank on control readiness, not on how interesting the use case is.
- Be ready to defend why the ones you excluded are not yet ready.

Record the evidence for Step 6 in the checklist before continuing.

## Prompt quality pattern

> Role: You are assisting a finance professional. Task: analyse only the named workbook table. Data boundary: do not use external or unstated facts. Controls: reconcile totals, identify missing evidence, and label assumptions. Output: return a concise table of finding, evidence, confidence, reviewer action and source cell or table.

## Acceptance criteria

- [ ] Every use case has a type, a justification, a highest-impact action, a named control and an accountable owner; the three selected are justified on control readiness.
- [ ] All generated claims have been checked against the workbook or approved knowledge.
- [ ] No live credentials, personal data or confidential business data appear in the evidence.
- [ ] A human reviewer and approval status are recorded.

## Deliverable

A classified use-case map with the control and accountable owner for each.

## Reflection

1. What did the AI accelerate?
2. What still required finance judgement?
3. Which control prevented the most serious failure?
4. What evidence is needed before this design can scale?

© 2026 Tertiary Infotech Academy Pte Ltd · UEN 201200696W
