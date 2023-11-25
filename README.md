# Azure-Data-Factory-Pipeline
I had created a Project of Azure Data Factory in which  we can downloads a .CSV file into Azure Blob Data lake Gen2 and then load it in SQL Database when triggered in the data pipeline

here is more detailed Description
I'm excited to share a project that I recently built using Azure Data Factory (ADF) to streamline the process of downloading CSV files, storing them in Azure Data Lake Storage, and loading them into a SQL Server database for easy querying.

The project starts by directly downloading the CSV file from an HTTP server using Azure Data Factory's HTTP connector. The downloaded file is then automatically stored in Azure Data Lake Storage (Blob storage)

Now we need to create a table in the SQL database by running a SQL query.
and this table header name & columns should match with the CSV file (Schema should be same)

Next, using Azure Data Factory's copy tool, the CSV file is loaded into the SQL Server database. This process can be easily scheduled or triggered using Azure Data Factory's built-in scheduling and event-based triggers, ensuring that the data is always up-to-date and readily available for analysis.

You can Further then Connect Power-Bi or other Visualization tool to get insights

Here is a Step by Step process-

Step1- First you need to have a subscription in Azure to start (you can get one by signing up free account)

Step2-Create Storage account & select Hierarchy namespace during creation, Then Create a container Blob with an empty folder

Step3-Create Azure data Factory, & Azure SQL database Server

Step4-Create a database in SQL server & then create table (Table schema should match with source file CSV)

Step5- Run Azure data factory studio and then create linked services & Datasets for HTTP server, Blob storage, SQL database

Step6- Create Data Pipeline and use the Copy tool twice

Step7-First copy will be from HTTP server to Blob storage

Step8- Second Copy will be from Blob storage to Azure SQL database table

Step9- Run validation & debug & then finally trigger

Step10- Run (Select * Table name) as SQL query and see if you got the output if Yes then you have successfully deployed & run the Pipeline

Overall, I'm thrilled with the power and flexibility of Azure Data Factory and the ease with which it can be used to create robust data integration and processing pipelines.
