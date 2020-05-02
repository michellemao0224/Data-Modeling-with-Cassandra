#Introduction

A startup called Sparkify wants to analyze the data they've been collecting on songs and user activity on their new music streaming app. The analytics team is particularly interested in understanding what songs users are listening to. Currently, they don't have an easy way to query their data, which resides in a directory of JSON logs on user activity on the app, as well as a directory with JSON metadata on the songs in their app.

They'd like a data engineer to create an Apache Cassandra database which can create queries on song play data to answer the questions, and wish to bring me on the project. My role is to create a database for this analysis. I'll be able to test my database by running queries given to my by the analytics team from Sparkify to create the results.

#Project Overview

In this project, I'll apply what I've learned on data modeling with Apache Cassandra and complete an ETL pipeline using Python. To complete the project, I will need to model my data by creating tables in Apache Cassandra to run queries. I am provided with part of the ETL pipeline that transfers data from a set of CSV files within a directory to create a streamlined CSV file to model and insert data into Apache Cassandra tables. 

#Dataset

###Event Dataset

For this project, I'll be working with one dataset: event_data. The directory of CSV files partitioned by date. Here are examples of filepaths to two files in the dataset:

```
event_data/2018-11-08-events.csv
event_data/2018-11-09-events.csv
```
#Project Template

To get started with the project, go to the workspace.
The project template includes one Jupyter Notebook file, in which:

```
    I will process the event_datafile_new.csv dataset to create a denormalized dataset
    I will model the data tables keeping in mind the queries you need to run
    I have been provided queries that you will need to model your data tables for
    I will load the data into tables you create in Apache Cassandra and run your queries
```

#Project Steps

Below are steps I follow to complete each component of this project.

###Modeling my NoSQL database or Apache Cassandra database

*    Design tables to answer the queries outlined in the project template
*    Write Apache Cassandra `CREATE KEYSPACE` and `SET KEYSPACE` statements
*    Develop my `CREATE` statement for each of the tables to address each question
*    Load the data with `INSERT` statement for each of the tables
*    Include `IF NOT EXISTS` clauses in ymy `CREATE` statements to create tables only if the tables do not already exist. I also include `DROP TABLE` statement for each table, this way I can run drop and create tables whenever I want to reset my database and test my ETL pipeline
*   Test by running the proper select statements with the correct `WHERE` clause

###Build ETL Pipeline

*    Implement the logic in section Part I of the notebook template to iterate through each event file in event_data to process and create a new CSV file in Python
*    Make necessary edits to Part II of the notebook template to include Apache Cassandra `CREATE` and `INSERT` statements to load processed records into relevant tables in my data model
*    Test by running `SELECT` statements after running the queries on my database

