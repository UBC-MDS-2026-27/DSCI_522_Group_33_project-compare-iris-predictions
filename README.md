# Iris Species Classification Model

DSCI 522: Milestone 1 project repository

## Authors

- Ramandeep Kaur
- Peter Kim
- Jiaqi Feng
- Carine Ishimwe

## Summary

We analyse the Iris dataset from the UCI Machine Learning Repository to answer the question: "Are sepal measurements or petal measurements better for predicting the species of an iris flower?" We compare two logistic regression models: one uses petal length and width, and the other uses sepal length and width. For a fair comparison, both models use the same training and test sets. We compare their accuracy and confusion matrices and find that the petal model predicts species more accurately than the sepal model (96.7% vs 76.7% test accuracy). This suggests that researchers who are short on time in the field could measure petals alone and still identify iris species reliably, although our data set is small and we tested only one type of model.

## How to run the analysis

Follow these steps to reproduce the analysis.

### Installation requirements

1. Quarto 1.10.18
2. uv 0.12.7
3. The required Python packages are recorded in `uv.lock`.

### Steps

Run the following commands in a terminal:

1. Move to the folder where you want the project:

   ```bash
   cd path/to/folder
   ```

2. Clone the repository and move into it:

   ```bash
   git clone https://github.com/UBC-MDS-2026-27/DSCI_522_Group_33_project-compare-iris-predictions.git
   cd DSCI_522_Group_33_project-compare-iris-predictions
   ```

3. Install the dependencies:

   ```bash
   uv sync
   ```

4. Render the report:

   ```bash
   uv run quarto render analysis/predict-iris-classification.qmd --to html
   ```

5. Open `analysis/predict-iris-classification.html` in a browser.

## Dependencies

- [uv](https://docs.astral.sh/uv/) 0.12.7, for managing the Python environment
- [Quarto](https://quarto.org/docs/get-started/) 1.10.18, for rendering the report (install it separately; `uv sync` does not install the Quarto program)
- Python 3.14 (uv installs it automatically)
- Python packages: altair, ipython, jupyterlab, numpy, pandas, scikit-learn and vl-convert-python

The full list of packages and versions is in [`pyproject.toml`](pyproject.toml) and [`uv.lock`](uv.lock).

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
