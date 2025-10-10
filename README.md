# Insurance Claims Classification Workbench

Exploratory code for claims-table preparation, paid/unpaid classification, leakage-aware feature selection and model evaluation.

Maintained by [Ahmed Jawed](https://github.com/ahmedjawedaj).

## Methods and engineering work

- Claim-level and line-level table preparation.
- Class imbalance and categorical feature handling.
- Gradient-boosting/classification experiments and leakage-sensitive features.
- ROC-AUC, precision/recall, F1 and confusion-matrix analysis.

## Repository contents

- [`claims_classification.ipynb`](notebooks/claims_classification.ipynb)
- [`data/README.md`](data/README.md): required external inputs and data handling.
- [`PROVENANCE.md`](PROVENANCE.md): original source-date evidence, attribution and publication changes.
- [`scripts/validate_sources.py`](scripts/validate_sources.py): notebook/Python syntax and exclusion checks.

## Recorded observations

- The source has 40 executed cells out of 41 code cells, with no saved exception outputs.
- All source outputs are removed from the publication to avoid redistributing row-level claims information.

## Setup and use

```bash
python -m venv .venv
source .venv/bin/activate
python -m pip install -r requirements.txt
cd notebooks
jupyter lab
```

Select the intended kernel and run the notebook top to bottom after providing its required inputs. GPU notebooks can consume substantial runtime; validation below does not start training.

## Data and weights

Use your own authorized cleaned_claims_dataset.csv and claims_lines_dataset.csv beside the notebook. Read data/README.md for the schema contract. Do not upload real claims data to issues or pull requests.

## Validation

```bash
python -m pip install -r requirements-validation.txt
python scripts/validate_sources.py
```

The publication checks validate notebook structure and compile source cells/Python modules. They do not reproduce training, GPU timing or ROS hardware behaviour. Cleaned notebooks have no captured outputs or stale execution counters.

## Scope and limitations

- Original data provenance, permissions and representativeness are not established by this code publication.
- No patient, insurer, provider, claim rows, trained models or business performance figures are published.
- The notebook is an exploratory workbench with sequential cell state, not a production API or a self-contained benchmark.

## References and attribution

- [scikit-learn evaluation](https://scikit-learn.org/stable/modules/model_evaluation.html)

See PROVENANCE.md for the distinction between original work dates and actual publication dates. This repository excludes instructor handouts, raw data, model weights and private records.
