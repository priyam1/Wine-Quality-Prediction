# Wine-Quality-Prediction

This project is implemented with Spark data frames Api and MLib libraries, with this Native spark implementation application is automatically parallelized and distributed natively.
Wine prediction application is developed using Spark and MLib. Running it on AWS EMR cluster automatically parallelize and distribute job execution. Hadoop Distributed Files system is used for locating dataset files and for storing trained models.
This assignment is to develop parallel machine learning (ML) applications in AWS platform. We are using Apache Spark to train an ML model in parallel on multiple EC2 instances. We are also using Spark’s MLib to develop and use ML model in cloud. Along with that creating a Docker container for the ML model to simplify model deployment.
Steps to follow: -

1.	First, we write and edit the code in Jupyter python notebook and create an EMR in AWS with 1 master and 4 slave.
2.	We need to log in to master EC2.
3.	Run dependency.sh, it will install all the required dependency.
4.	All the required CSV files are uploaded in S3 under source-data folder.
5.	As an input we put 2 datasets in each of the 4 slave nodes to train our ML model.
6.	These 2 datasets are TrainingDataSet.csv and ValidationDataset.csv.
Training Data set is used to train the model in parallel on multiple EC2 instances, Whereas Validation Data Set is used to validate the model and optimize the performance.
7.	Run Training.py as “spark-submi Training.py” – This will train and save the model in S3 under data-output and prints the F1 score.
8.	Login to the docker hub repo
9.	In the master run docker to build a container which will take the repository from the Docker hub and create the container.
10.	The container runs the validationData.csv and prints Test Error Link to docker hub image.
![image](https://user-images.githubusercontent.com/90930740/181677529-916245c9-e485-4d3e-b54d-a388bdd03658.png)
