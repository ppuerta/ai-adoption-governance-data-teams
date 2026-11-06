# 04 · Checklist before connecting an AI agent to your data

Use it before any agent, MCP connection or natural-language tool touches a warehouse. If you cannot answer an item, the answer is "not yet".

## Definitions
- [ ] The official definitions of the key metrics are written down (revenue, active customer, churn...).
- [ ] The agent receives those definitions as context. It does not choose its own.
- [ ] Each metric has an owner who can settle disputes.

## Access
- [ ] The connection is read-only and scoped to named schemas.
- [ ] Personal-data columns are excluded or masked at the database level (not just by instruction).
- [ ] Credentials are specific to this agent and can be revoked.
- [ ] Read-only was verified by attempting a write that should fail.

## Quality and verification
- [ ] A set of known questions with known answers exists, and the agent is tested against it.
- [ ] Answers that drive decisions state their assumptions and can be verified with a second path (e.g. a certified dashboard or a human check).
- [ ] You tested a question that invites a join-duplication or a wrong filter, and checked the result.

## Cost
- [ ] Query cost limits are set (bytes per query or per day).
- [ ] A dry-run or cost estimate is part of the flow for large tables.

## Traceability
- [ ] Queries and answers are logged with who asked.
- [ ] You can answer: "which data did this agent see last week?"

## Ownership and review
- [ ] A named owner is accountable for the agent.
- [ ] Incidents have a reporting path and a review.
- [ ] A review date is set (suggest quarterly).

## Evidence from a small test
In three fresh sessions with fictional order data, a read-only agent connection blocked every write attempt, and the agent did not try to get around it. In all three it returned customer emails when asked for contact details, without a warning about personal data. In an earlier run where the connector could not open the file, the agent read it through the shell instead.

Read-only limits changes. It does not limit what can be read, and a control in the connector does not bind an agent that has other tools. Three runs with one model on a small invented schema do not generalize. They are why the access section above asks for masking at database level. The dataset, steps and per-session results are in [`examples/mcp-readonly-test/`](examples/mcp-readonly-test/).
