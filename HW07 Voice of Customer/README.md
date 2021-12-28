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
ทำการจัดกลุ่ม review ของลูกค้า โดยทำการ Plot elbow เพื่อดูว่าจะกำหนดจำนวนกลุ่มอยู่ที่เท่าไร โดยจะเห็นจากกราฟเลือก K = 4 เนื่องจากจะเห็นว่าเมื่อจำนวนกลุ่มเพิ่มขึ้น กราฟจะเปลี่ยนแปลงเพียงเล็กน้อย

<img src="https://user-images.githubusercontent.com/78030264/147540454-05222f46-fbe0-46f5-99ea-0610b26443fd.png" width="600" >


## 5. Text Cleansing
ทำการ Clean ข้อมูลใน Text ที่ไม่มีประโยชน์ในการที่จะเห็น insight ภายในกลุ่ม โดยใช้ Regular expression 
> * Remove Special characters
> * Remove Emoji
> * Remove Digit
> * Remove White space
> * Add new word such as {"สตารบัก","ชานมไข่มุก","หัวหิน","ราชเทวี","มากกกกกกกกกกก","อเมซอน","ราชาติดี","เค้าดาว"}
 
## 6. Word frequency each group
### > Group 0
<img src="https://user-images.githubusercontent.com/78030264/147544655-1a284590-f668-42fd-9736-0cfa91200cb2.png" width="500" >

![wordcount0_bar (2)](https://user-images.githubusercontent.com/78030264/147545338-15498fed-3964-4c4e-b333-88f92c482a2e.png)

### > Group 1
<img src="https://user-images.githubusercontent.com/78030264/147546271-88ed4a64-06bd-4ca7-99e6-990df36ed203.png" width="500" >

![wordcount1_bar](https://user-images.githubusercontent.com/78030264/147546288-c3d4c684-5dfd-4ab2-927c-9e32aa9464a8.png)

### > Group 2
<img src="https://user-images.githubusercontent.com/78030264/147546287-72f3f120-509a-4b65-8e07-d6ebdbc90ceb.png" width="500" >

![wordcount2_bar](https://user-images.githubusercontent.com/78030264/147546294-ad5440a0-c8a1-4e59-9c79-9ab51cc37a00.png)

### > Group 3
<img src="https://user-images.githubusercontent.com/78030264/147546292-4dd5b08d-952f-4312-9cea-c7f64b20e355.png" width="500" >

![wordcount3_bar](https://user-images.githubusercontent.com/78030264/147546290-b68db026-e92f-43aa-b7f6-03970a32bf0d.png)

## 7. Conclusion
* ```Group 0``` เป็นกลุ่มรีวิวร้านอาหารโดยไม่กับเพื่อน
* ```Group 1``` รีวิวเกี่ยวกับชา,ชานมไข่มุก
* ```Group 2``` รีวิร้านเครื่องดื่มกาแฟ
* ```Group 3``` รีวิวร้านคาเฟ้น่ารักๆๆ สำหรับคนชอบอะไรน่ารักๆ นั่งทานได้

