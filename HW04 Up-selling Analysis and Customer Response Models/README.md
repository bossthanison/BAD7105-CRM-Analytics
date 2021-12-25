# HW04 Up-selling Analysis and Customer Response Models

## 1. Data

### 1.1 Response Data
ข้อมูล Response Campaign ของลูกค้าแต่ละคน

![Retail_Data_Response](https://user-images.githubusercontent.com/78030264/147379562-e7b83616-c249-4356-ab2c-8892d1e0377a.png)

### 1.2 Transactions Data
ข้อมูล Transaction ของลูกค้าที่ผ่านมา

![Transactions_Data](https://user-images.githubusercontent.com/78030264/147379649-73375ba6-826e-4b40-8966-9a1a14636b2a.png)

## 2. Import Library

[![](https://img.shields.io/badge/-Pandas-blue)](#) [![](https://img.shields.io/badge/-Numpy-blue)](#) [![](https://img.shields.io/badge/-imblearn-blue)](#) [![](https://img.shields.io/badge/-Sklearn-blue)](#) [![](https://img.shields.io/badge/-Matplotlib-blue)](#) 

## 3. Data preparation
เตรียมข้อมูลสำหรับการไปทำ Model โดยทำการสร้าง Feature ขึ้นมาใหม่ดังนี้

![preparation](https://user-images.githubusercontent.com/78030264/147379858-c5c7b768-3f26-4879-ba6d-256652a14f07.png)

### Feature
* ```Recency``` 
* ```Frequency```
* ```Monetary```
* ```AOU```
* ```Ticket size```

## 4. Oversampling SMOTE
เนื่องจากข้อมูลมีความ Imbalane ลูกค้า Response 6237 คน แต่ ไม่Response เพียงแค่ 647 คน

![imbalance](https://user-images.githubusercontent.com/78030264/147380020-67ec723c-6074-4e49-88df-dca724b2d695.png)

ใช้ Oversampling SMOTE เพื่อให้ข้อมูลมีความ Balance เนื่องจากข้อมูล Imbalane ทำให้เวลาไปทำโมเดล machine learning จะเรียนรู้ข้อมูลที่มากมากกว่า ทำให้โมเดลจะไม่ค่อยเรียนรู้ลูกค้าที่ไม่ Response 

![eww](https://user-images.githubusercontent.com/78030264/147380113-ff3b9e3f-f5e6-4f43-b2ea-58799ff3c2e5.png)


## 5. Model
* ```Model``` : XGBClassifier
* ```Parameter Tuning``` : {objective='binary:logistic', eval_metric='auc', learning_rate =0.005, n_estimators=600, max_depth=4, colsample_bytree=0.5}


## 6. Model Evaluation
### Train
> AUC = 0.81

<img src="https://user-images.githubusercontent.com/78030264/147380358-91af35af-7b1f-4f91-96c7-e98393e078ed.png" width="600" >

![train](https://user-images.githubusercontent.com/78030264/147380421-de5472b3-8082-4b1f-a04f-390aeadf1025.png)

### Test
> AUC = 0.72


<img src="https://user-images.githubusercontent.com/78030264/147380368-d1b3a88e-a52b-4036-b871-875f1e0be43a.png" width="600" >

![Test](https://user-images.githubusercontent.com/78030264/147380423-1357d411-a396-47dc-bbc4-96c8031c166c.png)

