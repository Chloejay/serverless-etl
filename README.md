# severless-etl

## Data Engineering Severless ETL

#### Tools:
AWS + <a href="https://dbeaver.io/">Dbeaver</a> <img src="https://dbeaver.io/wp-content/uploads/2015/09/beaver-head.png" height=80 width=80>

#### Steps to get started 
1. Set up RDS-MySQL
2. Create <a href="https://docs.aws.amazon.com/IAM/latest/UserGuide/id_roles.html">IAM role</a>, <a href="https://aws.amazon.com/vpc/">VPC</a>, Security group, config inbound port
(set to `Anywhere` when having `connection timeout` issue (both for RDS and Redshift))
3. Set up Redshift Cluster
4. Connect to Local Database Mysql, use DBeaver GUI, install connection jar and test connection
5. Data modeling to build relationship database

#### ETL
6. Workflow (data source: ecommerce data from Kaggle)
<ul>
<li>RDS MySQL: Transactional data</li>
<li><a href="https://aws.amazon.com/datapipeline/">AWS Data Pipeline</a></li>
<li>S3 Data Lake: CSV saved in S3</li>
<li>AWS Lambda Trigger: S3 files trigger <a href="https://docs.aws.amazon.com/lambda/latest/dg/welcome.html">Lambda Functions</a></li>
<li>AWS Glue: PySpark, transform and load data from S3 files</li>
<li>Redshift DWH: Perform ETL and load data to Redshift</li>
</ul>

#### BI (ad-hoc analysis)
7. AWS Athena
8. QuickSight for Dashboard

#### Resources
<a href="https://towardsdatascience.com/aws-glue-and-you-e2e4322f0805">AWS Glue and You </a>

#### Further materials
<a href="https://github.com/hasbrain/data-engineer-roadmap">Data Engineering Roadmap</a>