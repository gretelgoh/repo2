# Project README

# Project Title
BERT model for binary classification of emotion and non-emotion sentences in English dramatic literature

## Overview

This repository contains the code, datasets, and analysis results for the project. The repository includes notebooks for model fine-tuning, inference, evaluation, modernization, and interrater reliability, as well as the processed dataset and results of the analyses.

The files are organized into three main categories:

* **Code** — Jupyter notebooks used to process data, fine-tune and evaluate models.
* **Dataset** — Processed sentences from the **DraCor English corpus**, including the full dataset and the train/test split.
* **Results** — Outputs from the model evaluations, modernization evaluations.

---

## Reproducibility

The Jupyter notebooks document the different stages of the computational workflow. To reproduce the analyses, the notebooks should generally be executed in the order corresponding to the workflow:

1. Prepare/use the processed dataset.
2. Create or use the train/test split.
3. Fine-tune the model using `code_finetune.ipynb`.
4. Run model inference using `code_inferencing.ipynb`.
5. Generate modernization outputs using `code_modernizeAPI.ipynb`, where applicable.
6. Evaluate the models using `code_model_eval.ipynb`.
7. Evaluate modernization outputs using `code_modernize_eval.ipynb`.
8. Calculate interrater reliability using `code_interrater.ipynb`.
9. Use the resulting data for the play- and speaker-level analyses.

## Workflow

The general workflow of the project is:

```text
DraCor English Corpus
        │
        ▼
Processed sentences
        │
        ▼
dataset_full.csv
        │
        ├──────────────► dataset_train_test.csv
        │                       │
        │                       ▼
        │                Model fine-tuning
        │                       │
        │                       ▼
        │                Model inference
        │
        ▼
Modernization / Analysis
        │
        ├──────────────► Model evaluation
        │
        ├──────────────► Modernization evaluation
        │
        ├──────────────► Interrater reliability
        │
        └──────────────► DraCor play/speaker analysis
                                │
                                ▼
                             Results
```

## File Overview

For convenience, the complete repository can be summarized as follows:

```text
.
├── code_finetune.ipynb
├── code_inferencing.ipynb
├── code_interrater.ipynb
├── code_model_eval.ipynb
├── code_modernize_eval.ipynb
├── code_modernizeAPI.ipynb
│
├── dataset_full.csv
├── dataset_train_test.csv
│
├── results_model_eval.xlsx
├── results_modernize_eval.xlsx
├── results_play_DR.csv
└── results_speaker_DR_centrality.csv
```

## Repository Description

### Code

The following Jupyter notebooks contain the code.

| File                        | Description                                                                                              |
| --------------------------- | -------------------------------------------------------------------------------------------------------- |
| `code_finetune.ipynb`       | Code for fine-tuning the language model on the project dataset.                                          |
| `code_inferencing.ipynb`    | Code for running inference with the fine-tuned/model(s) and generating predictions or outputs.           |
| `code_interrater.ipynb`     | Code for calculating **interrater reliability**, used to assess the agreement between annotators.        |
| `code_model_eval.ipynb`     | Code for evaluating the performance of the model(s).                                                     |
| `code_modernize_eval.ipynb` | Code for evaluating the modernization outputs, including comparisons of model-generated modernized text. |
| `code_modernizeAPI.ipynb`   | Code for using the modernization API to generate modernized versions of the texts.                       |

---

## Dataset

### `dataset_full.csv`
The dataset is based on the **DraCor English corpus**, a collection of dramatic texts that can be used for computational analysis of plays and their characters, speakers, and dialogue.
The dataset contains extracted and processed sentences that are used for analysis.
The file containing the **full processed dataset** used in the project can be accessed via https://zenodo.org/records/21905873 



### `dataset_train_test.csv`

This file contains the **training and test split** of the dataset for model training and evaluation.


## Results

The `results` files contain the outputs produced by the analyses conducted in the project.

### `results_modernize_eval.xlsx`

Contains the results of the **modernization evaluation**.
These results are generated using `code_modernize_eval.ipynb` and contain the evaluation of the generated modernized text.

### `results_model_eval.xlsx`

Results of the **model evaluation**.
These results are generated using `code_model_eval.ipynb` and provide the evaluation outcomes for the out-of-box models.

### `results_play_DR.csv`

Contains the results of the **play-level analysis** for the DraCor dataset.

### `results_speaker_DR_centrality.csv`

Contains the results of the **speaker-level network analysis**, including speaker centrality measures for the DraCor plays.



### Quick Reference

| Category                     | Files                                                                                 |
| ---------------------------- | ------------------------------------------------------------------------------------- |
| **Fine-tuning**              | `code_finetune.ipynb`                                                                 |
| **Inference**                | `code_inferencing.ipynb`                                                              |
| **Interrater reliability**   | `code_interrater.ipynb`                                                               |
| **Model evaluation**         | `code_model_eval.ipynb`, `results_model_eval.xlsx`                                    |
| **Modernization**            | `code_modernizeAPI.ipynb`, `code_modernize_eval.ipynb`, `results_modernize_eval.xlsx` |
| **Full dataset**             | `dataset_full.csv`                                                                    |
| **Train/test dataset**       | `dataset_train_test.csv`                                                              |
| **Play-level analysis**      | `results_play_DR.csv`                                                                 |
| **Speaker/network analysis** | `results_speaker_DR_centrality.csv`                                                   |

---


---


