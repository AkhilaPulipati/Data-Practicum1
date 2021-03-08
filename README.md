# US Road Accidents Data Analysis
Road accidents are one of the major concerns in the country. The economic impact of traffic accidents cost hundreds of billions of dollars for US citizens every year. Reducing the traffic accidents has always been a challenge. The main objective of the project is to analyze what are the causes for accidents such as impact of precipitation or any environmental factors and to predict the probability of road accidents based on the existing accidents records. By performing data visualization, we can identify the car accidents zones, factors effecting accident severity, and locations etc. Identifying the key factors of how these accidents occur can help in implementing well informed actions.
## Dataset: https://www.kaggle.com/sobhanmoosavi/us-accidents
The dataset is taken from Kaggle site. The dataset contains countrywide car accidents records, which covers 49 states of USA. The data is collected from different sources like MapQuest, and Bing which contain records from February 2016- December 2020. It contains about 4.2 million records with 49 columns.
## Data Preprocessing
Missing values in the dataset are handled by replacing them with mean, mode and zero values. Some of the missing values with less than 5% of the data are dropped. Dropped the Turning_loop column which has only one value False which means they are no turning loop during the accident and is not used for our analysis.
## Data Visualization
Analyzed which states and cities has more accidents records, what are the top weather conditions during the accidents, accident occurring zones, Visualized number of accidents occurred by year/month/week/hour. Displayed state wise severity of accidents.
## Feature Selection
Features are selected based on the importance and correlation plot. These are the selected features for predicting the accidents severity: TMC, Severity, Start_Lat, Start_Lng, End_Lat, End_Lng, Distance(mi), Timezone, Number, Temperature(F), Wind_Chill(F), Humidity(%), Pressure(in), Visibility(mi), Wind_Speed(mph), Precipitation(in), Amenity, Bump, Crossing, Give_Way,Junction,No_Exit,Railway,Roundabout,Station,Stop,Traffic_Calming,Traffic_Signal,Year,Month,Hour,DayOfWeekNum, MonthDayNum,HourOfDay . Performed data transformation using label encoder. Selected Mountain Time zone region data for modeling. Before building the classifier, redefined severity 1,2 as 0 which is low severity and 3,4 as 1 which is high severity.
## Modeling
Implemented Knn, Neural network, Decision Tree, and Random forest algorithms for predicting the severity of accidents.
## Evaluation
Evaluated the model using Accuracy score, Classification Report and Confusion Matrix. Plotted a graph which compares the accuracy of all algorithms. The best accuracy achieved is 90% by Random forest algorithm.
## Conclusion
We have analyzed at what time an accident occurs, location of accidents, accidents zones, and other environmental factors which effect the severity of accidents. By giving the location details, information about the weather, time and surrounding information the classification models help one to predict whether accident would be more or less severe.


