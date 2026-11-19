# Laptop_Dataset
Data analysis project on laptop dataset. Used MySQL and Power BI / Analysis , visualized the results 


#  Laptop Data Analysis

Analysis of a laptop dataset using *MySQL* and *Power BI* to compare companies across laptop types by total price.

## 🛠️ Tools Used
- MySQL ( analysis and Query)
- Power BI (visualization,data cleaning)

## 🔍 What I Did
- Clean the data and prepared the laptop dataset ( 1303 uncleaned_data 1271cleaned data)
- which company has highest Revenue (eg:- Dell	with $17880598 and Lenovo with	$16841018)
- but number of sales has diffrent (Lenovo	16841018 with 290 counts  and Dell	 $17880598 with 284 )
- here is the diffrence
-Use BI for visualtions 


## 📊 Key Insights
Workstation	  Lenovo	507439	1
Workstation	    Dell	1172312	2
-Most Sales Typename

# SQL QUERY
create database Laptop ;
use laptop ;
select * from laptop_data_01 ;

select Company,count(Company)
from  laptop_data_01
group by Company
order by count(Company) desc ;

select  Company,round(sum(Price)),
row_number() over(order by sum(Price) desc) as Top_Revenue
from laptop_data_01
group by Company
order by sum(Price) desc ;
