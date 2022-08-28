# Descripton of Features
Our original dataset contained twelve different features. We chose to focus on and keep four of these features for our machine learning model. Those 
features were passenger ID, whether the passenger survived or not, passenger gender, and the economic class of each passenger. For this project, our team
wanted to see if we were able to predict survival of passengers aboard the Titanic based on passenger gender and economic class. These specific features
were chosen due to our background knowledge of the Titanic and that women and children were two of the groups to be ushered to safety first. Additionally,
we also inferred that higher class ranking passengers would more likely have a higher change of survival given the placement of their cabins (upper deck) on the boat
as well as their socio-economic status and privelege may have also allowed them a spot on a lifeboat.
Given that we knew the outcome of the survival rate of the passengers, we were able to use a supervised machine learning method with "Survival" as our target feature.
## Removed Data
![image](https://user-images.githubusercontent.com/102090016/187089166-73227925-4d56-4e4d-a10b-32893efc61a3.png)

Several columns from the original dataset were removed due to the presence of a large amount of null values and/or not aligning with the variables we wished to analyze.
From the image we can see that two columns were missing a significant amount of data. This lead us to remove the age column as it was not a variable we were looking at,
and the cabin number of each passenger as there were too many missing rows and we felt that data was not relevant to our study.
We removed two columns (Passenger Name and ticket number) due to the vast amount of unique values. The name of passengers is a string variable and is unable to pass through the machine learning model. Ticket number was also removed as each ticket number was unique to the passenger and would skew the data with that many unique data
points. Four more columns that held no relevance to our hypotheses were removed: sibsp (# of siblings / spouses aboard the Titanic), parch (# of parents / children aboard the Titanic), embarked (Port of Embarkation), and fare (passenger fare). Passenger fare was removed due to its redundancy with the class variable. 

## Data Split
Our dateset was pre-split into a train and test dataset by the data source. The test set contained data on 418 passengers and the train set held data on the remaining 891 passengers.


