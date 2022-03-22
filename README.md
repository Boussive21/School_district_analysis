# School_district_analysis
# Intro  
A school board wishes for Maria to go through the students_complete.csv and see if there are signs of academic dishonesty in the school districts. Looking at the reading and math grades at Thomas high school the school boards believe that they can get an accurate summation of how deep the issue is in the high school. The school board does believe that there has been significant manipulation of grades in the 9th grade groups but can’t pinpoints which ones have been manipulated and they can’t rule out the rest of the grades as well. So we have been tasked with creating a program that can sort out all the data and give an accurate snapshot of the school districts test score using Python in Jupiter notebook.
#Process
In Jupiter note book we created data frames that looked like school_data_complete_df = pd.merge(student_data_df, school_data_df, how="left", on=["school_name", "school_name"])
school_data_complete_df.head() this an example of one of the data frames we created to categorize the students. 
We also where able to remove suspected cheaters by NaaN and this lowered the overall for the students at those respective schools. student_data_df.loc[(student_data_df["school_name"] == "Thomas High School") & (student_data_df["grade"] == "9th")  & (student_data_df["math_score"] >0),"math_score" ] = np.nan
#Results
What doing this creates these types of results show:
 
•	Because of potential cheating in Thomas Highschool from the results reducing their score to  65 percent. 
•	The removal of dishonest results also removed create a over all passing rate of 64.9 percent
•	 This however still puts them in the middle of the pack in terms of test scores.  

#Conclusion
From the data we gathered there is there is we did see the intended results of Thomas school average plummeting and giving us a more accurate representation of the schools performance as whole. But one of the unintended consequences is by omitting all of ninth grades math results brings the whole school district down with it. Thus, tainting the results of the average if we were able exclude it from the data we would have a better dataset.    
![School_chart](https://user-images.githubusercontent.com/99147715/159393110-7495f687-db1f-4d6a-9211-a4787bb67b60.PNG)
![Total_schools](https://user-images.githubusercontent.com/99147715/159393166-a686b3c2-5e32-4e26-8285-73a381a06834.PNG)
