# 2024 ASA DataFest at UCLA
## Challenge Description
The CourseKata project aims to improve the learning experience of students studying statistics and data science by analyzing their interaction data with the online interactive textbooks. This dataset contains interactions from 1625 students across 48 college-level statistics and data science courses in the U.S. (2023). Your challenge is to examine this data to generate actionable insights and provide suggestions for improving the student learning experience.

## First Suggestion: 'Who' should instructors provide help? - Alert system
- To enhance the learning experience, providing the right help at the right time is crucial. With this in mind, I propose the idea of an alert system that identifies students who are likely to struggle and could possibly notifies teachers accordingly.

- The goal of this suggestion is to develop a predictive model that can estimate a student’s future performance in end-of-chapter (EOC) assessments based on their previous performance. Specifically, we aim to predict scores for future chapters by analyzing a student's scores up until that point using the 'checkpoint_eoc.csv' file.

- The dataset contains the following columns:

  **student_id**: A unique identifier for each student.

  **book**: The name of the book used in the course (in this case, "College / Advanced Statistics and Data Science (ABCD)").

  **chapter_number**: The chapter number corresponding to the EOC question.

  **EOC**: The score the student achieved on the EOC for that chapter.

  This structure allows us to leverage a student's past performance in earlier chapters (e.g., Chapter 1, 2, 3) to predict how they will perform in subsequent chapters.

## Second Suggestion: 'When' and 'How' Should Instructors Provide Help? - Analyzing Psychological Attitude to Identify Key Differences Between Top and Bottom Performers

- To examine how students feel during their learning process and to identify actionable ways instructors can intervene effectively.
  
- Specifically, we aim to uncover key psychological and behavioral differences between the top 10% performing students and the bottom 10% performing students. This insight will inform strategies for timely and impactful interventions.

- To conduct this analysis, we use two datasets, checkpoints_pulse.csv and page_views.csv, each capturing different aspects of student interactions and attitudes:

#### page_views.csv
This dataset contains detailed information about students' engagement and behavior during their interaction with course materials. The key variables are:

* chapter: The chapter where the item appears.
* class_id: Unique identifier for the class.
* was_complete: Indicates whether the student returned to an already completed page.

#### checkpoints_pulse.csv
This dataset captures students' psychological attitudes and perceptions during the course. Key variables include:

* construct: Psychological constructs measured (e.g., Cost, Expectancy, Intrinsic Value, Utility Value).
* response: Students’ responses to pulse-check items.
* class_id, student_id, and institution_id: Unique identifiers for tracking responses.
* chapter_number: Numeric chapter indicator.

### Analysis Approach
* Segmentation: Split students into the top 10% and bottom 10% performers based on EOC(End of Chapter test) score.
* Behavioral Analysis: Examine differences in engagement patterns between the two groups.
* Psychological Attitudes: Analyze construct responses from checkpoints_pulse.csv to compare attitudes like Expectancy, Utility Value, and Intrinsic Value.
* Integration: Cross-analyze behavior and attitudes to identify correlations between psychological constructs and performance.
