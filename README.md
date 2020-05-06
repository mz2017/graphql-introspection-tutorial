# SCI Custom Advisor For Lenovo Fast Start Project (EBA version)

This project was created using custom-advisor-base of July 16, 2018.

## Steps to deploy this project in IBM Cloud for a SCI tenant

1. Create a SQL database schema for log messages. Pre-seed necessary data. Related SQL can be found in file: `src/main/resources/db_schema_mysql.sql`.
2. Create a new Watson Assistant (Watson Conversation Service) instance for the advisor [Optional, can share with other instances if needed]. The latest WCS model was exported to file: `src/main/resources/WCS-Lenovo-FS-20180924.json`.
3. Acquire necessary credentials to be used for SCI, services, etc., such as SCI API credentials, database credentials, Watson service credentials, etc.
4. Create required custom data objects (such as WorkOrderTask, ProcessSal, etc.). Refer to the [Lenovo SDK project](https://git.ng.bluemix.net/sci-services/customers/sci-sdk-1.1.0-lenovo) for more details.
5. Update related service credentials in config.yml file (or use the version specific for the environment)
6. Build the project with right AppName for the deployment
7. Deploy the new build to IBM Cloud
8. Load required core object files through UI
9. Load custom object data through data upload utility. A reference mapping file is provided here: `src/main/resources/upload-mapping.xml`, and all data files used for development are stored in [box folder](https://ibm.ent.box.com/folder/53002256729).
10. Test custom advisor questions

## Distribution

This utility is intended for IBM Watson Supply Chain Insight (WSCI) Lab service team internal use only. Do not share with external parties without getting permission from the WSCI Lab team first.
