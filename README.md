# \# Data description

#### Team B - Yuval Sabag, Shani Bahat

This Markdown file describes the data folder structure and organization. Our data is based on Dr. Noga Cohen research - "Psychological experiment about social emotion regulation". The four attached tables contain data from an online survey that the participants filled on three different time periods of the trial. Each online survey was identical therefore all tables have identical columns.

The features in the data are described below:

#### General Details


|Column Name | Type | Description |
|------------|------|-------------|
|Start Date  | Date | the date the participant started the survey|
|End Date  | Date | the date the participant started the survey|
|IPAddress  | Character | the IP address the survey was taken from|
|Progress | Numeric| the percent of the survey that was filled|
|Duration (in seconds)  | Numeric | the amount of time (in seconds) filling the survey took|
|Finished  | Numeric | if the participant finished filling the survey Yes/No |
|Responseid | character | the response ID |
|workerID | character | the participant ID |

#### Emotional Regulation Information

The columns contains the participant rank to a given statement from (1) "Not Very" to (5) "Very"

|Column Name | Type | Description |
|------------|------|-------------|
|RRS_1-22  | Numeric | rumination: tendency to think negatively about past events – bad strategy|
|CES.D_1-20  | Numeric | depression|
|ERQ_reappraisal_1-10| Numeric | tendency to think differently about negative events – good strategy|
|IRI_1-28| Numeric | empathy, sometimes separated to emotional and cognitive|
|HAS_1-20| Numeric |helping attitudes|
|Rosenberg_SE_1-10| Numeric |self esteem|
|BAI_1-21| Numeric |anxiety|
|PSS_1-10| Numeric |perceived stress|
|GSE_1-10| Numeric |self efficacy|
|SEES_1-20| Numeric|self esteem|



#### Personal Information

| Column Name   | Type    | Description                                 |
|---------------|---------|---------------------------------------------|
| SES_Education | Numeric | number oh education years                   |
| SES_Degree    | Numeric | socioeconomic status                        |
| Age           | Numeric | the participant age                         |
| Gender        | Numeric | the participant gender. 0 = Male 1 = Female |
| Ethnicity     | Numeric | the participant ethnicity                   |

For our data analysis we combined data from the 3 given data sets into one table that contains personal characteristics of each participant as well as the sum of RRS and CES.D columns for each period of time.

In order to get our end to end code analysis, run the chunks in the attached rmd file in the given order.

# Data analysis review

#### 1. Loading & Cleaning the Data

-   Load libraries
-   Upload the data
-   Rename columns and delete unrelated lines
-   Sum related columns
-   Select relevant columns
-   Merge all the tables into one
-   Remove outliers

#### 2. Data Analysis

-   Summary Statistic
-   Initial analysis
-   Visualizations - Explore relationships between the different variables

#### 3. Model fit

-   Splitting data to train and test

-   Set seed

-   Build linear regression to predict the effect of the experiment on the long-term RRS index based on the initial RRS and CES.D rates and gender.

-   Fit a model to the training data set

-   Visualize the 3D model

-   Create surface to 3D plot

#### 4. Test the Model

-   Predict on the testing data set
-   RMSE index
-   R- squared index

Hope you like it, enjoy (-:
