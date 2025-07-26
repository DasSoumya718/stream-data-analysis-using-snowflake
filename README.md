# stream-data-analysis-using-snowflake
🔄 Real-Time Data Pipeline with SCD Type 1 & Type 2 using Snowflake, Apache NiFi, Docker & AWS
This project demonstrates a real-time, end-to-end data pipeline for handling Slowly Changing Dimensions (SCD) Type 1 and Type 2 using:

Apache NiFi for data ingestion

Python (Faker) to simulate realistic customer data

Snowflake as the data warehouse

AWS S3 as the staging layer

Docker and EC2 for orchestration and deployment

🔧 Components
1. Python Script (generate_customers.py)
Generates fake customer data using the faker library.

Simulates inserts and updates.

Saves data as CSV files in a shared Docker volume.

2. Apache NiFi
Picks up CSV files from the shared volume.

Pushes them to AWS S3 via PutS3Object.

3. AWS S3
Acts as a staging layer.

Triggers Snowpipe for auto-ingestion into Snowflake.

4. Snowflake SQL Scripts
Ingests data from customer_raw into:

customer table (SCD Type 1)

customer_history table (SCD Type 2)

Handles:

Inserts

Updates

Deletes (for SCD2, logical expiration)




📚 Tech Stack
🧪 Python (Faker)

🧩 Apache NiFi

❄️ Snowflake

☁️ AWS S3

🐳 Docker

🧠 JupyterLab (optional)

