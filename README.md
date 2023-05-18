The UK Food Standards Agency evaluates various establishments across the United Kingdom, and gives them a food hygiene rating. I've been contracted by the editors of a food magazine, Eat Safe, Love, to evaluate some of the ratings data in order to help their journalists and food critics decide where to focus future articles.

The magazine editors have some requested modifications for the database before I can perform any queries or analysis for them. I will make the following changes to the establishments collection:

An exciting new halal restaurant just opened in Greenwich, but hasn't been rated yet. The magazine has asked you to include it in my analysis.


I will find the BusinessTypeID for "Restaurant/Cafe/Canteen" and return only the BusinessTypeID and BusinessType fields.
Update the new restaurant with the BusinessTypeID I found.
The magazine is not interested in any establishments in Dover, so I will check how many documents contain the Dover Local Authority. Then, I will remove any establishments within the Dover Local Authority from the database, and check the number of documents to ensure they were deleted.
Some of the number values are stored as strings, when they should be stored as numbers.
I will then use update_many to convert latitude and longitude to decimal numbers, and also  use update_many to convert RatingValue to integer numbers.



Eat Safe, Love has specific questions they want me to answer, which will help them find the locations they wish to visit and avoid.
I will use NoSQL_analysis_starter.ipynb for this section of the challenge.

I will use count_documents to display the number of documents contained in the result, then display the first document in the results using pprint.
Convert the result to a Pandas DataFrame, print the number of rows in the DataFrame, and display the first 10 rows.
Determine which establishments have a hygiene score equal to 20.
Determine which establishments in London have a RatingValue greater than or equal to 4?
I will find the  top 5 establishments with a RatingValue of 5, sorted by lowest hygiene score, nearest to the new restaurant added, "Penang Flavours"
Lastly, find how many establishments in each Local Authority area have a hygiene score of 0, and sort the results from highest to lowest, and print out the top ten local authority areas.


