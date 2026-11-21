# Contributing to the Iris Species Classification project

This outlines how to propose a change to the Iris Species Classification project.

### Fixing typos

Small typos or grammatical errors in documentation may be edited directly using
the GitHub web interface, so long as the changes are made in the _source_ file.

- YES: you edit the Quarto source file `analysis/predict-iris-classification.qmd`.
- NO: you edit the rendered `analysis/predict-iris-classification.html` or `.pdf`.

### Prerequisites

Before you make a substantial pull request, you should always file an
[issue](https://github.com/UBC-MDS-2026-27/DSCI_522_Group_33_project-compare-iris-predictions/issues)
and make sure someone from the team agrees that it's a problem. If you've found
a bug, create an associated issue and illustrate the bug with a minimal
[reprex](https://www.tidyverse.org/help/#reprex).

### Setting up the project

Install [uv](https://docs.astral.sh/uv/getting-started/installation/) and
[Quarto](https://quarto.org/docs/get-started/), then clone the repository and
create the virtual environment from the root of the repository:

```bash
git clone https://github.com/UBC-MDS-2026-27/DSCI_522_Group_33_project-compare-iris-predictions.git
cd DSCI_522_Group_33_project-compare-iris-predictions
uv sync
```

To re-run the analysis and render the report:

```bash
uv run quarto render analysis/predict-iris-classification.qmd
```

If your change needs a new Python package, add it with `uv add` followed by
the package name (this pins an exact version in `pyproject.toml` and updates
`uv.lock`), and commit both files.

### Pull request process

- Create a new Git branch for each pull request (PR), starting from an
  up-to-date `main`. Do not commit directly to `main`.
- Give the branch a short name that describes the work,
  for example `fix-readme-typo` or `add-eda-figure`.
- Keep each branch small: one independent piece of work per branch.
- Before opening the PR, render the report
  (`uv run quarto render analysis/predict-iris-classification.qmd`)
  to check that the analysis still runs from start to finish.
- Open a PR into `main` and describe what changed and why.
  Link the related issue (e.g., "Closes #12").
- At least one other team member must review and approve the PR before it is merged.
  The reviewer, not the author, merges it.
- New code should follow the PEP8 [style guide](https://peps.python.org/pep-0008/).

### AI policy

You may use generative AI tools (for example, ChatGPT, GitHub Copilot, or Claude)
to help you contribute to this project, such as to explain errors, brainstorm,
draft code, or improve wording, under the following rules.

- **People, not AI agents, contribute.** Issues and pull requests must be
  opened, reviewed and merged by people, not by an AI agent or bot. Comments in
  discussions and reviews must reflect your own judgement.
- **Disclose substantial AI use.** If an AI tool generated a substantial part of
  your contribution (code, analysis, or text), say so in the pull request
  description: name the tool and briefly describe what it was used for and
  which files it affected. Minor uses, such as single-line autocomplete or
  spell-checking, do not need to be disclosed.
- **You are responsible for what you submit.** You must read, run, and
  understand everything in your contribution, whether or not an AI tool helped
  write it, and be able to explain it during review. You are also responsible
  for making sure it is correct and does not copy anyone else's work without
  proper attribution.

### Code of Conduct

Please note that this project is released with a [Contributor Code of
Conduct](CODE_OF_CONDUCT.md). By participating in this project you agree to
abide by its terms.

### Attribution

These contributing guidelines were adapted from the
[contributing guidelines](https://github.com/UBC-MDS/DSCI_522_project-template-breast-cancer-predictor/blob/main/CONTRIBUTING.md)
of the UBC-MDS Breast Cancer Predictor project.
The AI policy was adapted from the
[SymPy AI-generated code policy](https://docs.sympy.org/dev/contributing/ai-generated-code-policy.html)
and the [earthaccess AI policy](https://earthaccess.readthedocs.io/en/latest/contributor/ai-policy/).
