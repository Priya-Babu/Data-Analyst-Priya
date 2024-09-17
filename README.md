Project Portfolio for AWS Data Analytics Platform
Project Title: AWS Data Analytics Platform for Occupational Health and Safety Improvement at University Canada West
1. Project Title
AWS Data Analytics Platform for Enhancing Occupational Health and Safety Procedures
2. Project Goal
The primary objective is to improve the Occupational Health and Safety (OHS) procedures in the HR department at University Canada West (UCW) by analyzing workplace accidents data. The project leverages AWS services to provide data storage, analysis, and visualization to aid decision-making and performance enhancement.
3. Objective of the Project
•	Streamline the HR department’s handling of workplace accidents by developing a secure, scalable data analytic platform.
•	Perform in-depth analysis of workplace accident reports and other related data.
•	Visualize insights to inform policies, reduce accidents, and improve workplace safety.
Data Analytics Platform
https://github.com/Priya-Babu/Data-Analyst-Priya/blob/fe713df8e0da1db51a5fd2ec9c0482763fdc051a/images/Picture1.png
4. Tools/Technology Used
•	AWS S3: For scalable data storage.
•	AWS Glue & Glue DataBrew: For data extraction, cleaning, transformation, and pipeline implementation.
•	AWS Athena: For running SQL queries on data stored in S3.
•	AWS EC2: For hosting and publishing the results through a web server.
•	AWS IAM & KMS: For managing data security, access control, and encryption.
•	AWS CloudWatch & CloudTrail: For monitoring data, performance, and security metrics.
•	Excel: For data visualization and reporting.
5. Project Timeline
This project was completed in a phased approach over a period of 3 months. Each step, from data discovery to publishing and monitoring, was carefully planned and executed to ensure data security and accurate insights.
6. Roles and Responsibilities
•	Project Lead: Managed the overall design and implementation of the AWS Data Analytics Platform, ensuring alignment with project goals.
•	Data Engineer: Handled data discovery, ingestion, and storage processes using AWS S3 and Glue.
•	Data Analyst: Analyzed workplace accidents data with AWS Athena and visualized results using Excel.
•	Cloud Engineer: Implemented data protection, governance, and monitoring using AWS IAM, KMS, CloudWatch, and CloudTrail.
7. Detailed Project Description
•	Data Analytical Question Formulation: The goal was to enhance OHSP performance by focusing on the parameter of workplace accidents.
 
•	Data Discovery: Dummy workplace accident report files were generated and downloaded as Excel files, forming the foundation of the analysis.
Operational Dataset
 

•	Data Storage Design: Utilized a three-tier data structure in AWS S3 (Landing, Raw, Curated) for secure, scalable, and efficient storage.
AWS S3 Storage Design
 

•	Data Ingestion: Data from the operational environment was moved to the analysis environment (AWS S3).
Ingested Dataset in S3
 
•	Pipeline Design: The ETL process was designed using AWS Glue and Glue DataBrew to clean and structure the data.
AWS DataBrew – Cleaning and Structuring
 
 
The Cleaned and Structured Dataset from AWS DataBrew is Stored to S3 Raw Folder.
ETL Diagram (Designed in draw.io)
              


The designed ETL is implemented in AWS Glue to analyze data. The resultant data is stored in Curated S3 Bucket.
AWS Glue ETL Implementation
 
 
•	Data Analysis: AWS Athena was used to run SQL queries on the cleaned data stored in S3, generating insights into workplace accident trends and patterns.

AWS Athena – Table and Database Creation
 
•	Data Visualization: The analyzed data was exported to Excel for creating charts and dashboards that visualize accident trends, helping the HR team improve safety procedures.
The Analysed Data is visualized using Excel.
Data Analysis Report
 
•	Data Publishing: Results were published on an AWS EC2 web server, making them accessible to stakeholders via web applications.
AWS EC2 General Server
 
AWS EC2 Web Server
 
•	Data Protection, Monitoring & Governance: CloudWatch dashboards were used for real-time monitoring, and CloudTrail ensured that API activity was tracked for security purposes. IAM and KMS managed access control and encryption to ensure secure handling of sensitive information (Data Protection).
AWS Key Management Service
 
S3 Bucket Encrypted using the KMS Key
 
S3 Bucket backup is created using Replication Rule.
Replication Rule
 
AWS Glue – Quality Check
 
Quality of the dataset can be assessed using AWS Glue inbuild functions (Detect Sensitive Data and Evaluate Data Quality) and the passed data is stored in the S3 Trusted Folder.
AWS Glue Workflow
 
To run the ETL weekly, a schedule is created and is called using a workflow.
S3 Trust Folder
 
AWS CloudWatch Dashboard
 
To monitor the expense and usage, CloudWatch is used. An alarm is also created and added to the dashboard to alarm when the cost exceeds the threshold.
AWS CloudTrail
 
AWS CloudTrail is used to save the userlog in the S3 Bucket to track the API activity to prevent security breaching.
8. Challenges and Solutions
•	Challenge: Handling large datasets from the operational environment and ensuring data integrity during ingestion.
o	Solution: Used AWS Glue to automate the ETL process, ensuring efficient and accurate data transformation.
•	Challenge: Managing data security while providing accessibility to relevant stakeholders.
o	Solution: Implemented AWS IAM and KMS for strict access controls and encryption of data both in transit and at rest.
•	Challenge: Cost monitoring during the project’s runtime.
o	Solution: Set up CloudWatch alarms to monitor and alert when costs exceeded predefined thresholds.
9. Results/Outcomes
•	Enhanced Data Analysis: Through AWS Athena, the analysis provided actionable insights into workplace accidents, revealing trends and identifying areas for improvement in OHS procedures.
•	Improved Safety Practices: Visualized data helped HR refine policies, ultimately reducing the number of workplace accidents and improving overall employee safety.
•	Scalable and Secure Data Platform: The use of AWS services ensured the platform is scalable, secure, and easily adaptable to future analytical needs.
10. Conclusion
The AWS Data Analytics Platform provided a comprehensive solution to analyze workplace accidents, driving improvements in UCW’s Occupational Health and Safety procedures. By utilizing various AWS services, the project achieved reliable, secure, and scalable data management, along with insightful analysis that informed key decision-making in the HR department. The successful deployment of this platform can serve as a template for other departments seeking similar improvements through data-driven insights.

