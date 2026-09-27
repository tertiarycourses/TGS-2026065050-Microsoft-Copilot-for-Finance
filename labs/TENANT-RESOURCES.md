# Tenant resources — TGS-2026065050 Microsoft Copilot for Finance

Everything below was provisioned on the Tertiary Infotech tenant on 6 September 2026
and is used by the labs. **All finance data is synthetic.**

---

## 1. Learner sign-in

| Purpose | Account | Password | Portal |
|---|---|---|---|
| Tenant account 1 (SharePoint, Copilot Studio) | training1@tertiaryinfotech.onmicrosoft.com | Trainer will provide | https://m365.cloud.microsoft/ |
| Tenant account 2 (SharePoint, Copilot Studio) | training2@tertiaryinfotech.onmicrosoft.com | Trainer will provide | https://m365.cloud.microsoft/ |
| M365 Premium — Office 365 + Copilot 365 (6 pax) | training1-tertiary@outlook.com | Trainer will provide | https://m365.cloud.microsoft/ |
| M365 Premium — Office 365 + Copilot 365 (6 pax) | training2-tertiary@outlook.com | Trainer will provide | https://m365.cloud.microsoft/ |
| Trainer / admin (site and environment owner) | admin@tertiaryinfotech.onmicrosoft.com | Trainer will provide | https://m365.cloud.microsoft/ |

> Passwords are held by the trainer and in the repository `.env`, which is gitignored
> and never published. They are deliberately not printed in any distributed courseware.

**Which account when.** The **M365 Premium** accounts carry the Copilot 365 licence
used for Copilot in Word, Excel and PowerPoint (Topics 1 and 2). The **tenant**
accounts are used for SharePoint, Copilot Studio and the agents (Topics 3 to 6).

---

## 2. SharePoint — TGS-2026065050 Northstar Finance

**Site:** "TGS-2026065050 Northstar Finance" — https://tertiaryinfotech.sharepoint.com/sites/NorthstarFinance
Team site, private, M365 group `NorthstarFinance`. Members: training1, training2.
Owner: admin.

> **Open the site by URL the first time.** A private team site does not appear in
> "My sites" until the account follows it, so a learner who goes looking for it in
> the SharePoint site list will not find it and will assume they were left out.
> Both learner accounts have been set to follow this site, but if a learner still
> cannot see it: open the URL above, then click the star (**Follow**) in the top
> right. Verified 7 Sep 2026 — training1 and training2 each open the site and read
> both document libraries.

### Document libraries

| Library | Contents |
|---|---|
| **Finance Policies** | 4 approved policies — the agents' knowledge source |
| **Finance Reports** | 5 period reports — P&L, AR ageing, bank reconciliation, forecast, pipeline |

**Finance Policies**

| Document | ID | Effective | Owner |
|---|---|---|---|
| Expense and Claims Policy | POL-FIN-001 | 1 Jan 2026 | Financial Controller |
| Month-End Close Calendar and Controls | POL-FIN-002 | 1 Jan 2026 | Financial Controller |
| Delegation of Authority | POL-FIN-003 | 1 Mar 2026 | Chief Financial Officer |
| AI Usage and Data Handling Policy | POL-FIN-004 | 1 May 2026 | CFO and DPO |

**Finance Reports**

| Document | ID | Covers |
|---|---|---|
| Profit and Loss Report H1 FY2026 | RPT-FIN-001 | Actual vs budget by month, department and account; material variances |
| Accounts Receivable Ageing Report | RPT-FIN-002 | Ageing profile and 33 invoices ranked by value |
| Bank Reconciliation Working Paper | RPT-FIN-003 | 17 bank lines pre-classified against the policy match rules |
| H2 FY2026 Rolling Forecast | RPT-FIN-004 | Base, downside and upside by month and department |
| Sales Pipeline Report | RPT-FIN-005 | Pipeline by stage and the 20 largest open opportunities |

### Lists

| List | Rows | Used in |
|---|---|---|
| GL Transactions | 240 | Topics 2, 3 |
| PL Monthly | 240 | Topics 2, 3, 5 |
| Forecast | 240 | Topics 2, 3 |
| Sales Pipeline | 140 | Topics 2, 3 |
| Collections AR | 33 | Topics 3, 4, 5 |
| Bank Statement | 17 | Topics 3, 4, 5 |
| Chart of Accounts | 10 | Reference |

**Control totals — every artefact reconciles to these:**

| Measure | Value (SGD) |
|---|---|
| GL revenue | 30,402,639.18 |
| GL cost | -25,635,379.80 |
| **Net profit H1 FY2026** | **4,767,259.38** |
| AR outstanding at 30 Jun 2026 | 8,964,691.11 |

---

## 3. Microsoft 365 Copilot agent (Topic 1)

**Northstar Finance Helper** — built with the SharePoint Agent builder, grounded on
the whole Northstar Finance site. No code, and it answers with citations.

Open: https://m365.cloud.microsoft/chat/agent/SPO_NDA5YzM3NGEtYWEzMi00YTQ1LTllMzMtYWVlYjgyMjNiODU1LGJjYjJhYmUyLTA4YjEtNGJmMi1hMWQ1LWU0MDNiNGMzNWE0YywxOWQxZDY4YS1kYTM3LTRjZmItYjk0YS1lNTMwMmMxYmY4N2U_01LGABAFS3ZHCKGWWC3JE3Y5QSEEGW56BE

> Access: the agent is stored as `Northstar Finance Helper.agent` in the admin
> OneDrive. Learners open it from **m365.cloud.microsoft → Agents**, or the trainer
> shares the file. Learners also rebuild it themselves in Lab 3, which takes about
> five minutes.

Starter prompts configured on the agent:
- Who approves an expense claim of SGD 5,000 and when is it due?
- What are the month-end close deadlines and who signs off?
- Which receivables are escalated and what is the write-off authority?

**Verified answer** (6 Sep 2026): asked the first prompt, it cited
`expense-and-claims-policy` POL-FIN-001 effective 1 January 2026, gave Financial
Controller for the SGD 2,000.01–10,000 band, the 30-day submission deadline, the
60-day and 90-day rules, and noted that self-approval is prohibited.

---

## 4. Power Platform environment (Topics 4 to 6)

| Property | Value |
|---|---|
| Name | TGS-2026065050-Generative AI for Finance and Fintech |
| Environment ID | 872e83cc-2c96-e481-9a43-069264e5c999 |
| Type / region / currency | Sandbox / Asia / SGD |
| Dataverse | Enabled |
| Access | Open to the tenant (no security group) |

Copilot Studio: https://copilotstudio.microsoft.com/environments/872e83cc-2c96-e481-9a43-069264e5c999/home

> **Copilot Credits.** The tenant holds no prepaid credits; it bills through the
> pay-as-you-go plan `CopilotStudioPAYGTraining`. This environment has been added to
> that plan. If an agent replies *"This environment is out of credits"*
> (`EnforcementUsageCredits`), check the environment is still a target of the plan
> under **Power Platform admin centre → Licensing → Billing plans**.

---

## 5. Copilot Studio agents (Topics 4 and 5)

All five are **published**, grounded on SharePoint, with web search removed and an
explicit "I do not approve anything" boundary.

| Agent | Purpose | Direct link |
|---|---|---|
| Finance Policy Assistant | Policy Q&A with citations and refusals | [open](https://copilotstudio.microsoft.com/environments/872e83cc-2c96-e481-9a43-069264e5c999/agents/4304a810-8996-4817-aee9-a622d908d8b1) |
| Close Reconciliation Agent | Bank/AR matching, exceptions, escalation | [open](https://copilotstudio.microsoft.com/environments/872e83cc-2c96-e481-9a43-069264e5c999/agents/25a9fe16-ebbd-4cce-a822-034537d6bea1) |
| Collections Assistant | Ageing triage and DRAFT reminders for approval | [open](https://copilotstudio.microsoft.com/environments/872e83cc-2c96-e481-9a43-069264e5c999/agents/99d4f082-12f0-4662-b8db-ec2283221649) |
| FPA Variance Analyst | Material variances and management commentary | [open](https://copilotstudio.microsoft.com/environments/872e83cc-2c96-e481-9a43-069264e5c999/agents/897bb9d6-ffd1-4979-8955-56e90e073b31) |
| **Month End Close Supervisor** | Routes to the four specialists above | [open](https://copilotstudio.microsoft.com/environments/872e83cc-2c96-e481-9a43-069264e5c999/agents/f4421bf6-28b6-49fd-9813-75b51421db69) |

The supervisor holds all four as **connected agents**, each with a routing
description. That is the Topic 5 multi-agent system.

> These links open the **maker** view and need a Copilot Studio maker role. To give
> learners a chat-only surface, publish an agent to a channel (Teams, or a demo
> website under *Settings → Security → Authentication*). Choosing that setting for
> finance content is itself a Topic 6 lab.

---

## 5a. Copilot Studio workflows (Topic 4)

Two reference workflows are published in the course environment. Both carry the
**(DO NOT DELETE)** suffix so they survive environment tidy-ups.

| Workflow | Trigger | What it does | Link |
|---|---|---|---|
| **Collections Reminder Approval (DO NOT DELETE)** | Manual, input `InvoiceID` | Reads the invoice from Collections AR, then holds it at a **Human review** gate before anything can be sent | [open](https://copilotstudio.microsoft.com/environments/872e83cc-2c96-e481-9a43-069264e5c999/flows/ed3b6c1e-2a6a-b428-b6f7-ee840f89dc6a) |
| **Bank Reconciliation Lookup (DO NOT DELETE)** | When an agent calls the workflow, input `AgeingBucket` | Returns the invoices in an ageing bucket to the calling agent as a typed output | [open](https://copilotstudio.microsoft.com/environments/872e83cc-2c96-e481-9a43-069264e5c999/flows/b9b9030c-b84c-87b6-a553-158336af6b85) |

**Collections Reminder Approval** is the Lab 10 reference build:

- SharePoint **Get items** on Collections AR, filter query `Title eq '<InvoiceID token>'`,
  top count 1. The filter is literal text wrapping a **picker** token, never a typed expression.
- **Human review** node: channel **Teams** (the Outlook channel creates the request but does
  not deliver it), assigned to a resolved directory account, with two inputs —
  `Outcome` (Yes/No) and `ApproverName` (Text). **Both defaults are left blank** so that
  inattention results in rejection, never approval.
- **If/Else** on `Outcome` **Equals `Yes`** — the string, not boolean true. The picker shows
  the Yes/No input as boolean, but it publishes `Yes`.

**Bank Reconciliation Lookup** is the Lab 9 reference build, and it is attached as a **tool**
on the Close Reconciliation Agent. The Add-tool dialog states the rule plainly:

> Only workflows that use the "When an agent calls the workflow" trigger are shown.
> Power Automate cloud flows are not supported.

So the trigger type is what makes a flow usable as a tool. Publishing is necessary but not
sufficient.

## 6. Known behaviour worth teaching

- **Copilot Studio does not index Markdown.** This cost an hour and a half to find.
  The knowledge source reported *Status: Ready* and every search returned nothing.
  The same documents as `.docx` answered immediately. Microsoft 365 Copilot agents
  index `.md` perfectly well, which is why one surface worked and the other did not.
  Both formats are now in the libraries; point any Copilot Studio knowledge source
  at the Word versions.
- **Grounded agents refuse rather than guess.** While the source was un-indexed,
  every agent said it could not retrieve anything and declined to invent a
  threshold. That is the designed control working, not a fault.
- **Indexing is not instant.** A new SharePoint site takes 30 to 60 minutes to reach
  tenant search, and a Copilot Studio knowledge source is indexed separately again.
  The M365 Copilot agent picked the documents up noticeably sooner.
- **SharePoint knowledge reads documents, not list rows.** That is why the finance
  data is published both as lists (for Excel and flows) and as reports (for agents).
- **Connected agents accept published agents only.** Publish the specialists before
  building the supervisor.
- **A default value can undo a control.** A Human review node defaulting to Approve
  turns a gate into a rubber stamp, and the canvas looks identical either way.
- **The policy set contains a deliberate conflict.** POL-FIN-001 puts an SGD 5,000
  claim with the Financial Controller; POL-FIN-003 allows a department head up to
  SGD 5,000. The Finance Policy Assistant found this unprompted and escalated rather
  than choosing a side. Keep it: an agent that quietly picks one is more dangerous
  than one that refuses, and Topic 3 teaches exactly that.

---

© 2026 Tertiary Infotech Academy Pte Ltd · UEN 201200696W
