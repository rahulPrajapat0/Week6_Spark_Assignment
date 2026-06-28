==== Week6 Spark Assignment ====

--> Objective

The objective of this assignment is to understand Apache Spark architecture and perform efficient data processing using PySpark. The assignment demonstrates reading data, applying transformations, filtering records, handling schemas, building a data pipeline, and storing processed data in optimized formats.


--> Technologies Used

- Python
- PySpark
- Google Colab
- Apache Spark


--> Dataset

- Superstore Dataset (`data.csv`)

--> Tasks Performed

- Read CSV dataset
- Understand Spark Architecture
- Understand Lazy Evaluation
- Understand DAG (Directed Acyclic Graph)
- Print Schema
- Filter Data
- Select Required Columns
- Rename Columns
- Cast Data Types
- Add New Columns
- Handle Null Values
- Perform Transformations and Actions
- Perform Wide Transformation using GroupBy
- Understand Shuffle
- Understand Predicate Pushdown
- Build Data Pipeline (Read → Transform → Filter → Write)
- Save Processed Data as CSV
- Save Processed Data as Parquet

=== Data Pipeline ===

--> 
(read → transform → filter → write)


## Brief Performance Insights

- Spark uses "Lazy Evaluation", meaning transformations are executed only when an action (such as `show()` or `count()`) is called.
- Spark builds a Directed Acyclic Graph (DAG) to optimize the execution plan before processing data.
- Parquet provides better performance than CSV because it is a columnar storage format and supports compression.
- Predicate Pushdown allows Spark to read only the required data from Parquet files, reducing I/O operations.
- GroupBy is a wide transformation that causes Shuffle, where data moves across partitions.
- Spark DataFrames improve performance through query optimization and efficient memory management.
- Avoid using `collect()` on large datasets because it transfers all data to the Driver and may cause memory issues.
- Prefer `show()`, `filter()`, `select()`, and other distributed DataFrame operations for better performance.



=== Spark Architecture ===

Apache Spark consists of the following components:

- Driver Program – Creates SparkSession and coordinates the application.
- Cluster Manager – Allocates resources for execution.
- Executors – Execute tasks and return results to the Driver.


--> Output

The processed data is generated in:

- CSV Format
- Parquet Format

--> Conclusion

This assignment demonstrates the complete Spark data processing workflow using PySpark. It covers Spark architecture, data transformations, schema handling, filtering, performance optimization concepts, and building an end-to-end data pipeline for efficient big data processing.
