# Project 2 - ETL Mini Project
__Introduction

This readme file provides an overview of the ETL mini project that I completed. The project involved building an ETL (Extract, Transform, Load) pipeline using Python, Pandas, and either Python dictionary methods or regular expressions. The objective was to extract data from Excel files, transform it into the desired format, and load it into a Postgres database.

__Project Setup

To begin the project, I followed the provided instructions and set up my working environment. I created a new repository named "Crowdfunding_ETL" and added my partner as a collaborator. I then cloned the repository to my local machine and added the necessary files to the repository.

__ETL Process

Create the Category and Subcategory DataFrames
I started by extracting and transforming data from the "crowdfunding.xlsx" Excel file to create a category DataFrame. The category DataFrame had two columns: "category_id" and "category". I assigned sequential "category_id" values from "cat1" to "catn" based on the number of unique categories. The "category" column contained only the category titles. I exported this DataFrame as "category.csv" and saved it in my GitHub repository.

Next, I extracted and transformed the data from the same Excel file to create a subcategory DataFrame. The subcategory DataFrame had two columns: "subcategory_id" and "subcategory". I assigned sequential "subcategory_id" values from "subcat1" to "subcatn" based on the number of unique subcategories. The "subcategory" column contained only the subcategory titles. I exported this DataFrame as "subcategory.csv" and saved it in my GitHub repository.

__Create the Campaign DataFrame

I proceeded to extract and transform the data from the "crowdfunding.xlsx" Excel file to create a campaign DataFrame. The campaign DataFrame had several columns, including "cf_id", "contact_id", "company_name", "description", "goal", "pledged", "outcome", "backers_count", "country", "currency", "launch_date", "end_date", "category_id", and "subcategory_id".

I made the necessary conversions and renaming of columns as specified in the instructions. For example, I converted the "goal" and "pledged" columns to float data type, renamed the "blurb" column to "description", and converted the "launched_at" and "deadline" columns to the datetime format.

I also ensured that the "category_id" and "subcategory_id" columns had unique identification numbers matching those in the respective category and subcategory DataFrames.

Once the campaign DataFrame was created, I exported it as "campaign.csv" and saved it in my GitHub repository.

__Create the Contacts DataFrame

For this part, I chose Option 1: using Python dictionary methods to extract and transform the data from the "contacts.xlsx" Excel file.

I imported the contacts.xlsx file into a DataFrame and iterated through each row, converting it into a dictionary. Then, I extracted the dictionary values from the keys using a Python list comprehension and added the values for each row to a new list.

Next, I created a new DataFrame using the extracted data. I split each "name" column value into a first and last name and placed them in separate columns. Finally, I cleaned the DataFrame and exported it as "contacts.csv", saving it in my GitHub repository.

__Create the Crowdfunding Database

To create the Crowdfunding database, I inspected the four CSV files (category.csv, subcategory.csv, campaign.csv, and contacts.csv) and sketched an ERD (Entity-Relationship Diagram) using QuickDBD. The ERD provided a visual representation of the tables and their relationships.

Using the information from the ERD, I created a table schema for each CSV file. I specified the data types, primary keys, foreign keys, and other constraints for each table.

I saved the database schema as "crowdfunding_db_schema.sql" in the Postgres format and saved it in my GitHub repository.

Next, I created a new Postgres database named "crowdfunding_db". Using the database schema, I created the tables in the correct order to handle the foreign keys.

To verify the table creation, I ran a SELECT statement for each table and confirmed that the tables were successfully created.

Finally, I imported each CSV file into its corresponding SQL table. I ran a SELECT statement for each table to ensure that the data was correctly imported.

__Conclusion

In this project, I successfully completed the ETL process by extracting data from Excel files, transforming it into the desired format using Python and Pandas, and loading it into a Postgres database. I followed the instructions provided and organized my work by creating the necessary DataFrames, exporting them as CSV files, and creating the Crowdfunding database with the appropriate table schema. Overall, it was a valuable learning experience that enhanced my skills in data extraction, transformation, and loading.
