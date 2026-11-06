# 01 · The framework

Three ideas: **stages** (where you are), **risk tiers** (what is allowed where) and **owners** (who decides).

## 1. Adoption stages

| Stage | Goal | You are here if... | Exit criteria |
|---|---|---|---|
| **1. Explore** | Learn safely | People use AI individually, with no shared rules | A named owner, a one-page policy, a list of approved tools |
| **2. Pilot** | Prove value on 2-3 use cases | A few use cases have a baseline and a sponsor | Measured result against baseline for each pilot; incidents reviewed |
| **3. Standardize** | Make good practice the default | Shared prompts, templates, review rules, access patterns | Policy enforced in tooling (not just in a document); training done |
| **4. Scale** | Extend to new teams and agents | Governance holds as usage grows | Regular review cycle; metrics reported to leadership |

Without a baseline you cannot show that a pilot worked, so you cannot justify moving up. Do not move up a stage without evidence that the previous one works.

## 2. Risk tiers

Classify each use case by what the AI can see and what it can change.

| Tier | Typical use | Controls required |
|---|---|---|
| **Tier 1 · Low** | Boilerplate, documentation, explaining code, generating tests on non-sensitive code | Approved tool; human reviews output; no sensitive data in prompts |
| **Tier 2 · Medium** | Drafting SQL or models against real schemas; code review assistance | Tier 1 plus: read-only or scoped access; changes go through normal review and CI; assumptions listed in writing |
| **Tier 3 · High** | Agents with direct data access, natural-language access for business users, anything with write permissions or personal data | Tier 2 plus: named owner; official metric definitions provided to the agent; column-level restrictions on personal data; logging of queries; cost limits; a verification path for answers; sign-off before launch |

Rule of thumb: a read-only connection still exposes every table it can reach, so read-only alone is not governance.

## 3. Owners

| Role | Owns |
|---|---|
| **Data leader** | The policy, the stage, the metrics, escalation |
| **Data owner (per domain)** | Metric definitions and who may see what |
| **Security / privacy contact** | Approval of tools and Tier 3 access patterns |
| **AI champions (2-4 people)** | Shared prompts, templates, answering questions, feeding back what fails |
| **Every team member** | Verifying output before it ships. Accountability for the result stays with the person, not the tool |

## 4. Design principles

1. **Humans stay accountable.** AI proposes, a named person decides.
2. **Definitions before access.** An agent that picks its own definition of "revenue" will answer confidently and may be wrong for your business.
3. **Controls in tooling, not only in documents.** If a rule matters, enforce it in permissions, CI or review templates.
4. **Measure before you push.** Baseline first, then adoption.
5. **Make failures visible.** Log incidents and near-misses; review them in the open.
