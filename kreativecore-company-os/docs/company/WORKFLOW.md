# Kreative Core Workflow

## Standard Flow

```text
Company analysis
↓
Project inventory
↓
Problem and opportunity discovery
↓
Prioritization
↓
Issue creation
↓
Worker assignment
↓
Branch creation
↓
Implementation
↓
Developer self-check
↓
QA review
↓
Security review when relevant
↓
Correction loop
↓
Pull request
↓
Owner approval when required
↓
Merge
↓
Deployment
↓
Post-release validation
↓
Maintenance backlog
```

## Issue Template

```md
## Goal

## Business Reason

## Scope

## Out of Scope

## Responsible Worker

## Related Product

## Relevant Files

## Dependencies

## Implementation Steps

## Acceptance Criteria

## Test Plan

## Risks

## Owner Decisions Required
```

## Assignment Rules

- UI and layout: Frontend Developer
- Product behavior: Product Developer
- Architecture: CTO
- Prioritization: Product Manager and Company Manager
- Marketing: Marketing Manager
- Payment and refund: Finance & Payment Manager
- Quality validation: QA Engineer
- Security review: Security Reviewer

## Failure Handling

1. Record the failed criterion.
2. Identify the root cause.
3. Return the task to the correct worker.
4. Apply a fix.
5. Re-run validation.
6. Change approach if the same failure repeats.
7. Mark as blocked when unresolved.
8. Document the exact blocker and required decision.

## Recurring Reviews

### Per Pull Request

- Build
- Link check
- Syntax validation
- Security and secret scan
- Scope review
- Acceptance criteria review

### Weekly

- Open issues
- Blocked tasks
- Product status
- Broken links
- Dependency risk
- Content accuracy

### Monthly

- Roadmap review
- Marketing plan
- Payment and sales review
- Product performance
- Customer feedback
- New product opportunities
