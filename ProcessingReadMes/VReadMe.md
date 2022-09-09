## Titanic_Panic

# Machine Learning of Titanic Data
Our project uses machine learning to determine survival rates aboard the Titanic. We selected this dataset based on our interest in the historical event and using the detailed information to make machine learning predictions. Our data source is from [Kaggle](https://www.kaggle.com/competitions/titanic/data) and includes 12 columns of nearly 900 rows about individual passengers. For each passenger, there is information about their survival status, age, gender, class, and even the fare he or she paid for the trip. We focused on the variables of gender and class to predict the likelihood of survival. The original dataset is split into multiple CSV files and required merging via SQL Joins. 

# Hypothesis and Questions
* Hypothesis: The class of passenger impacts the survival rate aboard the Titanic.
* Alternative: The gender of passengers impacts the survival rate aboard the Titanic. 
* Null Hypothesis: The class of passenger does not impact the survival rate aboard the Titanic. 
* Does gender impact survival odds aboard the Titanic? 
* Does class of passenger impact survival odds aboard the Titanic?
* Can we achieve an machine learning accuracy rate above 80%?

# Preliminary Processing, Machine Learning Model, Database/Storage, and Use of Project Systems

## Preliminary Processing
The initial data processing included checking the values in the dataset. There were 891 rows across a variety of columns as pictured below. The key target of the learning was the survived category to check against the other variables/features with the main focus gender and boarding class. Based on our preliminary analysis, we nocited a greater number of deaths for males than females and those in the lower cabins. We decided to use gender and class as our features based on these observations.  The gender column required using encoding to split into male and female and using the three boarding classes as 1, 2, and 3. 

<p align="center"><img src="https://github.com/teachjanderson/titanic_panic/blob/Tyler/Report_Images/Train_df.png" width="600" />

After reviewing the initial data, we checked for null values across the dataframe. The cabin, embarked, and age categories had the most null values. In the final analysis, we removed the embarked and cabin columns. For age, we ran different models. One that included the age column with the mean age replacing any null values and another that removed the null values from the dataset. 

<p align="center"><img src="https://github.com/teachjanderson/titanic_panic/blob/Tyler/Report_Images/Null_Values.png" width="600" />

After cleaning the data for the model, the final dataset looked like the following:

<p align="center"><img src="https://github.com/teachjanderson/titanic_panic/blob/Tyler/Report_Images/Clean_df.png" width="600" />

In deciding which features to use in our model, we completed further analysis to compare rates of survival based on the different categories. In the images below, 0 represents non-survival and 1 represents survived for the passengers. We observed the categories of gender and boarding class had unique trends worth further exploration. After discussion of this analysis, we decided to use these as the primary features of our machine learning model. 

<p align="center"><img src="https://github.com/teachjanderson/titanic_panic/blob/Tyler/Report_Images/Condensed.png" width="800" />
