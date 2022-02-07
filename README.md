# LE202
#จากการสรุปความเข้าใจบน GitHub repo อย่างแรกเลย เราต้องทำความรู้จักกับ
## 1.What is GitHub Flavored Markdown?
หรือเรียกอย่างง่ายว่า GFM มันถือภาษาหนึ่งใน markdown ที่ให้ผู้ใช้งานให้สามารถติดต่อกับ GitHub.com และ GitHub Enterprise ได้. เป็นส่วนเสริมความสามารถให้กับ Markdown เช่น การใส่ตาราง การใช้ fence code block หรือการใส่ Task list 
## 2.Markdown 
Markdown คือภาษาหนึ่ง ที่คนสร้าง สร้างขึ้นเพื่อให้มนุษย์สามารถอ่านได้เข้าใจง่าย ๆ และด้วยความง่ายนี้มันก็สามารถแปลงกลับมาเป็นภาษาอื่น ๆ ได้ง่ายด้วยกันเช่น HTML, XHTML และ GitHub ก็นำมาใช้ ซึ่งอาจจะเพิ่มพวก feature เข้าไปเช่น task list, mention และอื่น ๆ 
### เรามาเริ่มทำความรู้จักกับ Markdown:
# หัวข้อ (Header)  
การสร้าง heading เราจะเพิ่ม # ก่อนหน้าหัวข้อของเรา ซึ่งจำนวนของ # ที่เราใช้จะผันตรงกับขนาดตัวอักษรของ heading
```
# The largest heading
## The second largest heading
###### The smallest heading
``` 
### ```Output Bold```
> # The largest heading
> ## The second largest heading
> ###### The smallest heading

# รูปแบบตัวอักษร (Styling text)
เราสามารถแสดงความสำคัญกับ รูปแบบตัวอักษร bold, italic หรือ strikethrough ใน comment fields และ .md fields.
## 1.	ตัวหนา (Bold)
```
### __This is Bold__
### **This is Bold**
```
### ```Output Bold```
> **This is Bold**

> __This is Bold__

## 2.	ตัวเอียง (Italics)
```
### _This is Italics_
### *This is Italics*
```
### ```Output Italics```
> _This is Italics_

> *This is Italics*

## 3.	ตัวหนา + ตัวเอียง (Bold + Italics)
```
### ___ This is Bold and Italics ___
### *** This is Bold and Italics ***
```
### ```Output Bold and Italics```
> ___This is Bold and Italics___

> ***This is Bold and Italics***

# การขีดฆ่าตัวอักษร(Strikethrough)
## 1.ขีดฆ่าธรรมดา(Strikethrough)
```
~This is Strikethrough~
```
### ```Output Strikethrough```
> ~This is Strikethrough~ 

# Quoting text
## เราสามารถเขียนข้อความด้วยเครื่องหมาย >
```
Text that is not quote
> Text that is a quote
```

# Quoting code
คุณสามารถเรียกโค้ดหรือคำสั่งที่เป็นประโยคด้วย single backtick(`) ข้อมูลที่มี single backtick(`) จะไม่ได้รับการจัดรูปแบบ คุณสามารถกด Ctrl+E เป็นคำสั่งลัดเพื่อไปยัง single backtick(`) สำหรับโค้ดที่มี Markdown นอกจากนี้การที่จะจัดรูปโค้ดหรือข้อความให้อยู่ในกล่อง สามารถใช้ triple backticks(```)

# Link
## 1. Link Wedsite
คุณสามารถสร้างลิงค์ได้ โดยนำลิงค์มาใส่ไว้ใน brakets[] และใส่ URL ไว้ในวงเล็บ().
```
This site was built[GitHub Pages ME](https://github.com/panitavan/LE202/edit/main/README.md)
```
> This site was built[GitHub Pages ME](https://github.com/panitavan/LE202/edit/main/README.md)

## 2. Link Image
คุณสามารถใส่รูปภาพได้โดยการเพิ่มเครื่องหมาย! และนำข้อความ alt ใส่ใน[] หลังจากนั้นนำลิงค์รูปภาพใส่ในวงเล็บ()
```
![This is a cute image](https://www.istockphoto.com/th/%E0%B8%A3%E0%B8%B9%E0%B8%9B%E0%B8%96%E0%B9%88%E0%B8%B2%E0%B8%A2/%E0%B9%81%E0%B8%A1%E0%B8%A7%E0%B8%82%E0%B8%B4%E0%B8%87%E0%B8%99%E0%B8%B1%E0%B9%88%E0%B8%87%E0%B8%AD%E0%B8%A2%E0%B8%B9%E0%B9%88%E0%B8%9A%E0%B8%99%E0%B8%9E%E0%B8%B7%E0%B9%89%E0%B8%99%E0%B9%83%E0%B8%99%E0%B8%AB%E0%B9%89%E0%B8%AD%E0%B8%87%E0%B8%99%E0%B8%B1%E0%B9%88%E0%B8%87%E0%B9%80%E0%B8%A5%E0%B9%88%E0%B8%99%E0%B9%81%E0%B8%A5%E0%B8%B0%E0%B8%A1%E0%B8%AD%E0%B8%87%E0%B9%84%E0%B8%9B%E0%B8%97%E0%B8%B5%E0%B9%88%E0%B8%81%E0%B8%A5%E0%B9%89%E0%B8%AD%E0%B8%87-%E0%B8%97%E0%B9%88%E0%B8%B2%E0%B8%AA%E0%B8%B1%E0%B8%95%E0%B8%A7%E0%B9%8C%E0%B9%80%E0%B8%A5%E0%B8%B5%E0%B9%89%E0%B8%A2%E0%B8%87%E0%B8%95%E0%B8%A5%E0%B8%81-gm1149347768-310714830)
```
>![This is a cute image](https://www.istockphoto.com/th/%E0%B8%A3%E0%B8%B9%E0%B8%9B%E0%B8%96%E0%B9%88%E0%B8%B2%E0%B8%A2/%E0%B9%81%E0%B8%A1%E0%B8%A7%E0%B8%82%E0%B8%B4%E0%B8%87%E0%B8%99%E0%B8%B1%E0%B9%88%E0%B8%87%E0%B8%AD%E0%B8%A2%E0%B8%B9%E0%B9%88%E0%B8%9A%E0%B8%99%E0%B8%9E%E0%B8%B7%E0%B9%89%E0%B8%99%E0%B9%83%E0%B8%99%E0%B8%AB%E0%B9%89%E0%B8%AD%E0%B8%87%E0%B8%99%E0%B8%B1%E0%B9%88%E0%B8%87%E0%B9%80%E0%B8%A5%E0%B9%88%E0%B8%99%E0%B9%81%E0%B8%A5%E0%B8%B0%E0%B8%A1%E0%B8%AD%E0%B8%87%E0%B9%84%E0%B8%9B%E0%B8%97%E0%B8%B5%E0%B9%88%E0%B8%81%E0%B8%A5%E0%B9%89%E0%B8%AD%E0%B8%87-%E0%B8%97%E0%B9%88%E0%B8%B2%E0%B8%AA%E0%B8%B1%E0%B8%95%E0%B8%A7%E0%B9%8C%E0%B9%80%E0%B8%A5%E0%B8%B5%E0%B9%89%E0%B8%A2%E0%B8%87%E0%B8%95%E0%B8%A5%E0%B8%81-gm1149347768-310714830)

# Lists
คุณสามารถทำ unordered list (ลิสต์ที่ไม่ต้องการการเรียงลำดับ แต่เน้นการนำเสนอเพื่อสร้างความเข้าใจเป็นหลัก) โดยใส่เครื่องหมาย - หรือ * นำหน้าข้อความของบรรทัดนั้น
```
- Apple
- Kiwi
- Cherry
```
### ```Output Lists```
- Apple
- Kiwi
- Cherry

หรืออีกวิธีนึงคือเรียงลำดับลิสต์ของคุณ โดยการใส่ตัวเลขนำหน้าในแต่ละบรรทัด
```
1.Dog
2.Cat
3.Bird
```
### ```Output Lists```
1. Dog
2. Cat
3. Bird

## 1. Nested Lists
คุณสามารถสร้าง nested lists(ลิสต์ซ้อนลิสต์) โดยเคาะ Space เข้าไปแบบตัวอย่างดังต่อไปนี้
```
* Tree
  * branch
  * root
    * Tap root
    * Fibrous root
```
### ```Output Nested Lists```
* Tree
  * branch
  * root
    * Tap root
    * Fibrous root

## 2. Task Lists
คุณสามารถสร้าง task list โดยใช้ –[x] สำหรับChecked ที่Taskนั้น ๆและใช้ –[ ] สำหรับTask ที่ไม่ได้ถูกChecked 
```
-[x] A
-[ ] B
-[ ] C
```
### ```Output Task Lists```
>-[x] A

>-[ ] B

>-[ ] C

# Mention people and teams
คุณสามารถกล่าวถึงผู้คนหรือ ทีมใน GitHub โดยพิม @ ตามด้วยชื่อผู้ใช้หรือชื่อทีม สิ่งนี้จะไปแจ้งเตือนพวกเขาและคนที่เรากล่าวถึงจะได้รับการแจ้งเตือนเสมอเมื่อเรามีการแก้คอมเม้นที่ต้องการส่งให้เขา

# Using Emoji
คุณสามารถแทรก emoji ในข้อความของคุณ โดยพิม **:EMOJICODE:**
```
BorntoDev :t-rex: | Sunflower :sunflower: | Tomato :tomato:
```
### ```Output Emoji```
> BorntoDev :t-rex: | Sunflower :sunflower: | Tomato :tomato:

# Paragraphs
คุณสามารถสร้าง paragraph ใหม่ได้ โดยการเว้นช่องว่างระหว่างข้อความ

# Footnotes
คุณสามารถเพิ่ม footnotes ไปยังคอนเท้นของเรา โดยใช้ bracket syntax: 

# Hiding content with comments
คุณสามารถบอก GitHub ซ่อน content จากการแสดงผลของ Markdown โดยวาง content ในคอมเม้นของ HTML
> <!- - ``` ... ``` - ->

# Ignoring Markdown formatting
คุณสามารถบอก GitHub ให้เพิกเฉยต่อรูปแบบ Markdown โดยใช้ \ ก่อน Markdown character

# Disabling Markdown rendering
เมื่อดู ไฟล์Markdown คุณสามารถคลิก <> ที่ด้านบนไฟล์เพื่อไม่ต้องประมวลผล Markdown และ เป็น file’s source แทน.

---

# ทบทวนความรู้เกี่ยวกับ ESP-01 microcontroller
### 01 digital 
คือ การนำสัญญาณไฟฟ้ามาแทนด้วยข้อมูลของเลขฐานสอง(Binary) โดยดูว่ามีสัญญาณ on/off หรือไม่ ซึ่งขึ้นอยู่กับค่าแรงดันของในแต่ละระบบข้อมูลที่นำไปใช้ ถ้า on จะเป็น 1, ถ้า off จะเป็น 0
### 02 voltage
แรงดันไฟฟ้า คือความต่างศักย์ของไฟฟ้าระหว่างจุดสองจุด แรงดันไฟฟ้ามีสองประเภทได้แก่   
1. กระแสสลับ(ไฟบ้าน) 230 V  
2. กระแสตรง(แบตเตอรี่) 1.6 V, (อุปกรณ์ USB) 5V
### 03 computer 
คอมพิวเตอร์มีวิวัฒนาการจากใหญ่มากๆ เป็นคอมพิวเตอร์ขนาดใหญ่ คอมพิวเตอร์ขนาดกลาง(desktop), คอมพิวเตอร์ขนาดเล็ก (single board computer), คอมพิวเตอร์ขนาดจิ๋ว (Arduino Microcontroller) เพราะขนาดเล็กลงจึงทำให้มีความเร็วสูงขึ้นและมีความจุเพิ่มขึ้น แล้วคอมพิวเตอร์เหล่านี้สามารถเชื่อมโยงด้วยอินเทอร์เน็ตด้วยความเร็วสูง
### 04 internet 
ทำให้อุปกรณ์อิเล็กทรอนิกซ์ต่างๆสามารถเชื่อมโยงกันได้ไม่ว่าจะมีสายหรือไร้สาย  
### 05 program lang
ภาษาคอมพิวเตอร์ถูกพัฒนาขึ้นมาเรื่อย ๆ เพื่อให้คนเขียนได้ง่ายขึ้น พัฒนาโปรแกรมได้ง่ายขึ้นเช่นกัน
### 06 platform IO
มีการพัฒนา soft-ware แบบเปิดที่ใช้วิธีการเขียนโปรแกรมแบบเดียว แต่สามารถเขียนใน Microcontroller ได้หลายรูปแบบ วิธีการเขียนโปรแกรมก็สามารถทำได้หลายรูปแบบ เช่น เขียนแบบ Arduino 
### 07 IOT set 1
การ run คำสั่ง เพื่อต้องการทราบข้อมูล

---

# ศึกษาการทดลองบน ESP-01 จำนวน 6 การทดลองต่อไปนี้
### 01 run example 1 
เป็นการเขียนโปรแกรมด้วย platform IO เพื่อ microcontroller ESP-01 ใช้ภาษา C หรือ C++ แบ่งออกเป็นสองฟังก์ชันคือ 1.setup จะรันครั้งเดียว โดยเซต serial ก่อนด้วยความเร็ว 115200 และ 2.ส่วน loop จะรันบนลูปตลอดไป จะมีการเพิ่มตัวแปรขึ้นเรื่อยๆ โดยที่ให้แสดงผลตัวแปรออกมา แล้วให้หน่วยเวลา 1 วินาที นำคำสั่งเข้าไปยัง microcontroller ด้วยคำสั่ง upload ในขณะที่รันเพื่อใน microcontroller รับคำสั่งใหม่เข้าไป กดปุ่มสีดำ(upload) และกดปุ่มสีแดง(reset) ระหว่างนั้นก็จะขึ้นเพอร์เซอร์ที่กำลังโหลดข้อมูล พอโปรแกรมโหลดเสร็จแล้ว เราจะใช้คำสั่ง pio device monitor เพื่อดูผลรับที่แสดงออกมาจากคอมพิวเตอร์ ซึ่งจะแสดงผลทุก ๆ 1 วินาที 

### 02 run example 2 
เขียนโปรแกรมเพื่อดันโปรแกรมบน microcontroller ESP-01 นำมาต่อกับ USB หลังจากนั้นเตรียม upload โปรแกรม โดยแบ่งออกเป็นสองฟังก์ชัน โดยมีส่วน set up และ ส่วน loop ซึ่งจะเป็นการวนลูปตลอดไป โดยเริ่มต้นจากการค้นหา Wi-Fi พอได้ wifi ก็แสดงผลว่ามี wifi รอบตัว หลังจากนั้น upload โปรแกรมเข้าสู่ microcontroller ด้วยคำสั่ง pio run -t upload เพื่อให้โปรแกรม upload ได้กดปุ่มสีดำแล้วก็ปุ่ม reset เมื่อโปรแกรม upload เสร็จสิ้น microcontroller จะเริ่มแสกนหา wifi หลังจากนั้นใช้คำสั่ง pio device monitor เพื่อให้แสดงผลผ่านหน้าจอเพื่อดูว่าเจอ wifi อะไรบ้าง แล้วแต่สัญญาณความแรงที่ได้รับ และกดปุ่นสีแดง(reset) เพื่อเริ่มทำงานใหม่

### 03 run example 3 
โปรแกรมที่รันบน microcontroller ESP-01 ซึ่งคอมพิวเตอร์มีอยู่ 2 พอร์ต คือพอร์ตเลข 0 และพอร์ตเลข 1 เมื่อต้องเขียนโปรแกรมให้นำมาติดกับ USB to 2 serial ports โดยใช้ adapter ซึ่งจะมีสายพอร์ต 0 (สายสีขาว) และพอร์ต 1(สายสีเหลือง) มาต่อเสียบก่อน โปรแกรมที่ 3 จะส่งเอาต์พุตออกมาที่พอร์ 0 เพื่อให้เห็นได้ด้วยตาจะนำมาต่อกับ LED เปล่งแสง เพื่อให้เห็นสว่างเป็น 1 ออกมา เมื่อจะเขียนโปรแกรมเราจะต่อคอมพิวเตอร์เข้าไป โปรแกรมจะเซตพอร์ตเลข 0 เป็น เอาต์พุต หลังจากนั้นก็วนลูป ทุก 0.5 วินาที นับ 0 กับ 1 ไปเรื่อย ๆ ถ้าได้เลขคู่ ให้ off  ถ้าได้เลขคี่ ให้ on หลังจากนั้น upload โปรแกรม ด้วยคำสั่ง pio run -t upload และเราก็จะกดปุ่มสีดำ(upload) และกดปุ่มสีแดง(reset) โปรแกรมก็จะถูก upload ไปยัง microcontroller หลังจากเสร็จสิ้นให้ป้อนคำสั่ง  pio device monitor เพื่อดูผลผ่านหน้าจอ ผลลัพธ์จะได้ว่า ทุก ๆ 0.5 วินาที จะได้ on/off สลับกันไป ถ้ามาดูที่ LED ส่องสว่างเฉพาะที่พอร์ต 0 จะเห็นได้ว่าจะมีการเปล่งแสงออกมาเมื่อขึ้น on

### 03 run rely
จะนำ microcontroller ที่เขียนโปรแกรมที่ 3 ไว้แล้ว มาต่อกับ relay เพื่อให้พอร์ต 0 ที่ปล่อย 0 กับ 1 มันจะส่งสัญญาณไปควบคุม relay ในการเปิดปิดสวิตช์ (สัญญาณ on เปิดสวิตช์, สัญญาณ off ปิดสวิตช์) ทุก ๆ 0.5 วินาที หลังจากนั้นนำ relay ไปต่อกับขั้วชาร์ตเพื่อจ่ายไฟให้กับ relay และ microcontroller มันก็จะควบคุม relay ให้เปิด/ปิด โดยทันที โดยที่จะได้เสียงหน้าสัมผัสของสวิตช์ไฟที่มันเปิดปิด

### 04 example 4
4 โปรแกรมทดลองนำสัญญาณอินพุตจากภายนอกเข้ามาใน microcontroller ซึ่งโปรแกรมแบ่งออกเป็นสองฟังก์ชันเช่นเดิม คือ ส่วนที่เป็น setup ซึ่งเราจะทำการเซตให้พอร์ต ให้พอร์ต 0 (สายสีขาว) เป็นอินพุต และพอร์ต 2 (สีเหลือง) เป็นเอาต์พุต และส่วนที่เป็น loop โปรแกรมจะวนลูป อ่านสัญญาณ(digital Read)จากพอร์ต 0 ถ้าอ่านได้เป็น 1 ให้ low ที่พอร์ต 2 (ไฟดับ) ถ้าอ่านได้เป็น 0 ให้ high ที่พอร์ต 2 (ไฟติด) จากนั้นป้อนคำสั่ง pio run -t upload ตามด้วยกดปุ่ม upload โปรแกรมก็จะขึ้นเพอร์เซ็นการ upload ขึ้นมาให้ จนเสร็จสิ้น พอเสร็จแล้วโปรแกรมจะเช็คพอร์ต 0 ว่าจะตัวอินพุตเข้ามาหรือไม่ ต่อมาป้อนคำสั่ง pio device monitor เพื่อดูผลผ่านหน้าจอ การการทดลองจะแสดงว่าอ่านได้ค่า 1 หมดเลย ซึ่งถ้านำสายไฟสีขาว(พอร์ต 0)มาจิ้มสายไฟสีดำ ก็จะอ่านค่าได้ 0 มีไฟติด นำมาจิ้มสายไฟสีแดงก็จะอ่านค่าเป็น 1 ไม่มีไฟติด การทดลองนี้เราจะนำขา sensor ไปต่อกับไฟเลี้ยง(สายสีแดง) อีกขาไปต่อกับเส้นสีดำ (สายดิน)  สัญญาณที่อยู่ตรงกลางคือสัญญาณจาก sensor ซึ่งจะนำมาต่อกับเส้นพอร์ต 0 ถ้ามีแสงสว่างเข้ามาจะเป็น 0 (LED เปล่งแสง) แต่ถ้ามืดมันก็แรงต้นทานสูงขึ้น จะเป็น 1 (LED ไม่เปล่งแสง) 

### 05 run wifi
โปรแกรมในการสร้าง Wifi-Web-Server ต้องต่อการ Wifi อันแรกใส่ชื่อ wifi พร้อมรหัสเข้าถึง โปรแกรมจะมีสองฟังก์ชันเหมือนเดิม คือ setup (ส่วนใหญ่คือการติดต่อกับ wifi ที่เราเลือกไว้ หลังจากนั้น setup เกี่ยวกับ Web-Server) กับ loop ต่อมา upload โปรแกรมขึ้นไปยัง microcontroller โดยการเสียบ microcontroller ไปที่ USB to 2 serial ports หลังจากนั้นกดปุ่ม upload และตามด้วยปุ่ม reset 

### 06 run wifi AP
เป็นโปรแกรมที่ใช้ wifi ต่างจากตัวอย่างที่ 5 ตรงที่ตัวอย่างที่ 5 เชื่อมโยงกับ wifi อยู่แล้ว แต่ตัวอย่างที่6 สร้าง wifi-access ขึ้นมาเอง ให้ ESP-01 เป็น access point ต้องตั้งชื่อ และกำหนดรหัส ตอนที่จะปล่อย wifi ให้คนมาเชื่อมต่อได้ ต้องกำหนด IPAddress local_ip/ gateway/ subnet เขียน wed-server ไว้ 1 ตัว สร้างaccess poin ด้วยคำสั่ง softAP (กำหนด ssid, passwprd) ลงไป และป้อนคำสั่ง upload โปรแกรม และกดปุ่ม reset เมื่อ upload เสร็จ ตัวนี้ก็จะสร้าง wifi- access point ขึ้นมา คำสั่ง pio device monitor เพื่อดูผลผ่านหน้าจอ หลังจากนั้นค้นหา wifi และลองป้อมรหัสเข้าใช้งานได้
