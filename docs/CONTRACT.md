# Bounty contract

Do not implement against folklore. Implement against this file.

## Identity

- Product: **Bounty**
- Repo: `computerpets-bounty`
- Category: Community
- Idea: Bug Bounty Board
- Port / surface: `8080`

## Must

- Stay canon with 210 species. No illegal hybrids. No swapped voices.
- Treat the desktop overlay as the main quest. This organ is optional until wired.
- Fail soft: the overlay keeps walking if this service is down, unless this *is* the overlay.
- No PII in public artifacts (Steam id, wallet, home path, webcam frames).

## Data

Bounty(id, severity, rewardAsset) · Report(id, redact, logsCid) · Payout(ref)

## Surface

- GET /v1/bounties — open, severity, reward
- POST /v1/reports — player filing (redact paths)
- POST /v1/payout — operator, Ledger ref

## Neighbors

- computerpets-forensics
- computerpets-console
- computerpets-sdk
- computerpets-ledger
- computerpets (issues)

## Failure doctrine

PII in a log → strip before public. Duplicate hash → attach to existing. No public exploit PoC until patched.

## Stack

TypeScript · React 19 · GitHub Issues mirror · severity SLA · optional Ledger payouts
