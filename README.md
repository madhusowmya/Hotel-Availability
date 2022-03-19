# Hotel-Availability
Predicting yearly availability of hotels, based on their features.


Conclusion
variable selection:
Dropped the latitude, longitude as they are granular and already represented by the region.
id, owner_id as they are irrelavent for prediction
No significant correlation is observed among the given features
Data Pre-Processing :
Filled the missing values in the number_of_reviews with 0's as reviews_per_month as 0
Performed standard scaler on numerical variables, label encoding on categorical variables
Model Building:
Used below classifiers to predict yearly_availability to train and validate the data
Built logisitic regression as base model with 84% accuracy, then performed hyper parameter tuning using Kfold, grid search techniques on the following classifiers and their accuracies are as shown below.

  1. Decision tree classifiers - 92.06
  2. Random forest classifiers  -92.8
  3. XGBoost classifier - 92.4
Model Interpretaton:
From the Random Forest classifiers results seems to be best model
As the Random forest model is built using multiple number of decision trees, it is not prone to overfitting, outlier, and will be more stable.
Also, From feature importance, we can infer that accomodation_type_private_room, owned_hotels, review_per_month seems to be highly effecting the yearly_availability.
