# MSDS_434_ModuleFour

gcloud config set project project_id

mkdir data

cp round_data.csv data

cd data

gsutil mb gs://bucketname    # create bucket

gsutil cp ~/data/round_data.csv gs://bucketname/round_data.csv

bq mk datasetname        # load dataset

bq load --autodetect --source_format=CSV datasetname.table_name gs://bucketname/round_data.csv



Go to BigQuery in GCP 
SELECT * FROM `project_id.datasetname.data_table` limit 10   # make sure to do ` not '


