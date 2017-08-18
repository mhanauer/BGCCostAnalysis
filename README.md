---
title: "BGC Cost Analysis"
output:
  word_document: default
  pdf_document: default
  html_document: default
---

```{r setup, include=FALSE}
knitr::opts_chunk$set(echo = TRUE)
```
I found that we served students on 21 days.  I also found that 16 students completed the program (i.e. we have completed pre and post testing on 16 students).  Salaries can be located below.  I acquired the hourly salary rate by dividing the salary rate by the number of weeks in year (52) times the number of hours standard hours in a work week (40).  I then located Rebecca and Karin's salaries online,  calculated Matt and Anna's hourly salary and used $15 per hour for HELPS people. 

Given that Rebecca stated that the intervention was provided 3 hours per day, I split the hours between Readable English and HELPS each receiving 1.5 hours per day.

I calculated the HELPS cost by taking the number of  days served times the cost of HELPS interventionists times 1, because I assumed the HELPS interventionists worked 1 hour per day, while Anna and Matt worked .5 hours per day.  

For the rest of the costs for everyone besides Anna, I took the assumed hours worked, which are located above and multiplied those hours by the hourly rate for the person.  For Anna, I assumed she worked 7 weeks (she worked two weeks prior to the start of the intervention to put it together).  I then found the costs for each intervention and included those costs for eight students (8 students in Readable English and 8 students in HELPS). 



Teacher salary = http://www1.salary.com/IN/Bloomington/Teacher-Elementary-School-salary.html

3 hours per day five days a week (account for missing days)
1.5 with Readable English and 1.5 with HELPS. 

Anna = 15 hours per week.
Rebecca = 20 hours total
Karin = 20 hours total
Matt = 15 hours total

21 total days over five weeks for the actual intervention

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

# Actual cost 
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

16 students completed the program, with approximately 63 hours of programming provided, which would have cost the Boys and Girls Club approximately $8,200.  (Not counting the scans, because I am not sure the scans benefit the club, but could add those in).



