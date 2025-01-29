# Power-Query-Data-Cleaning
## Power Query Data Cleaning Challenge


In this provided dataset [Dataset](https://docs.google.com/spreadsheets/d1458SFTSswQeU0lkEUi3XQTv2pPLDjzwxT1TcFbH-Ykg/edit?usp=sharing), questions about travel preferences were logged multiple times with the same ID and hash.


**Objectives**

- Remove duplicate records from that field while preserving the integrity of the data.
- You'll transform this data into a cleaner format where each question appears only once, paired with its corresponding answer.

### Step-by-Step Procedure:

1. Load the Data into ****Power Query:****


2. Select the data range (including headers) and go to Data > From Table/Range to load the data into Power Query.

3. ***Create a staging query*** using the Duplicate option
 - Remove Duplicate Rows
 - In Power Query, you will notice that each question and answer is repeated multiple times. Select the hash and message columns to remove duplicates, then go to Home > Remove Rows > Remove Duplicates.


4. ***Separate Questions and Answers:***
 
 i. Duplicate staging query into duplicate query questions staging
 
 ii. Filter type column for questions
 
 iii. Remove the type column
 
 iv. Rename the message column to question
 
 ![Staging query](/Users/alicemaphosa/Downloads/Excel_Data_Analytics_Course/Fundamentals of Excel/Data A  nalysysis/Staging query.png)
 
5. Repeat number 4 by first duplicating the staging query and filter for answers by applying the same procedure as above - call it duplicate query answers staging


6. ***Merge Questions and Answers:***

	- Go to Home > Merge Queries and merge the question and answer staging tables on the hash column.

	- Expand the merged table to include only the answer column from the answer table.

7. Rename the merged table

8. Load the Data Back to Excel:

