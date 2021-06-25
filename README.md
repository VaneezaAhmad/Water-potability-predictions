# Water Potability

This project predicts whether water is safe to drink ot not. A dataset from is taken kaggle.com which has 10 features and approximately 3500 observations. Mutliple Machine learning classification models were trained on the data to predict the accuracy and precision of the data to determine the potability of water. 


## Features 
    1. pH value: PH is an important parameter in evaluating the acid–base balance of water
    2. Hardness: Hardness is mainly caused by calcium and magnesium salts.
    3. Solids (Total Dissolved solids):
    4. Chloramines: Chloramine and chlorine are the major disinfectants used in public water systems.
    5. Sulfate: Sulfates are naturally occurring substances that are found in minerals, soil, and rocks.
    6. Conductivity: Conductivity is a measure of the ability of water to pass an electrical current
    7. Organic_carbon: Total Organic Carbon (TOC) is a measure of the total amount of carbon in organic compounds in pure water
    8. Trihalomethanes: Trihalomethanes (THMs) are the result of a reaction between the chlorine used for disinfecting tap water and natural organic matter in the water. 
    9. Turbidity: Turbidity is the measure of relative clarity of a liquid
    10. Potability (Target Variable): Indicates if water is drinkable, 1 = potable, 0 = not potable
  
  
## Model
15 classification models were used to train the data. Some performed better than others. The model that perfomed the best was Random Forest. It had an accuracy and precision of over 65%. Polynomial features of degree 2 was used to feature engineer. Grid search with cross Validation was used, to try different combinations of hyperparameters to tune the model for the best results. 

![alt text](https://github.com/VaneezaAhmad/Water-potability-predictions/blob/master/images/best_model.png)


## Business case 
We tried to reduce features to check if there was any kind of relationship between two features and the target. Something evident in ph against Sulfate and Chloramines. The rule is that if the product of their z scores is positive then the water is not potable and if it’s negative the water is potable.

![alt text](https://github.com/VaneezaAhmad/Water-potability-predictions/blob/master/images/busi_rule.png)
![alt text](https://github.com/VaneezaAhmad/Water-potability-predictions/blob/master/images/3d.png)


### Files in the Repository 
1. [Potability_EDA.ipynb](https://github.com/VaneezaAhmad/Water-potability-predictions/blob/master/Potability%20EDA%20.ipynb) is the main notebook. 
2. [water.ipynb](https://github.com/VaneezaAhmad/Water-potability-predictions/blob/master/water.ipynb) is the data testing notebook. 
3. [Predicting Water potability](https://github.com/VaneezaAhmad/Water-potability-predictions/blob/master/Predicting%20Water%20Potability.pptx) is the presentation. 
4. The folder [Data](https://github.com/VaneezaAhmad/Water-potability-predictions/tree/master/Data) contains:
    1. [Water_potability.csv](https://github.com/VaneezaAhmad/Water-potability-predictions/blob/master/Data/water_potability.csv): Contains whole Dataset
    2. [model_set.csv](https://github.com/VaneezaAhmad/Water-potability-predictions/blob/master/Data/model_set.csv): Contains 75% of the data from the whole dataset to train the dataset.
    3. [holdout_set.csv](https://github.com/VaneezaAhmad/Water-potability-predictions/blob/master/Data/holdout_set.csv): Contains 25% of the data from the whole dataset to test dataset on the best model from training set.
    4. [water_predictions.csv](https://github.com/VaneezaAhmad/Water-potability-predictions/blob/master/Data/water_predictions.csv): Contains predictions from holdout_set. 

### Authors 

[Clare Dunne](http://github.com/clareadunne)

[Vaneeza Ahmad](https://github.com/VaneezaAhmad)
