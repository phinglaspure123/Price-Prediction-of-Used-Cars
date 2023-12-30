
# Used Car Price Prediction

This project aims to predict the selling price of used cars based on various features using decision tree regression and random forest regression models.




## Features

### Target Variable

##### Selling_Price:
- Type: Numerical (Target Variable)
- Description: The price at which the car is ultimately sold.
- Significance: The main goal of the project is to predict this value accurately using the other features.

### Predictor Variables:

##### Car_Name:
- Type: Categorical
- Description: The name or model of the car 
- Significance: While not directly influencing price

##### Year:
- Type: Numerical
- Description: The year the car was manufactured.
- Significance: Newer cars generally command higher prices

##### Present_Price:
- Type: Numerical
- Description: The current price at which the car is being offered for sale.
- Significance: Reflects the seller's initial valuation of the car

#####  Kms_Driven:
- Type: Numerical
- Description: The total distance the car has been driven, typically measured in kilometers.
- Significance: Higher mileage often indicates more wear and tear, potentially reducing the car's value.

##### Fuel_Type:
- Type: Categorical
- Description: The type of fuel the car uses (e.g., petrol, diesel, CNG, electric).
- Significance: Fuel type can significantly impact price due to fuel efficiency, running costs.

##### Seller_Type:
- Type: Categorical
- Description: Indicates whether the seller is an individual or a dealer.
- Significance: Dealer prices might be higher due to overhead costs and potential warranties, but individual sellers might offer more flexibility in negotiation.

##### Transmission:
- Type: Categorical
- Description: The type of transmission the car has (e.g., manual, automatic).
- Significance: Automatic transmissions are often preferred for convenience, potentially commanding higher prices.

##### Owner:
- Type: Categorical
- Description: Indicates whether the car has had previous owners or is being sold by the first owner.
- Significance: First-owner cars might be perceived as better maintained and fetch higher prices.
## Data source

* kaggel:https://www.kaggle.com/code/pushpakhinglaspure/price-prediction-of-used-cars/input


## Model Development

### Decision Tree Regression:
Train a decision tree regression model using the training set.
- Advantages: Easy to interpret, works well with various data types, handles non-linear relationships.
- Disadvantages: Prone to overfitting, susceptible to changes in training data, less accurate compared to more sophisticated models.
#### Adjust hyperparameters:
- max_features: Number of features to consider at each split (e.g.,"sqrt", "log2").
- max_depth: Maximum depth of the tree (control overfitting).
- min_samples_split: Minimum samples required to split a node.
- min_samples_leaf: Minimum samples required at a leaf node.

### Random Forest Regression:
Train a random forest model, an ensemble of decision trees.
- Advantages: More robust to overfitting than decision trees, better accuracy due to ensemble learning, less sensitive to noise in data.
#### Adjust similar hyperparameters as in decision trees, plus:
- n_estimators: Number of trees in the forest.

## Residual Analysis
#### Decision Tree
![App Screenshot](https://www.kaggleusercontent.com/kf/157060995/eyJhbGciOiJkaXIiLCJlbmMiOiJBMTI4Q0JDLUhTMjU2In0..A1L6AwR1kuV2-j3gfhMGIw.8gfNdXD43ps8Hs6cTg4O1Lbj7X_A95rfzonre8sOhN4d--2kJ2TbUqEhM38iK5GxMEyYmVFRXaZFKw085vaKaMyvPi7ii6D3zKgzdiMITK-u3n-n_vuG0gzqPvrse-DJ-cJawOVUs-GNirxcheY2dD3Hk48x0WqbKWyomGwr6fkV7uCR5ILnix9FEyvNTCzhWRJVyYww6T8zE1885IKsbj3bsrqKZUhAj5t5gtkKowWQqXa-An5J98c92iyLk-zJyvXUJo5ZX_LowYX4O6YyZGDFpYmoN3hEAAwGs13NYOWZxwSLl8JnUM37yBMckGMXHp4NI-geqSMMDLJmuLxKIrPT6XWZc4nYY-vjMAmx8n-GLN8GqPuE9_Tq8sf792gbzG7IcTxcohteox95xcS_2Y0I6GGVd6ToZUv340v-5X9bFog76NF12Et0A-Ps3GuS69auMpcBS29A_SLqFrCF5NyKfvaq_Bf0rW7piHMaugblcA1xIHci1vUPwOWoNYTAVa1jYvRtMY86s_3xp8eaTuaewVHIwgdBfxh9pUC30K7AGayFl7i4tuA4ehXi8068NsQfeH_1GR3egkBMw6xKXOl3qZnaFmyNRoxu57HsLuBDqU4MTfAGODgf-SLAymxv1tccvlvquSjsHRVcmvWIP1wHdYlybsGX3zJ2WiJE-Uo8tDiLUuMqBGICgLnyjzdi.H7yMobnlAd8JTYxR-cGmQw/__results___files/__results___65_1.png)


![App Screenshot](https://www.kaggleusercontent.com/kf/157060995/eyJhbGciOiJkaXIiLCJlbmMiOiJBMTI4Q0JDLUhTMjU2In0..A1L6AwR1kuV2-j3gfhMGIw.8gfNdXD43ps8Hs6cTg4O1Lbj7X_A95rfzonre8sOhN4d--2kJ2TbUqEhM38iK5GxMEyYmVFRXaZFKw085vaKaMyvPi7ii6D3zKgzdiMITK-u3n-n_vuG0gzqPvrse-DJ-cJawOVUs-GNirxcheY2dD3Hk48x0WqbKWyomGwr6fkV7uCR5ILnix9FEyvNTCzhWRJVyYww6T8zE1885IKsbj3bsrqKZUhAj5t5gtkKowWQqXa-An5J98c92iyLk-zJyvXUJo5ZX_LowYX4O6YyZGDFpYmoN3hEAAwGs13NYOWZxwSLl8JnUM37yBMckGMXHp4NI-geqSMMDLJmuLxKIrPT6XWZc4nYY-vjMAmx8n-GLN8GqPuE9_Tq8sf792gbzG7IcTxcohteox95xcS_2Y0I6GGVd6ToZUv340v-5X9bFog76NF12Et0A-Ps3GuS69auMpcBS29A_SLqFrCF5NyKfvaq_Bf0rW7piHMaugblcA1xIHci1vUPwOWoNYTAVa1jYvRtMY86s_3xp8eaTuaewVHIwgdBfxh9pUC30K7AGayFl7i4tuA4ehXi8068NsQfeH_1GR3egkBMw6xKXOl3qZnaFmyNRoxu57HsLuBDqU4MTfAGODgf-SLAymxv1tccvlvquSjsHRVcmvWIP1wHdYlybsGX3zJ2WiJE-Uo8tDiLUuMqBGICgLnyjzdi.H7yMobnlAd8JTYxR-cGmQw/__results___files/__results___62_1.png)

#

#### Random Forest

![App Screenshot](https://www.kaggleusercontent.com/kf/157060995/eyJhbGciOiJkaXIiLCJlbmMiOiJBMTI4Q0JDLUhTMjU2In0..A1L6AwR1kuV2-j3gfhMGIw.8gfNdXD43ps8Hs6cTg4O1Lbj7X_A95rfzonre8sOhN4d--2kJ2TbUqEhM38iK5GxMEyYmVFRXaZFKw085vaKaMyvPi7ii6D3zKgzdiMITK-u3n-n_vuG0gzqPvrse-DJ-cJawOVUs-GNirxcheY2dD3Hk48x0WqbKWyomGwr6fkV7uCR5ILnix9FEyvNTCzhWRJVyYww6T8zE1885IKsbj3bsrqKZUhAj5t5gtkKowWQqXa-An5J98c92iyLk-zJyvXUJo5ZX_LowYX4O6YyZGDFpYmoN3hEAAwGs13NYOWZxwSLl8JnUM37yBMckGMXHp4NI-geqSMMDLJmuLxKIrPT6XWZc4nYY-vjMAmx8n-GLN8GqPuE9_Tq8sf792gbzG7IcTxcohteox95xcS_2Y0I6GGVd6ToZUv340v-5X9bFog76NF12Et0A-Ps3GuS69auMpcBS29A_SLqFrCF5NyKfvaq_Bf0rW7piHMaugblcA1xIHci1vUPwOWoNYTAVa1jYvRtMY86s_3xp8eaTuaewVHIwgdBfxh9pUC30K7AGayFl7i4tuA4ehXi8068NsQfeH_1GR3egkBMw6xKXOl3qZnaFmyNRoxu57HsLuBDqU4MTfAGODgf-SLAymxv1tccvlvquSjsHRVcmvWIP1wHdYlybsGX3zJ2WiJE-Uo8tDiLUuMqBGICgLnyjzdi.H7yMobnlAd8JTYxR-cGmQw/__results___files/__results___80_1.png)



![App Screenshot](https://www.kaggleusercontent.com/kf/157060995/eyJhbGciOiJkaXIiLCJlbmMiOiJBMTI4Q0JDLUhTMjU2In0..A1L6AwR1kuV2-j3gfhMGIw.8gfNdXD43ps8Hs6cTg4O1Lbj7X_A95rfzonre8sOhN4d--2kJ2TbUqEhM38iK5GxMEyYmVFRXaZFKw085vaKaMyvPi7ii6D3zKgzdiMITK-u3n-n_vuG0gzqPvrse-DJ-cJawOVUs-GNirxcheY2dD3Hk48x0WqbKWyomGwr6fkV7uCR5ILnix9FEyvNTCzhWRJVyYww6T8zE1885IKsbj3bsrqKZUhAj5t5gtkKowWQqXa-An5J98c92iyLk-zJyvXUJo5ZX_LowYX4O6YyZGDFpYmoN3hEAAwGs13NYOWZxwSLl8JnUM37yBMckGMXHp4NI-geqSMMDLJmuLxKIrPT6XWZc4nYY-vjMAmx8n-GLN8GqPuE9_Tq8sf792gbzG7IcTxcohteox95xcS_2Y0I6GGVd6ToZUv340v-5X9bFog76NF12Et0A-Ps3GuS69auMpcBS29A_SLqFrCF5NyKfvaq_Bf0rW7piHMaugblcA1xIHci1vUPwOWoNYTAVa1jYvRtMY86s_3xp8eaTuaewVHIwgdBfxh9pUC30K7AGayFl7i4tuA4ehXi8068NsQfeH_1GR3egkBMw6xKXOl3qZnaFmyNRoxu57HsLuBDqU4MTfAGODgf-SLAymxv1tccvlvquSjsHRVcmvWIP1wHdYlybsGX3zJ2WiJE-Uo8tDiLUuMqBGICgLnyjzdi.H7yMobnlAd8JTYxR-cGmQw/__results___files/__results___82_1.png)



## Potential Applications

##### Used Car Market:

- Buyers: Estimate a fair price for used cars before purchase, preventing overpaying or missing good deals.
- Sellers: Set competitive asking prices based on market data and car characteristics, increasing the speed of sale.

##### Automotive Industry:

- Analyze demand and pricing trends for different car models and segments.

##### Personal Finance:

- Track depreciation of owned vehicles for financial planning and investment decisions.

##### Research and Development:

- Study the relationship between car features, ownership history, and market value.
- Develop improved car valuation models for specific demographics or regions.
- Provide data insights for developing sustainable car ownership and recycling practices.
## 🔗 Links
[![linkedin](https://img.shields.io/badge/linkedin-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/pushpakhinglaspure)

 [![Kaggel](https://cdn.iconscout.com/icon/free/png-256/free-kaggle-3521526-2945029.png)](https://www.kaggle.com/pushpakhinglaspure)

