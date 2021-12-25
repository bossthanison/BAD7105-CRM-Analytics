# HW03 Cross-selling models

## 1. Generate Data
เนื่องจากไม่มีดาต้า เพื่อนนักศึกษาช่วยกันสร้างitem ของตัวเองขึ้นมาคนละ 1 อย่าง และแต่ละคนทำการโหวตว่าเคยซื้อหรือไม่เคยซื้อสินค้านั้นๆ เพื่อสร้าง Data ขึ้นมา

![Customer survey](https://user-images.githubusercontent.com/78030264/147367769-61bc00a8-7f2a-4a2f-a896-4469ac03d99a.png)


![data](https://user-images.githubusercontent.com/78030264/147367321-bb77e6c5-59d7-4cda-ba8d-1fccf68b481e.png)


## 2. Data preparation
เตรียมข้อมูลให้พร้อมก่อน
* ทำการลบแถวที่มีค่า Null ออก
* ทำการลบคอลัมน์ Timestamp ออกเนื่องจากไมได้ใช้งาน
* มีรายการสินค้าซ้ำกันคือ playstation5 และ PS5 ทำการเลือกลบออก 1 คอลัมน์ คือ PS5
* แปลงค่า ['เคยซื้อ','เคย'] เป็น 1 และ ['ไม่เคยซื้อ','ไม่เคย','ไม่','ไม่เคยซือ'] เป็น 0

## 3. Apriori
เป็นการหาความถี่ของ item ที่เกิดขึ้นร่วมกัน โดยรูปแสดงbah plot โดยเรียงลำดับจากมากไปน้อยเพื่อให้มองเห็น insight ได้ชัดเจนขึ้น โดยจะเห็นว่าเพื่อนร่วมห้องชอบกินแซลมอลกัน แล้วแซลมอลซื้อพร้อมกับยาดมค่อนข้างเยอะ(สงสัยจะเครียดจากการเรียน Haha)

![bah](https://user-images.githubusercontent.com/78030264/147376423-a1bc45b8-f5c2-41ad-8612-1a38d4ea5e2b.png)

## 4. Association_rules
เป็นการหากฏว่าถ้าซื้อไอเท็มชิ้นนี้ แล้วมีโอกาศที่จะซื้อไอเท็มอะไร เพื่อนำไป recommend ให้กับลูกค้าเพื่อเพิ่มยอดขายมากขึ้น

![rule](https://user-images.githubusercontent.com/78030264/147376514-74ca9b83-7fef-4fe7-ac44-aab4962775cb.png)

## 5. Conclusion
เมื่อคนซื้อหม้อทอดไร้น้ำมัน ก็มักจะซื้อแก้วเก็บความเย็นด้วย โดย support=0.536585 ,confidence=0.880000, lift=1.163871

![summary](https://user-images.githubusercontent.com/78030264/147376549-4b287732-d6de-465d-b7a6-4de7379f30be.png)
