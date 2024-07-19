
1. Acquire labelled or annotated data
	-  [[Gold Standard Data]]
2. Consider [[Ethical Considerations in ML]]
3. Perform [[Data Cleaning]]
4. Validation in small datasets
	- [[Cross-validation]]
5. Analyze Data and features using visualizations, dimension reduction
6. Perform [[Feature Engineering]]
7. Shortlist models
	-  pick complexity of the model for the perfect [[bias-variance tradeoff]]
8. Fine tune the model
	 - set [[Hyperparameters]]
		 - data transformations & feature engineering are hyperparameters too
		 - perform **random search**, **grid search**
		 - Automatic hyper parameterization using [[Auto-ML]]
9. Fit on training + validation data, test on test data
10. Pick best performing model or **aggregate** models via [[Ensemble methods]]
11. [[Evaluation of ML systems]]