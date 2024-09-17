**Project Portfolio for AWS Data Analytics Platform**

**Project Title:** AWS Data Analytics Platform for Occupational Health and Safety Improvement at University Canada West

**1. Project Title**

AWS Data Analytics Platform for Enhancing Occupational Health and Safety Procedures

**2. Project Goal**

The primary objective is to improve the Occupational Health and Safety (OHS) procedures in the HR department at University Canada West (UCW) by analyzing workplace accidents data. The project leverages AWS services to provide data storage, analysis, and visualization to aid decision-making and performance enhancement.

**3. Objective of the Project**
- Streamline the HR department’s handling of workplace accidents by developing a secure, scalable data analytic platform.
-	Perform in-depth analysis of workplace accident reports and other related data.
-	Visualize insights to inform policies, reduce accidents, and improve workplace safety.

**Data Analytics Platform**

![Picture1](https://github.com/user-attachments/assets/2d1d1e62-5ded-4bdc-9f00-b1cb060eb306)


**5. Tools/Technology Used**

-	**AWS S3:** For scalable data storage.
-	**AWS Glue & Glue DataBrew:** For data extraction, cleaning, transformation, and pipeline implementation.
-	**AWS Athena:** For running SQL queries on data stored in S3.
-	**AWS EC2:** For hosting and publishing the results through a web server.
-	**AWS IAM & KMS:** For managing data security, access control, and encryption.
-	**AWS CloudWatch & CloudTrail:** For monitoring data, performance, and security metrics.
-	**Excel:** For data visualization and reporting.
  
**6. Project Timeline**

This project was completed in a phased approach over a period of 3 months. Each step, from data discovery to publishing and monitoring, was carefully planned and executed to ensure data security and accurate insights.

**7. Roles and Responsibilities**

- **Project Lead:** Managed the overall design and implementation of the AWS Data Analytics Platform, ensuring alignment with project goals.
-	**Data Engineer:** Handled data discovery, ingestion, and storage processes using AWS S3 and Glue.
-	**Data Analyst:** Analyzed workplace accidents data with AWS Athena and visualized results using Excel.
-	**Cloud Engineer:** Implemented data protection, governance, and monitoring using AWS IAM, KMS, CloudWatch, and CloudTrail.

**8. Detailed Project Description**

-	**Data Analytical Question Formulation:** The goal was to enhance OHSP performance by focusing on the parameter of workplace accidents.
  
 ![Picture2](https://github.com/user-attachments/assets/91b90d3c-b45e-46ca-a9fa-8dc3fe02f1ca)

-	**Data Discovery:** Dummy workplace accident report files were generated and downloaded as Excel files, forming the foundation of the analysis.
  
**Operational Dataset**

![Picture3](https://github.com/user-attachments/assets/b790f118-8445-467e-a653-58587f03c1e5)

-	**Data Storage Design:** Utilized a three-tier data structure in AWS S3 (Landing, Raw, Curated) for secure, scalable, and efficient storage.

**AWS S3 Storage Design**

 ![Picture4](https://github.com/user-attachments/assets/2bd66230-d224-4785-a32d-455b179d07c5)

-	**Data Ingestion:** Data from the operational environment was moved to the analysis environment (AWS S3).
  
**Ingested Dataset in S3**

 ![Picture5](https://github.com/user-attachments/assets/e292a453-b793-4af3-a22c-28afb3b197d8)

**Pipeline Design:** The ETL process was designed using AWS Glue and Glue DataBrew to clean and structure the data.

**AWS DataBrew – Cleaning and Structuring**

![Picture6](https://github.com/user-attachments/assets/e8271c81-fcad-4796-a45d-1bda62a4d8bf)
![Picture7](https://github.com/user-attachments/assets/0c04b07f-17f5-44ed-a413-bfc9f1b90b8c)

The Cleaned and Structured Dataset from AWS DataBrew is Stored in the S3 Raw Folder.

**ETL Diagram (Designed in draw.io)**
              
 ![Picture8](https://github.com/user-attachments/assets/9f6f1ff0-5ec7-435d-a8f3-fb17a64efce1)

The designed ETL is implemented in AWS Glue to analyze data. The resultant data is stored in Curated S3 Bucket.

**AWS Glue ETL Implementation**

![Picture9](https://github.com/user-attachments/assets/ca8b44b7-7fff-4d50-b2ac-7fc821eba25d)
![Picture10](https://github.com/user-attachments/assets/d78bb924-ee00-48fb-94b3-bfc2f15ad593)

- **Data Analysis:** AWS Athena was used to run SQL queries on the cleaned data stored in S3, generating insights into workplace accident trends and patterns.

**AWS Athena – Table and Database Creation**

 ![Picture11](https://github.com/user-attachments/assets/5bafa8a6-feb9-4ea2-aef1-c785ffea7cf4)

- **Data Visualization:** The analyzed data was exported to Excel for creating charts and dashboards that visualize accident trends, helping the HR team improve safety procedures.
  
The Analysed Data is visualized using Excel.
  
**Data Analysis Report**

![Picture12](https://github.com/user-attachments/assets/eaf14251-3786-4d25-a56e-f0853c98efd5)
 
- **Data Publishing:** Results were published on an AWS EC2 web server, making them accessible to stakeholders via web applications.

**AWS EC2 General Server**

![Picture13](https://github.com/user-attachments/assets/82dfde18-fc2a-429d-9e3a-d91659ea2c1a)

**AWS EC2 Web Server**

![Picture14](https://github.com/user-attachments/assets/b221f9ed-ee32-494a-b03d-ec4e89be6a48)

- **Data Protection, Monitoring & Governance:** CloudWatch dashboards were used for real-time monitoring, and CloudTrail ensured that API activity was tracked for security purposes. IAM and KMS managed access control and encryption to ensure secure handling of sensitive information (Data Protection).

**AWS Key Management Service**

<img width="468" alt="Picture15" src="https://github.com/user-attachments/assets/12155a70-5c31-4ae4-b88f-0e36fc0b54e3">

**S3 Bucket Encrypted using the KMS Key**

 ![Picture16](https://github.com/user-attachments/assets/d8357f5c-c09f-4316-821c-ea1cabf88bd9)

**Replication Rule**

![Picture17](https://github.com/user-attachments/assets/0dd4f667-b6d0-415f-adb5-e54fe2b222b9)

S3 Bucket backup is created using the Replication Rule.

**AWS Glue – Quality Check**

![Picture18](https://github.com/user-attachments/assets/a39dc514-78f5-4609-8a8b-83617e4225bb)

Quality of the dataset can be assessed using AWS Glue inbuild functions (Detect Sensitive Data and Evaluate Data Quality) and the passed data is stored in the S3 Trusted Folder.

**AWS Glue Workflow**

 ![Picture19](https://github.com/user-attachments/assets/a38ea477-0b66-4acf-accc-12796c4ca088)

To run the ETL weekly, a schedule is created and is called using a workflow.

**S3 Trust Folder**

![Picture20](https://github.com/user-attachments/assets/42dd354c-bf8c-4ede-9d6d-ee66ea4ed4ca)

**AWS CloudWatch Dashboard**

 ![Picture21](https://github.com/user-attachments/assets/4c5ad589-66ba-4e51-b79a-7885d09d217b)

CloudWatch is used to monitor expenses and usage. An alarm is also added to the dashboard when the cost exceeds the threshold.

**AWS CloudTrail**

![Picture22](https://github.com/user-attachments/assets/2cb97933-d6f2-4db9-b372-51aecf38d83d)

AWS CloudTrail saves the user in the S3 Bucket to track the API activity to prevent security breaches.

**8. Challenges and Solutions**
- Challenge: Handling large datasets from the operational environment and ensuring data integrity during ingestion.
  - _Solution:_ Used AWS Glue to automate the ETL process, ensuring efficient and accurate data transformation.
- Challenge: Managing data security while providing accessibility to relevant stakeholders.
  - _Solution:_ Implemented AWS IAM and KMS for strict access controls and data encryption in transit and at rest.
- Challenge: Cost monitoring during the project’s runtime.
  - _Solution:_ Set up CloudWatch alarms to monitor and alert when costs exceed predefined thresholds.
   
**9. Results/Outcomes**

- Enhanced Data Analysis: Through AWS Athena, the analysis provided actionable insights into workplace accidents, revealing trends and identifying areas for improvement in OHS procedures.
- Improved Safety Practices: Visualized data helped HR refine policies, ultimately reducing the number of workplace accidents and improving overall employee safety.
- Scalable and Secure Data Platform: The use of AWS services ensured the platform is scalable, secure, and easily adaptable to future analytical needs.
  
**10. Conclusion**

The AWS Data Analytics Platform provided a comprehensive solution to analyze workplace accidents, driving improvements in UCW’s Occupational Health and Safety procedures. By utilizing various AWS services, the project achieved reliable, secure, and scalable data management, along with insightful analysis that informed key decision-making in the HR department. The successful deployment of this platform can serve as a template for other departments seeking similar improvements through data-driven insights.

