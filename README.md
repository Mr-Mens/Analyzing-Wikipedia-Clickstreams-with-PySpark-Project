# Analyzing Wikipedia Clickstream Data README

## Introduction

This project focuses on analyzing Wikipedia's clickstream data to uncover patterns in how users navigate from one article to another. Utilizing Apache Spark and PySpark for data manipulation and analysis, the project aims to provide insights into user behavior on Wikipedia, including the most popular pathways to specific articles and the overall structure of Wikipedia's internal link network.

## Project Setup

The project begins by setting up a Spark environment using PySpark, enabling the handling of large datasets typical of web clickstream data. A SparkSession is initiated to allow for distributed data processing and analysis.

## Data Importation and Initial Exploration

The data, representing various stages of user interaction—from visiting an article to clicking through to another article—is stored across CSV files. These files are read into Spark DataFrames, allowing for efficient manipulation and analysis of large-scale data.

## Data Manipulation Tasks

### Task 1: SparkSession Creation
A SparkSession object is created to facilitate the data analysis process, serving as the entry point for programming Spark with the DataFrame and SQL API.

### Task 2: RDD Creation
An RDD is created from a list of sample clickstream counts, providing a low-level abstraction for fault-tolerant, parallel processing of large datasets.

### Task 3: DataFrame Creation
The RDD is converted into a Spark DataFrame, enabling higher-level data manipulation and analysis operations.

### Task 4-6: Data Inspection and Cleaning
The project involves inspecting the initial data structure, dropping unnecessary columns, and renaming columns for clarity and consistency.

### Task 7: Schema Renaming
Columns are renamed to more accurately reflect their content, such as changing `referrer` to `source_page`.

## Querying Clickstream Data

The clickstream data is queried to extract specific insights:

- Filtering entries to focus on interactions leading to a particular article.
- Aggregating click counts by link category to understand the distribution of internal versus external links.
- Using both PySpark DataFrame operations and Spark SQL queries to achieve these objectives, demonstrating the flexibility of Spark in data analysis.

## Saving Analysis Results

The project concludes with the results of the analysis—specifically, the internal clickstream data—being saved to disk in both CSV and parquet formats. This allows for the data to be easily shared and further analyzed using different tools or methods.

## Conclusion and Cleanup

The project provides valuable insights into Wikipedia's clickstream data, highlighting the pathways through which users navigate the site. By saving the internal clickstream data for further analysis, the project lays the groundwork for more in-depth studies on user behavior and article popularity on Wikipedia. Finally, the SparkSession is closed to free up resources, marking the end of the analysis process.

## Challenges and Learnings

Analyzing clickstream data presents unique challenges due to its volume and complexity. This project showcases the power of Spark and PySpark in handling large datasets, offering a scalable solution for data analysis tasks. Through this project, we gain insights into not just user behavior on Wikipedia but also the practical application of big data technologies in uncovering patterns and trends within vast datasets.
