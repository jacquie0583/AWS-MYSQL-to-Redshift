# AWS-MYSQL-to-Redshift 
## A project that I’ve worked on, independently, that I am very passionate about...
Constructing pipelines to migrate data from MySQL workbench-RDS, Oracle and salesforce to a central location, Redshift.  Upon completion, allowing different teams to have access to varying databases

## Solution: 
    Completed in multiple stages.  First, MySQL workbench required JDBC and terraform connection.  Followed by a crawler who would gather the schema and transfer it to a data     
    catalogue.  Once the foundation was laid in the catalogue, glue ETL jobs, visual ETL, interactive notebooks, lambda used to facilitate the transfer.  To assure the data was 
    updated, a pipeline including crawlers, triggers, and glue jobs were used(diagram). 
    Monitoring and maintenance were done daily with CloudWatch, resource usage, Job type breakdown, Worker type breakdown, Job runs timeline.
