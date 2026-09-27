# Lab 9: Create the Environment and a Finance Agent Flow

**Course:** Microsoft Copilot for Finance (TGS-2026065050)  
**Mapping:** A3  
**Suggested time:** 120 minutes  
**Objective:** Provision a governed environment and build an agent flow that reads approved finance data.

## Scenario

Course work must be isolated from production. The finance team then wants a flow that assembles the reconciliation position on demand.

## Files

- `northstar-workflow-design-starter.xlsx` - learner working file
- `northstar-workflow-design-solution.xlsx` - completed formulas, controls and charts for review
- `evidence-checklist.md` - submission and verification checklist
- `flow-notes.md` - verified designer behaviour and traps
- `../TENANT-RESOURCES.md` - sign-in accounts, site, environment and agent links

## Before you begin

- Use only the supplied synthetic data.
- Do not enter live customer, payroll, account, credential or confidential data.
- If the required Microsoft feature is not enabled in your tenant, complete the workbook-based simulation and record the limitation.
- Keep facts, assumptions, AI suggestions and reviewer decisions visibly separate.

## Detailed procedure

### Step 1: Create a sandbox environment named for the course, in the Asia region with SGD currency.

- Open the Power Platform admin centre and create a new environment.
- Name it for the course code so it can be found and governed later.
- Choose Sandbox as the type and Asia as the region.

Record the evidence for Step 1 in the checklist before continuing.

### Step 2: Enable Dataverse, because agents and flows require it, and record the environment ID.

- Set the currency to SGD, then open Change default settings and enable the Dataverse data store.
- Agents and agent flows require Dataverse. It cannot be added quietly afterwards.
- Set the security group to None for a training cohort. That would be the wrong choice for production finance data.

Record the evidence for Step 2 in the checklist before continuing.

### Step 3: Confirm the environment is covered by a billing plan, or agents will fail with a credits error.

- Confirm the environment is a target of a billing plan.
- Without one, every agent reply fails with EnforcementUsageCredits and the cause is not visible from inside Copilot Studio.
- Record the environment ID: every Copilot Studio and admin URL contains it.

Record the evidence for Step 3 in the checklist before continuing.

### Step 4: Create an agent flow and give it a name ending in the do-not-delete marker.

- In Copilot Studio open Workflows and create one, naming it ending in (DO NOT DELETE).
- Open the trigger and change the type from Manual to When an agent calls the workflow.
- The Add-tool dialog on an agent says it outright: only workflows using that trigger are shown, and Power Automate cloud flows are not supported. Publishing alone is not enough.
- Add a typed input the agent will pass in, such as AgeingBucket as Text.

Record the evidence for Step 4 in the checklist before continuing.

### Step 5: Add a SharePoint Get items action pointing at the finance list, and set a filter query.

- Add a SharePoint Get items action.
- Pick the site from the dropdown, never a typed URL, and select the finance list.
- Build the filter query as literal text wrapping a picker token, and normalise the key inside the filter rather than after it.

Record the evidence for Step 5 in the checklist before continuing.

### Step 6: Insert every dynamic value with the picker rather than typing an expression.

- Insert every dynamic value with the lightning-bolt picker.
- Typed or pasted expressions are escaped by the editor, and a reference to a missing node resolves to empty rather than erroring.
- The node stays green and the flow returns nothing. This is the single most common failure in this designer.

Record the evidence for Step 6 in the checklist before continuing.

### Step 7: Add the flow as a tool on your agent, publishing the flow first so it becomes selectable.

- Add a Respond to the agent node and define a typed output, then bind it to the Get items Value array with the picker.
- Save, then Publish. Publishing takes 30 to 60 seconds and the status pill must read Published.
- Open your agent, choose Tools, Add a tool, then the Workflows category, and select your flow.
- Only published flows with the agent trigger appear there. Save and republish the agent afterwards.

Record the evidence for Step 7 in the checklist before continuing.

### Step 8: Test the flow, then read the run history node by node to confirm what actually executed.

- Test the flow, then open the run history and read the node outputs.
- A green run does not mean the work happened: a node left in Needs setup is skipped silently.
- Read the upstream node's outputs before proposing a second fix for any failure.

Record the evidence for Step 8 in the checklist before continuing.

## Prompt quality pattern

> Role: You are assisting a finance professional. Task: analyse only the named workbook table. Data boundary: do not use external or unstated facts. Controls: reconcile totals, identify missing evidence, and label assumptions. Output: return a concise table of finding, evidence, confidence, reviewer action and source cell or table.

## Acceptance criteria

- [ ] The environment exists with Dataverse and a billing plan; the flow is published and runs green; the run history shows the SharePoint action returning rows; the flow appears as a tool on the agent.
- [ ] All generated claims have been checked against the workbook or approved knowledge.
- [ ] No live credentials, personal data or confidential business data appear in the evidence.
- [ ] A human reviewer and approval status are recorded.

## Deliverable

A course environment and a published agent flow with documented tools and scope.

## Reflection

1. What did the AI accelerate?
2. What still required finance judgement?
3. Which control prevented the most serious failure?
4. What evidence is needed before this design can scale?

© 2026 Tertiary Infotech Academy Pte Ltd · UEN 201200696W
