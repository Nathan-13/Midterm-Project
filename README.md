# Midterm-Project
Nathan David & Sarabjit Matharu

## Project/Goals
Our data set contained monthly domestic flight records from 2000 to 2009. Parameters used are Origin, Destination, Origin City, Destination City, Passengers, Seats, Flights, Distance, Fly Date, Origin Population, Destination Population. Goal of this project is to find out patterns of flights in between various places. Which years and which regions we have more flights in & how different factors are contributing number of flights.

## Process

The very first step is to understand the data set. These are different parameters used in this project as below : 

Origin - String - Three letter airport code of the origin airport
Destination - String - Three letter airport code of the destination airport
Origin City - String - Origin city name
Destination City - String - Destination city name
Passengers - Integer - Number of passengers transported from origin to destination
Seats - Integer - Number of seats available on flights from origin to destination
Flights - Integer - Number of flights between origin and destination (multiple records for one month, many with flights > 1)
Distance - Integer - Distance (to nearest mile) flown between origin and destination
Fly Date - Integer - The date (yyyymm) of flight
Origin Population - Integer - Origin city's population.
Destination Population - Integer - Destination City's population.

Cleaning includes removing any duplicate values from this data set. As there is no column that can be used as a unique key for this data set so we created a new column named ID by combining following columns - Origin City + Destination City + Passengers + Fly Date. 

in this data set We have 591438 rows(including Duplicates) & 14 columns. Then we checked information of dataframe to view column names & rows of data set. A check is also performed to see if there is any null or NaN value present within dataset.

Then a duplicate check was performed. We had 10375 duplicate rows. We have 581063 rows after cleaning up.

After cleaning of data was done, next step was to import all libraries. Then create a dataframe to see all the columns & a glimpse of rows. 

## Results

Below are some of the findings from this dataset :
        Strong Positive Correlation: Passengers and Seats, Passengers and Flights
        Strong Negative Correlation: Passengers and Fly Date, Seats and Fly Date, Flights and Fly Date, Distance and Fly Date
        Most visited destination is Chicago followed by Atlanta & Dallas.
        We have most number of flights in 2004 followed by 2007.
        When looking as regions we have most number of flights from Midwest to Midwest. A higher volume of flights connects cities within the Midwest, Southeast, Southwest, and West regions. However, in the case of the Northeast region, there is a higher volume of flights connecting it to the Midwest region rather than within the Northeast itself.
        There are less travelling in within the West region and to other regions.

### Regression Model Results

    Regression Model:
    Both 'Seats' and 'Flights' have very low p-values (close to zero), indicating that they are statistically significant predictors. Overall, the model explains a substantial portion of the variance in 'Passengers,' and both 'Seats' and 'Flights' are statistically significant predictors. However, some aspects of model fit and distribution of residuals may need further investigation, particularly the non-normality of residuals indicated by the Jarque-Bera test.

    Classification Model:
    The classification model has a high accuracy of approximately 93.32%. It performs well in precision, recall, and F1-score for both classes, indicating that it can effectively distinguish between them (0 and 1). The classification report provides a detailed breakdown of the model's performance for each class.

### Dashboard in Tableau

    A dashboard is created for US Domestic Flights. 
        1. There is Regional Flight Pattern on the dashboard to show flight patterns in diffrent regions.
        2. Top 10 cumulative passengers from Origin Airport
        3. Top 10 cumulative passengers from Destination Airport
        4. We have a flydate filter
        5. Different regions & Airports are shows with diffrent colors.

## Challenges 
    This data set originally contained data from 1999 to 2001. It was very challenging to upload dataset to GitHub So we decided to study data from 2000 to 2009. There was no unique key to work with so combination of columns were used to make a unique ID.

## Future Goals
    If we have more time we will explore more in delpth flight pattrens. And also can extend our data base to include data from 1999 to 2000.
