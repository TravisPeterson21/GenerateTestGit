---
description: Write ETL code, populate and validate data in Generate
---

# Task 4.2

## **Overall Description of the Task**

During this task, an ETL Developer will use the completed ETL checklist (Activity 3.1.1) for the selected data set and write the code to move and transform the data from the SEA’s source system into the CEDS structured tables in Generate. Once the code is written, and data is successfully moved, the ETL Developer and SEA subject matter experts will check the data quality and validate that the data is accurate. When data quality issues are found, the ETL Developer will go back and modify the ETL code to correct the issue until the data are deemed accurate. Errors found in the legacy reporting process or files should be documented for use by the ETL developer and SME during Activity: 4.2.3 Compare Generate results with legacy ED_Facts_ data and resolve data quality issues.

## **Activities**

### **4.2.1 Write ETL code and complete Source System Reference Data Mapping**

SEA-specific SQL code must be written to move the data from the identified SEA source systems into the Staging Tables. All Generate data migrations are accomplished by running SQL Server Stored Procedures, which perform the ETL. They can be run either from the Generate Web-based application’s “Data Store” or directly through SQL Server. The ETL Developer(s) should approach this work by creating a single stored procedure for each data domain (such as Child Count, Discipline, Exiting, etc.) that migrates data for that domain into the staging tables. Reference the ETL checklist for that domain to get a list of the tables/fields that need to be populated to create each ETL.

The Generate SQL table **`Staging.SourceSystemReferenceData`** (SSRD) must be updated with the complete set of values for all categorical fields for each school year. This process is called the Source System Reference Data Mapping and should be completed by an ETL developer. The information for this table comes from the ETL checklist and is used in the data migration stage to determine how source system option set values correspond to CEDS option set values. The Generate Implementation Guide contains the step-by-step instructions for completing this process.

{% hint style="success" %}
<mark style="color:green;">**CEDS Tip**</mark>

If a data migration is run, and no entries are available in the SSRD table for the most current school year, the prior school year’s data will automatically populate the current year’s table. This table should be reviewed every year!
{% endhint %}

### **4.2.2 Migrate data**

Migrations move data from one database to another and are run independently. Plan to run the data migration from the CEDS Warehouse into Generate according to a schedule that corresponds to the ED_Facts_ file submission due dates and ensures source database(s) and data are available[3](https://ciidta.communities.ed.gov/#superscript%203). To protect the integrity and security of production data, all tasks performed during an ETL process/data migration should be done in the test or development environment first to eliminate errors or bugs that could have a negative impact on production data. Confirm with the IT department that no database maintenance is being performed or planned during the data migration

The Generate User Guide provides instructions for assigning access to individuals on the project team who are responsible for executing the data migrations through the Generate website. The Generate User Guide also has detailed instructions for how to use the Generate website to execute the stored procedures in each segment of the data migration.

Once the data migration is complete, confirm that the process worked as expected. Generate contains validation tools to assist ETL developers in verifying that data have successfully migrated across the Generate data layers. Errors and issues captured in the first stages of data migration are logged in the **`Staging.ValidationErrors`** table. The logs can be explored from the SQL Server database. ETL Developers should review the table and communicate any questions about the data with the project team. ETL checklists may need to be modified based on the results of the data migration through discussions between subject matter experts (SMEs) and ETL Developers. SMEs should make any changes to the ETL checklists and follow the governance process for the project team to re-finalize the document. The team will repeat the steps in the data migration activity for each ED_Facts_ data domain each year.

### **4.2.3 Compare Generate results with legacy ED**_**Facts**_** data and resolve data quality issues**

During the matching process, an ETL developer will pre-load previously reported ED_Facts_ data into tables on the Generate test/development server. The ETL developer will then run the data migrations in Generate on the same test/development server for the same school year as the previously reported ED_Facts_ data. They will complete this activity during the project phase to validate the ETL code. As a best practice, this activity should be performed once for each ED_Facts_ data domain during the project, but does not need to be repeated annually.

{% hint style="info" %}
#### <mark style="color:blue;">**Toolkit Tip**</mark>

Be sure that the ETL developers are practicing good code management and saving their ETL code versions using the established version control process identified in 4.3.1.
{% endhint %}

Once the data are available in the Generate reports, the ETL developer can identify any variances in the aggregate counts between the Generate report tables and the pre-loaded, previously reported ED_Facts_ data. The ETL developer will investigate possible root causes for any variances and identify individual student records that comprise the variances to look for patterns that could be affecting data quality. SMEs can also use the CIID Data Review Checklist to ensure the original files and Generate-produced ED_Facts_ files meet basic data quality standards. This tool should be used every time an ED_Facts_ file is produced from Generate to ensure the minimum data quality standards are addressed.

All data quality results should be shared with the project team who will then meet to review the results and identify solutions or possible next actions. Often, ETL code needs to be adjusted, and any changes that affect the ETL checklist should be documented in the Change Log-ETL worksheet that is part of each ETL checklist.  The changes should be run through the established governance process for sign-off. This data quality review process will repeat until the report values are accepted by SMEs.

Once the ETL developers receive final sign-off of approval from the SMEs and according to any exiting data governance processes for your SEA, the ETL code is considered final for that school year. The code can then be moved to the production environment and properly saved in that location. Be sure to store the finalized ETL Checklist in the appropriate location and reconfirm the staff assigned to maintain the document. The completed ETL is now ready for use to produce the future ED_Facts_ file(s) at the start of the next reporting cycle!

## **Resources**

* [**Generate Implementation Guide**](https://ciidta.communities.ed.gov/#communities/pdc/documents/16672)
* [**Generate Use Guide**](https://ciidta.communities.ed.gov/#communities/pdc/documents/17667)
* [**CIID Data Review Checklist**](https://ciidta.communities.ed.gov/#communities/pdc/documents/21449)
