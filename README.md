# Airbnb Big Data Management with MongoDB and Hadoop Tools

## Introduction
Airbnb became one-of-a-kind accommodation service that is used and recognized by the whole world. It allows the renting of houses or rooms owned by hosts to guests with the help of a technology tool. Over the recent years, Airbnb has been undergoing rapid development as an online platform community to provide access in accommodation and hospitalities globally. Due to the nature of its business, Airbnb has positioned itself as a data driven company; hence, invested heavily on its data infrastructure. 

## Problem Statement
The huge number of listings generate a lot of data (structured and unstructured) separately by location in compressed file by Airbnb which will be updated in frequent manner. The bulky number of files and frequent update of the data become problem for public users who are interested in understanding market of Airbnb based on the data. Even though it is not necessary to acquire data for all locations, the dataset for one selected location can be relatively huge. Hence, it becomes an issue for public users interested in understanding the Airbnb market based on the data due to the bulky number of files and frequent updates. The whole dataset must be collected, loaded, and organized to proffer data ready for query and analysis to gain valuable business insights. Commodity hardware machines are also unable to fulfill complex computational requirements. Thus, in resolving this issue, this project aim to develop an Airbnb database and create a pipeline using MongoDB and Hadoop architecture to ease the process of managing, loading, processing, querying, and analyzing Airbnb data based on location.

## Objectives 
1. To set up of database and build data pipeline for managing Airbnb data. 
2. To utilize data access tools such as MongoDB and tools in Hadoop architecture for managing Airbnb data.
3. To compare the effectiveness of MongoDB and different tools in Hadoop architecture for performing loading, query and running analysis on Airbnb data

## Data Sources
[Inside Airbnb](http://insideairbnb.com/get-the-data.html) is a website with a repository of data sourced from publicly available information such as listings, reviews, and calendar details from the original Airbnb site. The website provides datasets to Airbnb listings worldwide for about 108 locations. These data have been analyzed, cleansed, and aggregated where appropriate to facilitate the usage by the public in a compressed gz file. For this project, we demonstrated the data pipeline development using data from Singapore. However, a similar process can be conducted in acquiring data from other locations as the pipeline developed is flexible to be utilized for all locations. The data used in this project are *Listings, Reviews, and Calendars*. 

## Process Flows
As the Airbnb data is usually arranged by location, a shell script is created to automate the downloading process of the data files according to the user’s location preference with Airbnb listings from the Insider Airbnb website. Users are allowed to input the location, location URL, and compile date of the data. The data files (i.e., Listings, Reviews, and Calendar) are saved in a local file system under a specified directory with the folder named as per the location’s name. In this scenario, the files were saved in a ‘SINGAPORE’ folder. The downloaded files were unzipped before loading to HDFS storage as they were initially downloaded in a compressed gz format. Subsequently, MongoDB and different Hadoop Tools such as PySpark, Apache Pig, and Apache Hive were utilized to access, query, and analyze the data. ***Figure 1*** shows the process flow overview for the entire Airbnb data pipeline. The codes used for the entire process are available in this repository.

![](<!Image/Figure1.PNG>)


## Tools Used
- Ubuntu 
- Hadoop
- PySpark
- Apache Hive
- Apache Pig
- MongoDB Compass (Not saved in this repository)

## Scripts
- The data collection process is automated by running the ***BatchRun_Initial.sh*** file
- ***BatchRun_Tool.sh*** script (eg. BatchRun_Pig.sh) is the script that consolidate all codes for you to run in one go and record the time taken for each execution of code.
