# Working with Big Data - Spark Customer Churn

## Installations
- pandas==0.23.3
- numpy==1.12.1
- pyspark
- scikit-learn==0.19.1
- seaborn
- matplotlib

## Project Motivation
- This project presented an opportunity for me to work with Big Data tools, i.e. Spark. I will be working specifically with the PySpark API
- Also, as I am dealing with distributed systems, It is a good segue to experiment with setting up with clusters in the cloud.
  - Although It was recommended that I were to utilise Amazon Web Services (AWS)'s EMR for setting up the Hadoop clusters, I have gravitated towards the Google Cloud Platform (GCP). The equivalent to AWS's EMR is GCP's Dataproc.
  - Dataproc allows seamless and easy deployment of distributed clusters, and I will be working on the GCP platform throughout the whole project.

## Blog
- [Medium post](https://medium.com/@jiaren.kjr/sparkify-customer-churn-7e0041106cd8)

## Acknowledgements and references
- [Spark Docs](https://spark.apache.org/docs/3.1.1/)
- [Spark by Example](https://sparkbyexamples.com/)
- [Quora - Discussion over High ROC_AUC but low F1](https://www.quora.com/What-does-it-mean-to-have-high-AUC-but-low-F1-score)
- [GCP - Dataproc Docs](https://cloud.google.com/dataproc/docs)
  - [Introduction to Cloud Dataproc: Hadoop and Spark on Google Cloud](https://www.cloudskillsboost.google/focuses/672?catalog_rank=%7B%22rank%22%3A2%2C%22num_filters%22%3A0%2C%22has_search%22%3Atrue%7D&parent=catalog&search_id=16800999)
  - [Provisioning and Using a Managed Hadoop/Spark Cluster with Cloud Dataproc (Command Line)](https://www.cloudskillsboost.google/focuses/3398?catalog_rank=%7B%22rank%22%3A3%2C%22num_filters%22%3A0%2C%22has_search%22%3Atrue%7D&parent=catalog&search_id=16800999)

## Further improvements
1. I have only worked on a small subset (128MB) of the entire dataset (12GB) due to time constraints. An opportunity for subsequent improvement would be to:
  - Improve on my preprocessing and modelling pipelines.
  - Revisit code optimization (since there is a larger emphasis of focus for big data)
2. Experiment with utilizing HDFS (Hadoop Distributed File System) instead of retrieving data directly from my GCP Cloud Storage bucket.
  - One of the largest constraints of Big Data is reliance on latency of our Network to have our files transmitted between clusters easily. 
  - However, when utilising Cloud services, it is unlikely that there would be impedence on the latency since the CPU/RAM and Storage facilities will most likely be contained within the same data center.
  - Still it would be interesting to experiment with HDFS, so that I can utilise my clusters for Storage and not just CPU/RAM processing.
3. Improvements over feature engineering
  - This project is pretty open-ended, and I guess it's good since its more synonymous with real life where our data isn't entirely processed for modelling right away.
  - Other aspects of features that can be explored include, genres of music, and some columns which I have discarded (i.e. `userAgent` which shows the browser being used).
  - It may be interesting to find out whether individual's preference of browsers would impact churn
4. Improve understanding of bottlenecks when writing code for distributed systems
  - E.g. understanding how to optimize code to avoid repetitions
