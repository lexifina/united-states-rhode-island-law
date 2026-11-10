# United States (Rhode Island): law history in git

The law of Rhode Island as a git history: one file per provision, with `git blame` and `git log` working line by line. It follows the shared design of [lexifina/global-law](https://github.com/lexifina/global-law).

**What is in it now (a first build, not complete)**

| Folder | Act | Versions | History |
| --- | --- | ---: | --- |
| `constitution-*/` | Constitution of the State of Rhode Island: the preamble and 15 articles | 1 | 119 provisions; read from captures of 2024-06-17 |
| `chapter-NNNN-NNNN/` | General Laws: 61 of the 2519 chapters in force listed in the title indexes | 1 | 939 sections; each chapter dated by the newest capture among its section pages (2025-02-12 to 2026-10-31) |

**Source.** The General Laws of Rhode Island and the Rhode Island Constitution as published by the General Assembly on [webserver.rilegislature.gov](https://webserver.rilegislature.gov/Statutes/), read from Internet Archive captures because the host times out from the build machine. The General Laws are published one page per section; a chapter is taken only when its index page and every section it lists were captured. Only section headings, text and the "History of Section." notes are taken.

## Dates

The pages carry the current text only. Each chapter is therefore one version, "oldest version available", dated by the newest capture day among its section pages (the version note gives the range). The Constitution pages were last captured with text on 17 June 2024 (later captures are "not found" pages: the pages moved), so the Constitution is dated 2024-06-17. Later builds will add later versions on top.

## How it is checked

Every version is read back from git on the day it took effect and on the day before (`tools/check_repo.py`) and must match `corpus.json`; the results are in `REPRODUCE.md`.

## What "author" means

The author of a commit is the law that made the change, with an e-mail address that cannot exist (`<law key>@rilegislature-gov.invalid`). In this first build no dated history is available, so every commit is credited to the publisher as "oldest version available". The committer is always Lexifina.

## Limits

61 of the 2519 chapters in force listed in the title indexes are included (291 repealed, reserved or expired chapters are not counted). Left out so far: no capture of the chapter index (2051); chapter index lists no sections (263); a listed section has no capture (143); not every section page fetched or readable yet (1). Most chapter index pages were never captured by the Internet Archive, so most chapters cannot be shown complete and are left out. Session laws and regulations are not included. There is no history before the dates above.
