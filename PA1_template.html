---
title: "Reproducible Research: Peer Assessment 1"
output: 
  html_document:
    keep_md: true
---


## Loading and preprocessing the data



## What is mean total number of steps taken per day?



## What is the average daily activity pattern?



## Imputing missing values



## Are there differences in activity patterns between weekdays and weekends?

'''{r}
library("data.table")
library(ggplot2)
unzip("activity.zip",exidr="data")
'''

'''{r}
DTactivity<-data.table::fread(input="data/activity.csv")
'''

'''{r}
totsteps<-DTactivity[, c(lapply(.SD,sum,na.rm=FALSE)), .SDcols=c("steps"),by=.(date)]
head(totsteps, 10)
'''

'''{r}
ggplot(totsteps, aes(x=steps))+ geom_histogram(fill="blue", binwidth=1000)+labs(title="Daily Steps", x="Steps", y= "Frequency")
'''

'''{r}
totsteps[, .(meansteps= mean(steps, na.rm=TRUE), mediansteps=median(steps, na.rm=TRUE))]
'''
'''{r}
DTInterval<- DTactivity[, c(lapply(.SD, mean, na.rm=TRUE)), .SDcols=c("steps"), by=.(interval)]
ggplot(DTInterval, aes(x=interval, y= steps))+geom_line(color="blue", size=1)+labs(title="Average Daily Steps", x="Interval", y= "Average Setps per day")
'''

'''{r}
DTInterval[steps==max(steps), .(max_interval=interval)]
'''

'''{r}
nrow(DTactivity[is.na(steps),])
'''

'''{r}
DTactivity[is.na(steps), "steps"]<- DTactivity[, c(lapply(.SD, median, na.rm'TRUE)), .SDcols=c("steps")]
'''

'''{r}
data.table::fwrite(x=DTactivity, file="data/tidyData.csv", quote=FALSE)
'''

'''{r}
totsteps<-DTactivity[, c(lapply(.SD, sum)), .SDcols=c("steps"), by=.(date)]
totsteps[, .(meansteps=mean(steps), mediansteps=media(steps))]
ggplot(totsteps, aes(x=steps))+geom_histogram(fill="blue", binwidth=1000)+labs(title="Daily Steps", x="Steps", y="Frequency")
'''


'''{r}
DTactivity<- data.table::fread(input="data/activity.csv")
DTactivity[, date:=as.POSIXct(date, format="%Y-%m-%d")]
DTactivity[, 'Day of the Week':=weekdays(x=date)]
DTactivity[grep1(pattern="Monday|Tuesday|Wednesday|Thursday|Friday", x='Day of the Week'), "weekday or weekend"]<-"weekday"
DTactivity[grep1(pattern="Saturday|Sunday", x='Day of the Week'), "weekday or weekend"]<- "weekend"
DTactivity[, 'weekday or weekend' :=as.factor('weekday or weekend')]
head(DTactivity, 10)
'''

'''{r}
DTactivity[is.na(steps), "steps"]<- DTactivity[, c(lapply(.SD, median, na.rm=TRUE)), .SDcols=c("steps")]
DTInterval<- DTactivity[, c(lapply(.SD, mean, na.rm=TRUE)), .SDcols=c("steps"), by= .(interval, 'weekday or weekend')]

ggplot(DTInterval, aes(x=interval, yy= steps, color='weekday or weekend'))+geom_line()+labs(title="Average Daily Steps by Week type", x="Interval", y="Number of Steps")+facet_wrap(~'weekday or weekend', ncol=1, nrow=2)
