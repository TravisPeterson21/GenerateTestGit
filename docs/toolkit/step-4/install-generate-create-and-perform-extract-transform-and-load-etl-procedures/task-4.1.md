---
description: Install Generate Software
---

# Task 4.1

## **Overall Description of the Task**

The Generate tool consists of two main technical components - a Structured Query Language (SQL) database and a web application. The Generate installation package includes the full Common Education Data Standards (CEDS) data structure although the Generate application uses only a portion of CEDS necessary for EDFacts reporting. CEDS includes a broad scope of over 1,700 data elements spanning much of the P-20W spectrum (pre-kindergarten through workforce education) and provides a context for understanding the standards’ interrelationships and practical utility. While this toolkit was developed to support work on IDEA EDFacts files, SEAs can use Generate to produce any EDFacts files by repeating the steps in this toolkit for each additional data domain. In addition to supporting the existing federal reporting requirements, Generate supports the analysis and comparison of aggregate statistics. A full list of EDFacts file specifications in Generate are available on the [**ED**_**Facts**_** Communities website**](https://edfacts.communities.ed.gov/#program/generate).

The Generate web application uses the data in the CEDS Data Warehouse and Reports tables to create ED_Facts_ and related reports. Generate also contains Toggle, an important administrative feature that documents and inputs meta-data needed for Generate, including, for example, whether the SEA uses Developmental Delay as a disability category and for what ages. Instructions on the full functionality of Toggle are in the Generate User Guide.

## **Activities**

### **4.1.1 Ensure proper code and database management procedures are in place**

Most information technology (IT) departments have documented or standard procedures and server environments for ensuring code management and protecting data according to standard IT practices. The project team should consult with IT management to how the following technical standards will be addressed:

* Generate and the underlying CEDS data warehouse are installed in at least two environments: a staging/test/development environment that is not intended for data use but will be used by IT staff for testing, and a production or main environment that will be used for reporting.
* Database back-ups and recovery procedures are documented and completed on a regular basis. The back-up copies of the databases may be needed if a server crashes or unwanted changes are applied to the system. This proactive approach can save staff time in rebuilding the system should an adverse event occur.
* A source control management (SCM) system such as Team Foundation Server (Microsoft TFS), Bitbucket, or GitHub or alternative approach is adopted. If an SCM is available, set up a repository for tracking SEA specific code that is used to move the data from SEA system(s) to the CEDS SQL tables. For this project, document the appropriate details (repository name, location, list of files tracked, etc.) and ensure the project team can access this information. While not required for use of Generate, an SCM is highly recommended for maintaining code over time, avoiding version control issues, and recovering code in case of emergency.

### **4.1.2 Install Generate**

Read and review the latest Generate Installation and Configuration Guide. Send the guide to database administrators (DBAs) and other technical staff to review. The project team should confirm the date and server locations where the SQL database and web application will be installed. The technical staff will use the instructions for installing the SQL database and web application in the _**Generate Installation and Configuration Guide**_[_**2**_](https://ciidta.communities.ed.gov/#superscript%202).

## **Resources**

* [**Generate Use Guide**](https://ciidta.communities.ed.gov/#communities/pdc/documents/16673)
* [**Generate Installation and Configuration Guide**](https://ciidta.communities.ed.gov/#communities/pdc/documents/16673)

\
