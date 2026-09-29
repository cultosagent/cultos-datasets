# Cult OS Intel: Aeon reviews · Batch #1

AI code reviews of 21 public open-source pull requests, run by Cult OS through its Aeon review agent between 29 August and 25 September 2026. Each row is one repository. Every review is pinned to an exact commit and paid for on Base, so anyone can verify it.

## What's inside

| File | Contents |
|---|---|
| `cultos-intel-aeon-reviews-batch-1.jsonl` | One JSON object per repository, with full fields |
| `cultos-intel-aeon-reviews-batch-1.csv` | The same rows, with the main columns, for spreadsheets |

Each row has:
- **The pull request and commit:** the repository, pull request, exact commit reviewed, verdict and a one-paragraph summary.
- **Findings:** the count by severity and up to three finding titles.
- **Scope and payment:** the number of files reviewed, completion time, price where recorded, settlement transaction and a link to the original review record.
- **History:** how many reviews of that repository exist, which pull requests they covered, and whether the listed review corrects an earlier one.

## Numbers

| | |
|---|---|
| Repositories | 21 |
| Verdicts | 17 approve-ready, 3 discussion-needed, 1 blocked |
| Findings | 4, all medium severity |
| Period | 2026-08-29 to 2026-09-25 |

## How this batch was built

- **Source:** the public Cult OS review registry, 48 completed paid reviews.
- **One row per repository:** where a repository was reviewed more than once, the row shows the latest review. The other pull requests are listed in `pull_requests_reviewed`.
- **Excluded:**
  - Our own test repository, reviewed 13 times as a fixture, and the Cult OS repository itself.
  - Calibration runs.
  - One review that was later corrected: its replacement is listed and marked `corrected: true`.
- **Payment:** Cult OS paid for every review in this batch to build the dataset. The payments prove each review really ran through the paid pipeline. They are not customer purchases.
- **Price:** the price paid is recorded for 13 rows. Older records did not store it and are left empty rather than estimated.

## Verify any row

1. Open `pull_request_url` and confirm the commit in `commit` belongs to that pull request.
2. Open `settlement_url` to inspect the Base payment. Where recorded, verify the token contract, decimals and exact amount against the explicit settlement fields; payments may be USDC or CULTOS.
3. Open `record_url` to read the full original review: every finding, the files reviewed and the limitations.

## Integrity

SHA-256 of `cultos-intel-aeon-reviews-batch-1.jsonl`:

```
c35fe62778327a1dedb77596f7677765f7d01e8931b65025f990d0d68208177f
```

## Limits

- Reviews are AI-generated. An approve-ready verdict means the agent found no blocking issues in the files it reviewed; it is not a security guarantee.
- The sample is small and includes public repositories only.

## Payment metadata correction

Original commit: d8620f68ed0215d573a55a3ed7296da2b26597a8. Source registry snapshot: 999bce25d1a5c67e6b1720d9e5f71b9f2f7fa238.

The 13 recorded amounts comprise 10 USDC payments and 3 CULTOS payments.
The three CULTOS rows now have null price_usdc; no USD conversion is inferred.
Eight rows lack source amount/asset metadata and remain null, not zero.
Exact base-unit amounts are strings; settlement_amount is an exact decimal string.
CSV adds the same five settlement fields. Other review fields are unchanged.
Missing source payment metadata is not reconstructed or estimated.
No claim is made that a successful payment validates the substantive review findings.
The original publisher must version/adopt this correction and update the referenced pod evidence.

CSV SHA-256: c09d51bce291b37cdf3ee5c2c95a38d9ec8cf5f30c6adca28316f1843e09f761
