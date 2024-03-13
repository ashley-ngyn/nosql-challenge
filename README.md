# nosql challenge

## instructions ##
* Part 1: Database and Jupyter Notebook Set Up
    * Import the data provided in the establishments.json file from your Terminal. Name the database uk_food and the collection establishments.
    * Create an instance of the Mongo Client.
    * Confirm that you created the database and loaded the data properly:
        * List the databases you have in MongoDB. Confirm that uk_food is listed.
        * List the collection(s) in the database to ensure that establishments is there.
        * Find and display one document in the establishments collection using find_one and display with pprint.
    * Assign the establishments collection to a variable to prepare the collection for use.
* Part 2: Update the Database
    * An exciting new halal restaurant just opened in Greenwich, but hasn't been rated yet. The magazine has asked you to include it in your analysis.
    * Find the BusinessTypeID for "Restaurant/Cafe/Canteen" and return only the BusinessTypeID and BusinessType fields.
    * Update the new restaurant with the BusinessTypeID you found.
    * The magazine is not interested in any establishments in Dover. Remove any establishments within Dover.
    * Convert number values from string to numbers.
* Part 3: Exploratory Analysis
    * Use count_documents to display the number of documents contained in the result.
    * Display the first document in the results using pprint.
    * Convert the result to a Pandas DataFrame, print the number of rows in the DataFrame, and display the first 10 rows.
        * 1. Which establishments have a hygiene score equal to 20?
        * 2. Which establishments in London have a RatingValue greater than or equal to 4?
        * 3. What are the top 5 establishments with a RatingValue of 5, sorted by lowest hygiene score, nearest to the new restaurant added, "Penang Flavours"?
        * 4. How many establishments in each Local Authority area have a hygiene score of 0?
    

## sources ##
* 01: https://stackoverflow.com/questions/7431422/find-in-dictionary-by-value-in-mongo
    * to find valyes in a list within a dictionary
        * 'geocode.latitude': {'$toDouble': '$geocode.latitude'}

* 02: mongodb_aggregation_pipeline_solution
    * how to make pipeline and aggregate
        * pipeline = [match_query, group_query, sort_values]
        * results = list(establishments.aggregate(pipeline))

* 03: mongo_mini_project_part2_solution
    * use json_normalize to convert to pandas df
        * aggregated_df = pd.json_normalize(results)