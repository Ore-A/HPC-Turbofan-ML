# HPC Turbofan Engine Performance Optimization

## Table of Contents
- [Project Overview](#project-overview)
- [Why?](#why)
- [Code Structure](#code-structure)
- [Results](#results)
- [Multidisciplinary Optimization Approach](#multidisciplinary-optimization-approach)
- [Repository Files](#repository-files)
- [Usage](#usage)
- [Author](#author)

## Project Overview
This project aims to optimize the performance of a turbofan engine by analyzing and predicting its net thrust using machine learning techniques. Specifically, a Random Forest Regressor was used to indicate the net thrust and identify the most significant features contributing to engine performance. Subsequently, a scenario analysis was conducted to explore potential improvements in net thrust through feature adjustments.

## Why?
With advancements in aerospace technology, optimizing engine performance is crucial for enhancing fuel efficiency, reducing emissions, and ensuring reliability. This project leverages machine learning to gain insights into the key factors affecting engine thrust and explores how minor adjustments can lead to significant performance improvements.

## Code Structure
### 1. Data Loading and Preparation
- The dataset is loaded from a CSV file containing various parameters of a turbofan engine.

### 2. Feature Selection
- Correlation analysis is performed to select the most relevant features.
- Columns with low correlation to the target variable `NetThrust_kN` are identified and dropped to streamline the analysis.
- Selected features were used to define the feature matrix `X` and the target vector `y`.

### 3. Exploratory Data Analysis
- Pair plots are generated to visualize relationships between key features and the target variable `NetThrust_kN`.
- This step helps in understanding the data distribution and identifying potential correlations.

### 4. Model Training and Hyperparameter Tuning
- The dataset is split into training and testing sets.
- A Random Forest Regressor is chosen as a model for its robustness and ability to handle complex interactions between features.
- Grid Search with cross-validation is employed to find the optimal number of estimators for better performance.
- The final model is trained using the optimal parameters obtained from Grid Search.

### 5. Model Evaluation
- The final model is evaluated using Mean Absolute Error (MAE), Mean Squared Error (MSE), and R-squared metrics.
- Cross-validation is performed to ensure the model's reliability and robustness.
- Feature importance was analyzed to identify the most significant features affecting `NetThrust`.

### 6. Scenario Analysis
- A scenario analysis is conducted by adjusting the top three significant features identified from feature importance.
- Each feature is increased by 5%, and the impact on net thrust is predicted.
- The average improvement in net thrust is calculated and compared to the original predictions.

## Results
- The scenario analysis demonstrated an average improvement of 2.81% in net thrust by adjusting the top three features.
- The results highlighted the potential for performance optimization through targeted adjustments.

## Multidisciplinary Optimization Approach
This project implicitly employed a Multidisciplinary Optimization (MDO) approach by integrating and optimizing multiple interacting subsystems of the turbofan engine. The dataset included parameters from various aspects of engine performance, such as fuel consumption, nozzle velocities, and burner efficiency. By analyzing the interactions between these features and adjusting the most influential ones, the project demonstrated how targeted adjustments could lead to overall performance improvements.

## Repository Files
- `Turbofan_HPC_Efficiency.csv`: The dataset containing various parameters of the turbofan engine.
- `HPC_Turbofan_Engine_Performance_Optimization.ipynb`: Jupyter notebook with the full code implementation.
- `output.png`: Visual comparison of original and scenario predictions.
- `README.md`: This file, providing an overview of the project.

## Usage
1. Clone the repository.
2. Ensure you have the required libraries installed (`numpy`, `pandas`, `scikit-learn`, `seaborn`, `matplotlib`).
3. Open the Jupyter notebook `HPC_Turbofan_Engine_Performance_Optimization.ipynb` and run the cells sequentially.
4. Review the results and visualizations generated.

## Author
- Oreoluwa Abejide













