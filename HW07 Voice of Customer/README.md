# HW07 Voice of Customer

## 1. Import Library
[![](https://img.shields.io/badge/-Pandas-Yellow)](#) [![](https://img.shields.io/badge/-Numpy-Yellow)](#) [![](https://img.shields.io/badge/-tensorflow-Yellow)](#) [![](https://img.shields.io/badge/-Sklearn-Yellow)](#) [![](https://img.shields.io/badge/-Matplotlib-Yellow)](#) [![](https://img.shields.io/badge/-pythainlp-Yellow)](#) 

## 2. Data
ข้อมูลที่นำมาใช้วิเคราะห์คือ ข้อมูล Review ของลูกค้า Wongnai

<img src="https://i0.wp.com/www.siamwicker.com/wp-content/uploads/2020/07/8a567e896d37ac452d7a1be1030293cb.jpg?ssl=1" width="400" >

<img src="https://user-images.githubusercontent.com/78030264/147539155-5b5512ff-bd08-42ff-b1e9-a52451cba573.png" width="500" >

## 3. Embedding and Dimension reduction
เนื่องจากข้อมูลที่ได้มาเป็นText แต่เวลาคอมพิวเตอร์จะเข้าใจอะไรต้องเป็นตัวเลขเท่านั้น ดังนั้นเราต้องทำการ Embedding text ให้เป็นตัวเลขเวคเตอร์ก่อน

<img src="https://res.cloudinary.com/practicaldev/image/fetch/s--7WKACZnN--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://cdn-images-1.medium.com/max/1600/1%2A8Qy3hv5iLnKnWVhpjjl2jQ.png" width="500" >

หลังจากนั้นทำการลด dimension ลงมาเพื่อกรองเฉพาะ variance ที่สำคัญลงมา และทำให้ช่วยให้การคำนวนเร็วขึ้น


## 4. K-mean clustering
ทำการจัดกลุ่ม review ของลูกค้า โดยทำการ Plot elbow เพื่อดูว่าจะกำหนดจำนวนกลุ่มอยู่ที่เท่าไร โดยจะเห็นจากกราฟเลือก K = 4 เนื่องจากเพื่อจำนวนกลุ่มเพิ่มขึ้น กราฟจะเปลี่ยนแปลงเพียงเล็กน้อย

![Elbow (2)](https://user-images.githubusercontent.com/78030264/147540454-05222f46-fbe0-46f5-99ea-0610b26443fd.png)

## 5. Text Cleansing

## 6. Word frequency each group

## 7. Conclusion
