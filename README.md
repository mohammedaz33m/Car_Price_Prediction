# Car_Price_Prediction

![1](https://github-readme-stats.vercel.app/api/top-langs/?username=mohammedaz33m&theme=blue-green)

[![forthebadge made-with-python](http://ForTheBadge.com/images/badges/made-with-python.svg)](https://www.python.org/)


![Issues](https://img.shields.io/github/issues/mohammedaz33m/Car_Price_Prediction?style=plastic) ![forks](https://img.shields.io/github/forks/mohammedaz33m/Car_Price_Prediction?style=plastic) ![stars](https://img.shields.io/github/stars/mohammedaz33m/Car_Price_Prediction?style=plastic)

## For App Demo, please Click the link below:
### https://car-price-prediction-20.herokuapp.com/


![SCREENSHOT](https://github.com/mohammedaz33m/Car_Price_Prediction/blob/main/Images/htmledit.JPG)



## TO DOWNLOAD THE DATASET 
### VIsit : https://www.kaggle.com/nehalbirla/vehicle-dataset-from-cardekho

![SCREENSHOT](https://github.com/mohammedaz33m/Car_Price_Prediction/blob/main/Images/Kaggle_data.JPG)

## STEPS

## Before starting the project it is good to have it in a separate environment- So, to create one:

- > open Anaconda prompt ```base``` is the default location type ```conda create -n your_env_name python = 3.7``` (any_version_number)

![SCREENSHOT](https://github.com/mohammedaz33m/Car_Price_Prediction/blob/main/Images/a0.JPG)

-> Enter "y" when prompted 

![SCREENSHOT](https://github.com/mohammedaz33m/Car_Price_Prediction/blob/main/Images/a1.JPG)

- > It will be decativated upon creation so, activate it again by typing ```activate your_env_name```

- > Change the directory now to whereever you want to save your file ```cd desktop>B-drive>projectfolder```  (This is a dummy path. get your path here) 

![SCREENSHOT](https://github.com/mohammedaz33m/Car_Price_Prediction/blob/main/Images/path.JPG)

- > once in desired location type  ```jupyter notebook```

- > Create a new python file & follow the ```.ipynb``` file from repo

### 1. Load the dataset 
![SCREENSHOT](https://github.com/mohammedaz33m/Car_Price_Prediction/blob/main/Images/initialdata.JPG)

### 2. Perform Exploratory data analysis 
![SCREENSHOT](https://github.com/mohammedaz33m/Car_Price_Prediction/blob/main/Images/nullcheck.JPG)  

![SCREENSHOT](https://github.com/mohammedaz33m/Car_Price_Prediction/blob/main/Images/describe.JPG)  

### 3. Plot visualization
From the graph it is clear that the selling price is more for theose used by lesser number of owners
![SCREENSHOT](https://github.com/mohammedaz33m/Car_Price_Prediction/blob/main/Images/owner.JPG) 


This shows that the price of the cars from recent years have good resale value comared to the older. Quite logical!. 
One of the interesting thing to note here is that the trend eas not quite increasing, for years 2010-2012 there was a decrease in value even when the model was from recent years. #Reality :).

![SCREENSHOT](https://github.com/mohammedaz33m/Car_Price_Prediction/blob/main/Images/year.JPG)
 

From the plot we can observe that, the Vehicle fuel type- ```Diesel``` accounts for the majority of the data set whereas ```petrol``` & ```CNG``` have almost same in numbers, ```petrol``` being slightly greater.

![SCREENSHOT](https://github.com/mohammedaz33m/Car_Price_Prediction/blob/main/Images/fueltype.JPG)


This plot tells about the ```selling price``` vs ```Kms_driven```, we can observe that the most of the range lies within ```10,000 kms```

![SCREENSHOT](https://github.com/mohammedaz33m/Car_Price_Prediction/blob/main/Images/kmdriven.JPG)



### 4. Final dataset 
 ![SCREENSHOT](https://github.com/mohammedaz33m/Car_Price_Prediction/blob/main/Images/finaldata.JPG)

### Final dataset correlationship
 ![SCREENSHOT](https://github.com/mohammedaz33m/Car_Price_Prediction/blob/main/Images/finalcorr.JPG)
 
### 5. Correlation heatmap
 ![SCREENSHOT](https://github.com/mohammedaz33m/Car_Price_Prediction/blob/main/Images/corrheatmap.JPG)
 
### 6. Feature Importance 
 ![SCREENSHOT](https://github.com/mohammedaz33m/Car_Price_Prediction/blob/main/Images/featureimp.JPG)

### 7. Train & plot the predictions
 ![SCREENSHOT](https://github.com/mohammedaz33m/Car_Price_Prediction/blob/main/Images/predictions.JPG)
 
### 8. Results 
 ![SCREENSHOT](https://github.com/mohammedaz33m/Car_Price_Prediction/blob/main/Images/results.JPG)
 
## Exporting & Deployment

### Storing in a Pickle file

```python
import pickle
#open a file to store this data
file=open('random_forest_regression_model1.pk1','wb') # wb-Writebyte mode

#duming the information to this file
pickle.dump(rf_random,file)
```
## Next steps: To create requirements.txt

- > First open Anaconda prompt 

- > activate your env(environment_name) (Enter) 

- > Change directory to the folder of your Jupyter notebook (cd directory name)

- > Once ito the directory of folder type:  ```pip freeze > requirements.txt``` & check in the folder for the.txt file containing all libraries

## Copy these files in your folder

- create a ```app.py``` file (use the one above: copy paste in new JupyterNtebook & download as ```.py``` file)

- Create a ```.html``` file (use from above repo) remember to place this in subfolder```templates``` inside your main folder of project

- Also have ```procfile``` in your repo & have this ```web: gunicorn app:app```- use ```add file``` option in GitHub & save without any extension

### Again open Anaconda prompt

- > Activate your env & then, 

- > type ```pip install flask``` (Enter) 

- > type ```pip install jsonify``` (Enter)

- > type ```pip install requests``` (Enter)

- > Install other files using pip if prompted (example sklearn missing so use```pip install sklearn```)

- > Now change the directory to the project folder where you had saved your JP notebook initially useing ```cd desktop>B-drive>projectfolder``` (This is a dummy path. get your path here)

- > once in the directory typr ```python app.py```
![SCREENSHOT](https://github.com/mohammedaz33m/Car_Price_Prediction/blob/main/Images/app.JPG)

- > When it runs successfully locate the Address ```http://127.0.0.1:5000/```
![SCREENSHOT](https://github.com/mohammedaz33m/Car_Price_Prediction/blob/main/Images/address.JPG)

- > Copy paste the address in any browser window & check the functionality of your app.


# Deployment 

## Visit https://dashboard.heroku.com/apps

### Create new app : give an unique name to move ahead
![SCREENSHOT](https://github.com/mohammedaz33m/Car_Price_Prediction/blob/main/Images/heroku.JPG)

### Go to the deploy section & locate GitHub & connect it to yours if not done earlier.
![SCREENSHOT](https://github.com/mohammedaz33m/Car_Price_Prediction/blob/main/Images/deploy.JPG)

### Then write your repositiory name & hit deploy branch.
![SCREENSHOT](https://github.com/mohammedaz33m/Car_Price_Prediction/blob/main/Images/branch.JPG)

### Once it successfully deploys hit View
![SCREENSHOT](https://github.com/mohammedaz33m/Car_Price_Prediction/blob/main/Images/view.JPG)

## The Final outcome
![SCREENSHOT](https://github.com/mohammedaz33m/Car_Price_Prediction/blob/main/Images/final1.png)

   ![SCREENSHOT](https://github.com/mohammedaz33m/Car_Price_Prediction/blob/main/Images/final2.jpg)

## Thank you for your time





- >  Special thanks to Krish Naik for the support
