## About this repository

This is a learning (coursework) fork, not an original project. It is a fork of [ibm-developer-skills-network/mcino-Introduction-to-Git-and-GitHub](https://github.com/ibm-developer-skills-network/mcino-Introduction-to-Git-and-GitHub), a lab repository from IBM Skills Network for an introduction to Git and GitHub. The commits and branches described below are the practice work done in it.

### Upstream work and Kone's changes

Checked with `git log` and `git diff upstream/main main`:

- **Upstream:** both scripts, the issue templates, the pull request workflow, `CODE_OF_CONDUCT.md`, `CONTRIBUTING.md`, `LICENSE` (Apache License 2.0) and the README text below the line. Upstream's commits are by ritikaj23 and ibm-skills-network-bot (4 September 2025). None of these files was changed here, except for the one README line described next.
- **Kone's change on `main`:** Kone Tshivhinda (`konethegreat`) changed the README footer from `_© 2022 XYZ, Inc._` to `2023 XYZ, Inc.` in the commit "Fix typo in footer: Updated year to 2023" (20 April 2026). Branch `bug-fix-typo` points at the same commit.
- **`bug-fix-revert`:** one more commit by Kone from the same day, `Revert "Update README.md"`. It was never merged. Its `README.md` still contains unresolved merge-conflict markers (`<<<<<<< HEAD` and `>>>>>>> parent of d8324ad`), so it should not be merged as it is. The branch is kept as a record of the practice work.
- **Added in October 2026:** a `.gitattributes` file that keeps `*.sh` files on LF line endings, and this section.

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
