# Sources

Pinned upstream commit:

`3e52ed6afbecffc708223fd4dd88be64f3742362`

Repository:
https://github.com/Scottcjn/rustchain-bounties

## Claim map

### 1. Transfers can be two-phase and pending before settlement

Source:
https://github.com/Scottcjn/rustchain-bounties/blob/3e52ed6afbecffc708223fd4dd88be64f3742362/scripts/bounty_payout.py

Relevant published behavior:
- transfer may return `phase="pending"`
- pending has a confirmation window
- the balance does not move until the pending transfer clears
- code distinguishes `queued` from `settled`

### 2. pending_id / tx_hash do not by themselves mean paid

Source:
https://github.com/Scottcjn/rustchain-bounties/blob/3e52ed6afbecffc708223fd4dd88be64f3742362/github-tip-bot/tip.js

Relevant published behavior:
- the transfer response exposes `tx_hash`, `pending_id`, and `phase`
- the source comment explicitly distinguishes queued/pending from paid

### 3. Legitimate payout evidence requirements

Source:
https://github.com/Scottcjn/rustchain-bounties/blob/3e52ed6afbecffc708223fd4dd88be64f3742362/SECURITY.md

Section:
`What a real payment looks like`

Relevant published guidance:
- amount
- recipient wallet
- project-issued transfer identifiers such as `pending_id` / `tx_hash`
- confirmation timing
- unauthorized comments must not be treated as payment confirmation

### 4. Issue #16601 reward and submission rules

Source:
https://github.com/Scottcjn/rustchain-bounties/issues/16601

Package C:
- Shorts / clip kit
- base reward: 15 RTC
- <=60 seconds
- script + vertical-format visuals or exact capture instructions + hook + metadata
- public GitHub repo delivery
- maintainer acceptance required before payout
