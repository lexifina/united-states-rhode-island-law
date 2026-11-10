# How this repository was made (United States (Rhode Island))

This file is written by the build on 2026-11-10, the day the source data was retrieved.

## Sources

| Source | Address | Retrieved | Licence |
| --- | --- | --- | --- |
| General Laws of Rhode Island (webserver.rilegislature.gov/Statutes), read from Internet Archive captures | <https://webserver.rilegislature.gov/Statutes/> | 2026-11-10 | Statute text carries no copyright (Georgia v. Public.Resource.Org, 2020). No annotations are used. |

Every word of law in this repository comes from these sources. Lexifina reads them and records each act's dated versions, and the laws that made each change, in one corpus file. This repository is built from that file.

## What is in it

| Act | Title | Versions | Span |
| --- | --- | ---: | --- |
| `constitution-preamble` | Constitution of the State of Rhode Island, Preamble | 1 | 2024-06-17 to 2024-06-17 |
| `constitution-article-01` | Constitution of the State of Rhode Island, Article 1: Declaration of Certain Constitutional Rights and Principles | 1 | 2024-06-17 to 2024-06-17 |
| `constitution-article-02` | Constitution of the State of Rhode Island, Article 2: Of Suffrage | 1 | 2024-06-17 to 2024-06-17 |
| `constitution-article-03` | Constitution of the State of Rhode Island, Article 3: Of Qualification for Office | 1 | 2024-06-17 to 2024-06-17 |
| `constitution-article-04` | Constitution of the State of Rhode Island, Article 4: Of Elections and Campaign Finance | 1 | 2024-06-17 to 2024-06-17 |
| `constitution-article-05` | Constitution of the State of Rhode Island, Article 5: Of the Distribution of Powers | 1 | 2024-06-17 to 2024-06-17 |
| `constitution-article-06` | Constitution of the State of Rhode Island, Article 6: Of the Legislative Power | 1 | 2024-06-17 to 2024-06-17 |
| `constitution-article-07` | Constitution of the State of Rhode Island, Article 7: Of the House of Representatives | 1 | 2024-06-17 to 2024-06-17 |
| `constitution-article-08` | Constitution of the State of Rhode Island, Article 8: Of the Senate | 1 | 2024-06-17 to 2024-06-17 |
| `constitution-article-09` | Constitution of the State of Rhode Island, Article 9: Of the Executive Power | 1 | 2024-06-17 to 2024-06-17 |
| `constitution-article-10` | Constitution of the State of Rhode Island, Article 10: Of the Judicial Power | 1 | 2024-06-17 to 2024-06-17 |
| `constitution-article-11` | Constitution of the State of Rhode Island, Article 11: Of Impeachments | 1 | 2024-06-17 to 2024-06-17 |
| `constitution-article-12` | Constitution of the State of Rhode Island, Article 12: Of Education | 1 | 2024-06-17 to 2024-06-17 |
| `constitution-article-13` | Constitution of the State of Rhode Island, Article 13: Home Rule for Cities and Towns | 1 | 2024-06-17 to 2024-06-17 |
| `constitution-article-14` | Constitution of the State of Rhode Island, Article 14: Constitutional Amendments and Revisions | 1 | 2024-06-17 to 2024-06-17 |
| `constitution-article-15` | Constitution of the State of Rhode Island, Article 15: General Transition | 1 | 2024-06-17 to 2024-06-17 |

The build made 16 commits:

| Commits | Kind |
| ---: | --- |
| 16 | first version of an act |
| 0 | one law on its in-force day |
| 0 | changes no amendment note explains, credited to the publisher |

Other counts:
- 0 commits on the branch `future`: laws not yet in force on 2026-11-10.
- 0 commits dated 1 January 1970: in force before 1970, with the real day in their `In-force` trailer.
- 0 laws in the record.
- 16 tags.

## Dates

Each commit is dated at noon (America/New_York) on the day the change took effect. The other dates, enacted and published, are trailers.

When a law gives no date of its own, the default rule applies: No dated history is read: each chapter is the oldest version available, dated by the day of the newest Internet Archive capture among its section pages. https://webserver.rilegislature.gov/Statutes/

## How the history is built

`tools/build.py` turns the corpus into this history in one pass: one commit per law, on the day it took effect. The same corpus always gives the same commit hashes. `tools/check_repo.py` reads every version back from git and compares it with the corpus. `tools/on.py` shows the law as it stood on any date. The corpus format is described in `tools/SCHEMA.md`.

- Corpus: sha256 `a67fb0aaf868c26ee5fea26b6e096a4e10b9f97bcb8a79d48b09da1280730fcc` (91471 bytes).
- Builder blob hashes (`git hash-object`): `build.py` `3024ff164c261807dfc4d5b7b1b4a2cde4357da1`, `check.py` `5d719354ea4c62d240c93d2cae446307d81d9e81`, `on.py` `aff48cf1b68d50c7ba8f399ca32261871c301824`.
- Python 3.12.10; git version 2.46.0.windows.1.

## Checks

Not yet run for this build.

No second build of this corpus has been compared yet.

On GitHub this history follows the repository's first commit ("sources, before any law"), so each commit there has that parent and a committer time of its own; `tools/build.py` rebuilds the same files in the same commits, with the hashes quoted above.

## Decisions made by hand

- no request was made to the host itself.
- The General Laws are published one page per section. A chapter is published only when its chapter index (TITLEn/<ch>/INDEX.htm) has a capture and every section that index lists has one; the newest capture of each page was read.
- Each chapter is dated by the newest capture day among its section pages; the version note gives the range of capture days. A chapter whose sections were captured on different days is the text each section had on its own capture day.
- Kept: the section heading, text and the "History of Section." note printed under each section.

## What AI did and did not do

The scripts that read the sources and build this repository were written by Claude Code running Claude Opus 5.5 (`claude-opus-5-5`) under Lexifina's direction.

No model wrote, translated or corrected legal text. No model runs at build time. Every word of law in this repository comes from the official sources above.

The commit messages are written by `build.py` from the source data.

Model use at data-build time:
- none
