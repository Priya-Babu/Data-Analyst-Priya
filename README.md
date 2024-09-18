**Descriptive Analysis**

**Project Description:**

Descriptive Analysis of Workplace Accidents to Improve Occupational Health and Safety (OHS) Procedures

**Project Title:**

Enhancing Occupational Health and Safety Procedures using AWS Data Analytics at University Canada West (UCW)

**Objective:**

The primary goal of this project is to conduct a descriptive analysis of workplace accidents at UCW aimed at improving Occupational Health and Safety procedures. This analysis aims to summarize key characteristics of reported workplace accidents, identify trends, and generate actionable insights that can inform the HR department’s safety policies and accident prevention measures.

  **Descriptive Metric**

 ![Picture1](https://github.com/user-attachments/assets/d7394010-e6d6-4c5d-91d7-fdd6cd9c3ce9)

  **Data Analytics Platform**
 
![Picture2](https://github.com/user-attachments/assets/bde766c5-913f-4b46-83a2-b33cb86ced21)

**Dataset:**
The dataset used for analysis includes workplace accident reports generated using dummy data. The dataset contains the following key features:

The dataset includes OHS incident reports from University Canada West, with the following key features:

- Incident_ID: Unique identifier for each incident
- Date_of_Incident: Date when the incident occurred
- Incident_Type: Type of incident (e.g., slip, trip, fall, equipment-related)
- Severity: Severity level of the incident (e.g., minor, moderate, severe)
- Department: The department in which the incident occurred
- Employee_ID: Identification number for the employee involved
- Description: A brief description of the incident
- Action_Taken: Actions taken following the incident
- Hours_Worked: Hours worked before the incident
- Days_Lost: Number of workdays lost due to the incident
  
**Methodology:**

**1.	Data Collection and Preparation:**
- Load the dummy workplace accident report data using AWS S3 for storage and AWS Glue for data cleaning and preparation.
- Perform data cleaning with AWS Glue DataBrew to address missing values, correct data types, and standardize report formats.

  **AWS S3 Storage Design**

![Picture3](https://github.com/user-attachments/assets/e5d9257d-8645-48e8-aa8f-529dc064f559)

  **Ingested Dataset in S3**

 ![Picture4](https://github.com/user-attachments/assets/d3e9de7f-b720-4419-9f5c-f09d199e46b8)
  
  **AWS DataBrew – Cleaning and Structuring**
 
 ![Picture5](https://github.com/user-attachments/assets/0711f20b-9dca-40b9-a0e3-d56145ea8e79)

 ![Picture6](https://github.com/user-attachments/assets/032f0678-d099-4af7-9f69-d00bccc13062)
 
The Cleaned and Structured Dataset from AWS DataBrew is Stored in the S3 Raw Folder.

  **AWS Glue ETL Implementation**
  
 ![Picture7](https://github.com/user-attachments/assets/8f776a6d-7c20-4353-a824-9511c87b924d)

![Picture8](https://github.com/user-attachments/assets/bb3c7b79-58b7-4008-bdd9-7386adfe8cf2)

The Analyzed Dataset from AWS Glue is Stored in the S3 Curated Folder.

**2.	Descriptive Statistics:**

- Calculated summary statistics for key variables, including:
    - Total number of incidents per department
    - Average severity of incidents
    - Number of incidents by type
    - Number of workdays lost per department
- Queried incident data in AWS Athena, which allowed SQL-based analysis directly on S3 data.
  
**3.	Data Visualization:**

Use Excel and AWS Athena for analysis and create visual representations of findings.

  **AWS Athena – Table and Database Creation**

![Picture9](https://github.com/user-attachments/assets/584fde0d-f79c-46f1-9e91-e11fc469b61f)

  **Data Analysis Report**
 
![Picture10](https://github.com/user-attachments/assets/e0c99c7b-1187-4218-a5c0-b637ef5d5fab)

**4.	Data Governance and Security:**

- Managed data governance using AWS Glue's data classification and evaluation features.
- Implemented security protocols with AWS IAM and AWS KMS for data protection.
- Set up backups and recovery processes to safeguard incident records.
  
  **AWS Key Management Service**

 ![Picture11](https://github.com/user-attachments/assets/b1d47b5d-f838-436e-86db-8c9cef92734f)

  **S3 Bucket Encrypted using the KMS Key**

![Picture12](https://github.com/user-attachments/assets/90a8a3d3-09c8-48fe-842f-ecdcf749ec30)

S3 Bucket backup is created using the Replication Rule.

  **Replication Rule**
  
 ![Picture13](https://github.com/user-attachments/assets/d6f8a511-1969-4067-94e1-ab3daa41f707)

  **AWS Glue – Quality Check**

![Picture14](https://github.com/user-attachments/assets/a2d8ec5b-ebcd-4e69-a1f1-43ca208afc1e)

The dataset's quality can be assessed using AWS Glue inbuild functions (Detect Sensitive Data and Evaluate Data Quality), and the passed data is stored in the S3 Trusted Folder.

  **AWS Glue Workflow**

![Picture15](https://github.com/user-attachments/assets/e3b756b7-c425-4a7f-8692-eff83eb3be90)

A schedule is created to run the ETL weekly, and it is called using a workflow.

  **S3 Trust Folder**

![Picture16](https://github.com/user-attachments/assets/4a479632-6f7c-4493-822f-7e4c6fb7cd7c)

  **AWS CloudWatch Dashboard**

![Picture17](https://github.com/user-attachments/assets/8fb16baa-c404-4f23-b82e-11bddb3d0556)

CloudWatch is used to monitor expenses and usage. An alarm is also added to the dashboard when the cost exceeds the threshold.

  **AWS CloudTrail**

![Picture18](https://github.com/user-attachments/assets/05fdcfe1-a1e4-4228-b900-4160557acc3b)

AWS CloudTrail saves the userlog in the S3 Bucket to track the API activity to prevent security breaches.

**5.	Insights and Findings:**

The analysis revealed key trends and areas for improvement:

- High-Risk Departments: Certain departments (e.g., Facilities, Maintenance) showed a higher frequency of severe incidents.
- Incident Timing: Incidents tend to occur towards the end of shifts, correlating with increased fatigue.
- Common Causes: The most common incident types were slips, trips, and falls, which led to significant downtime.
  
**6.	Recommendations:**
- Training and Awareness: Conduct targeted safety training in high-risk departments.
- Fatigue Management: Implement break schedules to reduce fatigue-induced accidents.
- Safety Audits: Increase the frequency of safety audits in departments with higher incidents.
- Preventive Measures: Install slip-resistant flooring and improve signage in areas prone to slips and falls.
  
**Tools and Technologies:**

- AWS S3 for secure and scalable data storage.
- AWS Glue and DataBrew for data cleaning, structuring, and governance.
- AWS Athena for SQL querying and analysis.
- Excel for data visualization and reporting.
- AWS EC2 for data publishing and web hosting.
- AWS CloudWatch and CloudTrail are used to monitor data usage and security.
  
**Deliverables:**

- A comprehensive report detailing the methods, findings, and recommendations for improving OHS procedures.
- Data visualizations to highlight key safety risks and trends.
- A presentation summarizing actionable insights and recommendations for the HR and Safety departments.
  
This descriptive analysis project aims to clearly understand workplace accident patterns, enabling UCW to enhance Occupational Health and Safety procedures and create a safer working environment for all staff and departments.

