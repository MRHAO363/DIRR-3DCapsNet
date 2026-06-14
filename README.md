# DIRR-3DCapsNet

This repository provides the full experimental code and ablation experiment code for DIRR-3DCapsNet.
Open the corresponding .ipynb file in JupyterLab or Jupyter Notebook and run all cells.

## Files

- `DIRR-3DCapsNet.ipynb`: full experimental code of the proposed DIRR-3DCapsNet model.
- `ED only.ipynb`: ablation experiment using only the ED phase.
- `ES only.ipynb`: ablation experiment using only the ES phase.
- `ED + ES without Diff.ipynb`: ablation experiment without ES−ED differential feature fusion.
- `-3D-RoPE.ipynb`: ablation experiment without the 3D rotary positional encoding module.
- `-Local interactive routing.ipynb`: ablation experiment without the local interactive routing branch.

## Dataset

The experiments use the Automated Cardiac Diagnosis Challenge (ACDC) dataset.

The ACDC dataset is not redistributed in this repository. Please obtain the dataset from the official ACDC website.


Parameter descriptions:
CLASS_MAP: category mapping of the five cardiac phenotypes.
TARGET_SHAPE: final input shape after cropping and padding.
TARGET_SPACING: isotropic resampling spacing.
AUG_FACTOR: number of augmentation applications during training.
start_fold: the fold from which training starts.
results_file: JSON file used to save completed fold results.
CUSTOM_PREFIX: prefix used for saving model checkpoints.
The experiments use fivefold stratified cross-validation at the case level
The multi-seed experiments in the paper use the following random seeds:0, 42, 123, 1234, 3407
The package installation command is:pip install torch torchvision numpy scipy scikit-learn matplotlib nibabel torchio fvcore
