# Bounty

**Bug Bounty Board** — Public-facing issue tracker for the desktop client, overlay, and web apps.

Part of the [ComputerPets](https://github.com/RicheyWorks/computerpets) ecosystem. Index: [computerpets-ecosystem](https://github.com/RicheyWorks/computerpets-ecosystem).

> Status: **design scaffold**. This repository ships the contract, README, and layout so implementation can start without renaming the organ later.

## Why it exists

Crash logs from Forensics land here. Players file. Operators triage. Payouts (if any) go through Ledger, not a spreadsheet.

The flagship overlay already puts a living sticker on the real desktop (Rui first, 210 kinds). Bounty does not replace that. It is one organ.

## Stack

TypeScript · React 19 · GitHub Issues mirror · severity SLA · optional Ledger payouts

GroupId / namespace: `com.enterprisepet.bounty`  
Default listen: `8080`

## Talks to

- computerpets-forensics
- computerpets-console
- computerpets-sdk
- computerpets-ledger
- computerpets (issues)

## Contract

### Data

`Bounty(id, severity, rewardAsset) · Report(id, redact, logsCid) · Payout(ref)`

### Surface

- GET /v1/bounties — open, severity, reward
- POST /v1/reports — player filing (redact paths)
- POST /v1/payout — operator, Ledger ref

### Failure doctrine

PII in a log → strip before public. Duplicate hash → attach to existing. No public exploit PoC until patched.

## Layout

```
computerpets-bounty/
  README.md           this file
  LICENSE             MIT
  docs/CONTRACT.md    the same contract, frozen for implementers
  src/                implementation lands here
```

## Run (Windows)

PowerShell, from this folder, after the flagship helpers (Git, Node LTS 22+, JDK 21 as needed):

```powershell
cd app; npm install; npm run dev
```

You do not need this service to meet Rui. The [flagship start-here](https://github.com/RicheyWorks/computerpets/blob/main/docs/START-HERE.md) is still the first pet.

## Ecosystem

| Organ | Repo |
| --- | --- |
| Flagship desktop + Spring | [RicheyWorks/computerpets](https://github.com/RicheyWorks/computerpets) |
| This organ | [RicheyWorks/computerpets-bounty](https://github.com/RicheyWorks/computerpets-bounty) |
| Full map | [RicheyWorks/computerpets-ecosystem](https://github.com/RicheyWorks/computerpets-ecosystem) |

## License

MIT. See [LICENSE](LICENSE).

---

*Two hundred ten living kinds. Keep them so a line does not go quiet.*
