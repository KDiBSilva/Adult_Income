# Adult Income


### Examining Connections for Adults Earning an Income Greater or Less than 50K for a Non- Profit Organization.
Kristina DiBella Silva


There are multiple variables that account for annual income. This Non-profit wanted to use this dataset to explore the probability of an individual's income being higher or lower than $50,000, regardless of gender or cultural background. We are exploring the dataset to find what behaviors can earn an adult a higher income and what may restrict them. As well as evaluating the trends of discrimination

___

### Data Source
Information and dataset found from Kaggle:
https://www.kaggle.com/datasets/wenruliu/adult-income-dataset

Dataset information also resourced from UCI: 
https://archive.ics.uci.edu/ml/datasets/adult

For this dataset, there were 48842 rows and 15 columns.

### Data Dictionary
![image](https://github.com/KDiBSilva/Adult_Income/assets/122838459/762eb71a-7554-461d-b533-67d0f7206dcf)

This is the original Data Dictionary, however through exploration of the dataset a few adjustments were made. 
___


![image](https://github.com/KDiBSilva/Adult_Income/assets/122838459/c2665885-fec9-4ff1-baac-031578e6ee0f)

Occupation being a key factor for annual income, this bar plot shows the number of each employment role and their income level. We see that in this dataset the males are more likely to earn a higher income. We also see that for both genders the highest wages are within the "Exec-managerial" and "Prof-specialty" roles. In this dataset there is a higher count of observations for males which is what can show such a contrast, but still a notable observation. 

![image](https://github.com/KDiBSilva/Adult_Income/assets/122838459/47145825-a95e-4455-a51e-00b1032c9333)

There are females achieving the same levels of education. The imbalance is one factor but another thing to consider would be the amount of time in the career field as experience can determine a person's wages regardless of gender. 


![image](https://github.com/KDiBSilva/Adult_Income/assets/122838459/80ee9fa8-9566-4b65-a837-dd54a7525b95)


A step before a high paying job is the education to obtain these roles. This visual tells us that the level of education is indeed a factor for individuals earning greater than 50K. There is a higher count of instances of earning 50K or less, for those with PreK- High School completion of education. Whereas a Bachelors has the highest count of an income greater than 50K. People with an education from a Professional School or obtained their Masters or Doctorate have a consistent trend of income greater than 50K. Education is not a widely available opportunity in all countries and the amount of variables to pursue such extensive education can be a burden and a hardship on income and lifestyle, when sizable time is being taken for a particular career choice.

This Education column was condensed for data efficiency and Machine Learning performance. Values were reduced from 16 to 7 unique observations.


![image](https://github.com/KDiBSilva/Adult_Income/assets/122838459/60f9d0fc-95f8-4c06-ac62-b220cebec679)

This Continent feature previously reflected the native country for each individual, however this was compacted to continent for further use in our machine learning models. This dataset did not have any countries listed for the continent of Africa. We see a strong presence of individuals from North America, they are also observed to have the greater count of income over 50K. South America having the least. We saw in the previous plot that there were not many instances of higher education in Asia, Europe and South America which could be a correlated factor of these individuals not earning a higher income.
___
#### Models Tested
* K- Nearest Neighbors Classifier
* Logistic Regression
* Decision Tree Classifier
* Random Forest Classifier

#### Decision Tree Classifier was the chosen model

For Test Performance Scoring:

- Accuracy: 0.857092	

- Recall: 0.592288	

- Precision: 0.778508	

- F1 Score: 0.672749

Decision Tree Tuned Model has the second highest accuracy score of 85.7%. Random Forest was first with a slight increase of 85.8%.

Random Forest had more true negatives but Decision Tree had more true positives. Which is something all models struggled with, predicting true positives(income greater than 50K). With an off-balanced dataset it's important to more accurately capture the true positives as it is the lesser group, Decision Tree also had more false positives. Although this model is not perfect, the performance to determine the positive class, either true or false, is helpful in evaluating an imbalanced dataset. Determining whether an individual is likely to earn an income greater than 50K or equal to 50K or less. 



# Recommendations 

All models are  lacking in the ability to predict True Positives. This can be that the dataset is off balance with a greater number of individuals with an income of 50K or less. We could balance the data with under sampling to make the 50K or less match the greater than 50K observations, this would be the preferred method, instead of duplicating or randomizing additional data to the greater than 50K group to match the less than or equal to 50K group.

