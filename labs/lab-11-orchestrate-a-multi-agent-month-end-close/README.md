# Lab 11: Orchestrate a Multi-Agent Month-End Close

**Course:** Microsoft Copilot for Finance (TGS-2026065050)  
**Mapping:** K4 · A3  
**Suggested time:** 75 minutes  
**Objective:** Build a supervisor with connected specialist agents and prove the routing and the escalation.

## Scenario

Reconciliation, variance analysis and collections each need different expertise. A supervisor should route the work without ever becoming an approver.

## Files

- `northstar-multi-agent-close-starter.xlsx` - learner working file
- `northstar-multi-agent-close-solution.xlsx` - completed formulas, controls and charts for review
- `evidence-checklist.md` - submission and verification checklist
- `handoff-schema.json` - structured multi-agent handoff contract
- `../TENANT-RESOURCES.md` - sign-in accounts, site, environment and agent links

## Before you begin

- Use only the supplied synthetic data.
- Do not enter live customer, payroll, account, credential or confidential data.
- If the required Microsoft feature is not enabled in your tenant, complete the workbook-based simulation and record the limitation.
- Keep facts, assumptions, AI suggestions and reviewer decisions visibly separate.

## Detailed procedure

### Step 1: Build the specialist agents for reconciliation, variance and collections, each with a narrow scope.

- Build the three specialist agents, each with a narrow scope and an explicit prohibition.
- Use the Architecture sheet: reconciliation, variance and collections.

Record the evidence for Step 1 in the checklist before continuing.

### Step 2: Publish every specialist, because only published agents can be connected.

- Publish every specialist before going further.
- Connected agents accept published agents only. Unpublished ones simply do not appear in the picker.

Record the evidence for Step 2 in the checklist before continuing.

### Step 3: Create the supervisor agent and write instructions that make routing its job, not doing the work.

- Create the supervisor agent.
- Write instructions that make routing its job. State plainly that it does not perform the specialist work itself.

Record the evidence for Step 3 in the checklist before continuing.

### Step 4: Add each specialist as a connected agent with a routing description that says when to use it.

- Add each specialist as a connected agent.
- The description is required and it is what drives routing, so say when to use this specialist, not what it is.

Record the evidence for Step 4 in the checklist before continuing.

### Step 5: State the close sequence in the supervisor instructions so a blocked step is reported, not skipped.

- State the close sequence in the supervisor instructions.
- Reconciliation completes before variance analysis; commentary completes before controller review.
- If an earlier step is unresolved the supervisor must report the later step as blocked, not proceed without it.

Record the evidence for Step 5 in the checklist before continuing.

### Step 6: Complete the handoff contract: task, scope, source IDs, result, confidence and exceptions.

- Complete the Handoff Contract sheet.
- A handoff needs a structured payload. Prose loses precision at every hop between agents.

Record the evidence for Step 6 in the checklist before continuing.

### Step 7: Test routing with one question per specialist and confirm each reaches the right one.

- Run routing tests R01 to R04, one per specialist.
- Record which specialist actually answered. Routing is driven by your descriptions, so a miss is a description problem.

Record the evidence for Step 7 in the checklist before continuing.

### Step 8: Test a question that spans two specialists and check the supervisor keeps both answers intact.

- Run R05 and R06, which span two specialists.
- Check the supervisor keeps both sets of figures and both sets of caveats intact.

Record the evidence for Step 8 in the checklist before continuing.

### Step 9: Test a failure case where data is missing and confirm the supervisor reports the block honestly.

- Run R08, where the source data is unavailable.
- The correct behaviour is to report the block and name the missing input, never to produce a plausible number.

Record the evidence for Step 9 in the checklist before continuing.

### Step 10: Confirm no agent in the system can approve, post or send anything.

- Run R07 and confirm no agent in the system will approve, post or send anything.
- Complete the Failure Modes sheet with what you observed.

Record the evidence for Step 10 in the checklist before continuing.

## Prompt quality pattern

> Role: You are assisting a finance professional. Task: analyse only the named workbook table. Data boundary: do not use external or unstated facts. Controls: reconcile totals, identify missing evidence, and label assumptions. Output: return a concise table of finding, evidence, confidence, reviewer action and source cell or table.

## Acceptance criteria

- [ ] Each routing test reaches the correct specialist; the supervisor preserves specialist figures and caveats; a missing-data case is reported as blocked rather than answered; no agent can approve, post or send.
- [ ] All generated claims have been checked against the workbook or approved knowledge.
- [ ] No live credentials, personal data or confidential business data appear in the evidence.
- [ ] A human reviewer and approval status are recorded.

## Deliverable

A working supervisor, a handoff contract, routing tests and an escalation path.

## Reflection

1. What did the AI accelerate?
2. What still required finance judgement?
3. Which control prevented the most serious failure?
4. What evidence is needed before this design can scale?

© 2026 Tertiary Infotech Academy Pte Ltd · UEN 201200696W
