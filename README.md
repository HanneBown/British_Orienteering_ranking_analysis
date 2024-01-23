# Cambridge Spark Level 4 Data analyst bootcamp portfolio

Last week I completed the Cambridge Spark Level 4 Data Analyst bootcamp. As a part of the course, to practice and demonstrate all the skills we learned during the ten week intensive course, we had a portfolio task. For this task I downloaded the British Orienteering ranking data from https://www.britishorienteering.org.uk/rankings on 11th of December 2023. In this post I am going to showcase my data visualisation for the dataset. For my narrative on data cleansing and exploratory data analysis please have a look at the Jupyter notebook.

## Age and gender distribution of ranked orienteers

I think we need some more youngsters in the sport as there is a distinct plateau in the number of ranked orienteers between ages 20 and 40! This may partly be due to orienteers of this age having young families, and hence being less likely to get out there in the wildest of British weathers! When the age distrubution is broken down by gender, same patterns in the distribution are apparent, but with fewer ranked female than male orienteers across all the ages.

![Untitled](https://github.com/HanneBown/British_orienteering_ranking_data_analysis/assets/153863652/49b63b5e-2d3d-49c5-9829-6d85b987eb01)

![Untitled](https://github.com/HanneBown/British_orienteering_ranking_data_analysis/assets/153863652/8fc3a0e5-bd5e-4775-bd10-8396062b315f)

## Maximum ranking score for each age

I wanted to explore the maximum ranking score for each unique age within the ranking list to see what the peak performance age for orienteers was. A graph showing the maximum average ranking score for each unique age is shown below. It can be seen that orienteers up to approximately 40-years-old are evenly matched before the maximum average ranking score for each unique age starts to decrease. The idea of the ranking list is to 'predict' the outcome of a hypothetical orienteering race where everyone was competing together, and the ranking scores are based on individual orienteers' performances in races over the past 12-month-period. Therefore, it could be expected that the older age groups have noticeably lower maximum average ranking scores for each unique age as they are less able to compete against younger orienteers. This is indeed shown by the data. The data also highlights that females have lower maximum ranking score for each unique age than males. That said, there are some females whose scores are similar to the scores of males around the same age. 

![Untitled-1](https://github.com/HanneBown/British_orienteering_ranking_data_analysis/assets/153863652/805d647d-1784-4d5f-b100-655491afb3af)

![Untitled](https://github.com/HanneBown/British_orienteering_ranking_data_analysis/assets/153863652/217ef682-b1dd-4f85-99e0-b10e2116866b)

## Distribution of ranking scores 

The distribution of average ranking scores across all the ranked runners follows more or less a Bell shape curve - before plotting this figure I had removed any outliers that were more than 3 standard deviations smaller than the average.

![Untitled](https://github.com/HanneBown/British_orienteering_ranking_data_analysis/assets/153863652/6bacc7af-594b-4ae1-badd-eeab92f3d28a)

## Average ranking score by club

A graph of the mean average ranking score by club is shown below. There are roughly ten clubs with noticeably higher mean average ranking scores than others, followed by a gradual decrease in the mean average ranking score for the rest of the clubs. I have also included a graph for the top-25 clubs where the club names are more easily legible. It can be seen that eight out of the top-ten clubs are either university clubs or university alumni clubs. It could be assumed that the runners in these clubs are younger, and therefore perhaps fitter, scoring higher average ranking points. 

![Untitled-1](https://github.com/HanneBown/British_orienteering_ranking_data_analysis/assets/153863652/05aa8d08-bbb7-4014-ba18-e36cf161596c)

![Untitled](https://github.com/HanneBown/British_orienteering_ranking_data_analysis/assets/153863652/a5814871-9403-469b-b9b1-0ad80624f199)

## Average age of ranked orienteers by club

To test my hypothesis about the runners in university and university alumni clubs being younger, I plotted the average age by club. Again, there is too much data on this graph to enable detailed analysis, but the drastic drop in average age on the right hand side of the graph caught my attention. 

![Untitled-1](https://github.com/HanneBown/British_orienteering_ranking_data_analysis/assets/153863652/d45ae0ef-5130-4b37-8412-3b05daf033b6)

## Number of ranked orienteers by club

Another thing I noticed when looking at the graphs I had produced so far was the size of the error bars for mean average ranking score per club and mean age per club. This got me wondering about the numbers of ranked runners in each club, which is what I plotted next. The data shows that there is indeed a large span in the number of ranked runners in different clubs, with the range varying from one to more than 175. 

![Untitled](https://github.com/HanneBown/British_orienteering_ranking_data_analysis/assets/153863652/635ad654-b982-4b80-8d5b-218a7ca8d6c4)

## Building an interactive plot for average ranking score as a function of average age for ranked orienteers in each club

To bring all my observations, as well as lot of the learning from the bootcamp, together, I used plotly to build an interactive graph, you can view the interactive plot by scrolling to the bottom of the Jupyter notebook in here: https://nbviewer.org/github/HanneBown/British_Orienteering_ranking_analysis/blob/main/British%20Orienteering%20rankings%20data.ipynb 
I have also included a static version of the graph below but I do encourage you to have a play with the interactive features in the original plot! The graph displays the mean average ranking score as a function of mean age, grouped by club. A general trend of clubs with younger runners having higher average ranking score is apparent. Upon hovering over some of the datapoints at both extremities of ages, it can be seen that some of the clubs have fewer than ten ranked runners. This is something that may make the clubs look 'better' or 'worse' depending on the ability of the runners within the club, as the membership is not typical of the rest of the orienteering demographic.

![newplot(1)](https://github.com/HanneBown/British_orienteering_ranking_data_analysis/assets/153863652/b60e7dfc-affb-4f53-9657-70f1dca5028b)

