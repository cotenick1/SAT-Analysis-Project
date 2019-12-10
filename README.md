# How to Increase SAT Participation

----
## Problem Statement
 

The SAT released an updated format of its test in 2016.  However, we are finding that in most states, the ACT is the dominant test that is the more commonly taken test for high schoolers.  We have been given SAT and ACT data (as further detailed in the data dictionary below) and are tasked with determining how best to increase participation on the SAT, particularly in states that have low participation on the SAT (generally looking at states with less than 5% participation).  After cleaning and exploring the data, running analyses, and coming to recommendations based on the data, we are to provide these recommendations to the College Board.

This project was completed with General Assembly in September 2019.

----
## Data Directory

|Feature|Type|Dataset|Description|
|---|---|---|---|
|**State**|*string*|ACT and SAT|The state or Washington D.C. in question| 
|**2017 SAT Participation**|*float*|SAT|The percent of students in the 2017 graduating class that took the SAT|
|**2017 SAT Reading and Writing**|*float*|SAT|The average score on the SAT Reading & Writing section among students that took the test in a given state in 2017|
|**2017 SAT Math**|*float*|SAT|The average score on the SAT Math section among students that took the test in a given state in 2017|
|**2017 SAT Total**|*float*|SAT|The average total score on the SAT (Math + English & Reading) among students that took the test in a given state in 2017|
|**2018 SAT Participation**|*float*|SAT|The percent of students in the 2018 graduating class that took the SAT in a given state|
|**2018 SAT Reading and Writing**|*float*|SAT|The average score on the SAT Reading & Writing section among students that took the test in a given state in 2018|
|**2018 SAT Math**|*float*|SAT|The average score on the SAT Math section among students that took the test in a given state in 2018|
|**2018 SAT Total**|*float*|SAT|The average total score on the SAT (Math + English & Reading) among students that took the test in a given state in 2018|
|**2017 ACT Participation**|*float*|ACT|The percent of students in the 2017 graduating class that took the ACT in a given state|
|**2017 ACT English**|*float*|ACT|The average score on the ACT English section among students that took the test in a given state in 2017|
|**2017 ACT Math**|*float*|ACT|The average score on the ACT Math section among students that took the test in a given state in 2017|
|**2017 ACT Reading**|*float*|ACT|The average score on the ACT Reading section among students that took the test in a given state in 2017|
|**2017 ACT Science**|*float*|ACT|The average score on the ACT Science section among students that took the test in a given state in 2017|
|**2017 ACT Composite**|*float*|ACT|The average score on the ACT Composite, which represents an average of the four section scores, among students that took the test in a given state in 2017|
|**2018 ACT Participation**|*float*|ACT|The percent of students in the 2018 graduating class that took the ACT in a given state|
|**2018 ACT Composite**|*float*|ACT|The average score on the ACT Composite, which represents an average of the four section scores, among students that took the test in a given state in 2018|

----
## Executive Summary

My first step on this exercise was cleaning the data we were given.  Notably, the files I received contained errors with Maryland's data that needed to be reconciled with the source.  Additionally, I needed to scrub for any duplicates or errors in data types.  Finally, I was able to combine all 2017 and 2018 SAT and ACT data into one data frame to begin our Exploratory Data Analysis.

With our Exploratory Data Analysis, it was important to being to identify any trends that needed to be investigated further.  First off, I looked at distributions for each tests participation, subject, and total scores as well as the mean and median for each set of data.  With this, we came to our first interesting conclusion, which is that the data did not follow a normal distribution - states tended to have high or low participation on a test, high or low scores on a test, which led to a distribution heavily concentrated around the high and low end of the range. 

One other notable observation from this stage that informed the remaining stages was that the states that tended to have low participation on one test had high participation in another.  Moreover, states with low participation on the SAT actually had high average test scores.  This was helpful in informing what type of student was taking each test.  

From there, it was important to being to do an analysis of data relationships so that we could identify any trends in causation.  As mentioned above, I was particularly interested in examining the relationship between participation and score.  Scatterplots and correlation coefficients confirmed what I had observed during Exploratory Data Analysis - there was a strong negative correlation between participation and average score.   In conjunction with that, we observed correlations between scores on ACT and SAT and found a negative correlation.  We also examined relationships between different subjects across the two tests. 

Finally, as part of our conclusions, I looked at various statewide policies to implement the ACT or SAT.  I looked at states that encouraged the SAT or ACT or some combination of the two and various ways to increase participation on the SAT outside of mandatory requirements.  

----
## Conclusions and Recommendations

First and foremost, I would like to point out that while this data is helpful for uncovering some trends, to find more substantial cause and effect relationships we will need to find more substantial data sets (as I will cover later). That being said, there are some very interesting trends to look at that I believe are worth examining further.

In trying to find out a way to increase SAT Participation, the first think I wanted to see is if we should be convincing students to switch tests or simply to take a new test; as in, are students who don't take the SAT taking the ACT instead.  In looking at the states with the lowest SAT participation, we see that they all have extremely high ACT participation.  Largely speaking, these students take a test, its just not the SAT.

Next, fI watned to see if we could find a trend amongst how SAT and ACT scores are correlated with participation.  This was the most revealing portion of the exercise.  We found that average state score is (heavily) inversely correlated with participation; that is, low participation states had high average scores and high participation states had lower average scores. 

It is useful to think about why this is the case.  Intuitively, the conclusion I came to is that in states where the ACT is the norm, it is only those students who are most affluent and motivated who will seek out the SAT.  And this is where we run into our huge problem.  

For instance, I look at a state like Wisconsin, which maintains the second highest average SAT score yet only a 3% participation rate.  The takeaway here is not that students from Wisconsin are particularly bright (although that may be the case, but the point is that we don't really have data to support this claim).  Students in Wisconsin already face a high level of competition due to Wisconsin's prestigous public university system.  The last thing they need is to dip their toe into a more competitive test that may well make themn look weaker on testing compared to their peers due to the subset already taking the SAT.  

As such, my key takeaway on how to increase SAT participation is not in making the test more accessible or advertising heavier; they key is to allocate resources to free/discounted tutors and classess.  This will help close the preparation gap between wealthier/more skilled students and give students more confidence when choosing to prepare for the SAT.  Convince students that their scores can actually look good and you will see a bump in participation.  

I also chose Wisconsin as my test case due to its relatively high population density compared to its peers in the low SAT participation category.  It is constantly around the middle for the United STates in terms of population density - interestingly, rural states with lower population density tend to take the ACT.  I would want to choose a more densely populated states to capture any potential network effects - does work of the new training spread quickly?  Will it spread more amongst populous groups and areas?  I think this is a useful test case.

There are a number of areas to test as a follow up.  First off is adjusting for household income when calculation these scores.  The second is adjusting for cost of the tests - is there anything inherently different about the SAT that is minimizing participation.  Finally, doing a more formal population density analysis to see if there is anything to the idea that more densely populated areas are more likely to take one test. It seems to me this is more driven by state policy and tradition but this is certainly something worth looking at.

----
## Sources

http://worldpopulationreview.com/states/state-densities/

https://www.daytondailynews.com/news/too-much-testing-some-schools-angry-with-ohio-act-sat-mandate/5lPdirdJ68IuXs1ez7Mv7L/#

https://www.testive.com/colorado-sat-change-2017/

https://www.staradvertiser.com/2011/02/25/breaking-news/free-sat-act-prep-courses-available-online-to-hawaii-students/

https://git.generalassemb.ly/DSI-US-9/project_1/blob/master/data/sat_2017.csv

https://git.generalassemb.ly/DSI-US-9/project_1/blob/master/data/act_2017.csv

https://git.generalassemb.ly/DSI-US-9/project_1/blob/master/data/sat_2018.csv

https://git.generalassemb.ly/DSI-US-9/project_1/blob/master/data/act_2018.csv

https://blog.collegevine.com/here-are-the-average-sat-scores-by-state/

https://blog.prepscholar.com/act-scores-by-state-averages-highs-and-lows
