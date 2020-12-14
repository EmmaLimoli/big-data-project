# big-data-project
ETL and clean big data project 

<strong>The Goal:</strong> The goal of this project was to clean big data from Amazon using ETL. Once ETL was complete, I linked up the Google Colab notebook to Postgres to gleen more information from the data so queries could be created and analyzed further. Essentially, I was cleaing the data to prepare it to be used.

<strong>How This Was Achieved:</strong> I decided to analyze Ebook and Book data. This project was achieved by setting up a Spark Session with the Amazon data gz file.  Once the Spark Session was set up, I proceeded to perform ETL on the data. I counted the rows to see how much data I was working with. I also droped duplicates and changed the data structure types to match the schema file. Additionally, some columns had to be dropped since they weren't needed and the names changed. Lastly, I needed to connect to Postgres to be able to further analyze the data.

<h2>Notebook 1: Books</h2>
The books data was smaller than the Ebooks data. I wanted to look at the differences between how many people purchased Ebooks compared to regular books. I found that real books were purchased less than Ebooks. 
<br></br>
After setting up the Spark Session, I created four different tables to match the schema file. I did have issues with changing the separater when importing the data from a comma to a different character (\t). Once that was repaired, I created a review_id, products, customer_id, and a vine table. Each of these tables needed to change the data structures to match the schema file and the names of the columns needed to be updated as well. I ran into an issue with changing the name of a column last instead of first in the third table. I found that it was better to change the name of the column and then perform the change of the data structure rather than doing that first. 
<br></br>
Once the data was structured to match the schema file, I set up a connection to Postgres and then the separate connections to each of the four databases. Once the connection was set up, I ran the schema file in Postgres to ensure that everything was successful.

<h2>Notebook 2: Ebooks</h2>
As mentioned, I wanted to compare Ebooks to real books. The Ebooks had a lot more data and purchases than the books. This makes sense because Amazon offers a lot of Ebooks, but they also offer services to publish your own books, so some books are only available for purchase as an Ebook instead of a normal one.
<br></br>
I did much the same as I did for the first notebook. I didn't run into the same issues because I'd already problem-solved. I did notice that doing this the second time around it was a lot easier and I felt more comfortable with the process. I changed the data structures, the names of the columns, and dropped duplicates and NA columns to ensure the data was clean. There wasn't much that I did differently. Although, this data set was bigger than the previous one. I found it easier to work with and ran into less problems. 
<br></br>
<strong>Tools Used: Google Colab, PySpark, AWS, Postgres, SQL, ETL</strong> 
