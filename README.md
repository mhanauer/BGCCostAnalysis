---
title: "BGC Cost Analysis"
output: html_document
---

```{r setup, include=FALSE}
knitr::opts_chunk$set(echo = TRUE)
```
Getting numbers of summer reading program

Teacher salary = http://www1.salary.com/IN/Bloomington/Teacher-Elementary-School-salary.html

3 hours per day five days a week (account for missing days)
1.5 with Readable English and 1.5 with HELPS. 

Anna = 15 hours per week.
Rebecca = 20 hours total
Karin = 20 hours total
Matt = 15 hours total

21 total days over five weeks for the actual intervention
We started training and planning two weeks prior so 7 weeks total for Anna

Cost of HELPS materials: http://www.helpsprogram.org/materials.php

Cost of Readable English materials: https://www.readablenglish.com/au/teachers
```{r}
# Number of hours we served kids
hoursKidsServed = 21*3; hoursKidsServed

# Hourly pay
teacherSalHourly = 51611/(52*40)
AnnaHourly = 70000/(52*40)
MattHourly = 30000/ (52*40)
RebeccaHourly = 93000 / (52*40)
KarinHourly = 139150 / (52*40)
# $15 per hour.  I assumed that Anna and provided about 30 minutes of programming each day.  The 1.5 is half of 3 total hours, because HELPS was provided to half of the students.  So 1.5 minus .5 is 1 hour per day that extra HELPS people were used at $15 per day
helps = 15*21*1
teachers = teacherSalHourly*21*1.5
# We started two weeks prior to the five weeks.
Anna = AnnaHourly*15*7
Matt = MattHourly*15
Rebecca = RebeccaHourly*20
Karin = KarinHourly*20
# We had 8 students in HELPS
helpsMaterials = 8*55 
readableEnglishMaterials = 8*89

total = sum(helps, teachers, Anna, Matt, Rebecca, Karin, helpsMaterials, readableEnglishMaterials); round(total, 0)


```
Results:

16 students completed the program, with approximentaly 63 hours served.
Provided approximentaly $8,200 in free services to the club. (Not counting the scans, because I am not sure that helps the club, but could add those in).



