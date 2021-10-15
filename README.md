## Data Engineering and Analytics ##
***
### Instructions:
- Augment the data with a hash key
- Filter out the questionable data
- Write the data in a JSON file one record at a time
- Watch the data emitted in the previous task
- When the number of events reach 1000, output the events to a JSON file
- The output filenames should have a batch number e.g. the second 1000 records will go into a file
called 2.json
- List post codes based on fastest response . Hint ( Refer columns Request date and implementation Date )
- Top Agents based on postcode and amount
```
python main.py
```
***
### Local dev environment:
- JetBrains DataSpell and Jupyter Notebooks
- Apache Spark 3.1.2
- Python 3.8
- MacOs Silicon Processor
- Tested on Ubuntu Linux
***
### Delta Lake:
Delta Lake like dataflow:
![alt text](https://github.com/arturogonzalezm/challenge_transactions/blob/master/images/delta_lake.png?raw=true)
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