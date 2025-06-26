# 🐱 Cat Breed Classification with KNIME  

> **Clasificación de razas de gatos mediante técnicas de aprendizaje automático en KNIME**  

![KNIME](https://img.shields.io/badge/No-Code-KNIME-yellow?logo=knime&logoColor=white)
![License](https://img.shields.io/github/license/LynxPardelle/KNIMECatBreedsMachineLearning)

## Table of Contents

1. [Project Overview](#project-overview)  
2. [Dataset](#dataset)  
3. [Exploratory Data Analysis](#exploratory-data-analysis)  
4. [Modeling](#modeling)  
5. [Evaluation](#evaluation)  
6. [Conclusions & Reflections](#conclusions--reflections)  
7. [Reproducibility](#reproducibility)  
8. [Future Work](#future-work)  
9. [Citation](#citation)  
10. [License](#license)  

---

## Project Overview

This repository contains a **no-code data-science project built entirely in KNIME Analytics Platform**.  
The goal is to **predict the breed of a cat**—_Angora_, _Maine Coon_ or _Ragdoll_—using physical and behavioural attributes such as:

* Weight & Body Length  
* Eye & Fur colours  
* Country of origin  
* Preferred food, etc.  

The entire pipeline—data ingestion, cleaning, feature engineering, model training and evaluation—has been implemented through KNIME nodes, requiring **zero traditional coding**.

---

## Dataset

| Property | Value |
|----------|-------|
| **Source** | Kaggle – [It’s Raining Cats](https://www.kaggle.com/datasets/joannanplkrk/its-raining-cats) |
| **File**  | `cat_breeds_clean.csv` |
| **Records** | **1 071** rows |
| **Target** | `Breed` (Angora • Maine Coon • Ragdoll) |
| **Key Features** | `Weight`, `Body_length`, `Age_in_years`, `Eye_colour`, `Fur_colour_dominant`, `Country`, … |

---

## Exploratory Data Analysis

* **Scatter Plot**: Weight vs Body_length, colored by Breed.
* **Box Plot**: Distribution of weight per breed.

These plots revealed distinct clusters, especially for Ragdoll cats.

---

## Modeling

* **Model Used**: Decision Tree (Gini index)
* **Split**: 70% training / 30% test using `Partitioning` node
* **Tooling**: Native KNIME nodes (`Decision Tree Learner`, `Predictor`, etc.)

---

## Evaluation

### Confusion Matrix

| Actual \\ Predicted | Angora | Maine Coon | Ragdoll |
|---------------------|--------|------------|---------|
| Angora              | 86     | 2          | 0       |
| Maine Coon          | 2      | 100        | 1       |
| Ragdoll             | 0      | 0          | 131     |

### Performance Metrics

* **Accuracy**: 0.984
* **F-Measure (avg)**: 0.984
* **Cohen's Kappa**: 0.976
* **Recall**: All classes ≥ 0.971

---

## Conclusions & Reflections

- Physical features like weight and body length were highly influential.
- Decision Tree provided explainable, high-accuracy classification.
- KNIME enabled a fully traceable workflow without writing code.
- The tool is suitable for both educational and professional data projects.

---

## Reproducibility

1. Download [KNIME Analytics Platform](https://www.knime.com/downloads) (v4.7+)
2. Clone this repo:

```bash
git clone https://github.com/LynxPardelle/KNIMECatBreedsMachineLearning
```

3. Open workflow/CatBreedClassification.knwf in KNIME.
4. Press ▶️ to execute the full pipeline.

## Future Work

- Try ensemble methods (Random Forest, Gradient Boosting)
- Perform cross-validation for robust results
- pand dataset with more breeds and records

## Citation

Montaño Romero, Alec Jonathan (2025).
Clasificación de razas de gatos mediante técnicas de aprendizaje automático en KNIME.
[Repo](https://github.com/LynxPardelle/KNIMECatBreedsMachineLearning)

## License

This project is licensed under the MIT License. See the LICENSE file for details.
