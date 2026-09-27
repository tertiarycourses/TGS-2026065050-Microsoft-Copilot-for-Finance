# Lab 5: Analyse Variances and Build a Dashboard with Copilot

**Course:** Microsoft Copilot for Finance (TGS-2026065050)  
**Mapping:** K1 · A2  
**Suggested time:** 150 minutes  
**Objective:** Use Copilot in Excel to analyse budget variances and build an auditable management dashboard.

## Scenario

Northstar's CFO needs a monthly performance dashboard and commentary that survives scrutiny in the board meeting.

## Files

- `northstar-fpa-dashboard-starter.xlsx` - learner working file
- `northstar-fpa-dashboard-solution.xlsx` - completed formulas, controls and charts for review
- `evidence-checklist.md` - submission and verification checklist
- `../_data/` - the shared Northstar finance dataset (CSV)
- `../TENANT-RESOURCES.md` - sign-in accounts, site, environment and agent links

## Before you begin

- Use only the supplied synthetic data.
- Do not enter live customer, payroll, account, credential or confidential data.
- If the required Microsoft feature is not enabled in your tenant, complete the workbook-based simulation and record the limitation.
- Keep facts, assumptions, AI suggestions and reviewer decisions visibly separate.

## Detailed procedure

### Step 1: Review the Actuals, Budget and Assumptions tables and confirm they are proper Excel Tables.

- Open the workbook and confirm the Actuals, Budget and Assumptions ranges are proper Excel Tables.
- If any is a plain range, convert it with Ctrl+T before continuing.

Record the evidence for Step 1 in the checklist before continuing.

### Step 2: Ask Copilot to generate the SUMIFS, XLOOKUP and IFERROR formulas in the Analysis sheet.

- Ask Copilot to build the department summary using SUMIFS against the PL Data table.
- Ask for XLOOKUP where you need a mapped dimension, and IFERROR to handle blanks explicitly.

Record the evidence for Step 2 in the checklist before continuing.

### Step 3: Audit every generated formula: check ranges, absolute references and blank handling.

- Audit every generated formula before you trust it.
- Check the ranges cover the whole table, check absolute references are anchored, and test what happens on a blank.
- A generated formula is a proposal. It deserves the same audit as one a colleague wrote.

Record the evidence for Step 3 in the checklist before continuing.

### Step 4: Apply the materiality rule from the close policy and identify the material variances.

- Apply the materiality rule from POL-FIN-002: greater than SGD 50,000 or 10% of budget, whichever is lower.
- Flag the material lines. Aggregate the rest rather than listing them.

Record the evidence for Step 4 in the checklist before continuing.

### Step 5: Ask Copilot to create charts, then choose the chart type that matches the claim you are making.

- Ask Copilot to create charts, then decide whether the chart type matches the claim.
- Columns compare periods, lines show trend, and a waterfall shows a bridge. A pie chart shows almost nothing useful in finance.

Record the evidence for Step 5 in the checklist before continuing.

### Step 6: Build KPI tiles linked to the Analysis table, never to typed-in values.

- Build the KPI tiles on the Dashboard sheet as formulas referencing the Analysis table.
- Never type a value into a tile. A typed tile is correct exactly once, and then silently wrong forever.

Record the evidence for Step 6 in the checklist before continuing.

### Step 7: Ask Copilot to draft commentary, then delete every causal claim the data does not evidence.

- Ask Copilot to draft the commentary, then read it as a sceptic.
- Delete every causal claim the data does not evidence, or relabel it as a hypothesis with an owner to confirm it.
- Record the result on the Commentary sheet, separating fact from hypothesis in the dedicated column.

Record the evidence for Step 7 in the checklist before continuing.

### Step 8: Run the formula error scan and reconcile the dashboard to the control totals.

- Run a formula error scan across the workbook and resolve every error.
- Reconcile the dashboard KPI tiles to the control totals. The Reconciles column must read OK on every row.

Record the evidence for Step 8 in the checklist before continuing.

## Prompt quality pattern

> Role: You are assisting a finance professional. Task: analyse only the named workbook table. Data boundary: do not use external or unstated facts. Controls: reconcile totals, identify missing evidence, and label assumptions. Output: return a concise table of finding, evidence, confidence, reviewer action and source cell or table.

## Acceptance criteria

- [ ] All formula checks pass; total variance equals actual less budget; charts stay linked to source data; commentary separates evidenced fact from labelled hypothesis.
- [ ] All generated claims have been checked against the workbook or approved knowledge.
- [ ] No live credentials, personal data or confidential business data appear in the evidence.
- [ ] A human reviewer and approval status are recorded.

## Deliverable

An editable dashboard with actual, budget, variance and forecast views plus verified commentary.

## Reflection

1. What did the AI accelerate?
2. What still required finance judgement?
3. Which control prevented the most serious failure?
4. What evidence is needed before this design can scale?

© 2026 Tertiary Infotech Academy Pte Ltd · UEN 201200696W
