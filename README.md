# ZIMNAT-Insurance-Recommendation
## BUSINESS OBJECTIVE 
For insurance markets to work well, insurance companies need to be able to pool and spread risk across a broad customer base. This works best where the population to be insured is diverse and large. In Africa, formal insurance against risk has been hampered by lack of private sector companies offering insurance, with no way to diversify and pool risk across populations.

Understanding the varied insurance needs of a population, and matching them to appropriate products offered by insurance companies, makes insurance more effective and makes insurance companies more successful.

At the heart of this, understanding the consumer of insurance products helps insurance companies refine, diversify, and market their product offerings. Increased data collection and improved data science tools offer the chance to greatly improve this understanding.

WE will leverage data and ML methods to improve market outcomes for insurance provider Zimnat, by matching consumer needs with product offerings in the Zimbabwean insurance market. Zimnat wants an ML model to use customer data to predict which kinds of insurance products to recommend to customers. The company has provided data on nearly 40,000 customers who have purchased two or more insurance products from Zimnat.

Our challenge: for around 10,000 customers in the test set, we are given all but one of the products they own, and are asked to make predictions around which products are most likely to be the missing product. This same model can then be applied to any customer to identify insurance products that might be useful to them given their current profile.

## Data 
For both train and test, each row corresponds to a customer, assigned a unique customer ID (‘ID’). There is some information on the customer (when they joined, birth year etc). The customer’s occupation (‘occupation_code’) and occupation category (‘occupation_category_code’) are also provided, along with the branch code of the office they visit. The final 21 columns correspond to the 21 products on offer.

In Train, there is a 1 in the relevant column for each product that a customer has. Test is similar, except that for each customer ONE product has been removed (the 1 replaced with a 0). Your goal is to build a model to predict the missing product.

SampleSubmission shows the required submission format. For each customer ID, for each product, you must predict the likelihood that that product is one in use by the customer. Notice that the sample submission contains 1s for the products that are included in the test set, so that you can focus on the unknown products


Files available in data folder:

SampleSubmission.csv - is an example of what your submission file should look like. The order of the rows does not matter, but the names of the ID must be correct.
Train.csv - this is the file you will use to train your model.
Test.csv - this is the file you will use to test your model.
VariableDefintions.txt - descriptions of the variables

## Baselines
- baseline-1 with xgbosst loss - 1.41
- baseline 2 xgboost + considering the correlation between the products by summing up the the product values
loss -1.33
- baseline-3 xgboost + considering the correlation between the products by taking the index of the product that they actually subscribe to the products as integer loss 1.58
- baseline-4 xgboost + train the model by all train data without splitting loss -1.47



## Reference
- Catboost
https://www.kaggle.com/rajaswa/simple-catboost-classifier
https://www.kaggle.com/prashant111/catboost-classifier-in-python
- Predicting Purchased Policy for Customers in Allstate Purchase Prediction Challenge on Kaggle
  https://worldconferences.net/proceedings/aics2014/PAPER%20AICS/A049%20-%20PREDICTING%20PURCHASED%20POLICY%20-%20SABA%20ARSLAN.pdf
- How to improve model during kaggle challenge 
  https://github.com/justmarkham/kaggle-allstate/blob/master/allstate-presentation.pdf
- Complete Guide to Parameter Tuning in XGBoost with codes in Python (also see 1, 2) 3) 
https://www.analyticsvidhya.com/blog/2016/03/complete-guide-parameter-tuning-xgboost-with-codes-python/
- Stack Machine Learning Models - Get Better Results
https://mlfromscratch.com/model-stacking-explained/#/
- Ensemble Learning to Improve Machine Learning Results
https://blog.statsbot.co/ensemble-learning-d1dcd548e936?gi=8e1cbcc93959
- Stacking Classifiers for Higher Predictive Performance
https://towardsdatascience.com/stacking-classifiers-for-higher-predictive-performance-566f963e4840
- Fine-tuning XGBoost in Python like a boss
https://towardsdatascience.com/fine-tuning-xgboost-in-python-like-a-boss-b4543ed8b1e
- 8 Proven Ways for improving the “Accuracy” of a Machine Learning Model
https://www.analyticsvidhya.com/blog/2015/12/improve-machine-learning-results/
- How To Fine Tune Your Machine Learning Models To Improve Forecasting Accuracy
https://www.kdnuggets.com/2019/01/fine-tune-machine-learning-models-forecasting.html
- Mathematical on Boosting and other ML models: https://statweb.stanford.edu/~jhf/ftp/trebst
