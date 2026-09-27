# Lab 2: Draft a Financial Report with Copilot in Word

**Course:** Microsoft Copilot for Finance (TGS-2026065050)  
**Mapping:** K2 · A1  
**Suggested time:** 90 minutes  
**Objective:** Use Copilot in Word to draft a management report from approved figures and verify every number.

## Scenario

The H1 FY2026 results are approved. The CFO needs a management report by tomorrow, drafted from the approved figures and nothing else.

## Files

- `northstar-report-source-starter.xlsx` - learner working file
- `northstar-report-source-solution.xlsx` - completed formulas, controls and charts for review
- `evidence-checklist.md` - submission and verification checklist
- `../_data/` - the shared Northstar finance dataset (CSV)
- `../TENANT-RESOURCES.md` - sign-in accounts, site, environment and agent links

## Before you begin

- Use only the supplied synthetic data.
- Do not enter live customer, payroll, account, credential or confidential data.
- If the required Microsoft feature is not enabled in your tenant, complete the workbook-based simulation and record the limitation.
- Keep facts, assumptions, AI suggestions and reviewer decisions visibly separate.

## Detailed procedure

### Step 1: Open the source workbook and confirm the approved control totals before you draft anything.

- Open the starter workbook and go to the Control Totals sheet.
- Note the net profit for H1 FY2026: SGD 4,767,259.38. Every figure you publish must reconcile to this.
- Read the Approved Figures and By Department sheets. These are the only numbers you may use.

Record the evidence for Step 1 in the checklist before continuing.

### Step 2: Sign in to Microsoft 365 with the Copilot licence and open a blank Word document.

- Go to m365.cloud.microsoft and sign in with the Microsoft 365 Premium account from your account card.
- Confirm the Copilot icon is present in Word. If it is not, you are signed in with the wrong account.
- Open a blank Word document.

Record the evidence for Step 2 in the checklist before continuing.

### Step 3: Use Copilot to draft the report, referencing the source workbook and stating the reporting period.

- Open Copilot in Word and choose to draft with it.
- Reference the approved workbook so Copilot draws from it rather than inventing figures.
- State the reporting period explicitly: January to June 2026, as at 30 June 2026.

Record the evidence for Step 3 in the checklist before continuing.

### Step 4: Direct the draft with a prompt that names the role, the approved source, the required sections and the tone.

- Use the prompt on the Prompt sheet of the workbook rather than a one-line request.
- It names the role, the task, the permitted source, the required sections, the controls and the output shape.
- A one-line prompt produces a plausible report. A prompt contract produces a checkable one.

Record the evidence for Step 4 in the checklist before continuing.

### Step 5: Check every figure in the draft against the workbook and correct any that do not match.

- Open the Verification Log sheet and list every figure that appears in the draft.
- Check each against the Approved Figures sheet and record match or no match.
- Copilot rounds. A rounded figure in a management report is a wrong figure: replace it with the exact one.

Record the evidence for Step 5 in the checklist before continuing.

### Step 6: Remove or label any statement of cause that the data does not support.

- Read the draft for statements of cause, not just for numbers.
- The workbook shows what changed. It does not show why. Any 'driven by' or 'due to' claim is a hypothesis.
- Either delete the claim or label it explicitly as a hypothesis to confirm with the department head.

Record the evidence for Step 6 in the checklist before continuing.

### Step 7: Save the approved report; it becomes the source for the PowerPoint lab.

- Save the corrected report. This exact file is the source for the PowerPoint lab.
- If the report is wrong, the deck generated from it will be wrong in the same way and twice as visible.

Record the evidence for Step 7 in the checklist before continuing.

## Prompt quality pattern

> Role: You are assisting a finance professional. Task: analyse only the named workbook table. Data boundary: do not use external or unstated facts. Controls: reconcile totals, identify missing evidence, and label assumptions. Output: return a concise table of finding, evidence, confidence, reviewer action and source cell or table.

## Acceptance criteria

- [ ] Every figure in the report matches the source workbook exactly; causal claims are evidenced or labelled as hypotheses; the report names its period and as-at date.
- [ ] All generated claims have been checked against the workbook or approved knowledge.
- [ ] No live credentials, personal data or confidential business data appear in the evidence.
- [ ] A human reviewer and approval status are recorded.

## Deliverable

A Word management report with every figure traced to the source workbook.

## Reflection

1. What did the AI accelerate?
2. What still required finance judgement?
3. Which control prevented the most serious failure?
4. What evidence is needed before this design can scale?

© 2026 Tertiary Infotech Academy Pte Ltd · UEN 201200696W
