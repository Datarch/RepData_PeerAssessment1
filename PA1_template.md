---
title: "Reproducible Research: Peer Assessment 1"
output: 
  html_document:
    keep_md: true
---

# Reproducible Research: Peer Assessment 1  

*Monday, 8 June 2015*

-------------------------------------------------------------------------------

## Introduction

This report is created during the 1st Peer Assessment within Reproducible Research Coursera Course by John Hopkins Bloomberg School of Public Health.

This assignment makes use of data from a personal activity monitoring device.
This device collects data at 5 minute intervals through out the day. The data
consists of two months of data from an anonymous individual collected during
the months of October and November, 2012 and include the number of steps
taken in 5 minute intervals each day.

-------------------------------------------------------------------------------

## Data
The data for this assignment can be downloaded from the course web site in a zipped file:

- **Dataset**: [Activity monitoring data (52K)](https://d396qusza40orc.cloudfront.net/repdata%2Fdata%2Factivity.zip)

The variables included in this dataset are:

- **steps**: Number of steps taking in a 5-minute interval (missing values are
coded as NA)

- **date**: The date on which the measurement was taken in YYYY-MM-DD
format

- **interval**: Identifier for the 5-minute interval in which measurement was
taken

The dataset is stored in a comma-separated-value (CSV) file and there are a
total of 17,568 observations in this dataset.

To data is also available in .zip format within the [GitHub repository created for this assignment](http://github.com/rdpeng/RepData_PeerAssessment1), which was forked and cloned into the working directory.

The data is in a .zip file format and has to be extracted into the working directory to complete this assessment.

-------------------------------------------------------------------------------

## Loading and preprocessing the data

The Activity monitoring data is read using the read.csv() function into R:


```r
activityData <- read.csv("activity.csv")
```
The data set has the following catacteristics:

```r
dim(activityData)
```

```
## [1] 17568     3
```

```r
head(activityData)
```

```
##   steps       date interval
## 1    NA 2012-10-01        0
## 2    NA 2012-10-01        5
## 3    NA 2012-10-01       10
## 4    NA 2012-10-01       15
## 5    NA 2012-10-01       20
## 6    NA 2012-10-01       25
```

```r
tail(activityData)
```

```
##       steps       date interval
## 17563    NA 2012-11-30     2330
## 17564    NA 2012-11-30     2335
## 17565    NA 2012-11-30     2340
## 17566    NA 2012-11-30     2345
## 17567    NA 2012-11-30     2350
## 17568    NA 2012-11-30     2355
```

```r
str(activityData)
```

```
## 'data.frame':	17568 obs. of  3 variables:
##  $ steps   : int  NA NA NA NA NA NA NA NA NA NA ...
##  $ date    : Factor w/ 61 levels "2012-10-01","2012-10-02",..: 1 1 1 1 1 1 1 1 1 1 ...
##  $ interval: int  0 5 10 15 20 25 30 35 40 45 ...
```

```r
summary(activityData)
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

Here comes any preprocessing action in case of need:

-------------------------------------------------------------------------------

## What is mean total number of steps taken per day?

-------------------------------------------------------------------------------

## What is the average daily activity pattern?

-------------------------------------------------------------------------------

## Imputing missing values

-------------------------------------------------------------------------------

## Are there differences in activity patterns between weekdays and weekends?

-------------------------------------------------------------------------------
