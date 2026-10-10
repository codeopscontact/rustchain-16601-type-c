# Storyboard — 9:16 vertical, <=60s

No fabricated terminal output. All code captures must come from the pinned public source commit in `SOURCES.md`.

## 0:00–0:05 — Hook

**Visual**
Large typography:
`RTC QUEUED ≠ CONFIRMED`

Small footer:
`RustChain bounty payout states`

**Voice**
“An RTC bounty transfer can be queued and still not confirmed.”

## 0:05–0:17 — Two-phase payout

**Capture**
Open `scripts/bounty_payout.py` at the pinned commit.
Frame the comment beginning:
`Transfers are two-phase`

Then frame:
`phase=="pending"`
and the queued state text.

**Voice**
“In RustChain's public payout code, a transfer can return a pending phase…”

## 0:17–0:29 — Queued is not settled

**Capture**
Stay on `scripts/bounty_payout.py`.
Highlight the source statement that the balance moves when the confirmation window clears.

**On-screen labels**
`QUEUED`
↓
`CONFIRMATION WINDOW`
↓
`SETTLED`

Do not show a made-up pending ID or transaction hash.

## 0:29–0:40 — Second source

**Capture**
Open `github-tip-bot/tip.js` at the pinned commit.
Highlight the source comment:
`pending_id/tx_hash mean QUEUED ... not paid`

**Voice**
“The GitHub tip code says the same thing…”

## 0:40–0:51 — What counts as confirmed RTC transfer evidence

**Capture**
Open `SECURITY.md`, section `What a real payment looks like`.

Highlight only the published requirements:
- amount
- recipient wallet
- project-issued transfer identifiers
- confirmation timing

## 0:51–0:59 — Close

**Visual**
Three stacked states:

`ACCEPTED`
→ `RTC PENDING`
→ `RTC CONFIRMED`

Final line:
`Don't count pending RTC as confirmed.`

**Voice**
“So audit bounty revenue in three separate states…”
