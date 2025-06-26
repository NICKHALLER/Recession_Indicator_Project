# macro_indicator_project
## Using macroeconomic indicators to explore relationships and predict recessions

objective: To analyze data using exploratory data analysis (correlation heat maps, time series graphs), random forest and logistic models


data:
quarterly economic data since 1954 from Federal Reserve Economic Data
  - GDP Growth
  - Unemployment Rate
  - Federal Funds Rate
  - Yield Curve (10-year minus 3-month Treasury)
  - Consumer Sentiment
  - CPI Year-over-Year Inflation
  - NBER-defined Recession Indicator (binary)


EDA:
- Time series plots show how each indicator behaves around recessions
- Distribution comparisons reveal different patterns between recession and non-recession periods
- Correlation analysis shows the strongest predictors were:
  - Sentiment (negative, lag 0)
  - Fed Funds Rate (positive, lag 2–3)
  - Yield Curve (negative, lag 3–4)
  - CPI YoY (positive, lag 1)


Modeling:

Logistic Regression
- Accuracy: ~0.77  
- AUC: 0.78  
- Weak recall (0.00) and poor precision — failed to identify recessions well  
- Tended to classify all cases as non-recession

Random Forest Classifier
- Accuracy: 0.79  
- AUC: 0.79  
- Recall: 0.50 (caught 50% of recessions in test set)  
- Precision remained low — tradeoff between catching recessions and false positives

Evaluation Metrics
- Confusion matrix  
- Precision, recall, accuracy  
- Type I error rate (false positive rate)  
- ROC curve with AUC (Area under curve, higher is better)

Conclusion:
Predicting recessions is challenging using basic data and with my skillset, also since they are so rare it is hard to effectively identify one.
Random forest modeling out performed logistic regression in AUC, accuracy, and recall
Sentiment, Yield Curve, and Federal Funds rate were most predictive with varying lags
improvement could be made with resampling, data enginneering, and more advanced models


Nick Haller - Data Science and Math at University of Wisconsin-Madison
