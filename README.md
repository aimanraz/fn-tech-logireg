# Directing Customers to Subscription Through App Behavior Analysis
In present market, most of companies have a mobile presence which is an app. Some companies provide free products/services in their mobile apps in an attempt to transition customers to a paid/pro membership. For this case study we will categorize 3 things:
* Market or the target audience, this refers to the users who installed and also used the company's mobile app.
* Product/Paid membership. It often provide enhanced version of the free products already given for free, with the new features.
* Goal, the objective of this analysis is to use machine learning to predict which users will not subsribe to the paid membership, so that marketing department increase the effort to go into trying "persuade/convert" them to paid or pro users.

## Code and Resources Used 
**Python Version:** 3.8++

**Packages:** pandas, numpy, sklearn, matplotlib, seaborn.

## Data Collection and Description
The customer's app behaviour data consist of two csv files obtained from [SuperDataScience](https://www.superdatascience.com/courses) courses which also available on internet. The data for this project are manufactured fields based on trends found in real world case studies. The fields describe what companies usually track from their user, and the distribution are based on observed distributions in real world analysis. The appdata10.csv dataset provide us some attributes which are:
* *user* -> the user id
* *first_open* -> the day the user first open the app, when the user join, have time stamp
* *dayofweek* -> range 1-7, monday-sunday
* *hour* -> 24hr based 
* *age* -> the user age 
* *screen_list* -> describe every screen name that user have visited in the first 24 hrs
* *numscreens* -> basically len(screen_list), total screen list visited
* *minigame* -> this app has a minigame, 1 - user play the game in first 24 hrs, 0 - not play it
* *used_premium_feature* - 1 - if the user used any premium features of free-trial, 0 - never used
* *enrolled* -> 1 - the user ended up subscribed to the premium/pro version, 0 - they dont ended up subscribed
* *enrolled_date* -> the date they subscribed/enrolled with time stamp
* *liked* -> 1 - if the user any particular feature, 0 - if doesn't

While the top_screens.csv dataset provide a list of top visited screen from user.

## Data Cleaning and EDA
Standard data cleaning framework is applied such as null filtering, correcting data type and etc.

### Histograms of Numerical Columns

![Bar overall](https://github.com/aimanraz/fn-tech-logireg/blob/main/img/histogram_overall.png)

### Correlation Bar Chart with response
Some interesting insight can be drawn from this bar chart which are:
* More hour spend on app will likely make user not subscribe.
* Older people less likely to subscribe.
* More premium features used will tend make user less likely to subscribed (red flag for the pro features).

![Correlation bar](https://github.com/aimanraz/fn-tech-logireg/blob/main/img/correlation_bar.png)

### Correlation matrix

![Correlation matrix](https://github.com/aimanraz/fn-tech-logireg/blob/main/img/correlation_heatmap.png)

## Model Performance
By applying 10-fold cross validation, the model only able to achieve the final accuracy of 77.30 % with a standard deviation of +/- 0.012.

![]()

## Conclusion
The model were successfully developed. It can be used to further validated the the results by running th prediction on daily new installs, and see whther the accuracy is consistent or not. From there, the company can narrow the marketing efforts only to users 'unlikely' to subscribe.

let the data drive you...and beyond.
