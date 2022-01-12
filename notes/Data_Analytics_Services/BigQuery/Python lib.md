# Python Client Library
## Preliminary
 ### 1. Setting service account key
 IAM & Admin > Service Accounts > New Service account

 ### 2. install package
 pip install google-cloud-bigquery


## Create dataset
```python
from google.cloud import bigquery
# Getting aggount
SERVICE_ACCOUNT_JSON=r'path to account json'

client = bigquery.Client.from_service_account_json(SERVICE_ACCOUNT_JSON)
# Setting dataset parameters
dataset_id = "<dataset_id>"
# Construct a full Dataset object to send to the API.
dataset = bigquery.Dataset(dataset_id)
dataset.location = "US"
dataset.description= "desc"
# Send the dataset to the API for creation, with an explicit timeout.
# Raises google.api_core.exceptions.Conflict if the Dataset already
# exists within the project.
dataset_ref = client.create_dataset(dataset, timeout=30)

print(dataset_ref.dataset_id)
```

## Create table

```python
from google.cloud import bigquery
SERVICE_ACCOUNT_JSON=r'path to account json'

# Construct a BigQuery client object.
client = bigquery.Client.from_service_account_json(SERVICE_ACCOUNT_JSON)

# TODO(developer): Set table_id to the ID of the table to create.
table_id = "bigquery-demo-285417.dataset_new.table_py"

job_config = bigquery.LoadJobConfig(
    schema=[
        bigquery.SchemaField("name", "STRING"),
        bigquery.SchemaField("gender", "STRING"),
		bigquery.SchemaField("count", "INTEGER")
    ],
	source_format=bigquery.SourceFormat.CSV, skip_leading_rows=1, autodetect=True,
)
file_path=r'F:\record\Big Query\codes and data\names\yob1880.txt'
source_file = open(file_path, "rb")
job = client.load_table_from_file(source_file, table_id, job_config=job_config)

job.result()  # Waits for the job to complete.

table = client.get_table(table_id)  # Make an API request.
print(
    "Loaded {} rows and {} columns to {}".format(
        table.num_rows, table_id
    )
)
```

## Query

```python
from google.cloud import bigquery
SERVICE_ACCOUNT_JSON=r'path to account json'

# Construct a BigQuery client object.
client = bigquery.Client.from_service_account_json(SERVICE_ACCOUNT_JSON)
query_to_run = "your query here"

query_job=client.query(query_to_run)

print(query_job)
```