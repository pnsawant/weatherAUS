# Rainfall Prdiction Program

## Stuff - 
1. weatherAUS.csv (data file)
2. weatherAUS.ipynb (ML code)
3. /pickles (pickled model & preprocessors)
4. /web-app (code for deployed web app)
5. requirements.txt (list of packages)
6. /img (screenshot of web app)

## How to?
* Download zip of repo
* Create virtual env with ```pip -m venv <name-of-env>```
* Install packages with ```pip install -r requirements.txt```
* Run ```jupyter notebook``` in command line to see the code of weatherAUS.ipynb
* To check the deployed app locally firstly run ```cd ./web-app/``` & then ```python ./app.py```

## Deployed web app -
You can access the web app with the link - https://weather-aus.herokuapp.com/

Screenshot - 

![Web-App](https://github.com/sprsd/weatherAUS/blob/main/img/screenshot.PNG)

## About Code - 
### Preprocessing - 
* Interpolation & simple imputation with mean is done for numerical data
* Before label encoding of catgorical data it was imputed with mapping & interpolation for nomial data while imputation with mode for ordinal data
* The outliers in continous feature data were removed with IQR method after label encoding
### Model Creation - 
* Several models were tried; list of which is -
  1. Logistic regression
  2. Support vector machine (SVM)
  3. Decision tree
  4. Random forest classifier
  5. XGBoost Classifier
  6. CatBoost Classifier
* Feature scaling for logistic regression & SVM was done

## Conclusion - 
The model with CatBoost Classifier was found to work better as compared to other models & hence used for deploying.
  

