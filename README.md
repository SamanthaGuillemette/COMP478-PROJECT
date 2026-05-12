# Breast Cancer Classification from Ultrasound Imaging

Machine-learning pipeline for classifying breast-ultrasound images using a Random Forest model.
Course project for **COMP 478 — Image Processing** at Concordia University (2022).

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Python](https://img.shields.io/badge/python-3.8%2B-blue.svg)](https://www.python.org/)
[![Jupyter](https://img.shields.io/badge/jupyter-notebook-orange.svg)](https://jupyter.org/)

## Overview

Breast cancer is the most common cancer in women worldwide, and ultrasound is a widely used non-invasive imaging modality for screening and diagnosis. This project explores a classical machine-learning approach to **classifying breast-ultrasound images for cancer detection**: features extracted from the images are passed into a Random Forest classifier, which is trained and evaluated end-to-end inside a single reproducible Jupyter notebook.

The project was completed for an undergraduate Image Processing course, and complements an M.Sc. in molecular pathology focused on the Hippo signalling pathway in mammary carcinoma — a connection that motivates ongoing interest in computational approaches to breast cancer research.

## Results

| Model | Test accuracy |
|---|---|
| **Random Forest** | **83.56%** |

The notebook produces all preprocessing visualizations, training-time metrics, and evaluation plots inline, so results are fully reproducible end-to-end.

## Approach

The pipeline runs as a single Jupyter notebook (`COMP478_PROJECT_CODE.ipynb`, ~700 lines across 40 commits) and covers:

1. **Dataset loading and exploration** — breast ultrasound images organised by class.
2. **Preprocessing** — resizing, normalization, and conversion to a feature-ready representation.
3. **Feature extraction** — image-level features suitable for a classical classifier.
4. **Model training** — Random Forest from scikit-learn.
5. **Evaluation** — accuracy on a held-out test split, with diagnostic plots.

## Repository structure

```
COMP478-PROJECT/
├── COMP478_PROJECT_CODE.ipynb    # Full pipeline: preprocessing → model → evaluation
├── data/
│   └── ultrasound breast classification/   # Dataset (see "Reproduce" below)
├── LICENSE
└── README.md
```

## Reproduce

### Requirements

- Python 3.8+
- Jupyter Notebook or JupyterLab
- The following Python packages:

```bash
pip install numpy pandas scikit-learn matplotlib opencv-python pillow jupyter
```

### Run

```bash
git clone https://github.com/SamanthaGuillemette/COMP478-PROJECT.git
cd COMP478-PROJECT
jupyter notebook COMP478_PROJECT_CODE.ipynb
```

Then run the notebook top-to-bottom. The included dataset folder is referenced via relative paths inside the notebook.

## Why this project

This work sits at the intersection of two of our long-standing interests: computational methods for medical imaging, and breast cancer biology. The Random Forest baseline here is intentionally simple and interpretable — a useful comparison point for the deep-learning approaches that increasingly dominate this space.

## License

MIT — see [`LICENSE`](./LICENSE).

## Authors

This project was completed as a two-person team for COMP 478 at Concordia University.

| Name | GitHub |
|---|---|
| Samantha Guillemette | [@SamanthaGuillemette](https://github.com/SamanthaGuillemette) |
| Saleha Tariq | [@salehatrq](https://github.com/salehatrq) |
