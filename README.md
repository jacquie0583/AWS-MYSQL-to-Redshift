# AWS-Integration of multiple platforms-to-Redshift 

<p align="center"> <img width="100" height="100" src="RDS.png">       <img width="200" height="100" src="Red.png">
</p>
<p align="center">
    <img width="200" height="100" src="Glue.jpg">      <img width="100" height="50" src="Crawler.png"> <img width="50" height="50" src="DC.png">    <img width="200" height="100" 
   src="lambda.png">
</p>


## A project that I’ve worked on, independently, that I am very passionate about...
Constructing pipelines to migrate data from MySQL workbench-RDS, Oracle and salesforce to a central location, Redshift.  Upon completion, allowing different teams to have access to varying databases

## Solution: Completed in multiple stages.  
### MYSQL-to-Redshift       <p align="center">   <img width="200" height="100" src="mysql.png"> </p> 

      First, MySQL workbench required JDBC and terraform connection.  
      Followed by a crawler who would gather the schema and transfer it to a data catalogue.  
      Once the foundation was laid in the catalogue, glue ETL jobs, visual ETL, interactive notebooks,
      lambda used to facilitate the transfer.  
      To assure the data was updated, a pipeline including crawlers, triggers, and glue jobs were used(diagram). 
      Monitoring and maintenance were done daily with CloudWatch, resource usage, Job type breakdown, 
      Worker type breakdown, Job runs timeline.

<p align="center">
  <img width="900" height="400" src="Orchastration pipeline.png">
</p>

### Oracle to Redshift
<p align="center">
  <img width="200" height="50" src="oracle2.png">
</p>
      Oracle migration took a different means of transfer. 
      The tables first needed to be modified to MATERIALIZED VIEW format 
      and then transferred to Redshift.  
      This was accomplished by exporting and then copying. Example of M.V.

<p align="center">
  <img width="400" height="1000" src="Code.png">
</p>

### Salesforce to Redshift
<p align="center">
  <img width="200" height="100" src="sf.png">
</p>
      Salesforce migration was carried out through Appflow.  
      Flow setup started with connecting to source, mapping source fields 
      to destination then activating flows.  Other necessary tasks included:
            setting up KMS key, Field mappings stored in S3 as parquet format, 
            triggers set at on demand. Monitored through CloudWatch metrics.
      
      Setting up IAM roles and establishing policies allowed for different teams to 
      have access to varying databases.

<p align="left">
   <img width="100" height="50" src="Appflow2.png">
</p>
<p align="right">
   <img width="800" height="300" src="Appflow.png">
</p>

#### Where did you find the solutions?  
      Researching different architectural solutions for the various sources 
      and the alterations in schema design to allow for acceptable conversions to Redshift.
 
#### Why did the solution work?
      Organization, collaboration with multiple teams, excellent research skills
 
#### How were you sure the solution worked?
      Data Validation records displayed results consistent with the original database.

### Cloud Watch Dispayed in Organized Fashion in IDE
<p align="center">
  <img width="200" height="100" src="cloudwatch.png">
</p>
      In my role, I built a connection to the log files in serverless data integration service.
      To achieve this, I accessed the log files, organized them by table(operation), 
      built a pipeline to display the results on Redshift allowing for immediate 
      access to status of the tables. 

<p align="center">
   <img width="800" height="400" src="Access Logs Easily.png">
</p>

