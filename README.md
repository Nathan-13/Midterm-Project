# Midterm-Project: US Domestic Flights from 2000 to 2009
Completed by Nathan David & Sarabjit Matharu

## Project/Goals
This project aims to conduct a comprehensive examination and analysis of domestic flights within the United States from 2000 to 2009. The dataset was obtained from open source (Kaggle.com). To accomplish this objective, we have formulated specific research inquiries aimed at understanding the influence of various factors on domestic flight data during this period:

* Is there a correlation relationship between the population size of the departure city and the number of passengers on flights during this timeframe? 
* Do cities with larger populations tend to exhibit higher passenger counts on flights? 
* Can we pinpoint regional disparities in flight patterns for journeys from the West to the Midwest and other regions, as opposed to flights originating from other areas? 
* How do differences in population between the origin and destination cities contribute to these variations?


## Process

### 1. Planning Process
* Define the problem statement for the project.
* Conduct a thorough search and exploration of data to address the defined problem and research questions.
* Establish the project repository on GitHub and configure folders and files accordingly.

### 2. Data Cleaning and Transformation in Python:
In the data preparation phase, we load and evaluate the CSV data file containing US Domestic flight data from 2000 to 2009. After acquiring the data, we conduct a comprehensive data cleaning and transformation process to ensure data integrity. This process includes addressing inconsistencies, managing missing values, detecting and resolving duplicates, and standardizing data formats.
Note that all the data used for this project are saved in the 'data' folder.
* flights.csv - this is the row dataset.
* flights_clean.csv - the clean and transformed dataset fit for purpose.
* flights_reg.csv - clean dataset plus three additional columns (Years, Origin Region, and Destination Region)


### 3. Conducting Exploratory Data Analysis (EDA):
During this phase, we delve into the data, employing analytical techniques and creating visualizations to reveal valuable insights, uncover underlying patterns, and pinpoint emerging trends. This thorough analysis plays a pivotal role in comprehensively understanding the dataset's unique characteristics.

### 4. Model Building
In this stage, we will construct linear and logistic regression models to forecast the passenger count based on the number of seats available on a flight and the total number of flights in a given month.

### 5. Build a Dashboard
Develop an interactive Tableau dashboard, the Air Traffic Passenger of US Domestic Flight Dashboard in the workbook (this can be found in the data folder), that answers questions and showcases insights. And then the flight story that tells the story of this project. See the presentation/dashboard pdf in the data folder.
The following dataset files (saved in the 'data' folder) were used for this process:
* flights_region.csv - modified for Tableau dashboard development
* airports.csv - additional data with airport ID, latitude, and longitude for Tableau dashboard development.


## Results
Efficiently obtained the data and conducted data cleaning and transformation to align it with the project's objectives. Generated diverse visualizations to delve into flight attributes and patterns, explore correlations, and extract valuable insights (see the domestic_flight_EDA file in the notebook folder for details). Designed an interactive Tableau dashboard that provides answers to questions and presents vital insights for enhanced data exploration.

### Answer to Research Questions
1. The correlation heatmap for US Domestic Flights illustrates the following significant correlations:
* Strong Positive Correlations: Passengers and Seats, Passengers and Flights
* Strong Negative Correlations: Passengers and Fly Date, Seats and Fly Date, Flights and Fly Date, Distance and Fly Date
In addition, we observe weaker or negative correlations between the population size of the departure city and the number of passengers on flights, indicating that population size alone may not be a strong predictor of passenger numbers. These findings provide valuable insights into the dataset's relationships, encompassing solid and weak correlations.

2. Our analysis has pinpointed Chicago as the most frequently visited destination, closely followed by Atlanta and Dallas.

3. Regarding regional flight patterns, most flights are within the Midwest, with a substantial number connecting cities in the Midwest, Southeast, Southwest, and West regions. However, an interesting observation is that the Northeast region primarily links to the Midwest rather than having a significant number of intra-Northeast flights. Conversely, there is relatively less inter-regional travel within the West region compared to connections with other areas.

### Regression Model Results
1. Regression Model: Please refer to the 'model_building.ipynb' notebook in the designated notebook folder for comprehensive details. The results reveal that both 'Seats' and 'Flights,' as predictors for forecasting passenger numbers, exhibit exceptionally low p-values, indicating their statistical significance as predictive factors. The model effectively accounts for a substantial portion of the variance in 'Passengers,' with 'Seats' and 'Flights' proving statistically significant predictors.

2. Classification Model: The classification model has a high accuracy of approximately 93.32%. It performs well in precision, recall, and F1-score for both classes, indicating that it can effectively distinguish between them (0 and 1). The classification report provides a detailed breakdown of the model's performance for each class, see the 'model_building.ipynb' notebook.

### Dashboard in Tableau
This dashboard includes five main visualizations: 'Monthly Traffic Volume,' 'Top 10 Cumulative Passengers from Origin Airport,' 'Top 10 Cumulative Passengers of Destination Airport,' 'Regional Flight Patterns,' and 'Domestic Flights Path Map.'

To navigate the dashboard, you can specify the desired year (ranging from 2000 to 2009) using the "Year of Fly Date" filter. This selection will update all the above visuals to reflect the chosen year. Additionally, you can refine your exploration by selecting the three-letter code of the origin airport (e.g., 'HOU' for Houston) using the "Origin Airport" filter. This filter narrows down the monthly passenger traffic volume and displays flight paths to different destination airports associated with the selected origin airport.

Furthermore, you can utilize the "Origin Region" filter with the "Year of Fly Date" filter to examine the results of Regional Flight Patterns for both the origin and destination regions, facilitating a comprehensive analysis of flight patterns based on your criteria.


## Challenges 
The original dataset encompassed information spanning from 1999 to 2001. Uploading the entire dataset to GitHub posed significant challenges. Consequently, we focused our study on the data from 2000 to 2009. Without a unique identifier, we resorted to creating a unique ID by combining various columns.


## Future Goals
Given additional time, we plan to conduct a more thorough investigation into flight patterns. Additionally, we may consider expanding our database to incorporate data from 1999 to 2000.
