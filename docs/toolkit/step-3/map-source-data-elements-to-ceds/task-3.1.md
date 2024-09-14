---
description: Document data systems and elements associated with the data integration effort
---

# Task 3.1

## **Overall Description of the Task**

The project team will use the _ETL Checklist_ to create a data dictionary of all data elements and data sources required for EDFacts submissions, including detailed information on each element. The _ETL Checklist_ is a technical requirements document that provides the information ETL developers need to write the ETL. It provides clear and complete requirements on where the source data reside; and the rules for extracting, transforming, and loading the data into the CEDS Data Warehouse. The _ETL Checklist_ is also the official documentation for communicating within SEAs what data are used for reporting to EDFacts. EDFacts Coordinators and SMEs will use _ETL Checklists_ to communicate and officially track the business rules used for ED_Facts_ reporting

Upon completion of this task, the project team will have created and organized a list of all source elements needed for ED_Facts_ reporting and their attributes.  If issues arise during this process that cannot be addressed quickly and easily, consider using the Issue Tracker tool to document and keep track of items for future resolution.

## **Activities**

### **3.1.1 Locate or create a data dictionary for needed source systems and document metadata in the **_**ETL Checklist**_

To document source systems, SEAs may use existing data dictionaries such as system user guides, data manuals, or technical specifications. For each source system, SMEs identified in _Activity 2.1.2 Document Data Stewards and Systems_, will locate or create lists of required elements from each source

If no data dictionary exists, project teams can leverage the _CEDS Align_ template and online Align tool to create and manage a data dictionary or use the ETL Checklist as the basis for a data dictionary

Using the information from the data dictionary, begin entering metadata into the _ETL Checklists_. Download the _ETL Checklist(s)_ that are in the project’s scope from the [CIID website](https://ciidta.communities.ed.gov/#communities/pdc/documents/17074). Take some time to review the checklists and familiarize yourself with the tabs and columns. Navigate to the ETL tab within the workbook and scroll to the right (Row 2, CEDS Element Details, Columns R and S) to see the specific CEDS elements needed to align to your source data dictionary. The CEDS element metadata from the _ETL checklist_ will provide context to the SME in creating or locating items in the source system’s data dictionary.

Enter the following source metadata for each data source/set and the associated data elements from the data dictionary in the _ETL Checklists_ (Columns A-M):

* Common Name (System Name)
* Technical Name
* Database Name
* Schema Name
* Table Name
* Column Name
* Element Name
* Element Definition
* Data Type
* Length
* Option Set
* Option Set Description
* Data Steward

Review and update your data dictionary and _ETL Checklists_ on a regular basis, at least annually, reflecting any federal or SEA data element or definition changes. Each year, ED_Facts_ publishes release notes specifying changes in ED_Facts_ reporting requirements; these will need to be updated in each _ETL Checklist_.

### **3.1.2 Complete the Source-to-CEDS Alignments**

After the data dictionary is located or created, and metadata has been entered into the _ETL Checklist_, the project team including data stewards, will review the _ETL Checklist(s)_ to ensure all elements needed to address the scope defined in Step 1 are included in the dictionary. The team will also define and document the selection criteria (Column N) and transformation rules (Column O) in the _ETL Checklist._

For each _ETL Checklist_, schedule a team meeting to review the data dictionary information completed in the previous activity. This team should include a SME and technical staff who understand intended uses for the data elements in the data system in question. Use the ETL tab in the _ETL Checklist_ to review and confirm the data dictionary information and record the transformation rules. Data stewards will verify that they have addressed all discrepancies and verify that the proposed logic makes sense

Establish procedures and assign someone, e.g., data stewards or those responsible for the data, to maintain the ETL documentation to keep it current. Document the assignment in the _Roles and Responsibilities_ tab of the _Data Integration Project Planner_. As federal reporting requirements change, new data elements will be added or removed, and keeping this information up to date helps to ensure the data remains accurate.

## **Resources**

* [**ETL Checklist**](https://ciidta.communities.ed.gov/#communities/pdc/documents/17074)
