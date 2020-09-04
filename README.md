# -Machine-learning-multi-person-development-system-based-on-Hadoop-and-Spark
## 基於Spark和Hadoop的機器學習多人開發系統


![image](https://github.com/mv123453715/-Machine-learning-multi-person-development-system-based-on-Hadoop-and-Spark/blob/master/spark.png)
![image](https://github.com/mv123453715/-Machine-learning-multi-person-development-system-based-on-Hadoop-and-Spark/blob/master/hadoop.jpg)
 
## Step1 用docker安裝spark主機
+ [ cd spark]
+ [ docker-compose -f spark.yml up -d]
![image](https://github.com/mv123453715/-Machine-learning-multi-person-development-system-based-on-Hadoop-and-Spark/blob/master/docker.png)


## Step2 下載spark
+ [ ssh localhost -p 22200]
+ [ wget https://archive.apache.org/dist/spark/spark-2.3.1/spark-2.3.1-bin-hadoop2.7.tgz]
+ [ sudo tar xvfz spark-2.3.1-bin-hadoop2.7.tgz -C /opt/]

## Step3 設定spark
+ [sudo nano /opt/spark-2.3.1-bin-hadoop2.7/conf/spark-env.sh]
![image]https://github.com/mv123453715/-Machine-learning-multi-person-development-system-based-on-Hadoop-and-Spark/blob/master/spark%E8%A8%AD%E5%AE%9A.JPG)
+ [hdfs dfs -mkdir -p /tmp/spark-events]
+ [hdfs dfs -chmod -R 777 /tmp/]
+ [sudo nano /opt/spark-2.3.1-bin-hadoop2.7/conf/spark-defaults.conf]
![image]https://github.com/mv123453715/-Machine-learning-multi-person-development-system-based-on-Hadoop-and-Spark/blob/master/spark%E8%A8%AD%E5%AE%9Aserver.JPG)





