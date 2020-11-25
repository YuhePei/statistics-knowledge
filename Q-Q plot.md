Q-Q plot is quantile-quantile plot for short. And it can examine whether a set of data conform to a certain distribution. Also, it can test whether two data set have same distribution.

**how to draw Q-Q plot**

**one dataset**
1. Rank all the data in ascend order
2. Count the quantile for every data. for data Xi, its quantile Pi can bFe calculated as Pi=(i-0.5)/n. (note that at this place mines 0.5 is for to find limits, in other place the quantile need not mines 0.5)
3. Find the value the quantile Pi corresponces in theoretical distribution Yi for every Pi
4. Create the Q-Q plot using Xi as Y-axis and Yi as X-axis ~~(sounds a bit odd ahhh)~~ for each data 

**two dataset**
1. First we need to check whether two dataset have same data. if not, we need to fill the dataset with small data to the same amount of data with big data
2. Now that they have same amount of data, draw the Q-Q plot using one sameple as X-axis and another as Y-axis

**how to read Q-Q plot**

If points falling along a straight line, we can say the dataset conform to a certain distribution or two dataset come from same distribution. 
But we should be noticed that Q-Q plot just give us a quick and visual glance at the dataset distribution. It is not a strict proof.

**an example of R realization**

First we create a dataset fit standard normal distribution with 100 data and means of 10.
```
data <- rnorm(100,mean =10 )
```
Then we draw the Q-Q plot.
```
qqnorm(data)
```
We can see that point nearly falling along a straight line.
With the increase of the data, the straight line will meet more precisely.

**reference**
1. https://data.library.virginia.edu/understanding-q-q-plots/
2. https://www.jianshu.com/p/4c5a6dc44dda
