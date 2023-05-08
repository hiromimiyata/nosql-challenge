# nosql-challenge
Goal: To evaluate ratings data.

Part 1: Database and Jupyter Notebook Set Up
I imported the data from the "establishments.json" file into a MongoDB database named "uk_food" and a collection named "establishments" by copying the import command to a markdown cell in my Jupyter Notebook. Then, I imported the required libraries - PyMongo and pprint - and created an instance of the Mongo Client. To ensure that the database and data have been imported correctly, I listed the databases and collections in MongoDB, displayed one document using pprint, and assigned the establishments collection to a variable.

Part 2: Update the Database
I added a new halal restaurant in Greenwich to the database and then found the BusinessTypeID for "Restaurant/Cafe/Canteen" and returned only the BusinessTypeID and BusinessType fields. Next, I updated the new restaurant with the BusinessTypeID I found. To check how many documents contain the Dover Local Authority, I used a query to count the number of documents with Dover Local Authority. Then, I removed any establishments within the Dover Local Authority from the database, and checked the number of documents to ensure they were deleted. Lastly, I converted latitude and longitude to decimal numbers using update_many and converted RatingValue to integer numbers using update_many.

Part 3: Exploratory Analysis
I used count_documents to display the number of documents contained in the result, displayed the first document using pprint, converted the result to a Pandas DataFrame, printed the number of rows in the DataFrame, and displayed the first 10 rows to answer the following questions:

Which establishments have a hygiene score equal to 20?
Which establishments in London have a RatingValue greater than or equal to 4?
What are the top 5 establishments with a RatingValue of 5, sorted by lowest hygiene score, nearest to the new restaurant added, "Penang Flavours"?
How many establishments in each Local Authority area have a hygiene score of 0? I sorted the results from highest to lowest, and printed out the top ten Local Authority areas.
