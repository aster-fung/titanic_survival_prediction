# Welcome to the Titanic Survival Prediction Notebook!


This notebook is also available on Kaggle: 

https://www.kaggle.com/code/asterfung/titanic-eda-randomforest-gridsearch


## The Titanic Sinking Disaster:
The sinking of Titanic was one of the deadliest maritime disaster in history. The RMS Titanic with an estimated 2,224 people onboard sank 15 April 1912 in North Atlantic Ocean, resulting in death of more than 1,500 people. The disaster called for major changes in maritime regulations to implement new safety measures for example preparation of excess lifeboats and establishment of International Ice Patrol. 

While the competition rewards high prediction accuracy, this notebook also aims to understand the titanic story :) 


## The Dataset
The number of casualties of the sinking was reported by newspapers at the time. The British Board of Trade has reported the finalised number of casuality. Kaggle has further prepared the dataset in tabular format to host a competition in prediction model. 

https://www.kaggle.com/competitions/titanic/data

Below is the dataset description (courtesy of the Kaggle team):

### Data Dictionary

| **Variable** | **Definition**                             | **Key **                                       |
|--------------|--------------------------------------------|------------------------------------------------|
| survival     | Survival                                   | 0 = No, 1 = Yes                                |
| pclass       | Ticket class                               | 1 = 1st, 2 = 2nd, 3 = 3rd                      |
| sex          | Sex                                        |                                                |
| Age          | Age in years                               |                                                |
| sibsp        | # of siblings / spouses aboard the Titanic |                                                |
| parch        | # of parents / children aboard the Titanic |                                                |
| ticket       | Ticket number                              |                                                |
| fare         | Passenger fare                             |                                                |
| cabin        | Cabin number                               |                                                |
| embarked     | Port of Embarkation                        | C = Cherbourg, Q = Queenstown, S = Southampton |



### Variable Notes:

Pclass: A proxy for socio-economic status (SES)

    1st = Upper
    2nd = Middle
    3rd = Lower

Age: <BR>
    <t>Age is fractional if less than 1. If the age is estimated, is it in the form of xx.5

Sibsp: The dataset defines family relations in this way:

&ensp;Sibling = brother, sister, stepbrother, stepsister<br>
&ensp;Spouse = husband, wife (mistresses and fianc??s were ignored)

Parch: The dataset defines family relations in this way:

Parent = mother, father

Child = daughter, son, stepdaughter, stepson

Some children travelled only with a nanny, therefore parch=0 for them.
        
### What's new in version 4?
        
major updates
- Introduction: Brief introduction to the Titanic disaster 
- Introduction: Information about the dataset
- workflow overview: added a overview workflow section to guide readers
- EDA(inspect the dataset): added barplot to compare count of survived and loss passengers
- EDA(inspect the dataset): added lineplot of survival/loss count vs family members
- Feature engineering and selection: feature selection with correlation matrix and mutual information gain
- model optimization: gridsearch tune random forest parameters
- summarized findings in Highlights and Conclusion

minor changes
- fixed the numbers of each section
- cleared up some useless code

# Highlights


A random forest model was built to predict whether a passenger onboard Titanic could survive the Titanic disaster. The probability of surviving is half of the probability of dying during the disaster. Among various factors, the age, sex and the type of ticket were the most important factors that correlates to survivial. 

More details:
* From the test dataset, in a total of 891 passengers onboard, 342 passengers (38.27%) survived the titantic disaster and 549 passengers (61.68%) was lost.
* Younger passengers were more likely to survive the Titanic (p<0.05, T test). The mean age of the passengers who survived was 28.344 and that of those who were lost was 30.627. 
* Survial chance was partly determined by the ticket fare ( as implied in passenger class). Those passengers who survived paid more then those who were lost ( p<0.01, Mann-Whitney test). The mean fare paid by the survived group (37.8 pounds) was nearly a double of the mean fare paid by those who were lost in the Titanic disaster (19.72 pounds)
* Correlation study show that some features are correlated: Titles and Age, Fare and Pclass

## Workflow of this notebook

1. Import dataset and python modules
2. Exploratory data analysis<br>
    2.1 Inspect the dataset<br>
    2.2 Explore the features
3. Feature engineering and selection
4. Declare features and targets for models
5. Train "test" split
6. Models<br>
    6.1 Random forest<br>
    6.2 Xgboost
7. Model optimization 
8. Exporting prediction
9. Conclusion
10. Acknowledgements and reference