# Carneyology-1

Public source repository for **Carneyology**, Prime Rogue Inc.'s series on Prime Minister Mark Carney. Series page: https://primerogueinc.com/blog/category/series/carneyology/

## Contents

| Path | What it is |
|---|---|
| `sources/sources.md` | Every source consulted, grouped by topic, with retrieval dates |
| `research/01-pco-briefing-admiralty-assessment.md` | Pre-announcement, Admiralty-graded assessment of the Oct. 29, 2026 PCO national security briefing |
| `research/02-nss-backgrounder.md` | Backgrounder on Canada's National Security Strategy: 2004 policy, run-up, allied comparisons, transparency benchmarks |
| `SHA256SUMS` | SHA-256 checksum of every file in the repo |
| `SHA256SUMS.ots` | OpenTimestamps proof anchoring the latest `SHA256SUMS` in the Bitcoin blockchain |
| `timestamps/` | Every dated checksum snapshot with its own proof |

## Verifying

Check file integrity:

```
sha256sum -c SHA256SUMS
```

Verify the Bitcoin timestamp (requires `pip install opentimestamps-client`):

```
ots verify SHA256SUMS.ots
```

A new proof is "pending" for a few hours until the OpenTimestamps calendars commit it to a Bitcoin block. The GitHub Action in `.github/workflows/timestamp.yml` re-hashes the repo on every push, stamps changes, and upgrades pending proofs every six hours until they are complete.

## Note on the assessment

The research files were written before the Oct. 29, 2026 embargo lifted, and their predictions are deliberately left unedited so they can be graded against what was announced. The timestamps prove they predate the announcement.
