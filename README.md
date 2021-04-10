# School_District_Analysis
Module 4 coursework

## Project Overview
School District has requested an additional analysis of their 39,170 students' state-testing results to look into evidence of academic dishonesty. District has provided us with standardized testing results data for each student in the district including student ID, name, gender, grade, and high school they attend.

### Purpose of analysis
The district has requested an additional look into the standardized testing data in response to school board's belief there was academic dishonesty related to the math and reading test scores for the 9th grade class at Thomas High School (THS). The purpose of this analysis to remove the testing results for the 9th grade students at THS and report the differences in the following data summaries:
1. District Summary
2. Per School Summary
3. How removing 9th grade results from data affects Thomas High School's passing metrics relative to the other schools
4. How removing 9th grade results from data affects district summary results based on:

    a. Math and reading scores by grade by school
    
    b. Math and reading scores by school spending
    
    c. Math and reading scores by school size
    
    d. Math and reading scores by school type

## Resources
- Data Sources:
    - School data: schools_complete.csv
    - Student data: students_complete.csv
- Software: Python 3.7.6, Jupyter Notebook, Pandas, Numpy
- Documentation Help: https://stackoverflow.com/questions/37725195/pandas-replace-values-based-on-index

## Results
The results below show the changes in the summary data by removing the scores for THS's 9th grade students.


### District summary results
Analysis showed **no significant change in district-wide data** by removing the scores of THS 9th graders. The district summary is shown in Picture 1.1 below.

**Picture 1.1:** Overall District Test Performance

![Overall District Test Performance](https://github.com/joshuanallen/School_District_Analysis/blob/9aa3a2212ee98ffd144fc92617635652a77c3e35/Images/THS_9th_Removed/District_Summary_Data_Frame_wo_THS9.png)

### Per school summary results
Analysis showed **no change to school summary data outside of the data for THS**. The original school summary is shown in Picture 2.1 and updated school summary is shown in Picture 2.2.

The highlighted data shows the THS with small changes to the overall scores and passing percentages. The changes are outlined below:

- Average math score went down by 0.07 points
- Average reading score increased by 0.05 points
- Math passing percentage decreased by 0.08%
- Reading passing percentage decreased by 0.29%
- Overall passing percentage decreased by 0.32%

**Picture 2.1:** School test performance **before** THS 9th grade data removal

![School test performance before THS 9th grade data removal](https://github.com/joshuanallen/School_District_Analysis/blob/9aa3a2212ee98ffd144fc92617635652a77c3e35/Images/THS_9th_Kept/School_Summary_Data_Frame_og.png)

**Picture 2.2:** School test performance **after** THS 9th grade data removal

![School test performance after THS 9th grade data removal](https://github.com/joshuanallen/School_District_Analysis/blob/9aa3a2212ee98ffd144fc92617635652a77c3e35/Images/THS_9th_Removed/School_Summary_Data_Frame_wo_THS9.png)

### Thomas HS relative change results
Analysis shows the following changes to THS's students scores and passing metrics relative to other schools in the district after removing the 9th graders' scores from the data set shown in Picture 2.2:

- THS retains its 2nd school ranking by overall passing percentage despite a 0.32% drop
- THS retains its 7th school ranking by overall math passing percentage despite a 0.08% drop
- THS drops from its 1st to 3rd school ranking by overall reading passing percentage because of its 0.29% drop (falling behind Griffin and Cabrera HS)
- THS retains its 5th school ranking by average reading score despite a 0.05 point increase
- THS drops from its 4th to 6th school ranking by average math score despite a 0.07 point decrease


### Effect on district slicing results
Replacing THS 9th grade test scores affected the performance summaries in the following ways:

a. Average math and reading scores by grade by school (See Picture 4.1 and 4.2)
    - No effect on scores other than having absence of data (NaN) for Thomas HS in the 9th grade column

**Picture 4.1:** Average reading score by grade by school

![Average reading score by grade by school](https://github.com/joshuanallen/School_District_Analysis/blob/9aa3a2212ee98ffd144fc92617635652a77c3e35/Images/THS_9th_Removed/Avg_reading_scores_by_grade_by_school_wo_THS9.png)

**Picture 4.2:** Average math score by grade by school

![Average math score by grade by school](https://github.com/joshuanallen/School_District_Analysis/blob/9aa3a2212ee98ffd144fc92617635652a77c3e35/Images/THS_9th_Removed/Avg_math_score_by_grade_by_school_wo_THS9.png)

b. Scores by school spending (See Picture 4.3 and 4.4)
    - Insignificant effect for "$630-$644" category

**Picture 4.3:** Student test performance by per student spending **before** THS 9th grade data removal

![Student test performance by per student spending before THS 9th grade data removal](https://github.com/joshuanallen/School_District_Analysis/blob/9aa3a2212ee98ffd144fc92617635652a77c3e35/Images/THS_9th_Kept/Avg_scores_by_school_spending_per_student_og.png)

**Picture 4.4:** Student test performance by per student spending **after** THS 9th grade data removal

![Student test performance by per student spending after THS 9th grade data removal](https://github.com/joshuanallen/School_District_Analysis/blob/9aa3a2212ee98ffd144fc92617635652a77c3e35/Images/THS_9th_Removed/Avg_scores_by_school_spending_per_student_wo_THS9.png)

c. Scores by school size (see Pictures 4.5 and 4.6)
    - Insignificant effect for "Medium" size category

**Picture 4.5:** Student test performance by school size **before** THS 9th grade data removal

![Student test performance by school size before THS 9th grade data removal](https://github.com/joshuanallen/School_District_Analysis/blob/9aa3a2212ee98ffd144fc92617635652a77c3e35/Images/THS_9th_Kept/Avg_scores_by_school_size_og.png)

**Picture 4.6:** Student test performance by school size **after** THS 9th grade data removal

![Student test performance by school size after THS 9th grade data removal](https://github.com/joshuanallen/School_District_Analysis/blob/9aa3a2212ee98ffd144fc92617635652a77c3e35/Images/THS_9th_Removed/Avg_scores_by_school_size_wo_THS9.png)

d. Scores by school type (see pictures 4.7 and 4.8)
    - Insignificant effect for "Charter" school category

**Picture 4.7:** Student test performance by school type **before** THS 9th grade data removal

![Student test performance by school type before THS 9th grade data removal](https://github.com/joshuanallen/School_District_Analysis/blob/9aa3a2212ee98ffd144fc92617635652a77c3e35/Images/THS_9th_Kept/Avg_scores_by_school_type_og.png)

**Picture 4.8:** Student test performance by school type **after** THS 9th grade data removal

![Student test performance by school type after THS 9th grade data removal](https://github.com/joshuanallen/School_District_Analysis/blob/9aa3a2212ee98ffd144fc92617635652a77c3e35/Images/THS_9th_Removed/Avg_scores_by_school_type_wo_THS9.png)

## Summary
THS 9th graders test scores changed the overall THS test results minimally because their scores may not have been far off of the school averages for math and reading. The reading scores changed the most by the removal of the 9th grade THS data but not enough to significantly change district-wide results for any given category (size, type, funding level).

The heaviest effect the removal of the scores had on the new data was the change in the rankings for THS relative to the performance of other schools in the district. Specifically in the overall reading passing percentage and average math score; both of which decreased by 2 spots as a result of the changing data. However, the change did not affect the rankings for math passing percentage, overall passing percentage, and average reading score.

### Limitations of current data set
To further our analysis and understand if academic dishonesty did occur, we would have to analyze the scores across multpile years of data to show if the current 9th grade class performance is an outlier compared to the students' previous testing results and historical data for testing results for 9th graders at THS and across the district.
