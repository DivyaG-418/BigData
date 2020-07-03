# LAB 3.2 -> Exporting HDFS Data to an RDBMS

***Objective -> Export data from HDFS into a MySQL table using Sqoop.***

***Pre-requisites -> Hadoop cluster on EMR should be up and running***

Following are the steps to be performed in this lab:-

1. Create a new hdfs directory using mkdir command with name salarydata

<img src = "https://user-images.githubusercontent.com/63716706/86486234-5fd8f280-bd78-11ea-8d89-5a7d50ba29b5.jpg">

2. Put salarydata.txt into the salarydata directory in HDFS

<img src = "https://user-images.githubusercontent.com/63716706/86486238-636c7980-bd78-11ea-9be6-bd3f17fec529.jpg">

3. Check whether the file is created on hdfs

4. Create a new Table in the Database as salaries2 using following sql command

<img src = "https://user-images.githubusercontent.com/63716706/86486245-66676a00-bd78-11ea-9a53-ff6d7b7bfdcd.jpg">


*create table salaries2 (
gender varchar(1),
age int,
salary double,
zipcode int);*

5. Now export data from hdfs to database

6. Verify whether all records are been exported successfully

<img src = "https://user-images.githubusercontent.com/63716706/86486252-6a938780-bd78-11ea-8a1b-975cc2f18220.jpg">


























