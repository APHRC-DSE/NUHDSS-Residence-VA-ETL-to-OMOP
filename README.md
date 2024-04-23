# NUHDSS-Residence-VA-ETL-to-OMOP
This repository describes the ETL process for Nairobi Urban HDSS ETL to OMOP and how to visualize in ATLAS

It contains code, and information to extract, transform and load ALPHA source data from Nairobi Urban HDSS (NUHDSS) to a local instance OMOP database. 

## Software needed

- White rabbit
- Rabbit in a hat
- Usagi
- DBMS(Postgres, MySQL, SQLite etc)
- R
  
### STEPS FOLLOWED

1. Data cleaning and Exploratory data analysis.
2. Data Profiling and Mapping. 
3.Vocabulary Mapping. 
4. Data Mapping and ETL spec Implementation Guides: Rabbit in a hat, Athena and Usagi tools were used to create mappings from source data to OMOP terminologies. Athena is an online vocabulary mapping tool while Usagi can be downloaded and used offline.

5. Develop ETL (Extract Transform Load) pipeline: We used PostgreSQL to write SQL scripts for transforming source codes to OMOP terminologies. Penataho can equally be used for ETL

6. Data Quality Assurance: OHDSI library for quality assurance of the CDM 'DataQualityDashboard' was installed and run against the OMOP database. Visit [OHDSI DQD GitHub](https://github.com/OHDSI/DataQualityDashboard) for more information on DQD documentation and installation.

7. Generating Aggregated (Results tables) data for Atlas using Achilles R library by OHDSI for data characterization tool. This is an automated process using codes developed by [OHDSI](https://github.com/OHDSI/Achilles)

8. Visualization in Atlas : Aggregated data(results tables), OMOP tables and vocabulary tables were integrated with Atlas and webAPI


Visit [OHDSI GitHub](https://github.com/OHDSI/WebAPI/wiki/CDM-Configuration) for more information.
