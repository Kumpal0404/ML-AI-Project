# Prediction of the target column "N AufgewAmplitudeNom [MPa]"

This project investigates optimal hyperparameter selection and feature selection techniques to improve model performance for a regression-based and AI-based predections problem. Two models were evaluated: a Decision Tree Regressor and a Neural Network, with detailed comparisons of their performance under different tuning strategies.

##  Authors  
- **Kumpal Ganeshbhai Khokhariya**

  
## Decision Tree Regressor
- Best Hyperparameters: max_depth=21, min_samples_split=2, min_samples_leaf=1
- Training Performance: MSE = 0.036, MAE = 0.050, R² = 0.999
- Testing Performance: MSE = 2.853, MAE = 1.075, R² = 0.931

Observation: Achieved excellent predictive accuracy, with strong generalization and minimal variance between training and testing results.

## Neural Network
- Best Hyperparameters: hidden1_size=32, hidden2_size=64, learning_rate=0.001, num_epochs=100, batch_size=32, dropout_rate=0.2
- Training Performance: MSE = 34.352, MAE = 3.902, R² = 0.229
- Testing Performance: MSE = 32.633, MAE = 3.921, R² = 0.214

Observation: The neural network underperformed compared to the decision tree, showing high bias and limited predictive power despite hyperparameter tuning.

## Feature Selection Comparison
| Method                              | Features | Alpha (Lasso) | MSE       | MAE       | R²        |
| ----------------------------------- | -------- | ------------- | --------- | --------- | --------- |
| Mutual Information                  | 50–17    | –             | \~5.1     | \~1.5     | \~0.87    |
| Lasso                               | –        | 0.001–0.01    | 3.07–4.63 | 1.16–1.43 | 0.89–0.93 |
| Recursive Feature Elimination (RFE) | 50–17    | –             | **2.853** | **1.075** | **0.931** |

## Final Results
- Best Model: Decision Tree Regressor (R² = 0.931 on test data).
- Feature Selection: Recursive Feature Elimination (RFE) with 17 features is most effective.

## Software and Dependencies
- numpy
- pandas
- matplotlib
- scikit-learn
- tensorflow
- torch
- streamlit
- jupyter Notebook

## Future Work
- Further optimization of neural network architectures.
- Exploration of advanced feature selection methods.
- Experimentation with alternative ML/DL models and hyperparameter search strategies.

## License
This project is licensed under the MIT License. See the LICENSE file for details.
  
## Folder Contents
- `ProjectWork-Kumpal_khokhariya.ipynb` → Main notebook
- `ProjectWork-Kumpal_khokhariya.pdf` → PDF export of the notebook


