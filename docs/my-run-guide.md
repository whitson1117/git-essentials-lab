# Run the library demo

## Prerequisites

- Git 2.23 or later, to clone this repository.
- JDK 17 or later, with both `java` and `javac` available on PATH.
- Python 3.9 or later, available as `python3`.
- A terminal opened at the repository root, which contains `run.py`.

No Maven, Gradle, Java framework, or third-party Java dependency is required.
On Windows, Git Bash can be used; `py -3` can replace `python3` if that is
the installed Python launcher. Ensure a JDK (including the compiler), not
only a Java runtime, is available.

## Run

```bash
python3 run.py demo
```

The runner compiles the Java source into a temporary directory and runs a
deterministic library loan demonstration using the fixed date 2026-09-01.
It prints student and faculty borrowing limits, searches the catalog for
`git`, borrows *Git Essentials* for Alex, prints the loan receipt and due
date, then returns the book and prints the fee and remaining active loans.
The baseline uses two-book limits, a 14-day loan period, a nonnegative
100-per-day overdue fee, and case-sensitive title search.

## Verify

```bash
python3 run.py test
```

This command checks the baseline. To check a changed exercise, run the
current launcher's `lab.py check` command with that exercise ID and workspace.

## Git remotes

`origin` points to my fork, `whitson1117/git-essentials-lab`; `upstream`
points to the course repository, `oh-gnues/git-essentials-lab`.
Pushing `result/ex02` publishes this branch to my fork. It does not open a
pull request or merge into another branch. The remote alias `upstream`
stores a repository URL; a branch's tracking relationship is configured
separately, here between `result/ex02` and `origin/result/ex02`.
