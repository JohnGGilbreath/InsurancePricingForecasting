# BMI_Status XGBoost Regression
I have developed a regression model that will accurately predict the BMI (Body Mass Index) status based on the variables presented. I believe this is useful to not only healthcare, but can be laterally transformed to any industry. For healthcare plan agencies, however, this can be used in future insurance pricing models as a function to evaluate how prior conditions affect premiums paid.
## -Data Preprocessing
The first step is to load the .csv into jupyter notebook and check out the overall structure of the data, observing the column names, any null values, and the datatypes for each column. Then I looked at the numerical and statistical information with the describe function.
## -Exploratory Data Analysis (EDA)
### Histograms
Histograms are used to measure distributions of each column to visualize where the likely mode and means are. Using pandas I can observe the data through groups of histograms.
### Density
In this section I've graphed out the density plots in a straight line format, 1 density plot for each of the columns. 
Density plot is like a smoothed, curved representation of histogram but is used to visualize the distribution of data over a continuous interval, or time period. In certain situations, multiple variables can be laid over each other in a single graph.
### Outliers
Checking for outliers is an important step in preprocessing to eliminate any data that may adversely skew the regression. There are a number of texbook examples of outliers for the "Weight" and "Number of Major Surgeries" columns, but they are valid with this data. With weight, there is a BMI_Status column that will categorize those as "Obese", and the outlier for the number of major surgeries came from a number of records that have had 3 major surgeries.
### Bar Plots
The last column of the dataset shows the Price Premium that each of these people pay based on their various metrics, so I thought it was important to visualize each of the columns through bar plots as it pertains to the premium paid.
### BMI_Status
Since BMI is not a column, I created one using the height and weight. After that, I created bins for 4 different classifiers of BMI: Underweight, Normal, Overweight, and Obese. To see what these looked like, I created a horizontal boxplot, with BMI_Status on the y axis and Premium Price on the x-axis. 
## -Methodology
As stated in the top section, the goal here is to build an XGBoost regression model that can accurately predict the BMI Status of the individual based on their various datapoints. This is not a binary outcome prediction, so I did not use a classification model, and instead opted for regression model. Once I decided on regression models, I split the dataset into x and y, the dependent variable 'y' being 'BMI_Status'.
Then I split the train and test data into 70/30.
## -Results
The model was trained, and y_pred returned a simple accuracy score of 97.64%. To build on this project, the next thing I am going to do is cross-validate the model.
