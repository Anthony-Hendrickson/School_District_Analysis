# School_District_Analysis
Using Pandas to do analytics on school data

## Project Overview

#Purpose:
Overall, this project aimed to analyse information about school districts that was provided to us in 2 csv files using pandas in python. Specifically, we were asked to produce the following key metrics

* Total number of students
* Total number of schools
* Total Budget
* Average math score
* Average reading score
* Percentage of students who passed math
* Percentage of students who passed reading
* Overall passing percentage

Once the key metrics were established, we moved on to analysing the highest and lowest performing schools, considering their school size, spending per student.

## Results
Almost immediately we realized we had to do some cleaning of the data to remove 

In order to make the key metrics as meaningful as possible we needed to address a problem. The grade 9 students of Thomas High School, one way or another, had grades that were innacurate. This problem was identified to us by the individual who gave us the assignment. In order to address this problem we had to isolate these students and nullify their grades so that they wouldn't be accounted for in our key metrics. We tackled isolating these students and changing their grades to NaN for reading and math in the formulas pictured below:

![alt text](https://github.com/Anthony-Hendrickson/School_District_Analysis/blob/main/Resources/ninth_grade_thomas_high.PNG)

The way that we analysed the data (by overall performance, school size, and spending per student) gave us far more insight into our key metrics

* Total number of students - We were able to put this number into greater context by creating bins to categorize by school size, and this categorization allowed us to explore relationships between the size of the school and its performance.
**The total number of students was reduced by the removal of the Thomas High School grade nine students
* Total number of schools - This wasn't exactly a focal point of our analysis and wasn't the most useful key metric either
* Total Budget - We were able to put this number into greater context by creating bins to categorize by spending per student, and this categorization allowed us to explore relationships between spending per student and performance.
**The total budget remained the same, but the spending per student increased as a result of removing the Thomas High School 9th graders
* Average math score - We broke down the math scores so that they could ultimately be viewed by school and grade and relationships between grade, school and the advanced metrics mentioned above could be explored.
**The the average math score decreased as a result of removing the Thomas High School 9th graders
* Average reading score - We broke down the reading scores so that they could ultimately be viewed by school and grade and relationships between grade, school and the advanced metrics mentioned above could be explored.
**The the average reading score decreased as a result of removing the Thomas High School 9th graders
* Percentage of students who passed math - By isolating students who had scores of > 70 in math we were able to establish a percentage for the number of students who pass
**The the percentage of students who passed math decreased as a result of removing the Thomas High School 9th graders
* Percentage of students who passed reading - By isolating students who had scores of > 70 in reading we were able to establish a percentage for the number of students who pass
**The the percentage of students who passed reading decreased as a result of removing the Thomas High School 9th graders
* Overall passing percentage - By finding the intersection of students who passed both math and reading we were able to establish a percentage for the number of students who passed math and reading.
**The overall passing percentage decreased as a result of removing the Thomas High School 9th graders

Below you will see a sample of the "per_school_summary_df" which gives a sample of the outcome of our analyses at the widest scope:

--
![alt text](https://github.com/Anthony-Hendrickson/School_District_Analysis/blob/main/Resources/summary.PNG)


##Summary

Since the math and reading scores for the Thomas High School 9th graders were artifically inflated in our data set, removing them decreased our average math and reading scores, as well as the percentage of students who passed math, reading and both math and reading.

