# -Machine-learning-multi-person-development-system-based-on-Hadoop-and-Spark
## 基於Spark和Hadoop的機器學習多人開發系統


![image](https://github.com/mv123453715/-Machine-learning-multi-person-development-system-based-on-Hadoop-and-Spark/blob/master/spark.png)
![image](https://github.com/mv123453715/-Machine-learning-multi-person-development-system-based-on-Hadoop-and-Spark/blob/master/hadoop.jpg)
![image](https://github.com/mv123453715/-Machine-learning-multi-person-development-system-based-on-Hadoop-and-Spark/blob/master/%E7%B3%BB%E7%B5%B1%E6%9E%B6%E6%A7%8B%E5%9C%96.JPG)
 
## Step1 用docker安裝spark主機
+  cd spark
+  docker-compose -f spark.yml up -d

![image](https://github.com/mv123453715/-Machine-learning-multi-person-development-system-based-on-Hadoop-and-Spark/blob/master/docker.png)


## Step2 下載spark
+  ssh localhost -p 22200
+  wget https://archive.apache.org/dist/spark/spark-2.3.1/spark-2.3.1-bin-hadoop2.7.tgz
+  sudo tar xvfz spark-2.3.1-bin-hadoop2.7.tgz -C /opt/

## Step3 設定與啟動spark
+ [sudo nano /opt/spark-2.3.1-bin-hadoop2.7/conf/spark-env.sh]

![image](https://github.com/mv123453715/-Machine-learning-multi-person-development-system-based-on-Hadoop-and-Spark/blob/master/spark%E8%A8%AD%E5%AE%9A.JPG)
+ hdfs dfs -mkdir -p /tmp/spark-events
+ hdfs dfs -chmod -R 777 /tmp/
+ sudo nano /opt/spark-2.3.1-bin-hadoop2.7/conf/spark-defaults.conf

![image](https://github.com/mv123453715/-Machine-learning-multi-person-development-system-based-on-Hadoop-and-Spark/blob/master/spark%E8%A8%AD%E5%AE%9Aserver.JPG)
+ startspkb

![image](https://github.com/mv123453715/-Machine-learning-multi-person-development-system-based-on-Hadoop-and-Spark/blob/master/%E5%95%9F%E5%8B%95spark.png)


## Step4 安裝 Anaconda
+  wget https://repo.continuum.io/archive/Anaconda3-5.2.0-Linux-x86_64.sh -O /tmp/anaconda3.sh 
+  chmod +x /tmp/anaconda3.sh 
+ sudo /tmp/anaconda3.sh -u 
+ sudo /opt/anaconda3/bin/conda update conda
+ sudo /opt/anaconda3/bin/conda update anaconda
+ sudo /opt/anaconda3/bin/conda upgrade python
+ /opt/anaconda3/bin/python -V


## Step5 重啟Hadoop和Spark
+ stopspkb
+ stophdfs
+ exit
+ docker-compose -f spark.yml stop
+ docker-compose -f spark.yml start


## Step6 設定Spark使用 Anaconda
+ sudo nano /opt/spark-2.3.1-bin-hadoop2.7/conf/spark-env.sh
![image](https://github.com/mv123453715/-Machine-learning-multi-person-development-system-based-on-Hadoop-and-Spark/blob/master/spark%E8%A8%AD%E5%AE%9Apython.JPG)
+ starthdfs
+ startspkb
+ pyspark --master spark://spkmb:7077 --total-executor-cores 1 --executor-cores 1 --executor-memory 512m


## Step7 安裝 Hive
+ wget https://archive.apache.org/dist/hive/hive-2.3.3/apache-hive-2.3.3-bin.tar.gz
+ sudo tar xvfz apache-hive-2.3.3-bin.tar.gz -C /opt


## Step8 設定Jupyter Server
+ sudo nano /opt/bin/startjupyter
+ sudo chmod +x /opt/bin/startjupyter
+ hdfs dfs -mkdir /tmp/hive
+ hdfs dfs -chmod -R 777 /tmp/hive

## Step9 設定Jupyter
+ 開nwe 終端機
+ ssh dsa103@localhost -p 22103
+ jupyter notebook --generate-config
+ jupyter notebook password
+ ll .jupyter/

## Step10 啟動Jupyter
+ startjupyter
