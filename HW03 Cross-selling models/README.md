# HW03 Cross-selling models

## 1.Generate Data
เนื่องจากไม่มีดาต้า เพื่อนนักศึกษาช่วยกันสร้างitem ของตัวเองขึ้นมาคนละ 1 อย่าง และแต่ละคนทำการโหวตว่าเคยซื้อหรือไม่เคยซื้อสินค้านั้นๆ เพื่อสร้าง Data ขึ้นมา

![Customer survey](https://user-images.githubusercontent.com/78030264/147367769-61bc00a8-7f2a-4a2f-a896-4469ac03d99a.png)


![data](https://user-images.githubusercontent.com/78030264/147367321-bb77e6c5-59d7-4cda-ba8d-1fccf68b481e.png)


## 2.Data preparation
เตรียมข้อมูลให้พร้อมก่อน
* ทำการลบแถวที่มีค่า Null ออก
* ทำการลบคอลัมน์ Timestamp ออกเนื่องจากไมได้ใช้งาน
* มีรายการสินค้าซ้ำกันคือ playstation5 และ PS5 ทำการเลือกลบออก 1 คอลัมน์ คือ PS5
* แปลงค่า ['เคยซื้อ','เคย'] เป็น 1 และ ['ไม่เคยซื้อ','ไม่เคย','ไม่','ไม่เคยซือ'] เป็น 0

## 3.Apriori

## 4.Association_rules

## 5.Conclusion
