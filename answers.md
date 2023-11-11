Answers:
1) Given that the TA is Kinan, 
- I know that he must be atleast 22 and older since he is a grad student and thus would have a lower bound of 22 (unless he started college much earlier cause he's super smart). 
- From this criteria I can conclude that the TA likes one of Country, Pop, Rock, Metal or Classical. 
- This only rules out Hip Hop and House music. Thus I didn't find this super conclusive.
2) 
- I found Kinan's Facebook page where it says he was born in 1994 which implies that he must be 29. 
- I am not including the case where his birthday is later in November/December because there is no one who is aged 28 on the survey. 
- I also found that Kinan likes Metal music on his website. Thus I can put these 2 pieces of information together to deduce that the user that submitted age 29 and Metal must be Kinan. 
3) The TAs favorite color must be either Black or Yellow but given that limited data set I only have 50% chance of getting it right. It's easy to narrow it down to this because of the differencing attack used above limited my range of possibilities to just the 2 people who are age 29.
4)
- We know that Kinan's age = 29 and thus limit our data to: 25 or more
- This leaves the only options as Baseball, Basketball, E-Sports and Soccer
5)
- Combining with the previous year's data set we can conclude that it must be Soccer or E-Sports since we are looking at the intersection of the sets of data where agegroup is 25 or more.
- We also know that Kinan must have been greater than 25 last year so we are able to limit our data set 25 or more.
- If we use a more fine grained query, determining the TAs favorite sport is much easier since the only sport for the 2 people who are 29 is Soccer.

6)
- As epsilon approaches 0 we see that privacy increases as the counts reveal much less data about the data subjecs, e.g. for 0.01 it is impossible to tell what the original counts might have been. 
- Conversely, as epsilon increases, the privacy decreases but the data becomes more and more accurate e.g. for epsilon >= 10 it is essentially the same as not even applying differential privacy operator to it.
    - This means that privacy is reduced since increases in epsilon get us closer and closer to the original dataset.

7) 
- The most likely value is 1 as seen by the peak of the graph.
- The average is 0.92 since we divide the total value of the counts accrued of the iterations by number of iterations
- Without dp, the most likely value would be 1 and the average would also be 1. Thus we are not too far off from the original data set.
8)
- From the exposed averages I can deduce that the TA has more than 10 years of experience since avg age of people in that category is 28. 
- However, since this is taking the average of the ages, this data could be skewed if, for example, the 8-10 yrs of experience group with avg age of 23 had a significant number of people who were younger than 23, even if the data group contained the TA.

9) I can very confidently deduce that Kinan has more than 10 years of experience since there are only 4 people in this category and thus it would be very difficult for the mean to be heavily skewed. 
In summary,
- Kinan is 29 years old, likes Metal music, favorite sport is soccer, favorite color is either Black or Yellow and that he has more than 10 years of programming experience.

10)
- I don't believe that this is in any way a sufficient implementation for budget checks. A developer could maliciously or unmaliciously make concurrent queries and since there is no handling of thread safety such as using atomics, the budget check might pass for concurrent requests even if it wouldn't have passed had the requests been concurrent. Furthermore, if there are multiple instances of the BudgetTracker class in the program, they would each have their own budget and thus wouldn't actually be a global way to track the budget.
- On a high level, we would have to account for thread safety by introducing mutexes or atomic operators
- We would have to employ the Singleton design pattern to ensure there is only ever one instance of the BudgetTracker class.
- We would also have to include some compile time checks to ensure that developers are actually using the BudgetTracker wrapper rather than just directly querying the database.


