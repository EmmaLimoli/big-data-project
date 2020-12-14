# big-data-project
ETL and clean big data project 

<strong>The Goal:</strong> The goal of this project is to clean big data from Amazon using ETL. Once ETL was complete, I linked up the Colab notebook to Postgres to gleen more information from the data, so queries could be created.

<strong>How This Was Achieved:</strong> This project was achieved by setting up a Spark Session with the Amazon data sources. I decided to analyze Ebook and Book data. Once the Spark Session was set up, I proceeded to perform ETL on the data. I counted the rows to see how much data I was working with. I also droped duplicated and changed the data structure types to match the schema. Additionally, some columns had to be dropped and the names changed. Lastly, I needed to connect to Postgres to be able to further analyze the data.

<h2>Notebook 1: Books</h2>
The books data was smaller than the Ebooks data. I wanted to look at the differences between how many people bought Ebooks compared to regular books. I found that real books were bought less than Ebooks. 

After setting up the spark session, I created four different tables to match the schema file. I did have issues with changing the separater when importing the data from a comma to a different character (\t). Once that was repaired, I created a review_id, products, customer_id, and a vine table. Each of these tables needed to change the data structures to match the schema file and the names of the columns needed to be updated as well. I ran into an issue with changing the name of a column last instead of first in the third table. I found that it was better to change the name of the column and then perform the change of the data structure rather than doing that first. 

Once the data was structured to match the schema file, I set up a connection to Postgres and then the separate connections to each of the four databases. Once the connection was set up, I ran the schema file in Postgres to ensure that everything was successful.

<h2>Notebook 2: Ebooks</h2>
As mentioned, I  

<strong>Tools Used: Google Colab, PySpark, AWS, Postgres, SQL, ETL</strong> 
