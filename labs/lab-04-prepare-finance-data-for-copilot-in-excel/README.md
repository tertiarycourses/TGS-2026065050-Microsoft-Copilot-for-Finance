# Lab 4: Prepare Finance Data for Copilot in Excel

**Course:** Microsoft Copilot for Finance (TGS-2026065050)  
**Mapping:** K1 · A2  
**Suggested time:** 90 minutes  
**Objective:** Convert a messy finance export into an analysis-ready Excel Table with reconciled control totals.

## Scenario

The FP&A team receives a mixed-quality export from the billing system. Copilot will answer confidently on dirty data, so the data must be fixed first.

## Files

- `northstar-finance-data-readiness-starter.xlsx` - learner working file
- `northstar-finance-data-readiness-solution.xlsx` - completed formulas, controls and charts for review
- `evidence-checklist.md` - submission and verification checklist
- `../TENANT-RESOURCES.md` - sign-in accounts, site, environment and agent links

## Before you begin

- Use only the supplied synthetic data.
- Do not enter live customer, payroll, account, credential or confidential data.
- If the required Microsoft feature is not enabled in your tenant, complete the workbook-based simulation and record the limitation.
- Keep facts, assumptions, AI suggestions and reviewer decisions visibly separate.

## Detailed procedure

### Step 1: Open the starter workbook and read the data dictionary and the expected control total.

- Open the starter workbook and read the Data Dictionary sheet first.
- It states the expected type and the rule for every column. That is your definition of clean.
- Note the control totals on the Quality and Controls sheet before you change anything.

Record the evidence for Step 1 in the checklist before continuing.

### Step 2: Ask Copilot to describe the data quality issues, then verify each claim yourself.

- Open Copilot in Excel and ask it to describe the data quality issues in the Transactions sheet.
- Record what it says. Then verify each claim yourself against the actual rows.
- Copilot will answer confidently on dirty data. The point of this step is to see that happen.

Record the evidence for Step 2 in the checklist before continuing.

### Step 3: Convert the range to an Excel Table with Ctrl+T and standardise the headers.

- Select the data range and press Ctrl+T, confirming that the table has headers.
- Give the table a name in Table Design. This is the single highest-value action before using Copilot.
- A named table gives Copilot an explicit grain and column set instead of a guess.

Record the evidence for Step 3 in the checklist before continuing.

### Step 4: Correct dates, currencies and account codes without altering any transaction ID.

- Fix the seeded defects: a blank department, an invalid date, a duplicate journal ID, a blank account code, an amount stored as text, a cost with a positive sign, an impossible period and a blank amount.
- Never edit a JournalID to resolve a duplicate. Investigate which row is wrong.
- Convert text-formatted numbers to real numbers, or they will not sum.

Record the evidence for Step 4 in the checklist before continuing.

### Step 5: Add validation columns for missing keys, duplicates and sign errors.

- Build the three validation columns: required fields, duplicate check and sign check.
- The sign rule is that 4xxx accounts are positive revenue and everything else is negative cost.
- Conditional formatting will highlight the failures as you go.

Record the evidence for Step 5 in the checklist before continuing.

### Step 6: Reconcile the cleaned revenue and expense totals to the supplied control figures.

- Reconcile the cleaned revenue and cost totals to the Quality and Controls sheet.
- Net profit must equal SGD 4,767,259.38. If it does not, a row is still wrong or has been lost.
- Row count must be unchanged. Cleaning never deletes rows.

Record the evidence for Step 6 in the checklist before continuing.

### Step 7: Repeat your first Copilot question on the cleaned table and compare the two answers.

- Ask Copilot your original question again, now on the clean table.
- Record both answers side by side on the Copilot Comparison sheet.
- The gap between them is the lesson: the tool did not change, the data did.

Record the evidence for Step 7 in the checklist before continuing.

## Prompt quality pattern

> Role: You are assisting a finance professional. Task: analyse only the named workbook table. Data boundary: do not use external or unstated facts. Controls: reconcile totals, identify missing evidence, and label assumptions. Output: return a concise table of finding, evidence, confidence, reviewer action and source cell or table.

## Acceptance criteria

- [ ] Duplicate count is zero, required-field errors are zero, cleaned totals reconcile to the control figures, and the before-and-after Copilot answers are documented.
- [ ] All generated claims have been checked against the workbook or approved knowledge.
- [ ] No live credentials, personal data or confidential business data appear in the evidence.
- [ ] A human reviewer and approval status are recorded.

## Deliverable

A clean transactions table, a quality log and reconciled control totals.

## Reflection

1. What did the AI accelerate?
2. What still required finance judgement?
3. Which control prevented the most serious failure?
4. What evidence is needed before this design can scale?

© 2026 Tertiary Infotech Academy Pte Ltd · UEN 201200696W
