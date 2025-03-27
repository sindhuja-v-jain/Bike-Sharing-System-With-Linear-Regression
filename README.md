## Problem Statement ##
A bike-sharing system is a service in which bikes are made available for shared use to individuals on a short term basis for a price or free. Many bike share systems allow people to borrow a bike from a "dock" which is usually computer-controlled wherein the user enters the payment information, and the system unlocks it. This bike can then be returned to another dock belonging to the same system.


A US bike-sharing provider BoomBikes has recently suffered considerable dips in their revenues due to the ongoing Corona pandemic. The company is finding it very difficult to sustain in the current market scenario. So, it has decided to come up with a mindful business plan to be able to accelerate its revenue as soon as the ongoing lockdown comes to an end, and the economy restores to a healthy state. 


In such an attempt, BoomBikes aspires to understand the demand for shared bikes among the people after this ongoing quarantine situation ends across the nation due to Covid-19. They have planned this to prepare themselves to cater to the people's needs once the situation gets better all around and stand out from other service providers and make huge profits.


They have contracted a consulting company to understand the factors on which the demand for these shared bikes depends. Specifically, they want to understand the factors affecting the demand for these shared bikes in the American market. The company wants to know:

Which variables are significant in predicting the demand for shared bikes.
How well those variables describe the bike demands
Based on various meteorological surveys and people's styles, the service provider firm has gathered a large dataset on daily bike demands across the American market based on some factors. 


## Business Goal: ##
It is required to model the demand for shared bikes with the available independent variables. It will be used by the management to understand how exactly the demands vary with different features. They can accordingly manipulate the business strategy to meet the demand levels and meet the customer's expectations. Further, the model will be a good way for management to understand the demand dynamics of a new market. 

## Understanding the data ##
The data is provided in one file containing information of daily bike demand from 2018 to 2019 .
It has also recorded values of variables like weather , tempreture humidity etc for each day .

## Approach taken to undertsand the bike demand trends ##
 - Data is imported and inspected .
 - There were no null values or any type conversion needed
 - Dropping the 'casual' and 'registered' column as the sum of these columns in captured in the 'cnt' column. Also dropping the 'instant' column as it is just an index column.
 - Plotted pair plots and heat maps between the numerical variables to observe the relationships between them and the target variable 'cnt'. There were linear relationships and good correaltion found between temp and atemp variable and the cnt variable. Hence , a linear regression model can be built.
   ### Data preparation ###
     -Converted some numerical variables to categorical variables
     -Created dummy variables for categorical variables
     -Split the data into train and test.
     -Sacled the variables
     - Used RFE to select the independent variables to build the model.
     - Built the model using Statsmodel
     - Dropped variables using the VIF metric
     - And built the model again . Continued till all the VIF values went below 5, P values became 0 and R Squared value reached 81%.
   ### Model evaluation ###
     - Performed residual analysis and found that the error terms are normally distributed , which indicates that the model is a good one
     - Made predictions on the test data,  calculated R squared value for the same and it came out to be 76.9 % which is close the Rsquared value of the train set.
       
## Conclusion ##
The demand for shared bikes is good during winter and around the month of september .
It is also good when the weather situation is not extreme like during clear sky and no signs of rain.
It is recommended for Boombikes to promote their brand around this time and gain popularity so that customers choose them
when they are in need to rent a shared bike.

   
