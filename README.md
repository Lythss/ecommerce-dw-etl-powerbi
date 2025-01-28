# E-commerce Data Warehouse Project 🏪

## Overview 🎯
This project implements a comprehensive data warehouse solution for an e-commerce platform, featuring ETL processes with Talend, data storage in SQL Server, and analytics through Power BI. The solution follows a constellation schema design and includes robust data management practices including SCD (Slowly Changing Dimensions) implementation.

## Architecture 🏗️
- **ETL Tool**: Talend Open Studio
- **Database**: SQL Server
- **Visualization**: Power BI
- **Data Formats**: JSON and CSV input files

## Features ⭐
- Data splitting functionality (JSON/CSV)
- Comprehensive ETL pipeline implementation
- Constellation schema with multiple fact tables
- SCD (Slowly Changing Dimensions) management
- Dedicated data marts for Sales and Inventory
- Performance optimization through indexing and partitioning
- Role-based access control
- GDPR compliance measures

## Project Structure 📁
```
ecommerce-dw-etl-powerbi/
├── data_splitter/
│   └── split_script.py
├── talend_jobs/
│   ├── extraction/
│   ├── transformation/
│   └── loading/
├── sql/
│   ├── schema/
│   ├── dimensions/
│   ├── facts/
│   └── optimization/
├── power_bi/
│   ├── sales_mart/
│   └── inventory_mart/
└── docs/
```

## Implementation Steps 📝

### 1. Data Preparation 🔄
- Execute data splitter script to generate JSON and CSV formats
- Validate data integrity and format consistency

### 2. ETL Implementation 🔧
- **Extraction**: Connect to CSV and JSON data sources
- **Transformation**: 
  - Data cleaning and standardization
  - SCD implementation (Types 1, 2, and 3)
  - Business rules application
- **Loading**: Structured data loading into SQL Server

### 3. Data Warehouse Structure 🏢
#### Dimensions
- DateDimension
- ProductDimension (with SCD)
- CustomerDimension (with SCD)
- SupplierDimension
- ShipperDimension

#### Fact Tables
- SalesFact
- InventoryFact

### 4. Data Marts 📊
- **Sales Data Mart**: Sales analysis and customer insights
- **Inventory Data Mart**: Stock management and supplier performance

### 5. Analytics & Visualization 📈
#### Sales Analysis
- Sales trends
- Top performing products
- Customer segmentation
- Discount impact analysis
- Shipping performance

#### Inventory Analysis
- Stock levels
- Inventory availability
- Supplier performance
- Demand forecasting

## Setup Instructions 🚀
1. Clone the repository
2. Configure Talend Open Studio with provided job files
3. Execute SQL scripts for schema creation
4. Import Power BI templates
5. Configure security roles and permissions

## Security 🔒
- Role-based access control implementation
- GDPR compliance measures
- Data encryption standards
- Audit logging

## Performance Optimization ⚡
- Implemented indexes on frequently queried columns
- Table partitioning for improved query performance
- Optimized ETL processes with sub-jobs

## Requirements 💻
- Talend Open Studio
- SQL Server 2019+
- Power BI Desktop
- Python 3.8+

## Contributing 🤝
1. Fork the repository
2. Create a feature branch
3. Commit changes
4. Push to the branch
5. Create a Pull Request

## License 📄
MIT License

Copyright (c) 2024

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
