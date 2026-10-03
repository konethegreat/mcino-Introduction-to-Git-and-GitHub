## About this repository

This is a learning (coursework) fork, not an original project. It is a fork of [ibm-developer-skills-network/mcino-Introduction-to-Git-and-GitHub](https://github.com/ibm-developer-skills-network/mcino-Introduction-to-Git-and-GitHub), a lab repository from IBM Skills Network for an introduction to Git and GitHub. The commits and branches described below are the practice work done in it.

### Upstream work and Kone's changes

Checked with `git log` and `git diff upstream/main main`:

- **Upstream:** both scripts, the issue templates, the pull request workflow, `CODE_OF_CONDUCT.md`, `CONTRIBUTING.md`, `LICENSE` (Apache License 2.0) and the README text below the line. Upstream's commits are by ritikaj23 and ibm-skills-network-bot (4 September 2025). None of these files was changed here, except for the one README line described next.
- **Kone's change on `main`:** Kone Tshivhinda (`konethegreat`) changed the README footer from `_© 2022 XYZ, Inc._` to `2023 XYZ, Inc.` in the commit "Fix typo in footer: Updated year to 2023" (20 April 2026). Branch `bug-fix-typo` points at the same commit.
- **`bug-fix-revert`:** one more commit by Kone from the same day, `Revert "Update README.md"`. It was never merged. Its `README.md` still contains unresolved merge-conflict markers (`<<<<<<< HEAD` and `>>>>>>> parent of d8324ad`), so it should not be merged as it is. The branch is kept as a record of the practice work.
- **Added in October 2026:** a `.gitattributes` file that keeps `*.sh` files on LF line endings, and the notes above the line.

### Running the scripts

Both scripts are upstream's. They were run to check these notes, with GNU bash 5.2.21 (WSL Ubuntu) and Python 3.14.7.

| File | Run with | What it does |
| ---- | -------- | ------------ |
| `simple-interest.sh` | `bash simple-interest.sh` | Asks for the principal, the yearly rate and then the time in years, and prints principal * time * rate / 100 using integer arithmetic (`expr`). The answers 1000, 5 and 2 give `100`; a non-integer such as `2.5` fails with `expr: non-integer argument`. |
| `compound_interest.py` | `python3 compound_interest.py` (`py -3` on Windows) | Asks for the principal, the time and the rate and prints `p * (1 + r/100)^t` with two decimals. That is the total after compounding, not the interest alone: 1000, 2 and 5 give `1102.50`, although the output says "compound interest". |

`.gitattributes` exists because Git for Windows, with its default `core.autocrlf=true`, checks `simple-interest.sh` out with CRLF line endings and bash then fails with `$'\r': command not found`.

A variant of the simple interest script that uses `bc`, prints two decimals and has tests is in [github-final-project](https://github.com/konethegreat/github-final-project).

Pull requests opened against this repository are closed automatically by `.github/workflows/close_pr.yml`, which comments "Congratulations! You have completed the lab. Closing for maintainence purpose." (the spelling is upstream's).

---

# Introduction to Git and GitHub

## Simple Interest Calculator

A calculator that calculates simple interest given principal, annual rate of interest and time period in years.

```
Input:
   p, principal amount
   t, time period in years
   r, annual rate of interest
Output
   simple interest = p*t*r
```

2023 XYZ, Inc.
