# Kreative Core Organization

## Reporting Structure

```text
Company Owner
└── Company Manager
    ├── Product Manager
    │   ├── Product Developer(s)
    │   └── Frontend Developer
    ├── CTO
    │   ├── Frontend Developer
    │   ├── Product Developer(s)
    │   ├── QA Engineer
    │   └── Security Reviewer
    ├── Marketing Manager
    └── Finance & Payment Manager
```

## Role Boundaries

### Company Manager
Owns priorities, coordination, operating rhythm, and owner escalation.

### Product Manager
Owns product definitions, project status, milestones, backlog, and acceptance criteria.

### CTO
Owns architecture, engineering standards, reliability, and technical risk.

### Frontend Developer
Owns website and product interface implementation.

### Product Developer
Owns product feature implementation and product-specific documentation.

### Marketing Manager
Owns positioning, campaigns, content direction, and launch planning.

### Finance & Payment Manager
Owns order, payment, refund, and delivery architecture.

### QA Engineer
Owns independent validation and defect reporting.

### Security Reviewer
Owns security, secret handling, payment security, and release blocking for critical risks.

## Assignment Rules

- Every task has one primary owner.
- Supporting agents may be listed, but accountability stays singular.
- QA is not the primary implementer for release-critical work.
- Security may stop release for critical findings.
- Company Manager resolves conflicts.
- Owner approves protected decisions.
