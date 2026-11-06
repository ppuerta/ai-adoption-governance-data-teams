# 02 · AI usage policy template (data team)

Fill in the `[brackets]`. Keep the final version to one page so people actually read it.

---

**Team:** [name]  **Owner:** [role]  **Version / date:** [ ]  **Next review:** [date, suggest quarterly]

## 1. Purpose
Allow the team to use AI tools productively while protecting data, keeping quality high and keeping people accountable for results.

## 2. Approved tools
[List tools and the account type allowed, e.g. company-managed accounts only.] Anything not on this list needs approval from [security contact].

## 3. What you can do
- Use approved tools for code drafting, documentation, tests, explanations and review support.
- Include table and column names and schemas in prompts: [yes / only for non-sensitive tables].

## 4. What needs approval first
- Connecting an AI agent directly to a data warehouse or BI tool.
- Giving any AI tool write access.
- Offering natural-language access to business users.
- Using a new AI vendor.
Approval comes from: [owner] and [security contact]. Use the checklist in `04-pre-connection-checklist.md`.

## 5. What is not allowed
- Pasting personal data, credentials, secrets or confidential customer information into a tool not approved for it.
- Merging AI-generated code without review and passing CI.
- Presenting AI output to stakeholders as verified without checking it.
- [Add your own.]

## 6. Data handling
| Data class | Allowed in AI tools? |
|---|---|
| Public | [yes] |
| Internal | [approved tools only] |
| Confidential | [no / approved tools with contract terms checked] |
| Personal data | [no, unless explicitly approved and masked] |

## 7. Quality and review
- Every AI-assisted change goes through the same review and CI as any other.
- Assumptions about metric definitions are written down and agreed with the metric owner.
- Tests for business rules are written or approved by a person who understands the rule.

## 8. Agents and data access
- Access is scoped to named schemas. Personal-data columns are excluded or masked.
- Official metric definitions are provided to the agent: [location of the definitions].
- Queries are logged. Cost limits: [set per query / per day].
- Answers that drive decisions have a verification path: [how].

## 9. Incidents
Report incidents and near-misses to [channel / person] within [timeframe]. Reports are reviewed without blame. Examples: sensitive data pasted into a tool, a wrong number shipped, an agent query that exposed restricted data.

## 10. Training and support
New joiners complete [short training] in their first [month]. Questions go to [AI champions channel].

## 11. Review
This policy is reviewed every [quarter] against incidents, metrics and changes in tools or regulation.
