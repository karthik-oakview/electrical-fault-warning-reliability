# Electrical Fault Warning Reliability

This repository contains the analysis code and supporting results for:

**Can We Trust AI for Early Electrical Fault Warning?  
A Reliability Evaluation Across Changing Electrical Conditions**

## Study overview

The study evaluates machine-learning reliability across four public
electrical datasets using validation designs that hold out complete
physical units:

- NASA Battery: leave one battery out
- Leakage Current: leave one insulator out
- Microchip Arc Fault: leave one operating condition out
- Partial Discharge: cross-polarity transfer with recording files
  retained as independent units

## Repository contents

- `electrical_fault_warning_reproducibility.ipynb`  
  Complete Google Colab analysis notebook.

- `results/`  
  Per-unit, per-fold, event-level, calibration, ablation,
  risk-coverage, AURC, and warning-lead-time result tables.

- `figures/`  
  Publication-quality risk-coverage and reliability-diagram figures.

## Framework-development roles

NASA Battery and Leakage Current were used during development of the
Reliability-Aware Electrical Warning Framework.

Microchip Arc Fault and Partial Discharge were not used to develop or
tune the final framework rules.

## Software

The notebook was developed using Google Colab and Python 3.

Primary packages:

- NumPy
- pandas
- SciPy
- scikit-learn
- XGBoost
- Matplotlib

Random state 42 was used where supported.

## Data availability

The original public datasets are not redistributed in this repository.
They should be downloaded from their official sources:

1. NASA Li-ion Battery Aging Datasets
2. Leakage Current Dataset
3. Microchip ML Arc-Fault Detection repository
4. Partial Discharge Measurements of Voids in Layered Polymers and
   Cable Sample

The complete citations and source links appear in the accompanying
paper.

## Reproduction notes

The notebook was developed using this Google Drive root:

`/content/drive/MyDrive/Electrical_Failure_2026/`

Users may need to modify the configuration paths to match their own
directory structure.

Microchip reliability results are evaluated by signal window. Partial
Discharge reliability results are reported at the independent
recording-file level.

## ESP32 validation

The ESP32 experiment verifies numerical reproduction using prerecorded
held-out feature vectors. It does not demonstrate live sensor-based
arc-fault detection.

## Interpretation

The combined reliability framework did not consistently outperform
simpler uncertainty baselines. The repository preserves this negative
result as part of the study's reliability evaluation.# electrical-fault-warning-reliability
Code and results for evaluating AI reliability in electrical fault warning under changing conditions
