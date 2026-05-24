# MSc Mathematical Statistics Dissertation

## Understanding Health Insurance Cost Predictions Using Deep Neural Networks, Monte Carlo Simulation and Shapley Values

**Author:** Thabang Bongani Baloyi Junior  
**Programme:** MSc in Mathematical Statistics  
**Institution:** University of the Free State  
**Year:** 2026  
**Research area:** Health insurance analytics, deep learning, Monte Carlo simulation and explainable machine learning

This repository contains the LaTeX source files, figures and Python notebooks for my MSc dissertation in Mathematical Statistics. The dissertation investigates how deep neural networks can be used to predict individual health insurance charges, how Monte Carlo simulation can be used to explore the fitted model beyond the observed sample, and how Shapley-value methods can be used to interpret the model's predictions.

## Overview

The dissertation develops an integrated **DNN, Monte Carlo and Shapley** framework for health insurance cost prediction. A feed-forward deep neural network is trained as a nonlinear regression model for individual insurance charges. Monte Carlo simulation is then used to generate a synthetic policyholder population from fitted input distributions. Finally, Shapley-value attribution is applied to explain how different policyholder characteristics contribute to predicted costs.

The empirical analysis uses a public health insurance benchmark dataset containing **1,000,000 observations** and **11 predictor variables**, including numerical, binary and categorical variables. The modelling workflow includes exploratory data analysis, data partitioning, feature preprocessing, DNN hyperparameter comparison, Monte Carlo simulation, residual-augmented sensitivity analysis and Shapley-based model interpretation.

## Research Motivation

Health insurance cost prediction is not only a predictive modelling problem. It also requires careful interpretation, sensitivity analysis and communication of the drivers behind predicted costs. A neural network may provide a flexible predictive surface, but decision-makers also need to understand how the model behaves under simulated input scenarios and which variables contribute most strongly to high-cost predictions.

This dissertation therefore combines three complementary components:

1. **Deep Neural Networks** for flexible nonlinear regression.
2. **Monte Carlo Simulation** for distributional analysis and synthetic population generation.
3. **Shapley-Value Attribution** for interpretable feature-level explanations.

Together, these components support prediction, simulation and explanation within a single statistical learning framework.

## Repository Structure

```text
.
├── Research Proposal/
│   ├── src/                        # LaTeX source for the research proposal
│   └── Figures/                    # Figures used in the proposal
│
├── Thesis/
│   ├── Cover Page/                 # Dissertation cover page material
│   ├── Chapter 1/                  # Introduction
│   ├── Chapter 2/                  # Literature review
│   │   └── Figures/                # DNN architecture diagrams and related figures
│   ├── Chapter 3/                  # Methods and data
│   │   └── src/                    # Methodology LaTeX source
│   ├── Chapter 4/                  # Results
│   ├── Chapter 5/                  # Conclusion
│   └── Chapter 6/                  # Recommendations
│       └── Figures/                # Supplementary EDA and supporting figures
│
└── Notebooks/
    ├── chapter3_eda_insurance.ipynb             # Exploratory data analysis source notebook
    ├── chapter3_eda_insurance_executed.ipynb    # EDA notebook with executed outputs
    ├── chapter3_eda_insurance_output.ipynb      # Final EDA output notebook
    ├── chapter3_dnn_training.ipynb              # DNN training source notebook
    ├── chapter3_dnn_training_output.ipynb       # DNN training notebook with outputs
    └── chapter3_mc_shapley.ipynb                # Monte Carlo simulation and Shapley analysis
```

## Methodological Components

### 1. Exploratory Data Analysis

The exploratory analysis examines the empirical structure of the health insurance dataset before model fitting. This includes:

- Distributional profiling of numerical and categorical variables.
- Summary statistics for insurance charges and policyholder characteristics.
- Correlation analysis and dependence diagnostics.
- PCA-based diagnostics for structure in the numerical predictors.
- Data partitioning checks for training, validation and test consistency.

### 2. Deep Neural Network Regression

A feed-forward deep neural network is trained to predict individual health insurance charges from policyholder attributes. The modelling pipeline includes:

- Standardisation of numerical inputs.
- Encoding of categorical variables.
- Structured train, validation and test splitting.
- Sequential hyperparameter comparison.
- Comparison of activation functions, learning rates, batch sizes, optimisers and momentum settings.
- Final model evaluation using standard regression performance metrics.

The selected model uses **CELU activation** and **NAdam optimisation**, based on the structured hyperparameter comparison procedure used in the dissertation.

### 3. Monte Carlo Simulation

Monte Carlo simulation is used to propagate variation in policyholder characteristics through the fitted DNN model. The simulation framework includes:

- Fitting marginal input distributions to the training data.
- Generating synthetic policyholder populations from the fitted input law.
- Passing simulated feature vectors through the trained DNN.
- Comparing simulated and empirical distributions.
- Validating the independence-based simulation design through joint-distribution checks.
- Comparing the parametric simulation with bootstrap resampling of full training rows.

This component is used to study how the fitted neural network behaves across a broader input space than the observed sample alone.

### 4. Residual-Augmented Sensitivity Analysis

The residual-augmented analysis examines how fitted residual variability affects the simulated cost distribution. This provides an additional sensitivity check beyond deterministic fitted predictions from the neural network.

### 5. Shapley-Value Attribution

Shapley-value methods are used to interpret the trained DNN by decomposing predictions into feature-level contributions. The analysis includes:

- Gradient-based SHAP attribution for the fitted neural network.
- Aggregation of encoded-feature attributions back to raw variables.
- Global feature-importance summaries.
- Conditional summaries for high-cost predictions.
- Comparison of Shapley rankings under parametric Monte Carlo and bootstrap Monte Carlo designs.

The Shapley analysis is used to connect model predictions with interpretable drivers of health insurance costs.

## Technical Stack

The project uses the following tools and libraries:

| Area | Tools |
| --- | --- |
| Programming | Python 3 |
| Deep Learning | PyTorch |
| Explainability | SHAP |
| Data Processing | pandas, NumPy, scikit-learn |
| Visualisation | Matplotlib, Seaborn |
| Statistical Modelling | Monte Carlo simulation, regression diagnostics, PCA |
| Document Preparation | LaTeX |
| Version Control | Git, GitHub |

## Notebooks

The main computational work is contained in the `Notebooks/` directory.

| Notebook | Purpose |
| --- | --- |
| `chapter3_eda_insurance.ipynb` | Exploratory data analysis source notebook |
| `chapter3_eda_insurance_executed.ipynb` | EDA notebook with executed outputs |
| `chapter3_eda_insurance_output.ipynb` | Final EDA output notebook |
| `chapter3_dnn_training.ipynb` | DNN training and hyperparameter comparison |
| `chapter3_dnn_training_output.ipynb` | Executed DNN training outputs |
| `chapter3_mc_shapley.ipynb` | Monte Carlo simulation, residual sensitivity and Shapley attribution |

## Suggested Environment

The notebooks are designed for a Python 3 environment with the core scientific Python and machine learning stack installed. A typical setup is:

```bash
python -m venv .venv
source .venv/bin/activate
pip install numpy pandas scikit-learn matplotlib seaborn torch shap jupyter
```

For Windows PowerShell, activate the virtual environment with:

```powershell
.venv\Scripts\Activate.ps1
```

Then launch Jupyter:

```bash
jupyter notebook
```

## Suggested Execution Order

To reproduce the analysis, run the notebooks in the following order:

1. `Notebooks/chapter3_eda_insurance.ipynb`
2. `Notebooks/chapter3_dnn_training.ipynb`
3. `Notebooks/chapter3_mc_shapley.ipynb`

The executed notebooks are included to show saved outputs and support review of the empirical workflow.

## Dissertation Chapters

The dissertation is organised as follows:

- **Chapter 1:** Introduction and research background.
- **Chapter 2:** Literature review on deep learning, Monte Carlo simulation, Shapley values and health insurance cost prediction.
- **Chapter 3:** Methodology, data description and empirical design.
- **Chapter 4:** Empirical results and interpretation.
- **Chapter 5:** Conclusion.
- **Chapter 6:** Recommendations and further work.

## Academic Purpose

This repository is intended to support:

- Transparent academic review of the dissertation workflow.
- Reproducibility of the empirical analysis.
- Portfolio evidence for applied statistical learning, health insurance analytics, explainable AI and simulation-based modelling.
- Future development of the dissertation into publishable or extended research work.

## Disclaimer

This repository is part of an academic dissertation. The empirical work uses a public benchmark dataset and is intended for research and educational purposes. The results should not be interpreted as an operational underwriting, pricing or actuarial reserving model for a specific insurer.

## Author

**Thabang Bongani Baloyi Junior**  
MSc Mathematical Statistics  
University of the Free State

GitHub: [thabangTheActuaryCoder](https://github.com/thabangTheActuaryCoder)
