# psycho-v1

**Be crazy and lead.** Client-side tools only. No backends. No custody. No seed phrases.

I ship recovery and governance tooling for EVM networks that have actually broken in public — stuck nonces after RPC switches, two histories after a fork height, staking views that disagree, and evidence packs a holder can export without handing anyone a key.

Most of that work started on BlockDAG community chain 1404. That is domain experience, not the whole identity.

## What to look at first

| Repo | Why it exists |
|---|---|
| [splitkit](https://github.com/psycho-v1/splitkit) | Portable TypeScript kit: pin block hashes across RPC families, detect a history split, scan nonces, export an evidence JSON. Tests in CI. Not tied to chain 1404. |
| [chain1404-dao](https://github.com/psycho-v1/chain1404-dao) | Proposed dual-chamber governor. Voting weight is completed miner + staker *flow*, not raw balances. Foundry + tests. Not live. |
| [fairline-l1](https://github.com/psycho-v1/fairline-l1) | Separate open EVM L1 experiment. Not 1404. Private 3-validator devnet first. No mainnet claim until heads match. |

## 1404 rescue tools (kept, labelled)

These are static HTML/JS pages for holders on a forked book. They stay up because people still use them. They are not the portfolio.

- [kedge](https://github.com/psycho-v1/kedge) — vacate a stranded send (confirmed nonce only)
- [bdag-pending-fixer](https://github.com/psycho-v1/bdag-pending-fixer) — nonce scan + cancel/resend, safety lock against nonce gaps
- [Chain-1404-Stake-Manager](https://github.com/psycho-v1/Chain-1404-Stake-Manager) — community staking UI, halt on pin drift
- [Chain-1404-Desk](https://github.com/psycho-v1/Chain-1404-Desk) / [chain1404-evidence-pack](https://github.com/psycho-v1/chain1404-evidence-pack) — dual-history inspect + export
- [Bdag-Pool-Claim](https://github.com/psycho-v1/Bdag-Pool-Claim) — miner payout vault UI
- [chain1404-safe](https://github.com/psycho-v1/chain1404-safe) — Safe 1.4.1 factory notes for community 1404

## Rules I will not break

1. The wallet signs. This account never holds keys.
2. Community RPCs are labelled. Official / engineering endpoints are denied where the tool says so.
3. A pin (chain id, block hash at a height, implementation, owner) is a halt condition, not a warning banner.
4. Docs say what the tool is *not*: not a bank, not legal advice, not an official product.

## Contact

Telegram [@psycho_v1](https://t.me/psycho_v1)
