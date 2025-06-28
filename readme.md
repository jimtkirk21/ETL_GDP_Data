Country GDP ETL Project
Description
This project implements an Extract, Transform, Load (ETL) pipeline to fetch nominal GDP data for various countries from a Wikipedia page, transform it into a more usable format (GDP in billions USD), and then load it into both a CSV file and a SQLite database. This solution provides a clear, automated way to acquire and manage economic data, demonstrating core data engineering principles.

Features
Data Extraction: Scrapes country-wise nominal GDP data from a specified Wikipedia URL.

Data Transformation: Cleans and converts GDP values from millions to billions (USD) and formats them for consistency.

Data Loading: Stores the processed data into a CSV file and a SQLite database table.

Database Querying: Includes functionality to run SQL queries against the loaded database and print results.

Progress Logging: Maintains a log file to track the execution stages of the ETL pipeline.

Technologies Used
Python 3.x

requests: For making HTTP requests to fetch web page content.

BeautifulSoup4 (bs4): For parsing HTML and extracting data.

pandas: For data manipulation and analysis (DataFrames).

numpy: For numerical operations, specifically rounding.

sqlite3: For interacting with SQLite databases.

datetime: For timestamping log entries.

Setup & Installation
To set up and run this project locally, follow these steps:

Clone the repository:

git clone https://github.com/your-username/country-gdp-etl.git
cd country-gdp-etl

(Replace your-username with your actual GitHub username)

Create a virtual environment (recommended):

python3 -m venv venv
source venv/bin/activate  # On Windows, use `venv\Scripts\activate`

Install the required Python libraries:

pip install -r requirements.txt

Usage
To run the ETL pipeline:

Execute the main Python script:

python etl_script.py

Output Files:

A Countries_by_GDP.csv file will be created in the project root directory, containing the transformed GDP data.

A World_Economies.db SQLite database file will be created, containing the Countries_by_GDP table.

A etl_project_log.txt file will be created/updated with execution logs.

Database Query:
The script automatically runs a sample SQL query to select countries with GDP greater than or equal to 100 billion USD and prints the result to the console. You can modify the query_statement variable in etl_script.py to run different queries.

Project Structure
country-gdp-etl/
├── etl_script.py
├── requirements.txt
├── README.md
├── .gitignore
└── (output files: Countries_by_GDP.csv, World_Economies.db, etl_project_log.txt)

Supporting Files
etl_script.py
This is the main Python script containing the ETL functions and the execution flow.
(The full content of your provided Python code goes here)

requirements.txt
This file lists all the Python dependencies required for the project.

requests==2.32.3
beautifulsoup4==4.12.3
pandas==2.2.2
numpy==1.26.4

(Note: Versions are based on common recent stable releases. You might want to lock these to the exact versions you developed with if different.)

License
This project is licensed under the MIT License - see the LICENSE file for details.
(You would typically create a LICENSE file in your repository with the MIT License text)

Contributing
Contributions are welcome! Please feel free to open issues or submit pull requests.