# Twitter_data_pipeline



**Twitter Scraper Data Pipeline**

**Problem Statement**

Organization  wants to collect data from Twitter in order to better understand their target audience and their interests or  gain insights about their competitors. They want to collect tweets related to their products and services, as well as tweets from their competitors and industry influencers. and store them in a centralized location where  they  can perform further analysis and visualization.However, collecting this data manually is time-consuming and error-prone.They would need an automated data pipeline that can scrape Twitter data, extract relevant information, transform the data into a usable format, and load it into a data warehouse.


**Solution**

To solve this problem, we created a data pipeline using Snscrape, Airflow, EC2 instances, and an S3 bucket. The pipeline works as follows:

1.  Snscrape is used to scrape Twitter data based on specific search criteria, such as hashtags, keywords, or user accounts. The scraped   data is saved a csv file.
2.  Airflow is used to schedule and orchestrate the ETL (extract, transform, load) process. Airflow runs a DAG (directed acyclic graph) that consists of tasks for each step of the ETL process.
3.  EC2 instances are used to host the Airflow server and worker nodes. I chose EC2 instances because they are scalable, cost-effective, andeasy to set up.
4.  The extracted data is transformed using Python scripts to filter out irrelevant data, clean up the data, and convert it into a usable format.
5.  The transformed data is loaded into an S3 bucket, which serves as a data warehouse. S3 is a scalable and durable storage solution that allows us to easily access and analyze the data.

**Stacks Used**

* Snscrape - a  Python library that can be used to scrape data from social networking services (SNS). It scrapes things like user profiles, hashtags, or searches and returns the discovered items, e.g. the relevant posts.
* Airflow -Apache Airflow is a workflow management system that can be used to automate data pipelines.
* EC2 instances - virtual servers provided by Amazon Web Services (AWS).
* Python - a programming language used for data transformation.
* S3 Bucket - an object storage service provided by AWS.
