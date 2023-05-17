# Extended Project Grading

| Criteria | Weighting (%) | Score | Justification | Improvements |
|----------|---------------|-------|---------------|---------------|
|Code runs | 5 | 5 | | |
|Data preparation | 5 | 5 | Good preprocessing largely carried forward from the previous project but well adapted to continuous LOS response
|DT method(s) have been used | 10 | 10 | DT, XGboost, random forests adaboost and GBM with explicit arguments for some of the regularises
|Hyperparameter optimization | 10 | 10 | reasonable grid searches for all models - ideally I think you would pick one model and train it slightly more thoroughly
|Ensemble method(s) have been used | 10 | 10 | Stacking of kNN, RF, SVR and linar regression
|Complexity of ensemble used | 10 | 7 | Good variety of weak learners. I would have liked to see considerations of propagating featires to the super learner to see if this could help
|Neural Networks have been used| 10 | 8 | Keras implementation, make sure you investigate whether your neural Network's training has converged
|Complexity of Neural Network used | 10 | 5 | Consideration of grid search over training algorithms, would be good to also consider regularising using either drop out or explicit regularises
|Length of stay is predicted for each test patient | 5 | 5 |
|Accuracy itself | 10 | 6 | < 4.25
|Attempts made to interpret predictions | 5 | 5 | Decision tree feature importance considered, experimentation for SHAP and Lime - would be good to try to do these for your ensemble model. How do the importance compare with the decision trees
|Neat and understandable code| 5 | 3 | Good explanation of preprocessing, I would have liked to see more text showing you understand the models and their outputs though
|Improved Methods from class| 5 | 1 | Keras grid search


Score: 80
