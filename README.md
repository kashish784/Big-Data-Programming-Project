# A Scalable Big Data Predictive Analytics Platform for Peak Passenger Demand Forecasting Using PySpark and London's GTFS Dataset

## Project Overview

This project presents a scalable Big Data predictive analytics platform developed to forecast peak passenger demand using London's General Transit Feed Specification (GTFS) dataset. The solution demonstrates an end-to-end Big Data analytics pipeline, integrating distributed data processing, feature engineering, machine learning, database management, and data visualisation within the Apache Spark ecosystem.

The project has been implemented as part of the **Big Data Programming Project** module and demonstrates the practical application of PySpark, Spark SQL, and machine learning techniques for intelligent transport analytics.

---

## Business Problem

Urban transport operators generate massive volumes of operational data every day. Despite the availability of these datasets, extracting meaningful insights for demand forecasting remains challenging due to their volume and complexity.

This project addresses this challenge by developing a scalable predictive analytics platform capable of estimating passenger demand proxies using operational characteristics extracted from London's GTFS dataset.

The solution supports transport authorities and smart city planners in making evidence-based decisions regarding:

- Peak-hour service planning
- Resource allocation
- Operational efficiency
- Service scheduling
- Smart transport management

---

## Objectives

The primary objectives of this project are:

- Develop a scalable Big Data analytics pipeline using PySpark.
- Process large-scale GTFS transport datasets containing millions of records.
- Engineer operational features representing passenger demand.
- Compare multiple machine learning regression algorithms.
- Evaluate predictive performance using appropriate regression metrics.
- Store processed data and model outputs within a relational database.
- Demonstrate distributed computing concepts using Apache Spark.

---

## Dataset

The project uses the London GTFS dataset.
Link: https://data.bus-data.dft.gov.uk/timetable/download/gtfs-file/london/

### GTFS Files

- agency.txt
- routes.txt
- trips.txt
- stop_times.txt
- stops.txt
- calendar.txt
- calendar_dates.txt
- frequencies.txt
- feed_info.txt

---

## Dataset Scale

| Dataset | Records |
|----------|---------:|
| Routes | 1,063 |
| Trips | 456,521 |
| Stops | 24,782 |
| Stop Times | 17,257,720 |
| Processed Records | 8,178,359 |

The project substantially exceeds the assignment requirement of processing at least **100,000 records**, demonstrating genuine Big Data processing.

---

## Technologies Used

- Python
- Apache Spark
- PySpark
- Spark SQL
- Spark MLlib
- SQLite
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Plotly
- Google Colab

---

## Machine Learning Models

The following regression algorithms were implemented and compared:

- Linear Regression
- Decision Tree Regressor
- Random Forest Regressor
- Gradient Boosted Tree Regressor
  

---

## Feature Engineering

The predictive model uses operational features derived from GTFS data, including:

- Hour of operation
- Peak-hour indicator
- Timepoint indicator
- Average stops per trip
- Route frequency
- Estimated headway
- Segment duration
- Stop activity (demand proxy)

---

## Evaluation Metrics

Models were evaluated using:

- Root Mean Squared Error (RMSE)
- Mean Absolute Error (MAE)
- Coefficient of Determination (R²)
- Explained Variance
- Training Time

---

## Best Performing Model

| Model | RMSE | MAE | R² |
|-------|------:|------:|------:|
| Gradient Boosted Tree | 372.19 | 145.13 | 0.716 |

The Gradient Boosted Tree achieved the highest predictive performance and was selected as the final model.

---

## Big Data Techniques Demonstrated

The project demonstrates multiple distributed computing concepts, including:

- Spark DataFrames
- Distributed transformations
- Spark SQL
- Lazy evaluation
- Partitioning
- Dataset caching
- Execution plan analysis
- Window functions
- Distributed machine learning
- Pipeline-based modelling

---

## Database Integration

SQLite was used to:

- Store model performance metrics
- Store processed transport data
- Demonstrate secure parameterised SQL queries
- Enable persistent storage of analytical outputs

---

## Project Workflow

```
GTFS Dataset
      │
      ▼
PySpark Data Ingestion
      │
      ▼
Data Validation
      │
      ▼
Data Cleaning
      │
      ▼
Feature Engineering
      │
      ▼
Spark SQL Analytics
      │
      ▼
Machine Learning Models
      │
      ▼
Model Evaluation
      │
      ▼
SQLite Storage
      │
      ▼
Visualisation
      │
      ▼
Passenger Demand Prediction
```

---

## Project Structure

```
Project/
│
├── BigData_Programming_Project.ipynb
├── itm_london_gtfs.zip
├── london_gtfs_analytics.db
├── README.md
└── report/
```

---

## Installation

Clone the repository:

```bash
git clone https://github.com/kashish784/Big-Data-Programming-Project.git
```

Navigate to the project directory:

```bash
cd Project
```

Install the required packages:

```bash
pip install pyspark findspark pandas numpy matplotlib seaborn plotly
```

---

## Running the Project

1. Open the notebook in Google Colab or Jupyter Notebook.
2. Upload the `itm_london_gtfs.zip` dataset to the working directory.
3. Run all notebook cells sequentially.
4. Review the generated visualisations and model performance outputs.
5. Inspect the SQLite database for stored analytical results.

---

## Outputs

The notebook produces:

- Data quality reports
- Statistical summaries
- Correlation analysis
- Peak vs off-peak demand analysis
- Feature importance plots
- Model comparison tables
- SQLite database outputs

---

## Key Findings

- Over **17 million** operational records were processed using distributed computing.
- Feature engineering successfully generated demand proxy indicators from GTFS operational data.
- Ensemble learning methods outperformed Linear Regression.


---

## Future Improvements

Potential extensions include:

- Integration of real-time Automatic Vehicle Location (AVL) data
- Weather and disruption data integration
- Deep Learning models
- Graph Neural Networks
- Spark Structured Streaming
- Cloud deployment
- MLOps pipeline implementation
- Real-time passenger demand prediction

---
