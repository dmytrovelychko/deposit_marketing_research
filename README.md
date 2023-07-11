# Bank marketing deposit subscription research
## Task
Marketing campaigns are an essential part of the business. This is also true for banking services. Meanwhile, the estimation of marketing campaign performance and prediction of performance is a challenging task. Based on historical data related to direct marketing campaigns of a Portuguese banking institution try to predict subscription for deposit

Metrics: As for subscription prediction, we can't prefer precision or recall and the task is about binary classification, ROC AUC score will be used.

ROC AUC score >= 80%

Dataset for research available [here](https://archive.ics.uci.edu/dataset/222/bank+marketing)

## Technics used:
- EDA: Pair and multi-feature
- Preprocessing: data imputation, manual feature selection
- ML: Logistic regression, Random forest classifier, XGBClassifier, hyperparameters optimization, cross-validation

## Conclusion:
- XGBClassifier and RandomForest has close result metrics, but xgb performance is faster and has better result in generalization
- dataset is highly unbalanced and the model worse predict subscription results than NOT subscription
- model which is part of the business process requires more information about context and workflows
- social and economic context attributes highly correlated between each other or almost not correlated with subscription
- subscription results of marketing can have a seasonal bias which is poorly represented in the current dataset, it needs to be enriched with more features
- seasonable and timeline of contacts with clients during the current and previous campaigns should be done as separate research and possibly be used for building separate models to be used in ensembles for subscription prediction as can have a significant impact
- usage and proportion of records with previous and current campaign data needs to be taken into account during the designing of a prediction model
- possible improvements can be:
  - testing other types of models or ensembles
  - drop previous campaign information
  - enrich with more features that can correlate with the client's ability to subscribe with a deposit
  - make additional research about phone calls and seasonability of marketing campaign, investigate contact feature
