# School District Analysis

## Overview of Analysis

I was initially hired by Maria to help perform data analysis on performance trends for schools based on student funding and test scores.  Following completion of the analysis, the school board contacted Maria and wanted further analysis due to the files showing evidence of academic dishonesty in 9th grade test results for Thomas High School.

### Results

The first step in this analysis was to use the loc method to replace the ninth grade students math and reading scores with NaN in order to verify if these changes would affect the district analysis.
•	There was no discernable effect on the district summary. In the image below we see that prior to replacing Thomas High School ninth grade test scores with NaN, percentage passing math was 74.8%, the percentage passing reading was 85.7%, and the overall passing percentage was 64.9%.

 ![image](https://user-images.githubusercontent.com/104471775/172735312-0978ad5a-2981-4765-ba89-d94e073eeb71.png)


In the image below, we see that after replacing the Thomas High School ninth grade scores the percentages barely changed. 

 ![image](https://user-images.githubusercontent.com/104471775/172735338-a2a1d1c9-89de-4797-a79a-d7a6a13e3159.png)


•	The school summary was only affected in that Thomas High School’s averages increased.  All other school information did not change.  Total school budgets, per student budgets, average scores, and percentage passed did not change.  The only noticeable change to the school summary was the performance of Thomas High School. As seen in the images below, when Thomas High School data contained all four grade levels, the percentage of students passing math and reading was in the low 60’s.  
 ![image](https://user-images.githubusercontent.com/104471775/172735363-83d41e94-4029-41c2-9d90-3e14ef19fef6.png)

But when you discount ninth grade scores, Thomas High School appears to perform better with the percentage of students passing increasing into the 90th percentile.

 ![image](https://user-images.githubusercontent.com/104471775/172735383-dcfe5dbe-e1fb-4cea-95b8-3369531cc9af.png)


•	When compared to other schools in the district, Thomas High School maintained a position in the middle of all the schools in the district.  The top five performing schools nor the bottom five performing schools changed.
 ![image](https://user-images.githubusercontent.com/104471775/172735408-ccef8e01-36c4-4d80-8e96-c461bb2f6485.png)


![image](https://user-images.githubusercontent.com/104471775/172735430-e52e0f86-4e1c-42d2-945c-9a61f746e473.png)

 


•	Math and reading scores by grade were calculated by using the groupby method, (ninth_grade_math_scores = ninth_graders.groupby(["school_name"]).mean()["math_score"]).  The only scores affected by the change would be those of Thomas High School ninth graders. None of the other schools would be affected by the change nor would any of the other grade levels.

•	Scores by school spending remained the same.

•	Scores by school size changed minutely in the medium range. 
![image](https://user-images.githubusercontent.com/104471775/172735459-b4664122-208e-4e0f-8c42-e30ae23b1fa8.png)

  
![image](https://user-images.githubusercontent.com/104471775/172735474-e45d6914-371e-4522-8a79-ac5c211fd0c9.png)


 

•	Scores by school type did not change.


#### Summary
Changes:
1.	In the district summary, % overall passing changed to 64.9%.
2.	Thomas High School % passing math changed to 93%.
3.	Thomas High School % passing reading changed to 97%.
4.	Thomas High School overall passing percentage change to 91%.
