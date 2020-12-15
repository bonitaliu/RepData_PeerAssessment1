Reproducible Research: Peer Assessment 1
================
Bonita Liu
12/14/2020

## Reading the data

This code chunk shows how the data is read into R:

``` r
activity <- read.csv(file = "activity.csv")
```

## What is mean total number of steps taken per day?

The total number, mean, and median, of steps taken per day are as
follows:

### Total steps per day

``` r
as.data.frame(tapply(activity$steps, activity$date, sum))
```

    ##            tapply(activity$steps, activity$date, sum)
    ## 10/1/2012                                          NA
    ## 10/10/2012                                       9900
    ## 10/11/2012                                      10304
    ## 10/12/2012                                      17382
    ## 10/13/2012                                      12426
    ## 10/14/2012                                      15098
    ## 10/15/2012                                      10139
    ## 10/16/2012                                      15084
    ## 10/17/2012                                      13452
    ## 10/18/2012                                      10056
    ## 10/19/2012                                      11829
    ## 10/2/2012                                         126
    ## 10/20/2012                                      10395
    ## 10/21/2012                                       8821
    ## 10/22/2012                                      13460
    ## 10/23/2012                                       8918
    ## 10/24/2012                                       8355
    ## 10/25/2012                                       2492
    ## 10/26/2012                                       6778
    ## 10/27/2012                                      10119
    ## 10/28/2012                                      11458
    ## 10/29/2012                                       5018
    ## 10/3/2012                                       11352
    ## 10/30/2012                                       9819
    ## 10/31/2012                                      15414
    ## 10/4/2012                                       12116
    ## 10/5/2012                                       13294
    ## 10/6/2012                                       15420
    ## 10/7/2012                                       11015
    ## 10/8/2012                                          NA
    ## 10/9/2012                                       12811
    ## 11/1/2012                                          NA
    ## 11/10/2012                                         NA
    ## 11/11/2012                                      12608
    ## 11/12/2012                                      10765
    ## 11/13/2012                                       7336
    ## 11/14/2012                                         NA
    ## 11/15/2012                                         41
    ## 11/16/2012                                       5441
    ## 11/17/2012                                      14339
    ## 11/18/2012                                      15110
    ## 11/19/2012                                       8841
    ## 11/2/2012                                       10600
    ## 11/20/2012                                       4472
    ## 11/21/2012                                      12787
    ## 11/22/2012                                      20427
    ## 11/23/2012                                      21194
    ## 11/24/2012                                      14478
    ## 11/25/2012                                      11834
    ## 11/26/2012                                      11162
    ## 11/27/2012                                      13646
    ## 11/28/2012                                      10183
    ## 11/29/2012                                       7047
    ## 11/3/2012                                       10571
    ## 11/30/2012                                         NA
    ## 11/4/2012                                          NA
    ## 11/5/2012                                       10439
    ## 11/6/2012                                        8334
    ## 11/7/2012                                       12883
    ## 11/8/2012                                        3219
    ## 11/9/2012                                          NA

### Mean steps per day

``` r
as.data.frame(tapply(activity$steps, activity$date, mean))
```

    ##            tapply(activity$steps, activity$date, mean)
    ## 10/1/2012                                           NA
    ## 10/10/2012                                  34.3750000
    ## 10/11/2012                                  35.7777778
    ## 10/12/2012                                  60.3541667
    ## 10/13/2012                                  43.1458333
    ## 10/14/2012                                  52.4236111
    ## 10/15/2012                                  35.2048611
    ## 10/16/2012                                  52.3750000
    ## 10/17/2012                                  46.7083333
    ## 10/18/2012                                  34.9166667
    ## 10/19/2012                                  41.0729167
    ## 10/2/2012                                    0.4375000
    ## 10/20/2012                                  36.0937500
    ## 10/21/2012                                  30.6284722
    ## 10/22/2012                                  46.7361111
    ## 10/23/2012                                  30.9652778
    ## 10/24/2012                                  29.0104167
    ## 10/25/2012                                   8.6527778
    ## 10/26/2012                                  23.5347222
    ## 10/27/2012                                  35.1354167
    ## 10/28/2012                                  39.7847222
    ## 10/29/2012                                  17.4236111
    ## 10/3/2012                                   39.4166667
    ## 10/30/2012                                  34.0937500
    ## 10/31/2012                                  53.5208333
    ## 10/4/2012                                   42.0694444
    ## 10/5/2012                                   46.1597222
    ## 10/6/2012                                   53.5416667
    ## 10/7/2012                                   38.2465278
    ## 10/8/2012                                           NA
    ## 10/9/2012                                   44.4826389
    ## 11/1/2012                                           NA
    ## 11/10/2012                                          NA
    ## 11/11/2012                                  43.7777778
    ## 11/12/2012                                  37.3784722
    ## 11/13/2012                                  25.4722222
    ## 11/14/2012                                          NA
    ## 11/15/2012                                   0.1423611
    ## 11/16/2012                                  18.8923611
    ## 11/17/2012                                  49.7881944
    ## 11/18/2012                                  52.4652778
    ## 11/19/2012                                  30.6979167
    ## 11/2/2012                                   36.8055556
    ## 11/20/2012                                  15.5277778
    ## 11/21/2012                                  44.3993056
    ## 11/22/2012                                  70.9270833
    ## 11/23/2012                                  73.5902778
    ## 11/24/2012                                  50.2708333
    ## 11/25/2012                                  41.0902778
    ## 11/26/2012                                  38.7569444
    ## 11/27/2012                                  47.3819444
    ## 11/28/2012                                  35.3576389
    ## 11/29/2012                                  24.4687500
    ## 11/3/2012                                   36.7048611
    ## 11/30/2012                                          NA
    ## 11/4/2012                                           NA
    ## 11/5/2012                                   36.2465278
    ## 11/6/2012                                   28.9375000
    ## 11/7/2012                                   44.7326389
    ## 11/8/2012                                   11.1770833
    ## 11/9/2012                                           NA

### Median steps per day

``` r
as.data.frame(tapply(activity$steps, activity$date, median))
```

    ##            tapply(activity$steps, activity$date, median)
    ## 10/1/2012                                             NA
    ## 10/10/2012                                             0
    ## 10/11/2012                                             0
    ## 10/12/2012                                             0
    ## 10/13/2012                                             0
    ## 10/14/2012                                             0
    ## 10/15/2012                                             0
    ## 10/16/2012                                             0
    ## 10/17/2012                                             0
    ## 10/18/2012                                             0
    ## 10/19/2012                                             0
    ## 10/2/2012                                              0
    ## 10/20/2012                                             0
    ## 10/21/2012                                             0
    ## 10/22/2012                                             0
    ## 10/23/2012                                             0
    ## 10/24/2012                                             0
    ## 10/25/2012                                             0
    ## 10/26/2012                                             0
    ## 10/27/2012                                             0
    ## 10/28/2012                                             0
    ## 10/29/2012                                             0
    ## 10/3/2012                                              0
    ## 10/30/2012                                             0
    ## 10/31/2012                                             0
    ## 10/4/2012                                              0
    ## 10/5/2012                                              0
    ## 10/6/2012                                              0
    ## 10/7/2012                                              0
    ## 10/8/2012                                             NA
    ## 10/9/2012                                              0
    ## 11/1/2012                                             NA
    ## 11/10/2012                                            NA
    ## 11/11/2012                                             0
    ## 11/12/2012                                             0
    ## 11/13/2012                                             0
    ## 11/14/2012                                            NA
    ## 11/15/2012                                             0
    ## 11/16/2012                                             0
    ## 11/17/2012                                             0
    ## 11/18/2012                                             0
    ## 11/19/2012                                             0
    ## 11/2/2012                                              0
    ## 11/20/2012                                             0
    ## 11/21/2012                                             0
    ## 11/22/2012                                             0
    ## 11/23/2012                                             0
    ## 11/24/2012                                             0
    ## 11/25/2012                                             0
    ## 11/26/2012                                             0
    ## 11/27/2012                                             0
    ## 11/28/2012                                             0
    ## 11/29/2012                                             0
    ## 11/3/2012                                              0
    ## 11/30/2012                                            NA
    ## 11/4/2012                                             NA
    ## 11/5/2012                                              0
    ## 11/6/2012                                              0
    ## 11/7/2012                                              0
    ## 11/8/2012                                              0
    ## 11/9/2012                                             NA

### Histogram of total steps taken per day
![plot1](instructions_fig/hist_steps_day.png) 


``` r
total <- tapply(activity$steps, activity$date, sum)
total <- as.numeric(total) # change to numeric vector
hist(total, xlab = "Total steps per day", main = "Frequency distribution of total steps per day", breaks = 30)
```


## What is the average daily activity pattern?

The following code shows how the data is set up to achieve the plot
below, showing a time series plot of average steps taken in a day at
5-minute intervals.

``` r
library(ggplot2)

interval_steps <- as.data.frame(tapply(activity$steps, activity$interval, mean, na.rm = TRUE))
interval <- row.names(interval_steps)
is <- cbind(interval, interval_steps)
colnames(is) <- c("interval", "steps")
is$interval <- as.character(is$interval); is$interval <- as.numeric(is$interval) # convert character then numeric to avoid factor variable being converted into 1, 2, 3.... 
str(is) # check that format is correct in 'is', the dataframe for plotting
```

    ## 'data.frame':    288 obs. of  2 variables:
    ##  $ interval: num  0 5 10 15 20 25 30 35 40 45 ...
    ##  $ steps   : num  1.717 0.3396 0.1321 0.1509 0.0755 ...

Below is a time series plot of steps taken at 5-minute intervals
throughout a day, averaged across all days in the dataset. Each day has
288 intervals.

``` r
ggplot(data = is, aes(x = interval, y = steps)) + geom_line(col = "blue") + labs(title = "Steps Taken in a Day Per 5-minute Intervals", x = "Interval in Minutes", y = "Steps")
```

![plot2](instructions_fig/mean_steps_plot.png) 

To answer the question: **Which 5-minute interval, on average across all
the days in the dataset, contains the maximum number of steps?**, we can
use the following code to find that the answer is **interval 835** with
roughly **206** steps. This also corresponds to the above plot.

``` r
library(dplyr)
```

    ## 
    ## Attaching package: 'dplyr'

    ## The following objects are masked from 'package:stats':
    ## 
    ##     filter, lag

    ## The following objects are masked from 'package:base':
    ## 
    ##     intersect, setdiff, setequal, union

``` r
head(arrange(is, desc(steps)), 1)
```

    ##   interval    steps
    ## 1      835 206.1698

## Imputing missing values?

The total number of rows with missing values are 2304:

``` r
sum(is.na(activity))
```

    ## [1] 2304

I will fill in the missing numbers using **fill** from the **tidyr**
package. NA values are filled in with the nearest existing value
*below*. This data is saved in **new\_act**.

``` r
library(tidyr)
new_act <- activity %>% fill(steps, .direction = "updown")
```

We can check to see that all missing cases are filled in. The first line
of code tells us there are **17568** rows in this dataset and the second
line tells us that indeed, these rows are all complete.

``` r
dim(new_act)
```

    ## [1] 17568     3

``` r
length(complete.cases(new_act))
```

    ## [1] 17568

Below, I address the following section of the assignment: **Make a
histogram of the total number of steps taken each day and calculate and
report the mean and median total number of steps taken per day. Do these
values differ from the estimates from the first part of the assignment?
What is the impact of imputing missing data on the estimates of the
total daily number of steps**

``` r
total2 <- tapply(new_act$steps, new_act$date, sum)
total2 <- as.numeric(total2) 
par(mfrow = c(1, 2))
hist(total, xlab = "Total steps per day", main = "Before imputing", breaks = 30, col = "magenta")
hist(total2, xlab = "Total steps per day", main = "After imputing", breaks = 30, col = "green")
```

![plot3](instructions_fig/before_after_imputing.png) 

The above histogram shows that there isn’t very much change between the
historgams before versus after imputing the values other than that the
frequency of 0s increased a lot, due to the method of imputation used.

Looking at the mean and median number of steps taken before and after
imputation, we can see that the mean dramatically decreases after
imputation due to the increased number of 0s. The median has decreased
as well, though less dramatically.

``` r
summary(total2) # after imputing
```

    ##    Min. 1st Qu.  Median    Mean 3rd Qu.    Max. 
    ##       0    6778   10395    9354   12811   21194

``` r
summary(total) # before imputing
```

    ##    Min. 1st Qu.  Median    Mean 3rd Qu.    Max.    NA's 
    ##      41    8841   10765   10766   13294   21194       8

## Are there differences in activity patterns between weekdays and weekends?

Below is the code for sorting the data to create the plot comparing
weekend and weekday activity. As can be seen, people tend to be less
active during weekends, and tend to stay inactive until later on in the
day.

![plot4](instructions_fig/weekplot.png) 


``` r
library(lubridate)
```

    ## 
    ## Attaching package: 'lubridate'

    ## The following object is masked from 'package:base':
    ## 
    ##     date

``` r
new_act$date <- mdy(new_act$date)
weekdays <- weekdays(new_act$date)
new_act <- cbind(new_act, weekdays)
new_act$weekdays <- as.character(new_act$weekdays) # convert to character to use gsub

# categorize as 'weekday' or 'weekend'
new_act$weekdays <- gsub("Monday", "weekday", new_act$weekdays)
new_act$weekdays <- gsub("Tuesday", "weekday", new_act$weekdays)
new_act$weekdays <- gsub("Wednesday", "weekday", new_act$weekdays)
new_act$weekdays <- gsub("Thursday", "weekday", new_act$weekdays)
new_act$weekdays <- gsub("Friday", "weekday", new_act$weekdays)
new_act$weekdays <- gsub("Saturday", "weekend", new_act$weekdays)
new_act$weekdays <- gsub("Sunday", "weekend", new_act$weekdays)

# split
wdays <- filter(new_act, weekdays == "weekday")
wends <- filter(new_act, weekdays == "weekend")

# apply
weekday <- tapply(wdays$steps, wdays$interval, mean)
weekend <- tapply(wends$steps, wends$interval, mean)

# combine
interval <- unique(new_act$interval)

week_data <- cbind(interval, weekday, weekend); week_data <- as.data.frame(week_data)

# reshape the data
wk <- gather(week_data, week, steps, weekday:weekend)

# make plot
library(lattice)
xyplot(steps ~ interval | week, data = wk, layout = c(1,2), type = "l")
```

