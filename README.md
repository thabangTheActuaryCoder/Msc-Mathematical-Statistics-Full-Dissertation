  ---                                                                                                                                                                                                                
  MSc Mathematical Statistics - Full Dissertation                                                                                                                                                                    
                                                                                                                                                                                                                     
  University of the Free State                                                                                                                                                                                           
  MSc in Mathematical Statistics (2026)                                                                                                                                                                            
                                                                                                                                                                                                                     
  Title                                                                                                                                                                                                            

  Understanding Health Insurance Cost Predictions Using Deep Neural Networks, Monte Carlo Simulation and Shapley Values

  Repository Structure

  .
  ├── Research Proposal/
  │   ├── src/                        # LaTeX source for research proposal
  │   └── Figures/
  ├── Thesis/
  │   ├── Cover Page/
  │   ├── Chapter 1/                  # Introduction
  │   ├── Chapter 2/                  # Literature Review
  │   │   └── Figures/                # DNN architecture diagrams
  │   ├── Chapter 3/                  # Methods and Data
  │   │   └── src/                    # Methodology LaTeX source
  │   ├── Chapter 4/                  # Results
  │   ├── Chapter 5/                  # Conclusion
  │   └── Chapter 6/                  # Recommendations
  │       └── Figures/                # Supplementary EDA figures
  └── Notebooks/
      ├── chapter3_eda_insurance.ipynb             # Exploratory data analysis (source)
      ├── chapter3_eda_insurance_executed.ipynb    # EDA with executed outputs
      ├── chapter3_eda_insurance_output.ipynb      # EDA final output
      ├── chapter3_dnn_training.ipynb              # DNN training (source)
      ├── chapter3_dnn_training_output.ipynb       # DNN training with outputs
      └── chapter3_mc_shapley.ipynb                # Monte Carlo simulation and Shapley analysis

  Overview

  This dissertation investigates the use of deep neural network (DNN) regression for predicting individual health insurance charges, combined with Monte Carlo simulation to generate a synthetic policyholder
  population and Shapley-value attribution to explain the fitted model's predictions.

  The empirical analysis is conducted on a public health insurance benchmark dataset containing 1,000,000 observations and 11 predictor variables (numerical, binary and categorical). A feed-forward DNN with CELU
  activation and NAdam optimisation is trained and evaluated using a structured hyperparameter comparison procedure.

  Key Components

  - Exploratory Data Analysis: Distributional profiling, correlation analysis, PCA diagnostics and data partitioning validation.
  - DNN Regression: Feed-forward neural network trained on standardised inputs with sequential hyperparameter selection across activation function, learning rate, batch size, optimiser and momentum.
  - Monte Carlo Simulation: Parametric simulation using product-marginal fitted distributions, with joint-distribution validation and bootstrap resampling comparison.
  - Residual-Augmented Sensitivity Analysis: Sensitivity of the simulated cost distribution to fitted residual variability.
  - Shapley-Value Attribution: Gradient-based SHAP explanations aggregated from encoded features to raw variables, with global and high-cost conditional summaries.

  Technical Stack

  - Language: Python 3
  - Deep Learning: PyTorch
  - Explainability: SHAP (SHapley Additive exPlanations)
  - Visualisation: Matplotlib, Seaborn
  - Data Processing: pandas, NumPy, scikit-learn
  - Document Preparation: LaTeX

  Author

  Thabang Bongani Baloyi Junior
  MSc Mathematical Statistics, University of the Free State
