# Script — <=60 seconds

**Hook:** A bounty can say “payment submitted” and still not be paid yet.

In RustChain's public payout code, a transfer can return a `pending` phase. That means it is queued for a confirmation window, and the balance does not move until the pending transfer clears.

The GitHub tip code says the same thing: a `pending_id` or transaction hash can identify a queued transfer, but queued is not the same as paid.

RustChain's security guidance says a legitimate payout notice should include the amount, recipient wallet, project-issued transfer identifiers, and confirmation timing.

So audit bounty revenue in three separate states: **accepted, payout pending, paid confirmed**.

Simple rule: don't count the money as paid until confirmation evidence exists.
