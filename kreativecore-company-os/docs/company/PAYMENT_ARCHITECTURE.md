# Kreative Core Payment Architecture

## Objective

Create a real, secure, auditable payment and delivery system with IBAN support and a compliance-gated crypto option.

## Core Principles

- Real payment data must not be committed to the repository.
- The server, not the browser, determines product price and order state.
- Customer payment claims are not sufficient proof of payment.
- Payment must be independently verified before delivery.
- Production activation requires owner approval.
- Crypto activation also requires legal and compliance approval.

## Order States

```text
created
awaiting-payment
payment-reported
under-review
paid
failed
expired
refunded
partially-refunded
cancelled
```

## Delivery States

```text
not-ready
ready
delivered
delivery-failed
revoked
```

## Required Order Fields

- Order ID
- Product
- Product version
- Customer name
- Customer email
- Company name
- Country
- Billing details
- Payment method
- Currency
- Total amount
- Created date
- Payment status
- Delivery status
- License status
- Payment reference
- Audit history

Customer and transaction data must be stored outside the public repository.

## IBAN Payment Flow

1. Customer selects a product.
2. Server creates an order.
3. Server locks price and currency.
4. Customer receives bank details and a unique payment reference.
5. Order becomes `awaiting-payment`.
6. Customer may report payment.
7. Order becomes `payment-reported`.
8. Authorized staff independently checks the bank account.
9. Order becomes `paid` or returns to review.
10. Delivery or license generation begins.
11. Customer receives delivery and support instructions.
12. Audit log is updated.

## Secure Configuration

Use environment variables or secret storage:

```text
PAYMENT_BANK_ACCOUNT_NAME
PAYMENT_BANK_NAME
PAYMENT_IBAN_TRY
PAYMENT_IBAN_EUR
PAYMENT_IBAN_USD
PAYMENT_SWIFT_CODE
PAYMENT_SUPPORT_EMAIL
```

Do not add placeholder IBANs that could be mistaken for real accounts.

## Manual Verification

The first production version may use secure manual verification.

Authorized staff must be able to:

- View pending orders
- Review payment reports
- Record verification results
- Approve or reject payment
- Add an internal note
- Trigger delivery

A receipt upload may support review but must not be treated as definitive proof.

## Crypto Option

Crypto payment remains disabled until:

- Legal review is complete
- Compliance requirements are understood
- Accounting treatment is defined
- A suitable provider or custody model is approved
- Security review is complete
- Owner approval is recorded

Suggested lifecycle:

```text
research
legal-review-required
architecture-ready
compliance-approved
owner-approved
sandbox-testing
ready-for-activation
active
suspended
```

Never commit:

- Seed phrase
- Private key
- Exchange secret
- Withdrawal key
- Recovery code

## Crypto Technical Requirements

When approved, support:

- Exact network display
- Exact amount and expiry
- QR code
- Transaction detection
- Confirmation tracking
- Underpayment and overpayment handling
- Wrong-network detection
- Transaction hash logging
- Independent blockchain/provider verification
- Refund process
- Security audit logs

## Supported Currencies

Initial evaluation:

- TRY
- EUR
- USD

Price and exchange rate must be locked server-side when the order is created.

## Delivery

After verified payment, deliver through one or more of:

- Time-limited download link
- License key
- Account entitlement
- Installation guide
- Invoice or payment receipt
- Support channel

## Refunds

Document handling for:

- Payment before delivery
- Failed delivery
- Duplicate payment
- Underpayment
- Overpayment
- Technical incompatibility
- License revocation
- Partial refund

## Production Activation Checklist

- Order system works
- Bank details are provided by the owner
- Prices are approved
- Tax and invoice method are defined
- Privacy and sales terms exist
- Security review passes
- QA passes
- Test order completes
- Delivery is verified
- Logs and backup work
- Production secrets are configured
- Owner approval is recorded
