=# Log Data Uploader

A Python-based tool to parse, clean, and upload structured log data into a MySQL database for efficient storage and analysis.

## Features

- Reads column headers and log entries from text files
- Cleans and formats data before insertion
- Automatically maps columns to appropriate MySQL data types (INT, FLOAT, TEXT, etc.)
- Creates a unified table (`log_table_all`) if it doesn't exist
- Inserts all parsed rows into the MySQL database

## Folder Structure

log-data-uploader/
├── header.txt # Column headers separated by '|'
├── data.txt # Log data rows separated by '|'
├── uploader.py # Python script to upload log data into MySQL
## Requirements

- Python 3.x
- MySQL Server
- `mysql-connector-python` package

### Install MySQL connector:

```bash
pip install mysql-connector-python
db_config = {
    'host': 'localhost',
    'user': 'your_username',
    'password': 'your_password',
    'database': 'your_database'
}
python uploader.py

USE your_database;
SELECT * FROM log_table_all LIMIT 10;
