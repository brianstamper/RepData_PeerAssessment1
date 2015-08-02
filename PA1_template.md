# Reproducible Research: Peer Assessment 1

## Preliminary steps
Before working with the data, I'm going to set some display optins for this document and load some libraries.

```r
library(knitr) # Adding this here makes RStudio's Knit HTML button work

# Need to check if this is necessary. From the forums
# https://class.coursera.org/repdata-036/forum/thread?thread_id=83
opts_chunk$set(echo = TRUE,
               message = FALSE, warning = FALSE,
               cache = FALSE#,
               #cache.path = "cache/", 
               #fig.path = "figure/"
               )

library(dplyr)
```

```
## 
## Attaching package: 'dplyr'
## 
## The following objects are masked from 'package:stats':
## 
##     filter, lag
## 
## The following objects are masked from 'package:base':
## 
##     intersect, setdiff, setequal, union
```

```r
library(lubridate)
```

## Loading and preprocessing the data

```r
if (!file.exists("activity.csv")) {
  if (!file.exists("activity.zip")) {
    url <- "https://d396qusza40orc.cloudfront.net/repdata%2Fdata%2Factivity.zip"
    destfile <- "activity.zip"
    download.file(url, destfile, method = "curl")
    downloadDate <- date()
  }
unzip(zipfile = "activity.zip")
}

# Missing values are correctly handled by default 'NA',
# but dates need will be forced to strings and then converted
activity <- read.csv("activity.csv", stringsAsFactors = FALSE)
```


## What is mean total number of steps taken per day?



## What is the average daily activity pattern?



## Imputing missing values



## Are there differences in activity patterns between weekdays and weekends?
