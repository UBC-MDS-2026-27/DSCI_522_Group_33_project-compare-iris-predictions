# Iris Species Classification Model

DSCI 522: Milestone 1 project repository

## Authors

- Ramandeep Kaur
- Peter Kim
- Jiaqi Feng
- Carine Ishimwe

## Summary

We analyse the Iris dataset from the UCI Machine Learning Repository to answer the question: “Are sepal measurements or petal measurements better for predicting the species of an iris flower?” We compare two logistic regression models: one uses petal length and width, and the other uses sepal length and width. For a fair comparison, both models use the same training and test sets. We compare their accuracy and confusion matrices and find that the petal model predicts species more accurately than the sepal model (96.7% vs 76.7% test accuracy). This suggests that researchers who are short on time in the field could measure petals alone and still identify iris species reliably, although our data set is small and we tested only one type of model.

## Rendered report

View the rendered report at <https://ubc-mds-2026-27.github.io/DSCI_522_Group_33_project-compare-iris-predictions/>.

## How to run the analysis

Run these commands from the root of the repository. Docker must be installed and running.

1. If you do not already have an SSH key, create one on your computer:

   ```bash
   ssh-keygen -t ed25519
   ```

   Press Enter at each prompt.

2. Download the project image:

   ```bash
   docker compose pull
   ```

3. Render the report in the container:

   ```bash
   docker compose run --rm analysis-env uv run quarto render analysis/predict-iris-classification.qmd
   ```

   The rendered report is saved as `analysis/predict-iris-classification.html`.

The `--rm` option removes the one-off container when rendering finishes.

For instructions on changing the project, see [CONTRIBUTING.md](CONTRIBUTING.md).

## Dependencies

The project environment runs in the Docker image configured by `Dockerfile` and `docker-compose.yml`. Python package versions are recorded in `pyproject.toml` and `uv.lock`.

## Licenses

The project code is licensed under the MIT License.

The analysis report is licensed under the Creative Commons Attribution-NonCommercial-NoDerivatives 4.0 International (CC BY-NC-ND 4.0) License.

The Iris dataset is licensed under the Creative Commons Attribution 4.0 International (CC BY 4.0) License.

See [LICENSE.md](LICENSE.md) for details.

## AI use statement

We used Claude and ChatGPT to debug code errors and to proofread for grammar and typos before team members reviewed the code. For the Methods section of our report, we used Anthropic Claude Opus 5.5 to help create placeholders and TODOs to structure the section, which were subsequently filled in by the authors. All AI-generated content was reviewed and edited by the authors so that no placeholders or TODO statements were left in the final report.

No system files or CLAUDE.md files were used.

## GitHub URL

<https://github.com/UBC-MDS-2026-27/DSCI_522_Group_33_project-compare-iris-predictions>
