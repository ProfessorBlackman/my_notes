## Data import:
This works with csv data.
### Methods for Importing data:
- **Data Import Wizard:** For importing data in both standard and custom objects. Can import up to 50_000 records at a time.
- **Data Loader:** Supports up to 5 million records from either files or database.

**Use the Data Import Wizard When:**
- You need to load less than 50,000 records.
- The objects you need to import are supported by the wizard.
- You don’t need the import process to be automated.

**Use Data Loader When:**
- You need to load 50,000 to five million records. If you need to load more than 5 million records, we recommend you work with a Salesforce partner or visit the [AppExchange](http://appexchange.salesforce.com/) for a suitable partner product.
- You need to load into an object that is not supported by the Data Import Wizard.
- You want to schedule regular data loads, such as nightly imports.

**Before importing any data, prepare the data using the following Salesforce data import guidelines.** 

- Use your existing software to create an export file. You'll use this exported data file to now _import_ the data into Salesforce.
- Clean up the import file for accuracy and consistency. This involves updating the data to remove duplicates, delete unnecessary information, correct spelling and other errors, and enforce naming conventions.
- Compare your data fields with the Salesforce fields you can import into, and verify that your data will be mapped into the appropriate Salesforce fields. You might need to fine-tune the mapping before starting the import. For details, see [Field Mapping for Data Sources](https://help.salesforce.com/apex/HTViewHelpDoc?id=field_mapping_for_other_data_sources_and_organization_import.htm&language=en_US) in the online help.
- Make any configuration changes required in Salesforce to handle the imported data. For example, you might need to create new custom fields, add new values to picklists, or temporarily deactivate workflow rules.

## Export Data
### Methods of data export:
- **Data Export Service**—an in-browser service, accessible through the Setup menu. It allows you to export data manually once every 7 days (for weekly export) or 29 days (for monthly export). You can also export data automatically at weekly or monthly intervals. Weekly exports are available in Enterprise, Performance, and Unlimited Editions. In Professional Edition and Developer Edition, you can generate backup files only every 29 days, or automatically at monthly intervals only.
- **Data Loader**—a client application that you must install separately. It can be operated either through the user interface or the command line. The latter option is useful if you want to automate the export process, or use APIs to integrate with another system.