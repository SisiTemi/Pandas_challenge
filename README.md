# Pandas_challenge

PYCITY SCHOOL ANALYSIS

UsED Pandas and Jupyter Notebook, TO create a report that includes the following data, report must include a written description of at least two observable trends based on the data.

DISTRICT SUMMARY:

Perform the necessary calculations and then create a high-level snapshot of the district's key metrics in a DataFrame.

Include the following:

    Total number of unique schools

    Total students

    Total budget

    Average math score

    Average reading score

    % passing math (the percentage of students who passed math)

    % passing reading (the percentage of students who passed reading)

    % overall passing (the percentage of students who passed math AND reading)

SCHOOL SUMMARY:

Perform the necessary calculations and then create a DataFrame that summarizes key metrics about each school.

Include the following:

    School name

    School type

    Total students

    Total school budget

    Per student budget

    Average math score

    Average reading score

    % passing math (the percentage of students who passed math)

    % passing reading (the percentage of students who passed reading)

    % overall passing (the percentage of students who passed math AND reading)

Highest-Performing Schools (by % Overall Passing)
*Sort the schools by % Overall Passing in descending order and display the top 5 rows.
*Save the results in a DataFrame called "top_schools".

Lowest-Performing Schools (by % Overall Passing)
*Sort the schools by % Overall Passing in ascending order and display the top 5 rows.
*Save the results in a DataFrame called "bottom_schools".

MATH SCORE BY GRADE
*Perform the necessary calculations to create a DataFrame that lists the average math score for students of each grade level (9th, 10th, 11th, 12th) at each school.

READING SCORES BY GRADE
*Create a DataFrame that lists the average reading score for students of each grade level (9th, 10th, 11th, 12th) at each school.

SCORES BY SCHOOL SPENDING
*Create a table that breaks down school performance based on average spending ranges (per student).

Use pd.cut to categorize spending based on the bins.
Use the following code to then calculate mean scores per spending range.

spending_math_scores = school_spending_df.groupby(["Spending Ranges (Per Student)"])["Average Math Score"].mean()
spending_reading_scores = school_spending_df.groupby(["Spending Ranges (Per Student)"])["Average Reading Score"].mean()
spending_passing_math = school_spending_df.groupby(["Spending Ranges (Per Student)"])["% Passing Math"].mean()
spending_passing_reading = school_spending_df.groupby(["Spending Ranges (Per Student)"])["% Passing Reading"].mean()
overall_passing_spending = school_spending_df.groupby(["Spending Ranges (Per Student)"])["% Overall Passing"].mean()

Use the scores above to create a DataFrame called spending_summary.
Include the following metrics in the table:

    *Average math score

    *Average reading score

    *% passing math (the percentage of students who passed math)

    *% passing reading (the percentage of students who passed reading)

    *% overall passing (the percentage of students who passed math AND reading)

SCORES BY SCHOOL SIZE

Use the following code to bin the per_school_summary.

size_bins = [0, 1000, 2000, 5000]
labels = ["Small (<1000)", "Medium (1000-2000)", "Large (2000-5000)"]

Use pd.cut on the "Total Students" column of the per_school_summary DataFrame.
Create a DataFrame called size_summary that breaks down school performance based on school size (small, medium, or large).

SCORES BY SCHOOL TYPES

Use the per_school_summary DataFrame from the previous step to create a new DataFrame called type_summary.
This new DataFrame should show school performance based on the "School Type".
