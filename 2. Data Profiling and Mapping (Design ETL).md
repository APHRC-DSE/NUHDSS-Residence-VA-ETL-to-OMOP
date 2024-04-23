It is important to clearly separate the design of the ETL from the implementation of the ETL. Designing the ETL requires extensive knowledge of both the source data,
as well as the CDM. Implementing the ETL on the other hand typically relies mostly on technical expertise on how to make the ETL computationally efficient. 

Two closely-integrated tools have been developed to support the ETL design process: White Rabbit, and Rabbit-in-a-Hat
## 1. White Rabbit

To initiate an ETL process on a database you need to understand your data, including the tables, fields, and content.
This is where the White Rabbit tool comes in. White Rabbit is a software tool to help prepare for ETLs of longitudinal healthcare databases into the OMOP CDM.
White Rabbit scans your data and creates a report containing all the information necessary to begin designing the ETL.
All source code and installation instructions, as well as a link to the manual, are available on GitHub.
### Process Overview
The typical sequence for using the software to scan source data:
 - Set working folder, the location on the local desktop computer where results will be exported.
 - Connect to the source database or CSV text file and test connection.
 - Select the tables of interest for the scan and scan the tables.
 - White Rabbit creates an export of information about the source data.

## NUHDSS White Rabbit Scan report 
![NUHDSS Scan report](https://github.com/Chebet254/Images-/blob/main/nuhdss%20scan%20report.png)

## 2. Rabbit in a Hat
   
Rabbit-In-a-Hat is designed to read and display a White Rabbit scan document. White Rabbit generates information about the source data
while Rabbit-In-a-Hat uses that information and through a graphical user interface to allow a user to connect source data to tables and columns within the CDM.
Rabbit-In-a-Hat generates documentation for the ETL process, it does not generate code to create an ETL.
### Process Overview
The typical sequence for using this software to generate documentation of an ETL:
- Scanned results from WhiteRabbit completed.
- Open scanned results; interface displays source tables and CDM tables.
- Connect source tables to CDM tables where the source table provides information for that corresponding CDM table.
- For each source table to CDM table connection, further define the connection with source column to CDM column detail.
- Save Rabbit-In-a-Hat work and export to a MS Word document.
  
## NUHDSS Rabbit in a hat Mapping report 
- Source data Mapping Approach to CDMV5.4
![image](https://github.com/Chebet254/NUHDSS-Residence-VA-ETL-to-OMOP/assets/93149259/7564ec84-f11d-4f4a-8b6a-404d158ed9af)

- Person table Mapping
  ![image](https://github.com/Chebet254/NUHDSS-Residence-VA-ETL-to-OMOP/assets/93149259/23f24cb3-58fe-407f-8c1e-a83a147b5eaa)
## General Flow of an ETL
![Alt text](https://ohdsi.github.io/TheBookOfOhdsi/images/ExtractTransformLoad/flowOfEtl.png)
