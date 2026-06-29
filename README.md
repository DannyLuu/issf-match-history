# ISSF Match History

Private official-facing match history for ISSF-style pistol events.

This repository is intended to provide a clean record of competition participation, scores, score breakdowns, and supporting evidence for review. It is not a training journal.

## Scope

This repository tracks official or reviewable competition results only.

Included:

- Match names
- Match dates
- Club / host organization
- Location
- Event type
- Scores and maximum scores
- Percentage
- Placement, when available
- Classification, when available
- X-count, when available
- Score breakdowns from score sheets
- Links to evidence images or published result pages

Excluded:

- Training notes
- Practice-session analysis
- Firearm details
- Ammunition details
- Grip, sight, or equipment setup
- Personal technical notes

Training data should be kept separately.

## Repository Structure

```text
issf-match-history/
├── README.md
├── matches.csv
├── matches/
│   ├── template.md
│   ├── 2026-03-22-red-doolittle-standard-pistol.md
│   ├── 2026-03-22-red-doolittle-sport-pistol.md
│   ├── 2026-04-12-adrra-red-doolittle-standard-pistol.md
│   ├── 2026-04-12-adrra-red-doolittle-sport-pistol.md
│   ├── 2026-06-21-adrra-standard-pistol.md
│   └── 2026-06-21-adrra-sport-pistol.md
└── Evidence/
    └── YYYY-MM-DD Match Name - Event/
        ├── Competition Results.png
        └── Target Score.jpg
```

## Master Results Index

The master results file is:

[`matches.csv`](matches.csv)

This file is the main official-facing index. Each row represents one event result.

Current columns:

| Column | Purpose |
|---|---|
| `Date` | Match date |
| `Match Name` | Name of the competition or match |
| `Club` | Host club or organizing club |
| `Location` | Match location |
| `Sanctioning Body` | Governing or results body, if applicable |
| `Event` | ISSF event type |
| `Score` | Shooter score |
| `Maximum Score` | Maximum possible score |
| `Percentage` | Score percentage |
| `Placement` | Placement if available |
| `Class` | Shooter classification if available |
| `X Count` | Number of Xs if available |
| `Match Type` | Club Match, Official Competition, etc. |
| `Result Status` | Verification status |
| `Score Tracker URL` | Published online result link, if available |
| `Image Folder` | Evidence folder for the event |
| `Match Report` | Detailed Markdown report for the event |
| `Notes` | Short official-facing notes only |

## Match Reports

Individual event reports are stored in:

[`matches/`](matches/)

Each report should include:

- Result summary
- Score breakdown
- Evidence links
- Verification notes
- Change log

Use the template for new entries:

[`matches/template.md`](matches/template.md)

## Evidence Folder Convention

Evidence should be stored under:

```text
Evidence/YYYY-MM-DD Match Name - Event/
```

Recommended filenames:

```text
Competition Results.png
Target Score.jpg
Published Results.pdf
```

Examples:

```text
Evidence/2026-03-22 Red Doolittle Pistol Match - Standard Pistol/Competition Results.png
Evidence/2026-03-22 Red Doolittle Pistol Match - Standard Pistol/Target Score.jpg
Evidence/2026-03-22 Red Doolittle Pistol Match - Sport Pistol/Competition Results.png
Evidence/2026-03-22 Red Doolittle Pistol Match - Sport Pistol/Target Score.jpg
```

## Result Status Values

Use one of these values in `matches.csv` and match reports:

| Status | Meaning |
|---|---|
| `Pending` | Result entered but not yet checked |
| `Unofficial` | Result recorded, but not yet verified against evidence |
| `Verified` | Confirmed against score sheet, screenshot, or other evidence |
| `Published` | Result appears on a published result page |
| `Corrected` | Result was updated after a correction |

## Current Results Summary

| Date | Event | Score | Status |
|---|---|---:|---|
| 2026-03-22 | 25m Standard Pistol | 351 / 600 | Verified |
| 2026-03-22 | 25m Sport Pistol | 318 / 600 | Verified |
| 2026-04-12 | 25m Standard Pistol | 384 / 600 | Published |
| 2026-04-12 | 25m Sport Pistol | 384 / 600 | Published |
| 2026-06-21 | 25m Standard Pistol | 385 / 600 | Verified |
| 2026-06-21 | 25m Sport Pistol | 436 / 600 | Verified |

## Privacy and Access

This repository is private.

Viewers should be granted read-only access unless they are expected to maintain the records. Contents are for review only and should not be copied, redistributed, published, modified, or reused without permission from the repository owner.

## Maintenance Notes

When adding a new match:

1. Add evidence files under `Evidence/YYYY-MM-DD Match Name - Event/`.
2. Add or update the event row in `matches.csv`.
3. Create a Markdown report in `matches/` using `matches/template.md`.
4. Keep the entry official-facing. Do not add equipment, ammo, training notes, or personal analysis.
