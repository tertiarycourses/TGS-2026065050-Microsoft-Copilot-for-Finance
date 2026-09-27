# Labs - Microsoft Copilot for Finance

Course: TGS-2026065050

All 12 labs use one synthetic Northstar Finance scenario and build on each other: the report you verify in Lab 2 becomes the deck in Lab 3, the site you build in Lab 7 grounds the agent in Lab 8, and the specialists you publish in Lab 11 are orchestrated by a supervisor.

Detailed step-by-step procedures are in the Learner Guide. Each lab folder holds a starter workbook, a solution workbook, a README and an evidence checklist.

## Before you start

- Read [TENANT-RESOURCES.md](TENANT-RESOURCES.md) for your sign-in accounts, the SharePoint site, the Power Platform environment and the agent links. Your trainer will give you the passwords.
- All finance data is synthetic. Never substitute live customer, payroll or account data.
- Every artefact reconciles to net profit **SGD 4,767,259.38** for H1 FY2026. If your numbers disagree, something is wrong.

## Shared data

- `_data/` - the finance dataset as CSV (general ledger, P&L, forecast, sales, collections, bank, chart of accounts)
- `_knowledge/` - the four approved finance policies the agents are grounded on
- `_reports/` - the five period finance reports the agents retrieve
- `control-totals.json` in `_data/` - the figures every lab must reconcile to

## The labs

- [Lab 1: Compare Generative, Agentic and Agent AI for Finance](lab-01-compare-generative-agentic-and-agent-ai-for-finance/README.md) - K2 · A1
- [Lab 2: Draft a Financial Report with Copilot in Word](lab-02-draft-a-financial-report-with-copilot-in-word/README.md) - K2 · A1
- [Lab 3: Build a Financial Presentation and an M365 Finance Agent](lab-03-build-a-financial-presentation-and-an-m365-finance-agent/README.md) - K2 · A1
- [Lab 4: Prepare Finance Data for Copilot in Excel](lab-04-prepare-finance-data-for-copilot-in-excel/README.md) - K1 · A2
- [Lab 5: Analyse Variances and Build a Dashboard with Copilot](lab-05-analyse-variances-and-build-a-dashboard-with-copilot/README.md) - K1 · A2
- [Lab 6: Reconcile Accounts and Forecast with Copilot](lab-06-reconcile-accounts-and-forecast-with-copilot/README.md) - K1 · A2
- [Lab 7: Build the Finance SharePoint Site and Load Finance Data](lab-07-build-the-finance-sharepoint-site-and-load-finance-data/README.md) - K1 · A3
- [Lab 8: Ground a Finance Agent and Test Its Refusals](lab-08-ground-a-finance-agent-and-test-its-refusals/README.md) - K1 · A3
- [Lab 9: Create the Environment and a Finance Agent Flow](lab-09-create-the-environment-and-a-finance-agent-flow/README.md) - A3
- [Lab 10: Add a Human Approval Gate to a Finance Workflow](lab-10-add-a-human-approval-gate-to-a-finance-workflow/README.md) - A3
- [Lab 11: Orchestrate a Multi-Agent Month-End Close](lab-11-orchestrate-a-multi-agent-month-end-close/README.md) - K4 · A3
- [Lab 12: Secure a Finance Agent for PDPA and Human Oversight](lab-12-secure-a-finance-agent-for-pdpa-and-human-oversight/README.md) - K3 · A4 · A5
