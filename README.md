# big-data-project
ETL and clean big data project 

The Goal: The goal of this project is to clean big data from Amazon using ETL. Once ETL was complete, I linked up the Colab notebook to Postgres to gleen more information from the data, so queries could be created.

How This Was Achieved: This project was achieved by setting up a Spark Session with the Amazon data sources. I decided to analyze Ebook and Book data. Once the Spark Session was set up, I proceeded to perform ETL on the data. I counted the rows to see how much data I was working with. I also droped duplicated and changed the data structure types to match the schema. Additionally, some columns had to be dropped and the names changed. Lastly, I needed to connect to Postgres to be able to further analyze the data.

Notebook 1: Books
Creaed four different tables to match the schema file. Had issues with separating character (\t)

Notebook 2: Ebooks

Tools Used: Colab, PySpark, AWS, Postgres, SQL, 
