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



## 功能二：銷售量預測
將2015年1月~2016年1月資料投入做訓練
運用演算法多元回歸與XGBOOST然後做模型融合後降低誤差
建模後預測2016年2月的銷售量
![image](https://github.com/mv123453715/Sales-volume-forecasting-and-analysis-system/blob/master/%E9%8A%B7%E5%94%AE%E9%87%8F%E9%A0%90%E6%B8%AC.PNG)
 
+ [ 原理]
![image](https://github.com/mv123453715/Sales-volume-forecasting-and-analysis-system/blob/master/%E9%8A%B7%E5%94%AE%E9%87%8F%E9%A0%90%E6%B8%AC%E5%8E%9F%E7%90%86.PNG)
 
## 功能三：價格敏感計
利用LTSM預測出銷售量與價格之間的關係

![image](https://github.com/mv123453715/Sales-volume-forecasting-and-analysis-system/blob/master/%E5%83%B9%E6%A0%BC%E6%95%8F%E6%84%9F%E8%A8%88.PNG)

+ [原理]
![image](https://github.com/mv123453715/Sales-volume-forecasting-and-analysis-system/blob/master/%E5%83%B9%E6%A0%BC%E6%95%8F%E6%84%9F%E8%A8%88%E5%8E%9F%E7%90%86.PNG)

## 功能四：評論風向球
蒐集網路上客戶的評論進行好壞的分類，找出影響銷售量的因子
![image](https://github.com/mv123453715/Sales-volume-forecasting-and-analysis-system/blob/master/%E8%A9%95%E8%AB%96%E9%A2%A8%E5%90%91%E7%90%83.PNG)

+ [原理]
![image](https://github.com/mv123453715/Sales-volume-forecasting-and-analysis-system/blob/master/%E8%A9%95%E8%AB%96%E9%A2%A8%E5%90%91%E7%90%83%20%E5%8E%9F%E7%90%86.PNG)

## 功能五：銷售策略分析
運用決策樹與分類找出銷售量好的規則

![image](https://github.com/mv123453715/Sales-volume-forecasting-and-analysis-system/blob/master/%E9%8A%B7%E5%94%AE%E7%AD%96%E7%95%A5.PNG)


+ [原理]
![image](https://github.com/mv123453715/Sales-volume-forecasting-and-analysis-system/blob/master/%E9%8A%B7%E5%94%AE%E7%AD%96%E7%95%A5%E5%8E%9F%E7%90%86.PNG)

## 感謝名單
Josh, Filex, Angie, Gary, James, Kia, Iris,Tim

