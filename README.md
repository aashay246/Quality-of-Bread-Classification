# Quality-of-Bread-Classification
Classified the quality of bread (numerically represented between 3-8) into three categories - Low, Medium and Good

Our quality of bread dataset consisted of 12 variables including dependent variables (i.e. quality of bread). 

### Step 1

Identified the top three parameters in correlation with the quality of bread using correlation matrix. 

<img src="https://github.com/aashay246/Quality-of-Bread-Classification/blob/main/Corr_all.png" width="400"/>

The top three factors are:-
1. Alcohol Content
2. Sulphates Content
3. Volatile Acidity 

#### For better visualization of the relation between the three predictors and the quality of bread, we used box plot approach as all variables are continuous variables.

1. Increase in the alcohol content of the mixture increase the quality of bread as seen in the figure below:

<img src="https://github.com/aashay246/Quality-of-Bread-Classification/blob/main/AvQ.PNG" width="400"/>

2. Similarily, an increase in the sulphates content of the mixture increase the quality of bread as seen in the figure below:

<img src="https://github.com/aashay246/Quality-of-Bread-Classification/blob/main/SvQ.PNG" width="400"/>

3. However, an increase in the volatile acidity of the mixture decreased the quality of bread as seen in the figure below:

<img src="https://github.com/aashay246/Quality-of-Bread-Classification/blob/main/VvQ.PNG" width="400"/>

## Step 2

Check if the predictor variables follows normal distribution. This was achieved using "scipy.stats.normaltest"

If the variable followed a normal distribution (i.e. p-value > 0.05) then we would use StandardScalar to transform the data, otherwise we apply MinMax Scaler. 
Since the p-value for three selected variables were less than 0.05 we utilized MinMax Scaler to transform the data. 

The selected vairables were then transformed to a range between 0 and 1 using MinMax Scaler. This techniques maintains the shape of the distribution. 

<img src="https://github.com/aashay246/Quality-of-Bread-Classification/blob/main/Min_Max_Scaler.PNG" width="800"/>

