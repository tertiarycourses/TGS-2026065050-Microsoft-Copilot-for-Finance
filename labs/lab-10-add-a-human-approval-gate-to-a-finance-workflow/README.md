# Lab 10: Add a Human Approval Gate to a Finance Workflow

**Course:** Microsoft Copilot for Finance (TGS-2026065050)  
**Mapping:** A3  
**Suggested time:** 90 minutes  
**Objective:** Build a blocking human-in-the-loop approval gate and prove that inaction fails safe.

## Scenario

Collections wants to automate reminder drafting. Nothing may reach a customer without a person approving it first.

## Files

- `northstar-approval-gate-starter.xlsx` - learner working file
- `northstar-approval-gate-solution.xlsx` - completed formulas, controls and charts for review
- `evidence-checklist.md` - submission and verification checklist
- `flow-notes.md` - verified designer behaviour and traps
- `../TENANT-RESOURCES.md` - sign-in accounts, site, environment and agent links

## Before you begin

- Use only the supplied synthetic data.
- Do not enter live customer, payroll, account, credential or confidential data.
- If the required Microsoft feature is not enabled in your tenant, complete the workbook-based simulation and record the limitation.
- Keep facts, assumptions, AI suggestions and reviewer decisions visibly separate.

## Detailed procedure

### Step 1: Extend your flow so it drafts a payment reminder from the approved receivables data.

- Extend your flow so it drafts a payment reminder from the receivables data.
- Use the escalated accounts on the Approval Queue sheet as your test cases.

Record the evidence for Step 1 in the checklist before continuing.

### Step 2: Write the draft to an audit record before the approval gate, so the evidence exists either way.

- Write the draft to an audit record before the approval gate, not after.
- Logging before the gate is what lets someone later ask whether anything reached a customer that nobody reviewed.

Record the evidence for Step 2 in the checklist before continuing.

### Step 3: Add a Human review node and define its inputs, including an outcome and an approver name.

- Add a Human review node. It needs its own connection first: choose Not connected, then Create new connection, then Create.
- Define two inputs: Outcome as Yes/No and ApproverName as Text.
- The node will not save with zero inputs, and there is no built-in outcome property to reference.
- The type picker offers Text, Yes/No, Email, Number and Date. There is no Choice type, so put the approve/reject meaning in the Message text.

Record the evidence for Step 3 in the checklist before continuing.

### Step 4: Leave the outcome default blank so that inattention cannot become approval.

- Leave the Outcome default blank.
- A default of Approve means the field arrives already answered: confirming takes no thought and rejecting takes noticing.
- That converts a gate into a rubber stamp through a setting invisible on the canvas.

Record the evidence for Step 4 in the checklist before continuing.

### Step 5: Set the channel to Teams and address the request to a resolved directory account.

- Set the Channel to Teams.
- On a live tenant the Outlook channel created the request but never delivered it, to any address.
- For Assigned to, type the full address, wait for the directory lookup and click the resolved suggestion.

Record the evidence for Step 5 in the checklist before continuing.

### Step 6: Add an If and Else branch on the outcome and build both paths, including the rejection path.

- Add an If and Else on the Outcome, comparing against the literal Yes.
- The Yes/No input is shown as boolean in the picker but publishes the string Yes. Comparing against true never matches.
- Build the rejection branch too. An empty Else means rejecting silently does nothing.

Record the evidence for Step 6 in the checklist before continuing.

### Step 7: Publish, then run the approval path and record the evidence.

- Publish, then run the approval path and record the evidence on the Both Paths sheet.

Record the evidence for Step 7 in the checklist before continuing.

### Step 8: Run the rejection path and confirm nothing is sent and the rejection is recorded.

- Run the rejection path. Confirm nothing is sent and the rejection is recorded.
- A gate that has only ever been approved is untested.

Record the evidence for Step 8 in the checklist before continuing.

### Step 9: Compare a blank default with a pre-filled Approve default and explain the control difference.

- Complete the Default Comparison sheet.
- Explain in your own words why a blank default is a control and a pre-filled Approve is not.

Record the evidence for Step 9 in the checklist before continuing.

## Prompt quality pattern

> Role: You are assisting a finance professional. Task: analyse only the named workbook table. Data boundary: do not use external or unstated facts. Controls: reconcile totals, identify missing evidence, and label assumptions. Output: return a concise table of finding, evidence, confidence, reviewer action and source cell or table.

## Acceptance criteria

- [ ] The gate blocks until a person responds; both approval and rejection paths are evidenced; the draft is logged before the gate; the default is fail-safe and the learner can explain why.
- [ ] All generated claims have been checked against the workbook or approved knowledge.
- [ ] No live credentials, personal data or confidential business data appear in the evidence.
- [ ] A human reviewer and approval status are recorded.

## Deliverable

A workflow with a working approval gate, an audit trail and evidence of both decision paths.

## Reflection

1. What did the AI accelerate?
2. What still required finance judgement?
3. Which control prevented the most serious failure?
4. What evidence is needed before this design can scale?

© 2026 Tertiary Infotech Academy Pte Ltd · UEN 201200696W
