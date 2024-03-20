# DQLab-Tetris-Capstone-ETL-Pentaho
This repo contains the data visualization part (1/2) and other related files to submit for DQLab Tetris Batch IV program.
This code is an ETL process for manage seaweed dataset using pentaho and mysql.
In this project, I will extract data from many source (e.g official BPS, statistik-kkp, and open data jabar) as JSON and CSV files and load into mysql database.

This code is an ETL process for manage seaweed dataset using pentaho and mysql.
In this project, I will extract data from many source (e.g official BPS, statistik-kkp, and open data jabar) as JSON and CSV files and load into mysql database.

## Installation Guide
1. Clone the repository from GitHub:
```
git@github.com:abliskan/DQLab-Tetris-Capstone-Project-2024.git
```
2. Change the working directory to the project folder:
```
cd DQLab-Tetris-Capstone-Project-2024
```
3. Installing Java, Pentaho, and MySQL
### Java
- Download and install the latest Java JDK (i'm using java 18, you can use other version)
### Pentaho
- Download and install "Pentaho Community Edition"
### MySQL
- Download and install "MySQL Community Downloads"
4. Extract the files [file_name].ktr 
5. Create a new database for the transformed data
```
create database tetris-capstone-raw-data;
```
6. Connect to the database 
```
USE database tetris-capstone-raw-data;
```

## Dataset Preview
- The dataset before tranformation detail can be see in raw-data folder

## ETL process
### Extract from API Data Source - Open Data Jabar
[comming soon]

### Extract from Tabular Data Source - Statistik KKP
[comming soon]

### Extract from Tabular Data Source - BPS Statistik
[comming soon]

### Tranformation dataset
[comming soon]

### Load dataset into MySQL Table
[comming soon]

## Database Design
[comming soon]