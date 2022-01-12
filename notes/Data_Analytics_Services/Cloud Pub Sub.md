# Cloud Pub/Sub
Based on publishing/subscription pattern

![[pub-sub-pattern.png]]

Fully-Managed real-time messaging service allowing to efficiently send and receive messages between applications and services.



Service used for [[Ingestion]] data at scale

Integrated with [[Cloud Storage]] and [[Cloud Dataflow]]

End-to-end encryption, [[Identity & Access Management]] 

## Pubblishing code example
```python
from google.cloud import pubsub_v1
import time 

publisher = pubsub_v1.PublisherClient()

topic_name = 'projects/bigquery-demo-285417/topics/data_stream_from_file'
try:
    publisher.create_topic(topic_name)

except:
    print ('Topic already exists')

with open('food_daily.csv') as f_in:
    for line in f_in:
        # Data must be a bytestring
        data = line
        future = publisher.publish(topic_name, data=data)
        print(future.result())
        time.sleep(1)

```