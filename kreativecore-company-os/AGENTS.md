# Kreative Core Agent Instructions

Kreative Core is a multi-product digital company. This repository is not only a website; it is also the company's product catalog, documentation hub, sales interface, release surface, and operational control center.

## Required Reading

Before starting any task, read:

1. `/docs/company/KREATIVE_CORE_COMPANY_OS.md`
2. `/docs/company/ORGANIZATION.md`
3. `/docs/company/PRODUCT_PORTFOLIO.md`
4. `/docs/company/COMPANY_ROADMAP.md`
5. `/docs/company/WORKFLOW.md`
6. `/docs/company/RISK_REGISTER.md`

For payment-related work, also read:

7. `/docs/company/PAYMENT_ARCHITECTURE.md`

## Global Rules

- Inspect the repository before changing it.
- Do not assume a product is complete merely because it has a product page.
- Keep one focused task per issue and preferably one pull request per issue.
- Do not modify unrelated products or files.
- Do not rewrite working systems without a documented reason.
- Never commit API keys, private keys, wallet seed phrases, passwords, bank credentials, or customer data.
- Do not expose real customer or transaction data in the repository.
- New dependencies require justification.
- Tests, validation, and rollback considerations are required for critical changes.
- QA must be independent from implementation for release-critical work.
- Marketing claims must match technical reality.
- Payment, pricing, deployment, and public release changes require owner approval.
- Failed tests must not be described as successful.
- Blocked work must be reported clearly with the cause and next action.

## Standard Task Lifecycle

1. Understand the task and business purpose.
2. Inspect the relevant project and files.
3. Define scope and out-of-scope items.
4. Prepare an implementation plan.
5. Apply the smallest reasonable change.
6. Run available checks.
7. Compare the result with acceptance criteria.
8. Fix errors and rerun validation.
9. Submit for QA review.
10. Request owner approval where required.
11. Merge and release only after all gates pass.

## Human Approval Required

Do not activate or finalize the following without explicit approval from the owner:

- Real payment activation
- Production deployment
- Pricing changes
- Public release
- License model changes
- Large deletions
- Repository deletion
- Domain or hosting changes
- New paid services
- Legal or public claims
- Crypto payment activation
