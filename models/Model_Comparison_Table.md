| Modello                                     | Precision (classe 1) | Recall (classe 1) | F1-score (classe 1) | Accuracy | ROC-AUC |
|--------------------------------------------|-----------------------|--------------------|----------------------|----------|---------|
| 1. Dummy Classifier                         | 0.00                  | 0.00               | 0.00                 | 0.96     | 0.500   |
| 2. Heuristic Model                          | 0.0733                | 0.0354             | 0.0477               | 0.9485   | 0.5092  |
| 3. Logistic Regression                      | 0.00                  | 0.00               | 0.00                 | 0.96     | 0.6224  |
| 4. KNN (k=5) - numeric only                 | 0.09                  | 0.00               | 0.00                 | 0.96     | 0.5127  |
| 5. KNN + SMOTE (full dataset)              | 0.74                  | 1.00               | 0.85                 | 0.82     | 0.9479  |
| 6. KNN + SMOTE (only train)                | 0.04                  | 0.36               | 0.07                 | 0.66     | 0.5212  |
| 7. Random Forest (base)                    | 0.00                  | 0.00               | 0.00                 | 0.96     | 0.5799  |
| 7b. Random Forest (modificato, no SMOTE)   | 0.07                  | 0.59               | 0.13                 | 0.72     | 0.7182  |
| 8. Random Forest (tuned + SMOTE)           | 0.06                  | 0.02               | 0.03                 | 0.95     | 0.5637  |
| 9. XGBoost (scale_pos_weight)              | 0.06                  | 0.56               | 0.10                 | 0.64     | 0.6391  |
|10. XGBoost (tuned + scale_pos_weight)      | 0.06                  | 0.54               | 0.10                 | 0.65     | 0.6351  |
|11. XGBoost (SMOTE, no scale_pos_weight)    | 0.07                  | 0.00               | 0.01                 | 0.96     | 0.5010  |
|12. Voting Classifier (soft, no weights)     | 0.05                  | 0.27               | 0.08                 | 0.78     | 0.5580  |
|13. Voting Classifier (soft, weighted 3-2-1) | 0.06                  | 0.09               | 0.07                 | 0.91     | 0.5684  |
