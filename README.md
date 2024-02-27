# UK Food Standards Analysis

I was tasked with analyzing ratings data from the UK Food Standards Agency to assist the editors of Eat Safe, Love magazine in deciding where to focus future articles. Here's a breakdown of the tasks:

## Part 1: Database and Jupyter Notebook Set Up (NoSQL_setup_starter.ipynb)

### Setup Steps

1. I imported the data provided in the `establishments.json` file from the Terminal, naming the database `uk_food` and the collection `establishments`. The import command was copied to a markdown cell in the Jupyter Notebook.
2. Imported the necessary libraries: PyMongo and Pretty Print (pprint).
3. Created an instance of the Mongo Client.
4. Confirmed the successful creation of the database and loading of data:
   - Listed the databases in MongoDB, ensuring `uk_food` was included.
   - Confirmed the presence of the `establishments` collection.
   - Found and displayed one document from the `establishments` collection using `find_one` and displayed it with pprint.
5. Assigned the `establishments` collection to a variable for further use.

## Part 2: Update the Database (NoSQL_setup_starter.ipynb)

### Database Updates

1. Added information for a new halal restaurant, "Penang Flavours," in Greenwich to the database.
2. Identified and updated the BusinessTypeID for "Restaurant/Cafe/Canteen" for the new restaurant.
3. Removed establishments within the Dover Local Authority from the database per the magazine's request.
4. Converted string number values to decimal numbers for latitude and longitude, and RatingValue to integer numbers using `update_many`.

## Part 3: Exploratory Analysis (NoSQL_analysis_starter.ipynb)

Eat Safe, Love had specific questions to help them find locations to visit and avoid. Using the provided Jupyter Notebook `NoSQL_analysis_starter.ipynb`, I explored the dataset and found answers to the following questions:

1. Identified establishments with a hygiene score equal to 20.
2. Found establishments in London with a RatingValue greater than or equal to 4.
3. Determined the top 5 establishments with a RatingValue of 5, sorted by lowest hygiene score, nearest to "Penang Flavours" restaurant.
4. Counted establishments in each Local Authority area with a hygiene score of 0, sorted from highest to lowest, and printed out the top ten local authority areas.

The analysis provided valuable insights for Eat Safe, Love magazine to make informed decisions about future articles.
