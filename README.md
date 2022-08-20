## Titanic_Panic

# Machine Learning of Titanic Data
Our project will be using machine learning to determine which variables have an impact on survival rates aboard the Titanic. The Reason we selected this as our project is due to our interest in the historical event and the dataset included a variety of information to analyze in our machine learning model. Our data source is from [Kaggle](www.kaggle.com/competitions/titanic/data). The dataset is split into multiple CSV files and will require merging via SQL Joins. 

# Hypothesis and Questions
* Hypothesis: The class of passenger impacts the survival rate aboard the Titanic.
* Alternative: The gender of passengers impacts the survival rate aboard the Titanic. 
* Null Hypothesis: The class of passenger does not impact the survival rate aboard the Titanic. 
* Does gender impact survival odds aboard the Titanic? 
* Does class of passenger impact survival odds aboard the Titanic?
* Can we achieve an machine learning accuracy rate above 80%?

# Preliminary Processing, Machine Learning Model, Database/Storage, and Use of Project Systems

## Preliminary Processing
The initial data processing included checking the values in the dataset. There were 891 rows across a variety of columns as pictured below. The key target of the learning was the survived category to check against the other variables/features with the main focus gender and boarding class. The gender column required using encoding to split into male and female and using the three boarding classes as 1, 2, and 3. 

<p align="center"><img src="https://github.com/teachjanderson/titanic_panic/blob/Tyler/Report_Images/Train_df.png" width="600" />

After reviewing the initial data, we checked for null values across the dataframe. The cabin, embarked, and age categories had the most null values. In the final analysis, we removed the embarked and cabin columns. For age, we ran different models. One that included the age column with the mean age replacing any null values and another that removed the null values from the dataset. 

<p align="center"><img src="https://github.com/teachjanderson/titanic_panic/blob/Tyler/Report_Images/Null_Values.png" width="600" />

After cleaning the data for the model, the final dataset looked like the following:

<p align="center"><img src="https://github.com/teachjanderson/titanic_panic/blob/Tyler/Report_Images/Clean_df.png" width="600" />

## Machine Learning Model

Our initial model makes use of logistic regression. This model takes in the various features such as age, boarding class, and gender to calculate the likelihood that each person survives based on those features. Our training set matches the image above. We focused on the features of gender and class and our preliminary analysis revealed a strong correlation between those and survivability. To test this, we split the data into training and testing sets checking against the survived category. 

<p align="center"><img src="https://github.com/teachjanderson/titanic_panic/blob/Tyler/Report_Images/Condensed.png" width="600" />

## Database/Storage

The project will use SQLite to hold and manage our data along with some members making use of Postgres SQL to run queries prior to using our Machine Learning model. The final presentation will make use of Microsoft Powerpoint / Google Slides and Tableau. The link to our Google Slides can be found [here](https://docs.google.com/presentation/d/e/2PACX-1vSARBSO_xyOQqv3Wb4MGWp5oeDXIu8JB_nmKE-kFPynPddJQAdttd75yul_AkW9BFr50BoTmvyVGDm2/pub?start=false&loop=false&delayms=60000)

The relationships between our tables align on the boarding class and gender columns as seen in the ERD Below. To initiate the connection to SQLite, we embedded code into our notebook where necessary. 

<p align="center"><img src="https://github.com/teachjanderson/titanic_panic/blob/Tyler/Report_Images/ERD_Titanic.png" width="600" />

<p align="center"><img src="https://github.com/teachjanderson/titanic_panic/blob/Tyler/Report_Images/Connect_Database.png" width="600" />

# Communication Protocols 
The team communication protocols include briefing before and after each class session along with agreed upon norms for communication including Slack for sharing links, general requests, and support questions. Our team will meet live on Zoom using created channel and using class breakout rooms. The project deliverables are hosted on Github using branches and approving merges as deliverables are completed. Each team member has their own designated branch and we've made use of Google Colaboratory during shared work times involving coding. 
