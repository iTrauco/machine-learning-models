# readme

### Env Setup / Config  D
***Apache Spark & Jupyter Notebook***

System
- Ubuntu 20.04 LTS

#### Prereqs
1. Download Anaconda installer for debian `bash Anaconda-latest-Linux-x86_64.sh` 

2. create conda env and install packages(tensorflow, pyspark, jupyter-notebook, scipy)
 
```conda create tensorflow```
```conda activate tensorflow```
```conda install tensorflow jupyter```

3. System Wide
Install Java SDK with ```sudo apt-get install default-jdk ```

Install Scala w/ ```sudo apt-get install scala```

### BigQuery, GCS
```
gcloud services enable dataproc.googleapis.com \
  compute.googleapis.com \
  storage-component.googleapis.com \
  bigquery.googleapis.com \
  bigquerystorage.googleapis.com
```
create storage bucket
```
REGION=us-central1
BUCKET_NAME=<your-bucket-name>

gsutil mb -c standard -l ${REGION} gs://${BUCKET_NAME}
```
[install biquery to spark streaming connector .jar](https://github.com/GoogleCloudDataproc/spark-bigquery-connector?tab=readme-ov-file)
