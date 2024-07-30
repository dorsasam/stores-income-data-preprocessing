# Department Store Income Data Cleaning
## Project Description
This project aims to clean and standardise the country names in a dataset containing information on different department stores worldwide and their income. 
The main issue with the dataset is the inconsistency of the country names in the country column. 
The objective is to ensure consistent abbreviations for the country names using the Fuzzywuzzy library to find and match variations of country names to the closest standard variation. 
Exceptions that are not handled by the Fuzzywuzzy process will be addressed manually.

## Data Description
The dataset contains the following columns:

- id: Unique identifier for each department store.
- store_name: Name of the department store.
- store_email: Email address of the department store.
- country: Country where the department store is located (contains inconsistent country names).
- income: Income of the department store.
- date_measured: The date and time of the income measurement.

## Methodology
- **Initial Data Load**:
The dataset is loaded from the data directory.
- **Country Name Standardization**:
The Fuzzywuzzy library is used to match country name variations to their closest standard abbreviation.
A threshold is set to determine the closeness of the match.
- **Manual Handling**:
Any country names that are not matched by Fuzzywuzzy will be handled manually.
- **Save Cleaned Data**: The cleaned dataset is saved in the output directory.
  
## Installation
- Clone the repository:
```bash
git clone https://github.com/dorsasam/department-store-income-data-cleaning.git
```
- Navigate to the project directory:
```bash
cd department-store-income-data-cleaning
```
- Create a virtual environment and activate it:
```bash
python -m venv env
source env/bin/activate  # On Windows use `env\Scripts\activate`
```
- Install the required dependencies:
```bash
pip install -r requirements.txt
```
