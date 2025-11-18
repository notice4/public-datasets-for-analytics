How to Import a Dataset

This guide explains how to import any dataset from this repository into your project using Python, SQL, R, or Excel.
Choose the method that fits your workflow.

## 📥 1. Download the Dataset
Option A — Download manually

Open the desired dataset folder.

Click on the file (CSV, JSON, XLSX, etc.).

Press Download raw file.

Option B — Using Git
git clone https://github.com/<your-username>/public-datasets-for-analytics.git

## 🐍 2. Import Into Python
CSV
import pandas as pd

df = pd.read_csv("path/to/dataset.csv")
df.head()

Excel
import pandas as pd

df = pd.read_excel("path/to/dataset.xlsx")

JSON
import pandas as pd

df = pd.read_json("path/to/dataset.json")

## 🧠 3. Import Into SQL
SQLite
.mode csv
.import path/to/dataset.csv table_name

PostgreSQL (via psql)
\copy table_name FROM 'path/to/dataset.csv' CSV HEADER;

MySQL
LOAD DATA INFILE 'path/to/dataset.csv'
INTO TABLE table_name
FIELDS TERMINATED BY ','
IGNORE 1 ROWS;

## 📊 4. Import Into R
df <- read.csv("path/to/dataset.csv")
head(df)


Excel:

library(readxl)
df <- read_excel("path/to/dataset.xlsx")

## 🧮 5. Import Into Excel / Google Sheets
Excel

Open Excel

Go to Data → Get Data → From Text/CSV

Select the file

Google Sheets

Create a new sheet

Click File → Import

Upload the CSV / XLSX file

## 📦 6. Folder Structure

Every dataset typically includes:

data.csv — main dataset

README.md — description, columns, and source

LICENSE (optional) — usage rights

## ❓ Need Help?

If you have questions, want a new dataset added, or need help importing — open an Issue in the repository.