# HW06 Churn Prediction Model

## 1. DATA 
ข้อมูล Transaction ของ Supermarket

## 2. Import DATA To Bigquery

![bigquery](https://user-images.githubusercontent.com/78030264/147645637-d8f1f275-e6d4-4413-b5b5-1933a4e65d5e.png)

## 3. SQL Query
ทำการเขียน SQL เพื่อหาว่าในแต่ละเดือนลูกค้าของเรามีสถานะเป็นแบบไหนบ้าง โดยแบ่งเป็น 4 สถานะคือ
* ```NEW_CUSTOMER``` : ลูกค้าใหม่ที่พึ่งเข้ามาเดือนนี้
* ```REPEAT_CUSTOMER``` : ลูกค้าเก่าที่เดือนที่แล้วก็มา เดือนนี้ก็มา
* ```REACTIVATE_CUSTOMER``` : ลูกค้าที่เดือนที่แล้วไม่ได้มา แต่เดือนนี้มา
* ```CHURN_CUSTOMER``` : ลูกค้าที่ไม่ได้มาเกิน 30 วัน

**ตัวอย่าง Code SQL**
![sql](https://user-images.githubusercontent.com/78030264/147646366-733b248a-1bd2-46c0-aab9-3b14a9279b5f.png)

**ตัวอย่างผลลัพธ์ที่ได้**

![table](https://user-images.githubusercontent.com/78030264/147646119-1269f68e-96eb-4000-beb9-ab6cdeac09ad.png)

## 4. Visualization
ใช้ Datastudio ในการ Visualization เพื่อทำให้ดูข้อมูลเข้าใจมากขึ้น

![visualization](https://user-images.githubusercontent.com/78030264/147646231-f2b46c62-4ec6-4202-a10f-83041faf25a1.png)
