# ![dataengineercamp_logo](https://github.com/user-attachments/assets/5e669390-1404-4b18-9380-6cc2ac2a5e39) 
# [Data Engineer Camp](https://dataengineercamp.com): Capstone Project

## **Earthquakes ELT: Production Version**
Author: _Joshua Botticher_

** See Local_Earthquake_ELT repo for Local code version **

## Objective:
The purpose of this project was to put in use all of the skills and tools I have learned during the past 16 weeks as a student in Data Engineer Camp's botcamp. The objective of this project is to create a batch driven data ingestion process to use earthquake data to create dashboards using historical and incremental data from the USGS Earthquake API for public use.

## Consumers:
- Researchers: They use the data for analyzing seismic activity patterns and predicting future events.
- Students: They need access to earthquake data for educational projects and learning purposes.
- Educators: They require the data to teach seismic activity and its impacts.
- General Public: They seek to understand earthquake risks and safety measures.

## Questions I Want To Answer:
1) What are the most recent earthquakes and their magnitudes?
2) Which regions are experiencing the highest frequency of earthquakes?
3) What are the patterns and trends in seismic activity over the past year?
4) Which areas are most at risk based on historical data?


| `Source Name`  | `Source Type` | `Source Docs`                               | `Endpoint` |
| -------------  | ------------- | ------------                                | -----------|
|  USGS Earthquake Catalog    | rest api      | https://earthquake.usgs.gov/fdsnws/event/1/ | https://earthquake.usgs.gov/fdsnws/event/1/query|


## Architecture:
![architecture_earthquakes drawio-2](https://github.com/user-attachments/assets/30416493-e6cd-4531-9c23-70e9d336245e)

## Instructions:

1) Clone this repo.
2) Deploy Airbyte on an AWS EC2 Instance. Airbyte deployment docs: https://docs.airbyte.com/deploying-airbyte/on-aws-ec2
3) Create a Dagster cloud account and connect your Github repo to Dagster. Dagster cloud deployment docs: https://docs.dagster.io/deployment/open-source.
4) Create an AWS account and create an S3 bucket. See AWS docs: https://docs.aws.amazon.com/AmazonS3/latest/userguide/GetStartedWithS3.html#creating-bucket
5) Update environment variable in Dagster and Snowflake login info (dbt_earthquake->profiles.yml).
