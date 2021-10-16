## Data Engineering and Analytics ##

### Overview:
- The main purpose of the following implementation is to focus on the data life cycle across the different layers withing 
the ETL pipeline.
- The current implementation has been done locally trying to simulate the Delta Lake approach.
***
### Requirements:
- Augment the data with a hash key
- Filter out the questionable data
- Write the data in a JSON file one record at a time
- Watch the data emitted in the previous task
- When the number of events reach 1000, output the events to a JSON file
- The output filenames should have a batch number e.g. the second 1000 records will go into a file
called 2.json
- List post codes based on fastest response . Hint ( Refer columns Request date and implementation Date )
- Top Agents based on postcode and amount
***
### Local dev environment:
- JetBrains DataSpell and Jupyter Notebooks
- Apache Spark 3.1.2
- Python 3.8
- MacOs Silicon Processor
- Tested on Ubuntu Linux
***
### Delta Lake:
Delta Lake dataflow:
![alt text](https://github.com/arturogonzalezm/transactions_notebooks/blob/master/images/delta_lake_.png?raw=true)
- The notebook that is performing the ETL jobs is:
```
notebooks/ETL/transaction_pipelines.ipynb
```
- The notebooks that are calculating the fastest response and Top Agents based on postcode and amount as part of the 
presentation/reporting layer are:
```
notebooks/ETL/fastest_response_report.ipynb and notebooks/ETL/top_agents_report.ipynb
```
***
### Project/Folder structure:
```
└── transactions_notebooks/
    ├── data/
    │   ├── bronze/
    │   ├── gold/
    │   ├── raw/
    │   │   └── Transaction.csv
    │   ├── response/
    │   └── silver/
    ├── docs/
    │   └── SISU Coding Assessment Instructions.pdf
    ├── images/
    │   └── delta_lake.png
    ├── misc/
    │   ├── __init__.py
    │   └── constants.py
    ├── notebooks/
    │   ├── BI/
    │   │   ├── fastest_response_report.ipynb
    │   │   └── top_agents_report.ipynb
    │   └── ETL/
    │       └── transaction_pipelines.ipynb
    ├── README.md
    ├── requirements.txt
    └── schema_definition/
    ├── __init__.py
    └── schema.py
```