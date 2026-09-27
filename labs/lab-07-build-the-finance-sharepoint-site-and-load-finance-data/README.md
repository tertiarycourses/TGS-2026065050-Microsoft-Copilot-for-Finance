# Lab 7: Build the Finance SharePoint Site and Load Finance Data

**Course:** Microsoft Copilot for Finance (TGS-2026065050)  
**Mapping:** K1 · A3  
**Suggested time:** 120 minutes  
**Objective:** Create a governed finance site with typed lists and an approved document library.

## Scenario

Finance content is scattered across personal drives. The team needs one governed location that an agent can safely be grounded on.

## Files

- `northstar-sharepoint-build-starter.xlsx` - learner working file
- `northstar-sharepoint-build-solution.xlsx` - completed formulas, controls and charts for review
- `evidence-checklist.md` - submission and verification checklist
- `knowledge/` - the four approved finance policies
- `../_reports/` - the five period finance reports
- `../TENANT-RESOURCES.md` - sign-in accounts, site, environment and agent links

## Before you begin

- Use only the supplied synthetic data.
- Do not enter live customer, payroll, account, credential or confidential data.
- If the required Microsoft feature is not enabled in your tenant, complete the workbook-based simulation and record the limitation.
- Keep facts, assumptions, AI suggestions and reviewer decisions visibly separate.

## Detailed procedure

### Step 1: Create a team site named for the finance team and record its URL.

- Sign in to SharePoint with your tenant account.
- From the Build page choose Site, then the Standard team template.
- Name the site for the finance team, set it private, and record the resulting URL on the Site Build sheet.

Record the evidence for Step 1 in the checklist before continuing.

### Step 2: Create the Finance Policies and Finance Reports document libraries with clear descriptions.

- Create two document libraries: Finance Policies and Finance Reports.
- Give each a description that says what belongs in it. The description is what an agent sees when choosing a source.
- Keep them separate: policy changes rarely and needs version control; reports are point-in-time and are superseded each period.

Record the evidence for Step 2 in the checklist before continuing.

### Step 3: Upload the supplied policy documents and period reports.

- Upload the four policy documents to Finance Policies and the five period reports to Finance Reports.
- Upload the Word versions. Copilot Studio will not index Markdown, so a .md-only library grounds an agent on nothing.
- Check each document carries its ID, effective date and owner. A policy without an effective date cannot be cited safely.

Record the evidence for Step 3 in the checklist before continuing.

### Step 4: Create the finance lists and set every column to its correct type: currency, date, number or choice.

- Create the seven lists from the Lists sheet.
- Set every column to its correct type as you create it. Currency for money, Date for dates, Choice for controlled values.
- A number stored as text cannot be summed, filtered or charted, and the mistake is expensive to undo later.

Record the evidence for Step 4 in the checklist before continuing.

### Step 5: Import the supplied CSV data into the lists and verify the row counts.

- Import the CSV data from the labs/_data folder into the matching lists.
- Check the row counts against the Lists sheet: 240, 240, 240, 140, 33, 17 and 10.

Record the evidence for Step 5 in the checklist before continuing.

### Step 6: Reconcile the loaded data to the control totals in the data pack.

- Reconcile the loaded data on the Reconciliation sheet.
- Net profit must come to SGD 4,767,259.38 and AR outstanding to SGD 8,964,691.11.

Record the evidence for Step 6 in the checklist before continuing.

### Step 7: Review the site permissions and record who can see what, and why.

- Open the site permissions and complete the Permissions sheet.
- An agent grounded here can surface anything the asking user may already open. Broad access becomes broad disclosure.

Record the evidence for Step 7 in the checklist before continuing.

### Step 8: Note which content is sensitive enough to need a sensitivity label.

- Identify which content would need a sensitivity label in a real deployment.
- Nothing restricted is stored on this training site, and that is itself a design decision worth stating.

Record the evidence for Step 8 in the checklist before continuing.

## Prompt quality pattern

> Role: You are assisting a finance professional. Task: analyse only the named workbook table. Data boundary: do not use external or unstated facts. Controls: reconcile totals, identify missing evidence, and label assumptions. Output: return a concise table of finding, evidence, confidence, reviewer action and source cell or table.

## Acceptance criteria

- [ ] Both libraries and all seven lists exist with correct column types; row counts match the data pack; loaded data reconciles to the control totals; the permission review names each group and its justification.
- [ ] All generated claims have been checked against the workbook or approved knowledge.
- [ ] No live credentials, personal data or confidential business data appear in the evidence.
- [ ] A human reviewer and approval status are recorded.

## Deliverable

A finance site with policy and report libraries, typed lists and documented permissions.

## Reflection

1. What did the AI accelerate?
2. What still required finance judgement?
3. Which control prevented the most serious failure?
4. What evidence is needed before this design can scale?

© 2026 Tertiary Infotech Academy Pte Ltd · UEN 201200696W
