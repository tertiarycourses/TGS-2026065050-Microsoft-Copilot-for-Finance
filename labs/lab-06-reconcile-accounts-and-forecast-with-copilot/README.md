# Lab 6: Reconcile Accounts and Forecast with Copilot

**Course:** Microsoft Copilot for Finance (TGS-2026065050)  
**Mapping:** K1 · A2  
**Suggested time:** 120 minutes  
**Objective:** Apply deterministic matching rules and build a driver-based forecast with scenarios.

## Scenario

The controller must reconcile the bank statement to the receivables ledger and produce a defensible H2 forecast.

## Files

- `northstar-reconciliation-forecast-starter.xlsx` - learner working file
- `northstar-reconciliation-forecast-solution.xlsx` - completed formulas, controls and charts for review
- `evidence-checklist.md` - submission and verification checklist
- `../_data/` - the shared Northstar finance dataset (CSV)
- `../TENANT-RESOURCES.md` - sign-in accounts, site, environment and agent links

## Before you begin

- Use only the supplied synthetic data.
- Do not enter live customer, payroll, account, credential or confidential data.
- If the required Microsoft feature is not enabled in your tenant, complete the workbook-based simulation and record the limitation.
- Keep facts, assumptions, AI suggestions and reviewer decisions visibly separate.

## Detailed procedure

### Step 1: Review the bank and receivables tables and the match rules from the close policy.

- Read the Match Rules sheet. The four classifications come from POL-FIN-002 and are not negotiable.
- Note the escalation rule: above SGD 10,000 or older than 60 days goes to the Financial Controller.

Record the evidence for Step 1 in the checklist before continuing.

### Step 2: Apply exact, tolerance and reference-only match logic in the matching sheet.

- Work through the Bank Statement sheet and classify each line.
- Exact means amount and reference both agree. Tolerance means the amount differs by SGD 50 or less.
- Reference-only means the amount agrees but the narrative lost the invoice ID; it always needs reviewer confirmation.

Record the evidence for Step 2 in the checklist before continuing.

### Step 3: Classify every remaining line as an exception, with an age and an owner.

- Everything that is not a match is an exception. Give each one an age and a named owner.
- Bank-only items such as charges, FX adjustments and returned payments are exceptions, not noise.

Record the evidence for Step 3 in the checklist before continuing.

### Step 4: Confirm matched plus exception values reconcile to each source total.

- On the Reconciliation sheet, confirm that lines classified equals bank lines.
- An unclassified line is not a clean reconciliation; it is an unfinished one.

Record the evidence for Step 4 in the checklist before continuing.

### Step 5: Build the forecast from assumption cells for volume, price and cost, never hard-coded outputs.

- Move to the Forecast Assumptions sheet and set the driver cells.
- Every forecast figure must reference an assumption cell. A hard-coded output cannot be re-run.

Record the evidence for Step 5 in the checklist before continuing.

### Step 6: Create base, downside and upside scenarios by changing assumptions coherently.

- Build the base, downside and upside scenarios on the Forecast sheet.
- Change assumptions coherently: a downside that cuts revenue but leaves costs untouched is not a scenario, it is an error.

Record the evidence for Step 6 in the checklist before continuing.

### Step 7: Ask Copilot to summarise the reconciliation and the forecast, then verify every figure it states.

- Ask Copilot to summarise the reconciliation and the forecast.
- Verify every figure it states against your own sheets before you accept the summary.

Record the evidence for Step 7 in the checklist before continuing.

## Prompt quality pattern

> Role: You are assisting a finance professional. Task: analyse only the named workbook table. Data boundary: do not use external or unstated facts. Controls: reconcile totals, identify missing evidence, and label assumptions. Output: return a concise table of finding, evidence, confidence, reviewer action and source cell or table.

## Acceptance criteria

- [ ] Matched plus exception values reconcile to both sources; every unresolved item has a reason, age and owner; scenarios are driven by assumption cells; escalation items above the policy threshold are flagged.
- [ ] All generated claims have been checked against the workbook or approved knowledge.
- [ ] No live credentials, personal data or confidential business data appear in the evidence.
- [ ] A human reviewer and approval status are recorded.

## Deliverable

A reconciliation report with an owned exception queue and a base, downside and upside forecast.

## Reflection

1. What did the AI accelerate?
2. What still required finance judgement?
3. Which control prevented the most serious failure?
4. What evidence is needed before this design can scale?

© 2026 Tertiary Infotech Academy Pte Ltd · UEN 201200696W
