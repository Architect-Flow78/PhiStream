# PhiStream
Data Quality & Streaming ETL: Building PhiStream in Python for Infinite Datasets

Why load 100GB of data into RAM when you can evaluate it as a continuous, stable flow? 

Most standard Data Quality tools require massive memory overhead to profile and clean datasets. I built PhiStream — a lightweight, streaming Data Quality Engine in Python designed to process infinite datasets on minimal hardware. 

Instead of treating data validation as a static block, I approach it as a continuous phase cycle (where the absolute unit of a closed cycle is π=1). By enforcing strict non-intersection rules (acting as a topological Φ operator), the engine instantly bifurcates anomalies from clean data into isolated streams. The primary pipeline never breaks, and the system maintains absolute stability regardless of input size.

⚙️ Core Engineering Features:
• Streaming Mathematics: Integrated Welford's Algorithm to calculate running mean, variance, and standard deviation on the fly, entirely bypassing MemoryError bottlenecks.
• Probabilistic Cardinality: Built a custom HyperLogLog (HLL) sketch to estimate distinct elements across massive datasets with a near-zero memory footprint.
• Dynamic Rule Engine: Evaluates complex constraints (pandas.eval) chunk-by-chunk without hardcoding schemas.
• Zero-Dependency Architecture: Built purely on pandas/numpy for high-performance anomaly detection in IoT sensor data and financial time-series.

I am open to feedback, pull requests, and discussions on optimizing algorithmic complexity. 

#DataQuality #ETL #DataEngineering #Python #StreamingData #AnomalyDetection #DataScience #BigData #QuantitativeAnalysis
