# HW02 Customer Segmentation
## 1. Import Library
[![](https://img.shields.io/badge/-Pandas-red)](#) [![](https://img.shields.io/badge/-Numpy-red)](#) [![](https://img.shields.io/badge/-Scipy-red)](#) [![](https://img.shields.io/badge/-Sklearn-red)](#) [![](https://img.shields.io/badge/-Matplotlib-red)](#) 
## 2. Covert transaction data to customer single view

เนื่องจากข้อมูลที่ได้มาเป็นข้อมูล Transaction data (1 แถวเป็น 1 การซื้อ) แต่เราจะแบ่งกลุ่มของลูกค้า ดังนั้นเราจึงต้องทำการแปลงข้อมูลให้อยู่ในรูป Costomer sigle view (1 แถวเป็น 1 ลูกค้า)

![transaction_csv_data](https://user-images.githubusercontent.com/78030264/147189651-96385a33-c789-46ce-b31c-9c7686dd07d8.png)

โดยทำการเลือก Feature สำหรับการแปลงดังนี้
### Feature
* ```TotalSpend```  : ค่าใช้จ่ายทั้งหมดของลูกค้า
* ```TotalVisits``` : จำนวนครั้งทั้งหมดที่เข้ามาในร้าน
* ```TotalProd``` : จำนวนสินค้าที่รายการไม่ซ้ำที่ซื้อในร้าน
* ```SHOP_WEEKDAYS``` : วันไหนที่ลูกค้าเข้ามาในร้านบ่อยสุด
* ```SHOP_HOURS``` : ชั่วโมงไหนที่ลูกค้าเข้ามาในร้านบ่อยสุด
* ```BASKET_DOMINANT``` : ประเภทของสินค้าแบบไหนที่ลูกค้าซื้อบ่อยสุด
* ```TicketSize``` : ค่าใช้จ่ายที่ซื้อต่อจำนวนครั้งที่เข้ามา
## 3. Exploratory data

## 4. K-mean

## 5. PCA for visualization
![download](https://user-images.githubusercontent.com/78030264/147134747-c9fdb94b-7bf5-42c3-afa9-5869abe59b65.png)
## 6. Interpret results
![download (1)](https://user-images.githubusercontent.com/78030264/147134865-c7fa494d-3d3f-4a86-a5f6-42a622087abf.png)
## 7. Conclusion
