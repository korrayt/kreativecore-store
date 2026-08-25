# Kreative Core Risk Register

| ID | Risk | Category | Likelihood | Impact | Owner | Mitigation | Status |
|---|---|---|---|---|---|---|---|
| R-001 | Product pages may claim capabilities not backed by working code | Product / Reputation | Medium | High | Product Manager | Verify product readiness against code, install, test, and release evidence | Open |
| R-002 | Secrets or payment credentials may be committed | Security | Medium | Critical | Security Reviewer | Secret scanning, environment variables, repository rules | Open |
| R-003 | IBAN payment may be approved without independent verification | Finance / Fraud | Medium | High | Finance & Payment Manager | Manual bank verification and audit log | Open |
| R-004 | Crypto payment may conflict with applicable law or compliance duties | Legal / Compliance | Medium | Critical | Company Manager | Keep disabled until professional review and owner approval | Open |
| R-005 | Customer data may be stored in the public repository | Privacy | Low | Critical | Security Reviewer | Store data outside GitHub; document retention and access rules | Open |
| R-006 | Website and product code may diverge | Product / Technical | High | High | CTO | Release checklist linking claims to product evidence | Open |
| R-007 | Deployment may fail without rollback | DevOps | Medium | High | CTO | Validate deployment, preserve previous release, document rollback | Open |
| R-008 | Marketing may publish unsupported claims | Reputation | Medium | High | Marketing Manager | Product and QA sign-off on capability claims | Open |
| R-009 | A single large agent task may create unrelated changes | Operations | High | Medium | Company Manager | Small issues, clear ownership, scope review | Open |
| R-010 | Payment activation before tax, invoice, or refund setup | Finance / Legal | Medium | High | Finance & Payment Manager | Production activation checklist and owner approval | Open |

## Risk Handling Rules

- Critical risks may block release.
- Every open high or critical risk must have an owner.
- Accepted risks require owner approval and a recorded reason.
- Closed risks must include evidence of mitigation.
