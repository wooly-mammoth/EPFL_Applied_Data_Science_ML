
# List of Tasks, Module-1: Introduction to Data Analysis
# A. Importing, cleaning and numerical summaries
1. Download the data set data.csv from the Resources tab.
2. Import the data as a pandas DataFrame.
3. Check the number of observations.
4. Obtain the column headings.
5. Check the data type for each column.
6. Check if there are any missing values.
7. If necessary remove any observations to ensure that there are no missing values and the values in each column are of the same data type.
8. Obtain the mean, minimum and maximum value for each column containing numerical data.
9. List the 10 happiest countries, ordered by their happiness score.
10. List the 10 least happy countries, ordered by their happiness score.
# B. Indexing and grouping
1. Group the data points by region and save them into separate .csv files ex. a Western Europe.csv with all the data for countries in Western Europe and so on for the other 5 regions.
2. Compute the mean happiness score for each region and rank the regions from most happy to least happy.
3. Compute the number of countries in each region that have a happiness score above 6.0.
4. Compute the difference between the maximum and minimum happiness score for each region. Which region has the largest range of happiness scores?
# C. Bar plot of the Happiness Score
1. Obtain a horizontal bar plot of the Happiness Score of the top 10 happiest countries. Your bar chart should have the names of the countries are listed vertically along the y-axis and the x-axis should have labels for each number from 0 to 8. Ensure that the chart has an appropriate title and labels.
2. You will now adapt the code for the horizontal bar chart you obtained in step 1 to turn into a stacked bar chart where the overall happiness score is divided into the seven parts corresponding to the columns:
Economy
Family
Health
Freedom
Generosity
Corruption
Dystopia
Choose a distinct color for each category and include an appropriate legend with your chart.
3. Obtain the same stacked horizontal bar chart as in step 2 but this time instead of the top 10 countries consider all countries from the region Africa.
# D. Histogram of Job Satisfaction
Obtain a histogram of the Job Satisfaction using the following categories:
40%-50%
50%-60%
60%-70%
70%-80%
80%-90%
90%-100%
# E. Pairwise Scatter plots
Obtain scatter plots of the Happiness Score versus each of the other variables. Your plots should be displayed as multiple plots table and obtained with one command as opposed to separate commands for each plot.
# F. Correlation
Obtain the correlation between the Happiness Score and each of the other variables. Which variable has the highest correlation with the Happiness Score?
# G. Probabilities
Compute the probability that randomly selected country with Happiness score over 6.0 is from Western Europe. You will have to use pandas to count the appropriate quantities.
# H. Matrices
Define a matrix whose rows correspond to countries and the columns to the regions. Fill in the matrix with 0/1 values where entry (i,j) is a 1 if the country in row i is in the region in column j and a 0 otherwise.



# List of Tasks, Module-2: Applied Data Analysis
Below you will find a list of tasks for this project. Note that the tasks described here are more high-level and less specific than those you were giving in the first project. The goal is to provide you with more freedom to implement the analysis in ways in which you best see fit and also explore the questions which most interest you. Of course, there will be more than one solution to achieving each of these tasks. Your overall grade will depend not only on the completion of the tasks but also on your ability to demonstrate the following competencies through your code and analysis:

Efficient use of tools covered in the course
Correctness of the analysis and interpretation of results
Ability to communicate and document your findings through plots and text (Markown cells)
# A. Data import and high level exploration
First, you will download the data and do some exploratory data analysis (EDA).

Download: Get the data from the Kaggle link provided and import it into Pandas. The dataset should include 356'027 samples and 163 columns.

### Exploratory data analysis: 
The goal at this stage is to get familiar with the data and create an overview of it using Python code. Keep in mind that the table has 163 columns which means that you will need to search for the interesting columns and focus on exploring them. There are many strategies to handle this part and several solutions will be accepted, but here are some ideas to help find interesting columns and explore their content:

What is the proportion of missing values per column/row? Should you keep, fill or remove these missing values? What would be the implications?
What are the different columns data types?
What are the mean/min/max/median values of numerical columns? Do you spot any issue from analyzing those statistics? ex. a negative amount of sugar, a maximum value extremely far from the 75% percentile (outlier?)
For numerical columns, how does the variable distribution look like? ex. using histograms or scatter/violin/density plots
Are there columns that contain lists? ex. lists of ingredients, tags
Are there columns that are very similar in their content?
Are columns with text always written using the same alphabet?
For categorical columns, what are the top 10 most frequent values?
Are there duplicate products?
Right after, in task B, we will ask you to answer 3 research questions. The exploratory data analysis (EDA) questions from above will help you get a high-level understanding of the data set and help you find/design 3 research questions that you're interested in and that seem feasible.

To answer those 3 research questions, you will very likely only need to analyze a subset of the 163 columns! Identify those columns and clean them as much as necessary to get reasonable results. But remember to stay pragmatic about your cleaning. If something influences the accuracy and reliability of your results, consider changing it. Otherwise, it is good to acknowledge, comment and move on.

For this task and the next ones, please make sure to include a Markdown cell along with your outputs (visualisations, DataFrames) in order to reveal your findings using English sentences. This enables to step back, ask yourself whether the findings do make sense, and also share intuitions with readers.

# B. In-depth analysis
Thanks to your previous exploratory data analysis, you now have a good intuition of what's in your dataset and what are its strengths and weaknesses. You will now work with the data to investigate some properties of your choice. Your goal is to choose 3 interesting questions to answer about the data and perform the necessary steps for the analysis.

The questions that you choose must be complex enough to allow for some substantial data manipulation. As a guideline, below is a sample topic of analysis:

Topic: Investigation on additives identified in the Open Food Facts dataset

Are products number of additives correlated with their nutrition scores?
Are there countries with more or less risky additives? This additional list may help.
What product category is most prone to having many additives?
For each of your 3 questions, choose the appropriate visual methods to communicate your findings.

# C. Text data
You will filter and group your data based on the ingredients_text column. Your goal is to find the five most common ingredients. Be careful with text normalization:

punctuation e.g. "water." vs"water"
capitalization e.g. "water" vs "Water"
white spaces removal e.g. " water" vs "water"

# D. Time-series analysis
You will investigate more closely the created_datetime and last_modified_datetime. First, you will analyze the mean time difference between these two values. And second, you will analyze the total number of items created each month over the full timeline of the data. For the second question, you will also choose an appropriate method to visualize your findings.

# E. Build a database
You will build a database to hold your data. It is up to you to define appropriate tables and well as primary keys for connecting them. (The focus is definitely more on just using the basic methods/tools introduced in the course and not on building a complex database.) In particular, you can follow the following list of steps:

- Restrict your data to 1000 entries and 5 columns of your choice
- Create a connection to a sqlite3 database
- Create one or multiple tables, at least one of the tables should have a PRIMARY KEY
- Fill the database with your data
- Run at least one query to demonstrate that it works correctly
# F. Finding correlations
You will try to find correlations between the different data fields. Your goal is to identify the variables which most affect the nutritional score and provide some insight into which factors cause both a low or a high nutritional score.

