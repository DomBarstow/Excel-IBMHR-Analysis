# Excel-IBMHR-Analysis

We are going to look at the following dataset:

https://www.kaggle.com/datasets/pavansubhasht/ibm-hr-analytics-attrition-dataset/data
Which is a fictional dataset created by IBM Data Scientists. 

Before we begin, please note in the excel file, the “Original Data”, and the “Key”. Some of the categories in the data have numerical data which is linked to a categorical response. We may change some of this numerical data out for the categorical responses, but that will be clearly stated here. The “Key” page will not be edited, nor will the “Original Data”.  

Next we will make a “Working Sheet”, wherein we can cleanse the “Original Data” without making permanent alterations, this protects from silly mistakes and typos.

First step of cleansing, we check for any duplicates in the data. Using excels handy “Remove Duplicate” feature, we have:

No Duplicates.PNG

Phew, looks like our data is already in pretty good shape.
Next, lets adjust all the column lengths so we can investigate the data more clearly:

[Columns Adjusted](https://github.com/DomBarstow/Excel-IBMHR-Analysis/blob/main/images/Columns%20Adjusted.PNG?raw=true)

Now, having investigated our column headers, it appears as though there might be some superflous columns, “EmployeeCount”, “Over18?” and “StandardHours” all seem to contain the same data for every entry. To examine, let’s apply a filter to our column headers.

From examining the column headers, we can see that the those three headers, have the same values for all entries, being:
“EmployeeCount” = 1
“Over18?” = Y
“StandardHours” = 80

Now that we have them recorded here, we can safely delete their respective columns.
For our next step in data cleansing, we are going to perform a “Find & Replace” on the column “BusinessTravel”, several entries have “_” which we want to replace with “ “.

Find and Replace.PNG

Eagle eyed readers will have also noticed the lack of any spaces in our column names, so we will also remedy this manually now.

A further edit to make, is that from the original data it seems that “Daily Rate”, “Hourly Rate” and “Monthly Rate” are not well defined or understood, and given we have the “Monthly Income” for each row, then we will discard those three columns.

Now, let’s add currency to the “Monthly Income” column. Given that IBM in an American company, we will assume the income is in dollars. 

[Currency](https://github.com/DomBarstow/Excel-IBMHR-Analysis/blob/main/images/Currency.PNG?raw=true)

Due the wide range of Age data (18-60), we also are going to create a new column, called “Age Bracket”. We will categorise each age into one of the following:

Baby Boomer: 60+
Generation X: 44-59
Millennial: 28-43
Zoomer: 18-27

These ages would align approximately (there is some debate over the start/end point of each generation) if this data was taken in 2024, and if it is fictional data, we will assume that it is.

[Age Brackets](https://github.com/DomBarstow/Excel-IBMHR-Analysis/blob/main/images/Age%20Bracket.PNG?raw=true)

Now we have the data cleansed and organised to our liking, it is time to make our pivot tables, and create some charts:

[Charts and Pivots](https://github.com/DomBarstow/Excel-IBMHR-Analysis/blob/main/images/Chart.PNG?raw=true)

Before finally organising into a dashboard, and adding some slicers:

[Dashboard](https://github.com/DomBarstow/Excel-IBMHR-Analysis/blob/main/images/Dashboard.PNG?raw=true)

We have now finished the project, showing how we can take the original data, cleanse it, and represent it graphically, all in excel.
