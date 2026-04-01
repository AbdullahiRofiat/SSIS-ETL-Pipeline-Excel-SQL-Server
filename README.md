![ETL Dashboard Preview](./Screenshot_20260401_210048.png)

# SSIS ETL Pipeline: Excel → SQL Server

## Overview
Professional **ETL pipeline** built with **SQL Server Integration Services (SSIS)** to automate migration of **inventory data from Excel** to a **SQL Server database (`checkpoint_db`)**. Designed for **data integrity, scalability, and operational efficiency**.

## Tech Stack
- **ETL Tool:** SSIS  
- **Source:** Microsoft Excel  
- **Destination:** SQL Server (OLE DB)  
- **DB Management:** SSMS  

## Workflow
1. **Extract:** Retrieve Excel data using SSIS Excel Connection Manager.  
2. **Transform:** Use **Data Conversion** to align Excel types with SQL Server schema.  
3. **Load:** Insert validated data into `product` table via OLE DB Destination.  

## Key Achievements
- ✅ Migrated **33 inventory records** without errors.  
- ✅ Verified items like cutlery (*couteau, cuiller*), plates (*assiette*), and tablecloths (*nappe*).  
- ✅ Clean schema: `ProductID`, `Description`, `Quantity`—ready for queries & reports.  

## Business Impact
- Reliable Reporting: Avoided Excel-to-SQL type mismatches.  
- Operational Readiness: Supports **Full Load** with automated table cleanup.  
- Portable Design: Parameterized Excel paths & connection strings for multi-environment deployment.  

## Enhancements
- Automate table cleanup via SSIS **Execute SQL Task**.  
- Log bad rows to a **"Bad Data" file** for error handling.  
- Enable **logging & auditing** for row counts, execution times, and compliance tracking.  

 
