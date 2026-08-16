
create database [Tableau Project 1]

use [Tableau Project 1]

select Gender,count(*) [Count] from [dbo].[Depression+Student+Dataset]
group by Gender

update [dbo].[Depression+Student+Dataset] 
set Gender= 'F' where Gender = 'Female'

update [dbo].[Depression+Student+Dataset]
set gender= 'M' where Gender= 'Male'

select * from [Depression+Student+Dataset]

--to check null values

select * from [Depression+Student+Dataset]
where Age is null

--checking age variables for to make age group 

select Age,count(*) [Count of age]from [Depression+Student+Dataset]
group by Age
order by Age asc

--adding age group coloum 
alter table [dbo].[Depression+Student+Dataset]
add Age_Group varchar(max)

select * from [Depression+Student+Dataset]

update [dbo].[Depression+Student+Dataset]
set Age_Group=
case when Age between 18 and 24 then 'A1'
Else case when Age between 25 and 30 then 'A2'
else 'A3' end end

select * from [Depression+Student+Dataset]

select age_group,count(*)  from [dbo].[Depression+Student+Dataset]
group by Age_Group

--now we are making a new column for identity of every row 

alter table [dbo].[Depression+Student+Dataset]
add index_column int identity(1,1)

--altering depression column values from digits to yes or no but the data type of this column needs to change 

alter table [dbo].[Depression+Student+Dataset]
alter column depression varchar(Max)

update [dbo].[Depression+Student+Dataset]
set Depression= 'No' where Depression=0


update [dbo].[Depression+Student+Dataset]
set Depression= 'Yes' where Depression='1'

select Depression,count(*) from [dbo].[Depression+Student+Dataset]
group by Depression
