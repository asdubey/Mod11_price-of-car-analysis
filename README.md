# Mod11_price-of-car-analysis

# What factors impact the used car price?

![](images/kurt.jpeg)

Overview
This project is intended to provide the recommendation to the dealers on what does consumer value most when they purchase used cars. This will help the dealership to stock appropriate inventory and improve sales along with profit margins.

### CRISP-DM Framework
Used the CRISP-DM framework for this project. CRISP-DM (Cross Industry Standard Process for Data Mining) is a widely used framework for data science and machine learning projects. It provides a structured approach to solving data-driven problems and consists of six major phases - Business understanding, Data understanding, data preparation, modeling, evaluation and deployment.

<center>
    <img src = images/crisp.png width = 50%/>
</center>


### Business Understanding

For the used car market there is fierce competition and profitability of business highly depends on the rotation of the inventory. For this business to be successful dealerships need to sell the car sooner and at higher prices. In order to achieve this they stock the right cars. So, accurately predicting the price of the car becomes essential. The goal of this exercise would be to identify the key features which can help with this prediction.

### Data understanding

The original dataset contained information on 3 million used cars and is available on Kaggle. From this dataset a smaller set of 426K cars was extracted for faster processing. 

### Data description
1. **id**: Identifier for each car sale record.
2. **region**: The geographic region where the car is sold.
3. **price**: The sale price of the car.
4. **year**: The year in which car was manufactured.
5. **manufacturer**: The brand or manufacturer of the car.
6. **model**: The model of the car.
7. **condition**: The condition of the car.
8. **cylinders**: The number of cylinders in the engine.
9. **fuel**: The type of fuel the car uses (gas, diesel, electric, hybrid, etc.).
10. **odometer**: The mileage of the car (how much the car has been driven in miles or km).
11. **title_status**: The status of the car's title (clean, salvage, rebuilt, etc.).
12. **transmission**: The type of transmission (other, automatic, manual, etc.).
13. **VIN**: The Vehicle Identification Number, a unique code given to every vehicle.
14. **drive**: The type of drivetrain (fwd, awd, rwd, 4wd, etc.).
15. **size**: The size category of the car (compact, mid-size, full-size, etc.).
16. **type**: The type or category of the car (truck, sedan, SUV, hatchback, van, etc.).
17. **paint_color**: The exterior color of the car.
18. **state**: The state where the car was sold.

### Data Preparation

- During this phase the data cleaning was performed, i.e removing null data and features of less to no significance.
- Dataset was split into 70/30 training to test ratio to be used for modeling.
- Data transformation was performed on many features e.g. various type of encoding, scaling and polynomial feature.

### Modeling

During this phase various modeling techniques were used and scored. Goal is to identify the appropriate predictive model for forecasting. This was little challenging due to number of features available. Had to adjust features to come up with better models.


### Evaluation 

In this phase the evaluation of the models was performed. Scores of different type of modeling techniques were compared. My observation is that the LinearRegression performed slightly better than the Ridge or Lasso model. For best Ridge model alpha as 10 was best score. Following are the details : 

. LinearRegression: Cross-validation RMSE = 6068.6658

- Evaluate the best models on the test set
- LinearRegression: RMSE = 6036.1497, R2 = 0.7105

2. Ridge : {'alpha': 10.0}, RMSE = 6068.7236

- Evaluate the best models on the test set
- Ridge: RMSE = 6036.1477, R2 = 0.7105


3. Lasso : {'alpha': 10.0}, RMSE = 6068.7236

- Evaluate the best models on the test set
- Lasso: RMSE = 6036.1477, R2 = 0.7105

### Conclusion 

Based on the data analysis and model evaluations , we understand now which features influence the decision of the customer most. Using this dealership can optimize their process and improve the sales.

1. Age of the vehicle has the most significant impact. Newer model sells for highest prices. Maintain such inventory will help with the profit increase.
2. How much has the car been driven. In this case lesser the better.
3. Number of cylinders has positive impact, i.e. more the number of cylinder or bigger the engine higher the price.
4. Diesel cars sold for higher price than any other fuel type.


### Future

There were many features which had little to no impact on the prediction of the price. Analysis should be performed by removing such features. If the prediction can include the actual make and model, it will be easier for dealership to target the vehicles.