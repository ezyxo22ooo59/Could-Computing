# Could-Computing

## Final Project: YouTube Trending Videos Analysis and Prediction Summary

(See implementation report for more detail)

### Background and Business Plan:
This project, undertaken by Group 7 in the APAN5450 Cloud Computing course at Columbia University, focuses on analyzing and predicting trends in YouTube videos. The primary aim is to provide businesses with insights into viewer preferences, helping them tailor advertisements based on trending content in different countries. The analysis explores key factors influencing viewer behavior, such as likes, dislikes, publish time, comment counts, and view counts.

### Data Source and Description:
The dataset used for this project is sourced from Kaggle and contains YouTube Trending Videos Statistics. It comprises 2.79 GB of data, including JSON files and CSV files across 11 regions worldwide. For this analysis, the team utilized data from six regions: the USA, Canada, France, Russia, South Korea, and Japan.

### Team Responsibilities:
Xiaoting Teng: VPC setup and EC2 instance setup with key pairs
Yiwen Yin: Upload and restore data in S3
Keqi Yu: Data cleaning in AWS Glue
Chang Yuan: Data integration from S3 and configuration
Emily Ziyi Xiao: Classification in SageMaker

### Cloud Architecture Description:
The project's cloud infrastructure includes several AWS services:
- Amazon EC2: Planned for future use with Flask applications to facilitate model deployment.
- Amazon Virtual Private Cloud (VPC): Ensures granular security control over instance and subnet traffic.
- Amazon Simple Storage Service (S3): Utilized for cost-effective data storage, backup, and restoration.
- Amazon Glue: Employed for serverless data integration, simplifying data cleaning and visualization.
- Amazon SageMaker: Used to build, train, and deploy machine learning models for predicting audience behaviors and view counts.

### ETL Process:
Upload the dataset to S3.
Perform data cleaning using AWS Glue.
Generate ML models using SageMaker.
Conduct output analysis.

### Security Plan:
The security plan encompasses:
- IAM Role: Managing permissions through default LabRole, with plans to create a specific role for future use.
- Public Subnets in EC2: Allowing access and analysis from various platforms.
- NAT Gateway: Ensuring secure access from private subnets to the internet.

### Cost Analysis:
The estimated cost of the project includes an upfront cost of $29.78 and a monthly cost of $55.10, covering expenses for VPC, EC2 instances, S3 storage, AWS Glue, and SageMaker.

### Success Criteria:
- Quantitative: Achieving cost-effectiveness and secure data import for analysis and prediction.
- Qualitative: Ensuring data quality and meaningful analysis to understand social reality through viewer behaviors.

### Implementation and Results:
#### The project implementation involved:
Setting up VPC, EC2 instances, subnets, and security groups.
Uploading and accessing datasets in S3, followed by data cleaning in AWS Glue and analysis in SageMaker.
Generating visualizations and insights into trending videos.

#### Data Cleaning:
The data cleaning process involved connecting to the S3 bucket from AWS Glue, merging data files, converting date columns, and deleting abnormal data, resulting in a cleaned dataset with 1,011,848 rows and 27 columns.

#### Analysis Results:
- Identified most viewed, liked, and disliked videos on the trending page.
- Developed bar plots to visualize top-performing videos.
- Determined the optimal publish time for YouTube videos, with the best range being from 8 AM to 7 PM and the top hour being 9 AM.
- Implemented machine learning models (SVM and Logistic Regression) to predict view counts, with SVM achieving a slightly better RMSE result of 0.1906 compared to LR's 0.2527.

### Conclusion:
This project successfully demonstrates the use of AWS cloud services to analyze and predict trends in YouTube videos. The insights generated can help YouTubers and businesses optimize their content strategy and target advertisements effectively. The approach and methodology outlined in this project can be replicated by others to conduct similar analyses and gain valuable audience insights.
