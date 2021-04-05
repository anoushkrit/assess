# Assessment 

## 1. Visualise


## 2. Clean

## Observations

1. While finding the values like mean, median , top, I further go to know that columns are not of int64 type where they need to be, hence , going back to the first cell and changing the type of the columns to int / float where required. 
2. Column Names in calcium and calciumcorrect pose a mismatch with the key error due to the CAPS letter names. 
3. Spelling mistake in column names
   

## 3. Predict

**3. Predict adults and revenue (amount_in_usd*adults) using data from here using any ML/DL algorithm and also share your thought process behind selecting an algorithm, feature etc**

Output Label: `adults` and `revenue`
Input Label: 

### Preprocessing 

1. Removing the redundant columns which only have the same value in all of the rows.
2. Also removing colummns which won't carry any significant value as the predictor
3. In the case of `order_no` it was used initially in the regressor becasue it was having multiple values, somewhat like a passenger booked a ride to and fro and had different destination. Also was not unique in its values. But was unique row entry. 

But after seeing that it is affecting the regressor badly because of its high variance and the amount of information it is carrying. 

<img src = "https://miro.medium.com/max/1250/1*Q0PrzYheyZTU4E0Og5AW4A.png" width = 600>

### Model 

#### 1. Decision Tree Regressor
   The first choice was decision regressor because of a good combination of ordinal and categorical variables being in the dependent variables. 

   However, as we know Decision Tree Regressor works better for huge amount of data and overfits on less data. Hence, this is what happened and the score turned out to be 1.0, completely overfitting. 


#### 2. Random Forest Regressor 

To combat the overfitting but actually this may increase the accuracy which is already overfitted. 

With Random Forest Regressor we again get the score of 1.0. 



