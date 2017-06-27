# Interview_Practise
Interview Practice (Data Analyst)
By Sargam Shah
Interview Questions:
1.	Describe a data project you worked recently
I recently worked on a project which aimed at Data Wrangling of Openstreet Map Data. Data wrangling is, basically, cleaning the data and converting it into a format which is acceptable by the database in use. Data Wrangling takes about 75-80 % of the time involved in the data analysis process and it needs to be done correctly. I could achieve success in this task and discovered interesting facts about the city I chose.  
I started off by selecting a region of San Antonio. I used Python to first explore the data and Jupyter notebooks to thoroughly document my work. Auditing the data gave me insights on the total paths in the city, total users who contributed to the map information. I solved problems encountered due to human error such as abbreviated street addresses, viz, Carrolton Rd instead of Carrolton Raod, and improper zip codes such as TX 78012 instead of simply putting 78012.
I converted XML to JSON to prepare the data for MongoDB using Python. Later, I loaded the data in MongoDB and made it ready for further exploratory analysis tasks. I performed few queries using aggregations to find out top five restaurants, list of amenities etc in the city of San Antonio.
After this project, I have become confident in the crucial data wrangling part of the data analysis.


2.	You are given a ten-piece box of chocolate truffles. You know based on the label that six of the pieces have an orange cream filling and four of the pieces have a coconut filling. If you were to eat four pieces in a row, what is the probability that the first two pieces you eat have an orange cream filling and the last two have a coconut filling? 
Follow-up question: If you were given an identical box of chocolates and again eat four pieces in a row, what is the probability that exactly two contain coconut filling? 
7.1 % probability that first two are orange and last two are coconut.
Calculations: 6/10 * 5/9 * 4/8 *3/7
Follow-up : There are 6 combinations. So, multiplying by 6, we get 0.07 * 6 = 0.42.
Thus there is approx.. 42 % probability of getting exactly two coconut filling. 






3.	Given the table users: construct a query to find the top 5 states with the highest number of active users. Include the number for each state in the query result. Example result:
  
SELECT state, SUM(active)
from users
GROUP BY state
ORDER BY SUM(active) DESC
LIMIT 5

4.	Define a function first_unique that takes a string as input and returns the first non-repeated (unique) character in the input string. If there are no unique characters return None. Note: Your code should be in Python.

from collections import defaultdict
def first_unique(word):
    '''initiate defaultdict for count'''   
    counts = defaultdict(int)
    ''' create empty list'''
    l = []
    '''loop through each character in a string'''
    for c in word:
        counts[c] += 1
        '''if there's first unique character, append them to list'''
        if counts[c] == 1:
            l.append(c)
    ''' if list only contains 1 character, return the result'''        
    for c in l:
        if counts[c] == 1:
            return c
    ''' otherwise, return "None"" '''
    return "None"


5.	What are underfitting and overfitting in the context of Machine Learning? How might you balance them?
In Machine Learning, 

6.	If you were to start your data analyst position today, what would be your goals a year from now?


https://www.linkedin.com/jobs/view/362041007/
