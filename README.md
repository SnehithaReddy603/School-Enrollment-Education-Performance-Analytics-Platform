# School Enrollment & Education Performance Analytics Platform

## Project Overview
A comprehensive data analytics solution for education departments to analyze enrollment trends, student performance, and support data-driven decision making in educational planning.

## Business Problem
Education departments face challenges with:
- Enrollment data scattered across multiple disconnected files
- Time-intensive manual reporting processes
- Limited visibility into student enrollment patterns
- Difficulty identifying at-risk students and capacity planning issues

## Solution Architecture
This platform provides an automated, end-to-end analytics solution that processes education data through a structured pipeline and delivers actionable insights through interactive dashboards.

## Technology Stack
- **Data Processing**: Python, Pandas, PySpark
- **Workflow Orchestration**: Apache Airflow, Custom Scheduler
- **Cloud Analytics**: Databricks
- **Data Storage**: CSV, Parquet files
- **Visualization**: Power BI
- **Version Control**: Git

## Project Structure
```
education_analytics/
├── data/
│   ├── raw/                    # Source enrollment data
│   └── powerbi_data/          # Dashboard-ready exports
├── medallion_architecture/
│   ├── bronze/                # Raw data ingestion
│   ├── silver/                # Cleaned and validated data
│   └── gold/                  # Business analytics and KPIs
├── airflow_dags/              # Workflow orchestration
├── databricks_notebooks/      # Cloud analytics notebooks
├── medallion_pandas.py        # Main ETL pipeline
├── spark_analytics.py         # PySpark distributed processing
├── pipeline_scheduler.py      # Automated scheduling
└── export_powerbi.py         # Dashboard data export
```

## Key Features

### Data Processing Pipeline
- **Bronze Layer**: Raw data ingestion with validation
- **Silver Layer**: Data cleaning, standardization, and quality checks
- **Gold Layer**: Business aggregations and analytics-ready datasets

### Analytics Capabilities
- Year-over-year enrollment trend analysis
- School performance benchmarking and classification
- Student demographic distribution analysis
- At-risk student identification and dropout prediction
- Regional and district-level comparisons

### Automation & Orchestration
- Scheduled daily data processing
- Error handling and retry mechanisms
- Data quality validation and monitoring
- Automated dashboard data refresh

## Installation & Setup

### Prerequisites
```bash
pip install pandas numpy pyspark schedule pyarrow
```

### Running the Analytics Pipeline

#### Complete Pipeline Execution
```bash
python medallion_pandas.py
```

#### PySpark Distributed Analytics
```bash
python spark_analytics.py
```

#### Automated Scheduling
```bash
python pipeline_scheduler.py
```

#### Power BI Data Export
```bash
python export_powerbi.py
```

## Data Schema
- **school_name**: Educational institution identifier
- **region**: Geographic district or area
- **academic_year**: Academic year (2020-2024)
- **grade**: Student grade level
- **gender**: Student gender classification
- **enrollment_count**: Number of enrolled students
- **performance_score**: Academic performance metric (0-100)
- **attendance_rate**: Student attendance percentage

## Analytics Outputs

### Enrollment Trends
- Total enrollment by academic year and region
- Year-over-year growth rate calculations
- At-risk student identification and counts

### School Performance Analysis
- Performance tier classification (Excellent/Satisfactory/Needs Improvement)
- Average performance scores by institution
- Dropout risk percentage calculations

### Demographic Insights
- Gender distribution analysis by grade level
- Enrollment patterns across academic years
- Regional demographic comparisons

## Power BI Integration
The platform exports analytics data in Power BI compatible formats:
- `enrollment_trends.csv` - Trend analysis data
- `school_performance.csv` - School benchmarking data
- `demographics.csv` - Student demographic insights

### Dashboard Connection Steps
1. Open Power BI Desktop
2. Select Get Data > Text/CSV
3. Navigate to the `powerbi_data/` directory
4. Import the exported CSV files
5. Create visualizations and reports

## Business Impact
- **Process Automation**: Reduces manual reporting effort by 80%
- **Data-Driven Insights**: Enables evidence-based educational planning
- **Early Intervention**: Identifies at-risk students for timely support
- **Resource Optimization**: Supports capacity planning and resource allocation

## Technical Implementation
The solution implements a medallion architecture pattern for data processing:
1. **Ingestion**: Raw data validation and storage
2. **Transformation**: Data cleaning and standardization
3. **Analytics**: Business logic and KPI calculations
4. **Export**: Dashboard-ready data preparation

## Monitoring & Logging
- Pipeline execution logging with timestamps
- Data quality validation checkpoints
- Error handling and notification system
- Automated retry mechanisms for failed processes

## Future Enhancements
- Real-time data streaming capabilities
- Machine learning models for predictive analytics
- Advanced visualization with interactive dashboards
- Integration with student information systems

## Project Team
- **Developer**: K.Snehitha
- **Institution**: Vellore Institute Of Technology
- **Project Type**: Capstone Project

## License
This project is developed for educational purposes as part of capstone program.
