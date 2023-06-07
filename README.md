# Crowdfunding ETL
## Introduction
In this ETL mini project, I have built an ETL pipeline using Python, Pandas, and regular expressions to extract and transform data from Excel files. The project involves creating four CSV files and using the CSV data to create an Entity-Relationship Diagram (ERD) and a table schema. Finally, I have uploaded the CSV data into a Postgres database.

## Project Setup
To get started with the project, follow these steps:

1. Create a new repository named "Crowdfunding_ETL" and add your partner as a collaborator.
2. Clone the repository to your local computer.
3. Rename the "ETL_Mini_Project_starter_code.ipynb" file by appending your first name initial and last name to the filename, for example, "ETL_Mini_Project_NRomanoff_JSmith.ipynb".
4. Add the renamed Jupyter notebook file and the "Resources" folder containing the "crowdfunding.xlsx" and "contacts.xlsx" files to the repository.
5. Push the changes to GitHub.

## ETL Process
The ETL process for this mini project is divided into the following subsections:

## Create the Category and Subcategory DataFrames
1. Extract and transform the data from the "crowdfunding.xlsx" Excel file to create a category DataFrame. The DataFrame will have a "category_id" column with entries going sequentially from "cat1" to "catn" (where n is the number of unique categories) and a "category" column containing only the category titles.
2. Export the category DataFrame as "category.csv" and save it to your GitHub repository.
3. Extract and transform the data from the "crowdfunding.xlsx" Excel file to create a subcategory DataFrame. The DataFrame will have a "subcategory_id" column with entries going sequentially from "subcat1" to "subcatn" (where n is the number of unique subcategories) and a "subcategory" column containing only the subcategory titles.
4. Export the subcategory DataFrame as "subcategory.csv" and save it to your GitHub repository.

## Create the Campaign DataFrame
1. Extract and transform the data from the "crowdfunding.xlsx" Excel file to create a campaign DataFrame. The DataFrame will have the following columns:
* "cf_id"
* "contact_id"
* "company_name"
* "description" (renamed from "blurb")
* "goal" (converted to float data type)
* "pledged" (converted to float data type)
* "outcome"
* "backers_count"
* "country"
* "currency"
* "launch_date" (renamed from "launched_at" and converted to datetime format)
* "end_date" (renamed from "deadline" and converted to datetime format)
* "category_id" (with unique identification numbers matching those in the "category_id" column of the category DataFrame)
* "subcategory_id" (with unique identification numbers matching those in the "subcategory_id" column of the subcategory DataFrame)
2. Export the campaign DataFrame as "campaign.csv" and save it to your GitHub repository.

## Create the Contacts DataFrame
Use regular expressions to extract and transform the data from the "contacts.xlsx" Excel file:

1. Import the "contacts.xlsx" file into a DataFrame.
2. Extract the "contact_id", "name", and "email" columns using regular expressions.
3. Create a new DataFrame with the extracted data.
4. Convert the "contact_id" column to the integer type.
5. Split each "name" column value into a first and last name and place each in a new column.
6. Clean the DataFrame and export it as "contacts.csv". Save it to your GitHub repository.

## Create the Crowdfunding Database
* Inspect the four CSV files and sketch an ERD of the tables using QuickDBD.
* Use the information from the ERD to create a table schema for each CSV file. Specify the data types, primary keys, foreign keys, and other constraints.
* Save the database schema as a Postgres file named "crowdfunding_db_schema.sql". Save it to your GitHub repository.
* Create a new Postgres database named "crowdfunding_db".
* Using the database schema, create the tables in the correct order to handle the foreign keys.
* Verify the table creation by running a SELECT statement for each table.
* Import each CSV file into its corresponding SQL table.
* Verify that each table has the correct data by running a SELECT statement for each.

## Conclusion
By completing this ETL mini project, I have successfully built an ETL pipeline using Python, Pandas, and regular expressions. The pipeline extracts data from Excel files, transforms it using various methods, and creates CSV files and a Postgres database. The project demonstrates proficiency in handling data extraction, transformation, and loading tasks, as well as database schema design and table creation. The resulting CSV files and database provide structured and organized data that can be further analyzed and queried for insights.
