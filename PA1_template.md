# Reproducible Research - PA1_template




## Q1 Loading and preprocessing the data


```
## [1] "English_United States.1252"
```

```
##      steps                date          interval     
##  Min.   :  0.00   2012-10-01:  288   Min.   :   0.0  
##  1st Qu.:  0.00   2012-10-02:  288   1st Qu.: 588.8  
##  Median :  0.00   2012-10-03:  288   Median :1177.5  
##  Mean   : 37.38   2012-10-04:  288   Mean   :1177.5  
##  3rd Qu.: 12.00   2012-10-05:  288   3rd Qu.:1766.2  
##  Max.   :806.00   2012-10-06:  288   Max.   :2355.0  
##  NA's   :2304     (Other)   :15840
```
## Q2 What is the average daily activity pattern



```
## 'data.frame':	17568 obs. of  3 variables:
##  $ steps   : int  NA NA NA NA NA NA NA NA NA NA ...
##  $ date    : Date, format: "2012-10-01" "2012-10-01" ...
##  $ interval: int  0 5 10 15 20 25 30 35 40 45 ...
```



```
## # A tibble: 61 × 3
##          date totalSteps    na
##        <date>      <int> <int>
## 1  2012-10-01         NA   288
## 2  2012-10-02        126     0
## 3  2012-10-03      11352     0
## 4  2012-10-04      12116     0
## 5  2012-10-05      13294     0
## 6  2012-10-06      15420     0
## 7  2012-10-07      11015     0
## 8  2012-10-08         NA   288
## 9  2012-10-09      12811     0
## 10 2012-10-10       9900     0
## # ... with 51 more rows
```

![](PA1_template_files/figure-html/unnamed-chunk-5-1.png)<!-- -->



```
## [1] 10766.19
```

```
## [1] 10765
```
## Q3 What is the average daily activity pattern



```
## # A tibble: 6 × 2
##   interval average_steps
##      <int>         <dbl>
## 1        0     1.7169811
## 2        5     0.3396226
## 3       10     0.1320755
## 4       15     0.1509434
## 5       20     0.0754717
## 6       25     2.0943396
```

![](PA1_template_files/figure-html/unnamed-chunk-9-1.png)<!-- -->


```
## # A tibble: 1 × 2
##   interval average_steps
##      <int>         <dbl>
## 1      835      206.1698
```
## Q4 Imputing missing values

1. Calculate and report the total number of missing values in the dataset (i.e. the total number of rows with NAs)##


```
## [1] 2304
```
2. Devise a strategy for filling in all of the missing values in the dataset.

Strategy: filling in missing data with the mean number of steps across all days with available data for that particular interval.

3. Create a new dataset that is equal to the original dataset but with the missing data filled in.



4. Make a histogram of the total number of steps taken each day and Calculate and report the mean and median total number of steps taken per day.

![](PA1_template_files/figure-html/unnamed-chunk-13-1.png)<!-- -->

```
## [1] 10766.19
```

```
## [1] 10766.19
```


## Q5 Are there differences in activity patterns between weekdays and weekends?


1. Create a new factor variable in the dataset with two levels – “weekday” and “weekend” indicating whether a given date is a weekday or weekend day.



2.Make a panel plot containing a time series plot (i.e. type = "l") of the 5-minute interval (x-axis) and the average number of steps taken, averaged across all weekday days or weekend days (y-axis)


Plots of weekdays and weekend activity
![](PA1_template_files/figure-html/unnamed-chunk-17-1.png)<!-- -->





