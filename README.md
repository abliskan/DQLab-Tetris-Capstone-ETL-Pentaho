# DQLab-Tetris-Capstone-ETL-Pentaho
This repo contains the ETL process part (2/2) and other related files to submit for DQLab Tetris Batch IV program.
This code is an ETL process for manage seaweed dataset using pentaho and mysql.
In this project, I will extract data from many source (e.g official BPS, statistik-kkp, and open data jabar) as JSON and CSV files and load into mysql database.

## Installation Guide
1. Clone the repository from GitHub:
```
git@github.com:abliskan/DQLab-Tetris-Capstone-ETL-Pentaho.git
```
2. Change the working directory to the project folder:
```
cd DQLab-Tetris-Capstone-ETL-Pentaho
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
![ETL_API](https://github.com/abliskan/DQLab-Tetris-Capstone-ETL-Pentaho/blob/main/asset/images/Capture-1-1-pentaho.PNG)
- data source 1: [open-data-jabar, "Produksi Perikanan Budidaya Rumput Laut Berdasarkan Kabupaten/Kota di Jawa Barat"](https://opendata.jabarprov.go.id/id/dataset/produksi-perikanan-budidaya-rumput-laut-berdasarkan-kabupatenkota-di-jawa-barat)

### Extract from Tabular Data Source - Statistik KKP
![ETL_csv_1](https://github.com/abliskan/DQLab-Tetris-Capstone-ETL-Pentaho/blob/main/asset/images/Capture-1-2-pentaho.PNG)
- data source 2: [statistik-KKP, "Produksi Perikanan Budidaya"](https://statistik.kkp.go.id/home.php?m=prod_ikan_budidaya_kab#panel-footer)
- data source 3: [statistik-KKP, "Data Luas Lahan Perikanan Budidaya Rumput Laut Menurut Provinsi (satuan: m2)"](https://statistik.kkp.go.id/home.php?m=luaslahan&i=7#panel-footer-kpda)

### Extract from Tabular Data Source - BPS Statistik
![ETL_csv_2](https://github.com/abliskan/DQLab-Tetris-Capstone-ETL-Pentaho/blob/main/asset/images/Capture-1-3-pentaho.PNG)
- data source 4: [BPS, "Kode Relasi BPS dengan Kemendagri"](https://sig.bps.go.id/bridging-kode/index)

### Tranformation and Load dataset
![ETL_csv_3](https://github.com/abliskan/DQLab-Tetris-Capstone-ETL-Pentaho/blob/main/asset/images/Capture-3-mysql.PNG)
- sorting column "year" by ASC order -> join 3 different table -> load into database

## Database Design
![mysql_db_design](https://github.com/abliskan/DQLab-Tetris-Capstone-ETL-Pentaho/blob/main/asset/images/Capture-4-mysql.PNG)

## Final Output Table
![Data_table](https://github.com/abliskan/DQLab-Tetris-Capstone-ETL-Pentaho/blob/main/asset/images/Capture-5-mysql.PNG)
