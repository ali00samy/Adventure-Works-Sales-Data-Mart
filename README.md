# Sales Data Mart

## Project Overview
The **Sales Data Mart** project is designed to build a data mart for sales-related data using SSIS (SQL Server Integration Services). The project includes ETL (Extract, Transform, Load) processes to populate dimension and fact tables. The ETL processes handle both full and incremental data loads, ensuring that the data mart remains up-to-date and optimized for reporting and analytics.

## Objectives
- Create a sales data mart with structured dimension and fact tables.
- Implement ETL processes for:
  - **Full Loads**: Initial data population.
  - **Incremental Loads**: Updating data while maintaining existing records.

## Tools & Technologies
- **SSIS (SQL Server Integration Services)**: For designing and managing ETL workflows.
- **SQL Server Management Studio (SSMS)**: For database management and query execution.
- **AdventureWorks 2019 Database**: Sample dataset used as the source for this project.

## ETL Packages
The project includes the following SSIS packages:
1. **Dim Customer ETL.dtsx**: Populates the Customer dimension table.
2. **Dim Date ETL.dtsx**: Populates the Date dimension table.
3. **Dim Product ETL.dtsx**: Populates the Product dimension table.
4. **Dim Territory ETL.dtsx**: Populates the Territory dimension table.
5. **Fact Sales ETL.dtsx**: Full load of sales data into the Fact table.
6. **Fact Sales ETL - Incremental Load.dtsx**: Handles incremental loading of sales data.

## Steps to Replicate
### Prerequisites
1. Install **SQL Server** and **SSIS** (SQL Server Data Tools).
2. Download and restore the **AdventureWorks 2019** database.
3. Set up Azure SSIS Integration Runtime (optional, if using Azure resources).

### Step-by-Step Instructions
1. **Clone the Repository**:
   - Clone this project repository to your local machine.

2. **Configure Connection Managers**:
   - Update the `DistDB.conmgr` and `SourceDB.conmgr` connection managers with your database credentials and server details.

3. **Load SSIS Packages**:
   - Open the SSIS project in Visual Studio.
   - Review the ETL packages for customization if needed.

4. **Execute ETL Packages**:
   - Start with the dimension packages (`Dim Customer`, `Dim Date`, etc.) to populate the dimension tables.
   - Execute the **Fact Sales ETL** package for the full load.
   - Use the **Fact Sales - Incremental Load ETL** package for periodic updates.

5. **Validate the Data**:
   - Verify the data in the data mart tables by running SQL queries in SSMS.

## Sample Data
This project uses the **AdventureWorks 2019** database as its primary data source. You can download it from [Microsoft's official page](https://learn.microsoft.com/en-us/sql/sample/worldwide-importers/wideworld-importers-oltp-database?view=sql-server-ver16).

## Features
- Automates the creation of sales-related dimension and fact tables.
- Supports full and incremental data loads.
- Leverages SSIS's robust ETL capabilities for efficient data transformation.
- Compatible with Azure SSIS for cloud-based deployments.

## Future Enhancements
- Add error handling and logging mechanisms to the ETL workflows.
- Include additional dimensions or measures for advanced analytics.
- Implement SSRS reports for visualizing the data mart insights.
