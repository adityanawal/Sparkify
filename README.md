# Sparkify: Exploring churn in a music streaming service

## Motivation

Predicting when a user is about to cancel or downgrade their service can be a make or break event for a service, especially streaming ones that have plenty of competition in the market. This project will sxplore one such service, termed Sparkify !, and see if we can use a machine learning model to predict such events, so that one can take action to prevent them.  
  
  
I have a blog post on this [here](https://link.medium.com/rzdfDrOcyab) for an overview.

### Key Questions Asked :  

1.) Which features in the dataset will be relevant for analyzing churn ?  
2.) Can we predict churn events with a machine learning model ?  
3.) Which model will be best for predicting the churn metric ?

## Files Included  
1.) **Sparkify.ipynb** : A jupyter notebook file with the code  
2.) **mini_sparkify_event_data.zip** : The dataset used for the analysis. Please unzip before using. All rights reserved with Udacity.  
3.) Churn and not_churn.pkl Pickle files : Used for storing feature transformed datasets for easier modeling. Not required - generated in the code.  

## Prerequisites  
### Languages :  
Python 3  
Apache Spark  

### Libraries
Pandas  
Plotly  
Numpy  
ua-parser  

### Optional  
Jupyter Notebook  

## Summary of the Results :

Features Chosen :  
1.) **Categorical Features**: Gender, Level (free vs paid), Browser and Platform (OS). State and City were initially considered but there were too many categories if we considered them, so they were dropped.  

2.) **Numerical features** : Page events (Add friend, Add to Playlist etc), No. of songs, No. of artists, No. of sessions, listening time, age (how long the person has been a user for).   

Two approaches were chosen :   
1.) **User Based**: Modeling the differences between users based on their overall behavior  
2.) **Event Based**: Time sensitive, modeling the features that led up to the churn event.   
  
Two Models were used :   
1.) **Logistic Regression**  
2.) **Random Forest (& Gradient Boosted Trees)**  
  
  
In the end, the second approach turned out to have more accurate results, with the Logistic regression model the better option.  
![Results Image](https://github.com/adityanawal/Sparkify/blob/main/results.JPG)

## Authors
Aditya Nawalgaria

## Acknowledgments
The team of the [Udacity Nanodegree program](www.udacity.com)  
