
# Modelling a Data Warehouse

**Project Description**: # Modelling a Data Warehouse

## Project Description

This project focuses on designing and developing a data warehouse using Pentaho Data Integration, with the goal of transforming and optimizing data for analytical purposes. We aim to create a centralized repository that allows for efficient reporting of our soccer data.

## Key Objectives

### Goal
- To design and develop a data warehouse using Pentaho.

### Approach
1. **Download and Install Pentaho Software**: Start by acquiring and setting up the Pentaho software suite, which provides essential tools for data integration and analysis.

2. **Create a Data Warehouse**: Define the architecture and structure of the data warehouse, including fact and dimension tables.

3. **Data Retrieval**: Retrieving data from the soccer.sql obtained from kaggle

4. **ETL Process (Extract, Transform, Load)**: Perform ETL processes to clean, transform, and load the retrieved data into the data warehouse.

5. **OLAP Operations**: Utilize the data warehouse to execute OLAP (Online Analytical Processing) operations, such as slicing, dicing, to extract valuable insights from the data for analytical purposes.

Through these steps, we facilitate data accessibility and analysis, making it easier to derive meaningful insights from the soccer database.


## Table of Contents

1. [Getting Started](#getting-started)
2. [Prerequisites](#prerequisites)
3. [Installation](#installation)
4. [Data Preparation](#data-preparation)
5. [ETL Process](#etl-process)
6. [OLAP Cube Design](#olap-cube-design)
7. [Usage](#usage)
8. [Contributing](#contributing)
9. [License](#license)

## Getting Started

Harnessing the capabilities of data warehousing and Online Analytical Processes (OLAP), offering an efficient and streamlined approach to dissecting the intricacies of soccer.
1.1 Background

## Installations
- MariaDB
- Pentaho Data Integration
- Pentaho Workbench
- Pentaho Analysis Server
- Qlik
- [Kaggle dataset](https://www.kaggle.com/hugomathien/soccer)

1. **Database Setup**
   - Start XAMPP and import the database from the "Data/soccer.zip" file. This will create the "soccer" database.
   - You can follow the instructions in [this guide](https://stackoverflow.com/questions/44366004/fatal-error-out-of-memory-allocated-761004032-tried-to-allocate-755370216-by) to import a large database file into XAMPP's MySQL.

2. **Data Warehouse Schema Initialization**
   -  To initialize the data warehouse schema,run all the scripts located in the "Transformation/Scripts" folder in the order of their filenames 

3. **Pentaho Data Integration Setup**
   - Download and install Pentaho Data Integration.
   - Copy the binaries from the "Other Utilities" folder and paste them into the "lib" folder within the Pentaho Data Integration directory.

4. **Running ETL Transformations**
   - Open the transformations in the "Transformation" folder.
   - Run each transformation in the following order:
     - "month_dim.ktr"
     - "season_dim.ktr"
     - "league_dim.ktr"
     - "team_dim.ktr"
     - "match_goals_fact.ktr"

This simplified format provides clear steps for setting up the database, initializing the data warehouse schema, configuring Pentaho Data Integration, and running the ETL transformations in a sequential and easy-to-follow manner.

## Data Preparation

**1. Data Collection:**
   - Our data is from a SQL database.
   - Downloaded the dataset from the source.

**2. Data Inspection:**
   - We examined the dataset to understand its structure, including the tables, columns, and data types.
   - We also checked for missing data, duplicate records, and outliers.

**3. Data Loading:**
   - Store the cleaned and preprocessed dataset in a new MariaDb, 
   - Ensure that the data is structured and formatted for easy access and analysis.
## ETL Process

The ETL (Extract, Transform, Load) process in this project involves several essential steps for migrating data from a transactional database to a data warehouse using Pentaho Data Integration. Here's an explanation of each ETL step:

**1. Extraction (E):**
   - In the extraction phase, data is sourced from the "soccer" database.

**2. Transformation (T):**
   - In the transformation phase, data undergoes several operations to prepare it for loading into the data warehouse. These operations included:

     - **Data Cleaning**: This step involved handling missing values, removing duplicates, and addressing outliers. 
     
     - **Data Integration**: Data from multiple tables or sources were integrated or joined to create a unified dataset. This could included merging data related to matches, teams, and seasons.
     
     - **Data Conversion**: e.g., changing date formats, this step ensured that the data is in the correct format.
     
     - **Aggregation**: Aggregating data was necessary to create summary statistics or perform calculations, such as aggregating match statistics over multiple seasons.
     
    
**3. Load (L):**
   - In the load phase, the transformed and prepared data was loaded into the data warehouse. This data warehouse was implemented using Pentaho Data Integration.

,This are the  specific steps mentioned in the project:

1. **Run XAMPP and import database from Data/soccer.zip. This will create soccer database.**
   
2. **Run all scripts in Transformation/Scripts folder in ordered manner according to file name. Those scripts initialize the data warehouse schema.**
   
3. **Download and open Pentaho Data Integration.**

4. **Copy binaries in Other Utilities folder to lib in Pentaho Data Integration folder.**
   

5. **Open transformations in Transformation folder and run them with respect to this ordering:**


The ETL process described in this project involved a combination of data extraction, transformation, and loading activities to create a structured data warehouse from the initial transactional database. It is a  crucial process for preparing the data for efficient analytical querying and reporting.

## Usage
**Instructions for Using the OLAP Cube with Pentaho Tools:**

1. **Accessing the OLAP Cube**:
   - Ensure that you have Pentaho Analysis Server installed and running.
   - Connect to the Pentaho Analysis Server through a client tool like Pentaho Analyzer 
2. **Selecting the OLAP Cube**:
   - Choose the OLAP cube you want to work with. This cube should be designed based on your data warehouse schema, containing fact and dimension tables.

3. **Basic OLAP Operations**:

   - **Slice**: Slicing involves selecting a specific value from one dimension to view a "slice" of data. For example, you can slice by a specific time period, such as a month or year.

   - **Dice**: Dicing allows you to select values from multiple dimensions to view a smaller subset of data. For instance, you can dice data by both time and product categories to analyze sales within a particular timeframe and product group.


**Sample OLAP Operation Example**:

Let's consider an example of analyzing soccer match data using an OLAP cube.

**Step 1: Accessing the OLAP Cube**
   - Open your OLAP client tool (e.g., Pentaho Analyzer).
   - Connect to the Pentaho Analysis Server.

**Step 2: Selecting the OLAP Cube**
   - Choose the "Soccer_OLAP" OLAP cube, which contains data from the data warehouse, including facts like match results and dimensions like time, teams, and leagues.

**Step 3: Performing OLAP Operations**

   - **Slice**: Slice the data by selecting a specific month (e.g., June seson). This will provide insights into matches played during that season.

   - **Dice**: Dice the data by choosing a particular season and a specific league (e.g., "Premier League"). This will give you a subset of data for analysis within the chosen season and league.

These OLAP operations provide you with flexible ways to explore and analyze soccer match data using the OLAP cube, allowing you to gain insights from different angles and levels of granularity.

## Contributing

Collaborators on This Project:

    Ridge: Research
    David: Code development
    Derick and Simala: Report generation
    Sharon, Lindah, Lorraine, Claudine, Monilade: Installation and pipelines
    Kabutu and Henry: Report editing
---

