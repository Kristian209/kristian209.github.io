---
layout: post
title:  "Data-lit: Collections(1.2) SQL Techniques"
date:   2019-02-11 18:49:44 -0800
categories: data lit
---
Today I completed 1.2 of the Data lit course. I learned essential SQL techniques.

Creating a table:
```
create table exercise_logs (
  id integer primary key autoincrement,
  type text,
  minutes integer,
  calories integer,
  heart_rate integer
);
```
Inserting data:
~~~
insert into exercise_logs(type, minutes, calories, heart_rate) values ('biking', 30, 100, 110);
~~~
Accessing data:
~~~
/* To select all records from a database */
select * from exercise_logs;
/* To find all the activities a user engaged in and the total amount of calories
 they burned doing that activity */
 select type, sum(calories) as total_calories
 from exercise_logs
 group by type;
~~~
Grouping data:
~~~
select count(*),
 case
 when heart_rate > 220 - 30 then 'above max'
 when heart_rate > round(.9 * (220 - 30)) then 'above target'
 when heart_rate > round(.5 * (220 - 30)) then 'within target'
 else 'below target'
 end as 'heart_rate_zone'
 from exercise_logs
 group by heart_rate_zone;
~~~
To dynamically grab data with a query and use that result in another query we
have subqueries.
```
create table drs_favorites (
  id integer primary key, /* unique identifier */
  type text,             /* type of activity */
  reason text           /* reason why doctor recommends it */
);
insert into drs_favorites
(type, reason)
values ('running', 'improves cardiovascular health.');
```
Using like to find all the activities in the exercise_logs table that doctors
recommended for improving cardiovascular health:
~~~
SELECT * FROM exercise_logs WHERE type IN (SELECT type FROM drs_favorites WHERE reason LIKE "%cardiovascular%");
~~~
GitHub: https://github.com/Kristian209/Data-lit/blob/master/sql101.sql
