project overview:

This project extracts divers data from the Spotify API,including album,artist,songs from a playlist and stores it in AWS Simple Storage Service(S3) for analysis. The ultimate goal is to establish an automated pipeline hosted on AWS for data extraction and processing.

Data Processing pipeline steps:

1.Data Extraction:
A Python script on AWS Lambda extracts the information in JSON format and uploads it to AWS S3 bucket.This triggered using Amazon CloudWatch on a daily basis.

2.Data Transformatiom:
A second Lambda function is triggered whenever a new data is created in the S3 bucket.It takes the data from s3bucket and extracts the info for album,artist and songs and then stores in three different CSV files in S3bucket.

3.Data Loading into Snowflake:
By creating file format and 



![image](https://github.com/naziya-shaik/spotify_snowflake_project/assets/111407441/42b9ed73-01de-405a-b667-2c0e7f63048c)

![Screenshot (239)](https://github.com/naziya-shaik/spotify_snowflake_project/assets/111407441/6d6ec166-a4c8-4a37-9ef7-ed6260154442)
