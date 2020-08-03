# AIAI-Economic-Freedom-Case-Study

***The Case : Economic Freedom***

***Working File***

This file gives an evolution of metrics relating to “economic freedom” for 5 decades for all the
countries of the planet. EFW index has become more comprehensive and the available data more complete. As a result, the number and composition of the components for many countries vary across time. This makes it difficult to directly compare index values from earlier periods with later periods. The EFW Panel Dataset adjusts the regular EFW index in two ways. (1) From the most-recent year annually back to 2000, by autoregressively "backcasting" the data, meaning we use actual values in later years to estimate the missing values for earlier years. (2). using 2000 as the base year, changes in a country’s scores backward in time are based only on changes in components that were present in adjoining years.

https://query.data.world/s/4xw22cieov57pfdwdf2pbiu2d65u42

***Objective:***

*  Review its features in Excel or any other editor.
*  Make necessary adjustments
*  Integrate this file in your “sandbox
*  Develop a first analysis
*  Explore the various functionalities of a BI solution (cosmetics, analytics,
   calculations, etc.)
*  Submit a screenshot of your work with 3 learning points that you deemed
   relevant.

***Data Dictionary***

***COLUMN NAME TYPE DESCRIPTION***

Column Name | DataType
------------| ------------
year | year
iso_code | string
countries| string
summary_index| decimal
size_of_government |decimal
legal_system_property_rights |decimal
sound_money |decimal
freedom_to_trade_internationally |decimal
regulation |decimal

1. ## Review its features in Excel or any other editor:
The Excel file has been adjusted because it does not respect the table format

![](https://github.com/sangeethamano84/AIAI-Economic-Freedom-Case-Study/blob/master/EFW_csv.png)
 


Cleaned the Excel file by removing the text content that are given as description on the sides of the data columns and imported the cleaned file as CSV file.

cleaned file is uploaded in Pyramid Data Modeling. 

2. ## Make necessary adjustments:

Data Model refers to the logical inter-relationships and data flow between different data elements. It documents the way data is stored and retrieved.

![](https://github.com/sangeethamano84/AIAI-Economic-Freedom-Case-Study/blob/master/DataModel.png)
The delimiter has to checked to upload CSV file to extract the data correctly. The data is stored in memory by selecting In-Memory DB option and Build button is pressed to upload the data.

3. ## Integrate this file in your “sandbox”:

 The Data is prepared for ***ETL***.
 ![](https://github.com/sangeethamano84/AIAI-Economic-Freedom-Case-Study/blob/master/ETL.png)
 The data is stored in the Database and the file is integrated and experimented without affecting the source data.
 * The uploaded data is connected to the source and set-on-demand or scheduled extract is chosen to an appropriate timing.
 * The field formats are adjusted and granularity is reduced and the process of calculations are performed on necessary fields.
 * Make the data available for instant and easy comsumption.
 
 Data quality is done for high quality of information by oversight of the information, identifying, understanding and correcting flows in data.
 Fixed the data in the source system.
 
* Number of Empty values: Fixed the missing values in data by count the number of fields that are empty within a dataset and filling the missing field by mean,       median or avg of the data.
 * Wrong  format: The correct format of data type of each field is oversighted.

 Improved data quality for better decision making and consistant improvment in result.
 
 ### ***Data Profiling***
 Data Profiling is the process of reviewing source data, understanding strcture, content, interrelationship and identfying potential for data.

  ![](https://github.com/sangeethamano84/AIAI-Economic-Freedom-Case-Study/blob/master/columnconfig.png)
  
   ***Structure discovery***: 
 validating the data is consistant and formatted corretly and performing mathematical check(eg. sum, min, max).
 
 * Distinct count and percent: Identifying distinct values and count of distinct values in each column.
 * Percent of zero/blank/null values: Identifies missing or unknown data, to fill the missing values with default values.
 * Min/Max/Avg string length: Identify the appropriate data types and sizes in target database. Setting column width enough for data is to improve the performance.
 
 Data model structure helps to define relational tables, primary and foreign keys and stored procedures. The data relationship allows relational database to split and store data in different tables.
 
 4. ## Develop a first analysis:
    Discovered data with data visualization by dimensions and measures.
    * ***Correlated Legal System and Sound Money***:
![](https://github.com/sangeethamano84/AIAI-Economic-Freedom-Case-Study/blob/master/Correlated%20legal%20system%20and%20sound%20money.png)
This visualization discovered the Correlation between attributes the Legal System & Property Rights and Sound money. 
In the observation, As the Legal System & Property Rights decreases the Sound money also decreases and vice versa. It shows these two attributes are highly correlated.
    * ***Legal System & Property by Year***:
 ![](https://github.com/sangeethamano84/AIAI-Economic-Freedom-Case-Study/blob/master/Legal%20%26%20property.png)
 This visualization shows Measure value of Legal System & Property by Year as Dimensions. The Iso-code is applied as a filter to extract the values according to the selected filter.
 In the observation, the selected ISO -CODE, is GNB which represent the country Guinea - Bissau. In year 2015 the Legal System & Propery is higher with value 3.86.
    * ***Size of Government and Regulation by Summary-index***:
![](https://github.com/sangeethamano84/AIAI-Economic-Freedom-Case-Study/blob/master/Government%20and%20regulation.png)
This visualization shows Measure value of Summary-index with X-axis as Size of Government and Y-axis as Regulation. 
In the observation, The Summary-index values are measured as size. The bigger the size, bigger the value and vice versa. 
The biggest measured size of Summary-index is: 197.31, which belongs to the country Hong Kong with Regulation of 200.18 and Size of Government is 202.28.
The smallest measured size of Summary-index is: 13.90, which belongs to the country Laos with Regulation of 12.62 and Size of Government is 17.11.
   * ***Summary Index of the Country by Year***:
![](https://github.com/sangeethamano84/AIAI-Economic-Freedom-Case-Study/blob/master/country%20summary%20index.png)
This visualization shows Measure value of Summary index and Dimension as Countries by Year. The Year is applied as a filter to extract the values according to the selected filter.
In the observation, the selected Year, is 2015 the shown trend visualization of Summary index values of countries. 
The Country with higher Summary Index value is Hong Kong with 8.97 in year 2015.
   * ***Sum of Summary index of all years by Country***:
![](https://github.com/sangeethamano84/AIAI-Economic-Freedom-Case-Study/blob/master/sum%20summary%20by%20year.png)
This visualization show the Measure value of sum of summary index, the formula of summation of summary index values of all years is done and applied in X-axis.
The Dimension value of Regulation in Y- axis and visualized by size of Freedom of trade internationally.
In the observation, The visualization shows that the country HongKong has highest value of Freedom of trade internationally 208.34 measured by summary index and regulation.
 5. ## Explore the various functionalities of a BI solution:
   * ***Linear Regression of Freedom of Trade Internationally***:
![](https://github.com/sangeethamano84/AIAI-Economic-Freedom-Case-Study/blob/master/Freedom%20of%20trade%20Linear%20Regression.png)
This visualization shows the Linear Regression of Freedom of Trade Internationally over Legal Systems & Property, The year is applied as a filter.
In the observation, the regression line fits to the value. Hence, the linear regression model can be applied to the Economic Freedom dataset.

![](https://github.com/sangeethamano84/AIAI-Economic-Freedom-Case-Study/blob/master/Outliers%20Multi%20Varient.png)
The Linear Regression model as few outliers to filter the model for the perfect fit.
The visualization show the fit IN and OUT values of the Linear Regression model









 
 
