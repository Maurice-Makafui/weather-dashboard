
**Achieving the Weather Dashboard Project**

This is a comprehensive guide on how I successfully completed the Weather Dashboard project, utilizing Python, AWS S3, and the OpenWeather API. By following these steps, I learnt how to interact with APIs, set up a Python environment, configure AWS CLI, and handle files with AWS S3.


1.
##Create an OpenWeather Account and Obtain API Key
Step:
•	I visited the OpenWeather website and created an account.
•	After logging in, I navigated to the API section and generated an API key. This key was used to fetch weather data for different regions.
Lesson Learnt:
•	API Integration: I learnt how to create and use an API key to interact with external APIs (like OpenWeather). The API key is a critical part of securely accessing the data provided by the service.



2.
##Set Up My Work Environment in VSCode
Step:
•	I created a new directory for the project and opened it in VSCode.
•	Inside the project directory, I created a .env file. This file will store sensitive information like the OpenWeather API key and the AWS S3 bucket name. 
o	Example: 
o	WEATHER_API_KEY=your_openweather_api_key
o	AWS_BUCKET_NAME=unique_bucket_name


Lesson Learnt:
•	Environment Setup: I learnt how to use .env files to securely store sensitive data such as API keys. This is a good practice to avoid hardcoding sensitive information in my source code.



3. 

##Set Up AWS in My Terminal
Step:
•	I logged into my AWS console and navigated to IAM (Identity and Access Management).
•	I created a new IAM user and attached the "AdministratorAccess" and "AmazonS3FullAccess" policies.
•	I generated an access key and secret key for the new IAM user.
•	In VSCode terminal, I ran aws configure and entered the Access Key ID and Secret Access Key when prompted.
Lesson Learnt:
•	AWS CLI Configuration: I learnt how to configure AWS CLI using IAM credentials. This allows me to interact with AWS services (like S3) directly from my terminal using Python.
________________________________________

4.
 ##Set Up My Python Environment
Step:
•	I downloaded and installed Python on my machine (Windows or Linux, based on my system).
•	I set up environment variables as needed.
Lesson Learnt:
•	Python Setup: I gained experience in setting up a Python environment on my machine, including installing Python and configuring the system for running Python scripts.

________________________________________


5. 

##Folder Structure Setup
Step:
•	I organized my project folder structure as follows:
•	weather-dashboard/
•	├── src/
•	│   ├── __init__.py
•	│   └── weather_dashboard.py
•	├── .env
•	├── .gitignore
•	└── requirements.txt

	I added .gitignore to prevent sensitive files from being tracked by Git:
•	.env
•	.git

•	In the requirements.txt, I listed the necessary Python packages needed for the smooth run:
•	boto3==1.26.137
•	python-dotenv==1.0.0
•	requests==2.28.2



#Lesson Learnt:
•	Project Organization: I learnt how to structure a Python project to ensure clarity and maintainability. This also includes using. gitignore to keep sensitive files out of version control.



6. 
##Install Required Python Packages
Step:
•	I ran the following command to install the packages in requirements.txt: 
•	python -m pip install -r requirements.txt
Lesson Learnt:
•	Dependency Management: I learnt how to manage project dependencies with requirements.txt. This ensures all the required libraries are installed in one go.


7. 
##Write the Script to Fetch and Store Weather Info
Step:
•	I imported the required libraries:
•	import requests
•	import boto3
•	from dotenv import load_dotenv
•	import json
•	import os
•	I fetched weather data from the OpenWeather API and parsed it into JSON format.
•	I created an S3 bucket and uploaded the weather data as a JSON file.
Lesson Learnt:
•	API Data Handling: I learnt how to fetch and process data from an API and parse it into a format suitable for storage (JSON). This skill is essential for working with many types of external data sources.
•	AWS S3 Integration: I learnt how to interact with AWS S3 to upload files from Python using boto3. This is crucial for cloud storage automation.





8. 

##Run the Python Script
Step:
•	After writing the script, I navigated to the src folder and ran the following command: 
•	python weather_dashboard.py
Lesson Learnt:
•	Testing and Debugging: I learnt the importance of testing my code regularly to ensure it works as expected. Running the script helped verify that all components were correctly integrated.






9. 

##Final Check and Housekeeping
Step:
•	After running the script, the terminal should show: 
o	The S3 bucket is created successfully.
o	Weather data is displayed in the terminal and uploaded to the S3 bucket.
•	I went to my AWS console and checked the S3 bucket to confirm the presence of the uploaded files.
•	Once verified, I emptied the bucket and deleted it to prevent unnecessary charges.
Lesson Learnt:
•	Resource Cleanup: I learnt the importance of cleaning up cloud resources (like S3 buckets) after use to avoid unexpected costs. This is an important best practice when working with cloud services.


**Summary of Lessons Learnt**
1.	Working with APIs: I learnt how to fetch data from an external API (OpenWeather) and parse it into a format usable by my application.
2.	Environment Setup: I gained experience in setting up a Python development environment, including managing sensitive data with .env files.
3.	AWS CLI Configuration: I learnt how to configure AWS CLI with IAM credentials, allowing me to interact with AWS services such as S3 directly from the terminal.
4.	Folder Structure and Project Organization: I understood the importance of structuring my project correctly and using. gitignore to keep sensitive data secure.
5.	Python Package Management: I installed and managed dependencies using pip and requirements.txt to ensure my project runs smoothly.
6.	AWS S3 Integration: I learnt how to use the boto3 library to interact with AWS S3, including creating buckets and uploading files.
7.	Error Handling and Debugging: I gained skills in debugging common issues like missing credentials or AWS permission errors.
8.	Resource Cleanup: I learnt to clean up AWS resources after use to avoid unnecessary billing and to keep the project efficient.



By completing this project, I gained hands-on experience working with APIs, AWS S3, and Python, and learnt key cloud computing practices. I’m now equipped with the knowledge to integrate and automate cloud-based services in my future projects!
