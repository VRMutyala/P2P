Bronze Layer - Employees

Objective -This notebook ingests Employees master data from the Landing Volume into the Bronze Delta table.

## Activities

- Read CSV using explicit schema
- Perform source validation
- Execute data quality checks
- Detect duplicate records
- Store duplicate records in Audit schema
- Add audit metadata
- Load Bronze Delta table
- Validate load
