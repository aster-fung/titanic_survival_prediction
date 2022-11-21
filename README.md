# Welcome to the Titanic Survival Prediction Notebook!



## The Titanic Sinking Disaster:
The sinking of Titanic was one of the deadliest maritime disaster in history. The RMS Titanic with an estimated 2,224 people onboard sank 15 April 1912 in North Atlantic Ocean, resulting in death of more than 1,500 people. The disaster called for major changes in maritime regulations to implement new safety measures for example preparation of excess lifeboats and establishment of International Ice Patrol. 

## The Dataset
The number of casualties of the sinking was reported by newspapers at the time. The British Board of Trade has reported the finalised number of casuality. Kaggle has further prepared the dataset in tabular format to host a competition in prediction model. 

https://www.kaggle.com/competitions/titanic/data

While the competition rewards high prediction accuracy, this notebook also aims to understand the titanic story more in a data science way :) 


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
&ensp;Spouse = husband, wife (mistresses and fiancés were ignored)

Parch: The dataset defines family relations in this way:

Parent = mother, father

Child = daughter, son, stepdaughter, stepson

Some children travelled only with a nanny, therefore parch=0 for them.

## Workflow of this notebook

1. import dataset and python modules
2. exploratory data analysis<br>
    2.1 inspect the dataset<br>
    2.2 explore the features
3. feature engineering and selection
4. declare features and targets for models
5. train "test" split
6. models<br>
    6.1 random forest<br>
    6.2 xgboost
7. model optimization 
8. exporting prediction
9. conclusion
        
### What's new in version 4?
        
major changes: 
- Introduction: Brief introduction to the Titanic disaster 
- Introduction: Information about the dataset
- Workflow overview: added a overview workflow section to guide readers
- EDA(inspect the dataset): added barplot to compare count of survived and loss passengers
- EDA(inspect the dataset): added lineplot of survival/loss count vs family members
- Feature engineering and selection: feature selection with correlation matrix

minor changes
- fixed the numbers of each section
