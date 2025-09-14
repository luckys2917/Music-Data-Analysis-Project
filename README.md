# Music-Data-Analysis-Project
..
...
....
#About The Project
This project involves a deep-dive analysis of a digital music store's database. By writing a series of SQL queries, I have explored the dataset to uncover insights and answer key business questions. The analysis covers customer behavior, sales performance, and genre/artist popularity across different countries.

The primary goal is to leverage data to understand business performance and identify potential opportunities, such as which city to target for a promotional music festival or which artists to feature.

#Business Questions Explored
 Employee Hierarchy: Who is the senior-most employee based on their job title and level?

Answer: The query identifies the single employee with the highest value in the levels column. The output will be one row containing the title, last_name, and first_name of this employee.

2. Global Sales: Which countries have the highest number of invoices?

Answer: The query counts the total number of invoices for each country and lists them in descending order. The output will be a table of all billing_country names and their corresponding invoice counts, starting with the country that has the most invoices.

3. Top Transactions: What are the top 3 highest invoice totals?

Answer: The provided query SELECT total FROM invoice ORDER BY total DESC will list all invoice totals from highest to lowest. To get only the top 3, the query would need to be modified to SELECT total FROM invoice ORDER BY total DESC LIMIT 3;. This modified query would return the three single highest values from the total column in the invoice table.

4. Market Performance: Which city has the highest total sales?

Answer: The query calculates the sum of all invoice totals for each city and returns the single city with the highest sum. The output will be one row containing the billing_city and its total InvoiceTotal.

5. Customer Value: Who is the best customer?

Answer: The query finds the customer who has spent the most money in total. It calculates the sum of all invoices for each customer and returns the customer_id, first_name, last_name, and total_spending for the single customer with the highest total.

6. Genre-based Customer Segmentation: What are the contact details of all customers who listen to Rock music?

Answer: The query returns a list of all unique customers who have purchased tracks from the 'Rock' genre. The output will be a table with the email, first_name, and last_name for each of these customers, sorted alphabetically by email.

7. Artist Popularity: Who are the top 10 rock music artists?

Answer: The query counts the number of 'Rock' genre songs for each artist in the database and returns the top 10. The output will be a list of 10 rows, each containing the artist's name and their total count of rock songs (number_of_songs), ordered from most songs to least.

8. Track Analysis: Which tracks have a song length longer than the overall average song length?

Answer: The query first calculates the average length (in milliseconds) of all tracks in the database. It then returns a list of all tracks whose milliseconds value is greater than that average. The output is a table of track name and milliseconds, ordered from the longest song to the shortest.

9. Customer-Artist Spending: How much has each customer spent on the single best-selling artist?

Answer: This query first identifies the single artist who has earned the most money. Then, it calculates how much each customer has spent specifically on tracks by that one artist. The final output is a list showing customer_id, first_name, last_name, the artist_name of the best-selling artist, and the total amount_spent by the customer on that artist.

10. Genre Popularity by Country: What is the most popular music genre for each country?

Answer: The query determines the top genre for each country based on the highest number of purchases. The output is a table showing each country, the name of its most popular genre, the total purchases for that genre, and its genre_id. If there's a tie for the most popular genre in a country, the query is written to return all tied genres.
.
.....
........
#Key SQL Concepts Demonstrated
This project showcases a variety of SQL techniques, from basic to advanced:

Data Retrieval & Filtering: SELECT, FROM, WHERE, DISTINCT

Sorting & Limiting: ORDER BY (ASC/DESC), LIMIT

Aggregate Functions: COUNT(), SUM(), AVG()

Grouping Data: GROUP BY

Joins: Combining data from multiple tables (JOIN).

Subqueries: Nesting queries to perform complex filtering.

Common Table Expressions (CTEs): Using the WITH clause to improve the readability and structure of complex queries.

Window Functions: Using ROW_NUMBER() with PARTITION BY to perform advanced ranking within specific categories.
Answer: The query identifies the top-spending customer within each country. The output is a table listing the billing_country, the customer_id, first_name, last_name, and the total_spending for that country's top customer. If there's a tie for the top spender in a country, the query will provide all customers who are tied.
