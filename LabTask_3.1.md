# LAB 3.1 -> Importing RDBMS Data into HDFS

***Objective -> Import data from a database into HDFS.***

***Pre-requisites -> Hadoop cluster on EMR should be up and running***

Following are the steps to be performed in this lab:-

1. Create an Amazon RDS database.

2. Connect this database with MySQL Workbench.

3. Now create a new salaries table using following sql command

    ```
    *create table salaries (
    gender varchar(1),
    age int,
    salary double,
    zipcode int);*
    ```
4. Load the data given in salaries.txt file into this salaries table using following sql command

    *load data infile '<path-to-file>/salaries.txt' into table salaries fields terminated by ',' ;*    
    
*  Close current SQL connection
        *  Right click on your Connection and select 'Edit Connection'
        *  Click on Advanced
        *  Add following line to 'Others'

            OPT_LOCAL_INFILE=1
       *  Now Reconnect to your database
       
5. Now, ssh to your EMR cluster and make sure Sqoop is pre installed in this cluster. 

6. Run sqoop import command to import data from sql database to hdfs

 <img src = "https://user-images.githubusercontent.com/63716706/86486170-43d55100-bd78-11ea-96cb-62d1416d79bd.jpg">

7. Now check whether salaries directory is created on hdfs with 5 files present as shown below

<img src = "https://user-images.githubusercontent.com/63716706/86486181-4768d800-bd78-11ea-80ac-63ed9037e918.jpg">

8. To verify whether data is present in these file use cat command

<img src = "https://user-images.githubusercontent.com/63716706/86486193-4b94f580-bd78-11ea-8536-e8e38699cfd0.jpg">

9. Now we will import only salary and age data from the database and put it into new directory named salaries2

<img src = "https://user-images.githubusercontent.com/63716706/86486196-4d5eb900-bd78-11ea-86ea-0c9e12af6af8.jpg">

10. Now check whether salaries2 directory is created on hdfs with 2 files present as shown below

<img src = "https://user-images.githubusercontent.com/63716706/86486198-4f287c80-bd78-11ea-9b55-b189f9de7f7f.jpg">

11. To verify whether data is present in this file use cat command

<img src = "https://user-images.githubusercontent.com/63716706/86486202-50f24000-bd78-11ea-8629-dc8ac8cfcb4c.jpg">

12. Now we will use --split-by command to split our data accoring to a certain column value and put it into new directory named salaries3

<img src = "https://user-images.githubusercontent.com/63716706/86486211-5485c700-bd78-11ea-829d-9e9f141faa0d.jpg">

13. Now check whether salaries3 directory is created on hdfs with 3 files present as shown below

<img src = "https://user-images.githubusercontent.com/63716706/86486216-56e82100-bd78-11ea-86c1-e35cf97af117.jpg">

14. To verify whether data is present in this file use cat command

<img src = "https://user-images.githubusercontent.com/63716706/86486225-5b143e80-bd78-11ea-88c1-74d829c144f1.jpg">

























































