# __การสำรวจไมโครคอนโทรลเลอร์ 5 model__ 
## 🌻 1. RISC-V 
Reduced Instruction Set Computer(RISC-V) based instruction set architecture(ISA)

RISC-V ไม่ใช่ CPU, สิ่งนี้คือสถาปัตยกรรมคำสั่ง ISA(Instruction Set Architecture) ISA เฉพาะเจาะจงกับชุดคำสั่งและรีจิสเตอร์บางตัว. ISA ไม่ได้เฉพาะเจาะจงว่า RAM ควรอยู่ส่วนไหน เป้าหมายของ ISA คือการเปิดใช้งานความเข้ากันได้แบบไบนารีระหว่างโปรเซสเซอร์ 2 ตัวที่ใช้ ISA เดียวกัน แม้ว่าสถาปัตยกรรมการใช้งานฮาร์ดแวร์ที่แตกต่างกันก็ตาม ใน RISC-V ISA มีส่วนขยายต่างๆ เช่น 32 บิต 64 บิต เป็นต้น

![RISC-V](https://www.extremetech.com/wp-content/uploads/2019/10/SiFive-CPU-Feature-768x425.jpg)
### ```Price```: ไม่มีค่าใช้จ่าย เนื่องจากRISC-V ISA อยู่ภายใต้ใบอนุญาตโอเพนซอร์สที่ไม่ต้องเสียค่าธรรมเนียมในการใช้งาน โดยบริษัทจำนวนมากเสนอให้ฮาร์ดแวร์ RISC-V เป็นระบบปฏิบัติการโอเพ่นซอร์สที่รองรับ RISC-V และชุดคำสั่งได้รับการสนับสนุนในชุดเครื่องมือซอฟต์แวร์ยอดนิยมหลายตัว
> reference [source](https://electronics.stackexchange.com/questions/576154/where-is-the-ram-stored-on-a-risc-v-cpu) [price](https://www.eenewseurope.com/en/worlds-fastest-64bit-risc-v-core-claims-5ghz-speed/) [port](https://groups.google.com/a/groups.riscv.org/g/sw-dev/c/cxsJpen-caA/m/6Kv73ZuDAgAJ?pli=1)
>### ```Port```: OpenJDK port, Hotspot port, libffi port

## 🌻 2. RP2040 
by Raspberry Pi Pico

Raspberry Pi เลข 2 ถัดมาคือจำนวน Dual Core และเลข 0 ในหลักถัดมาคือชนิดของ Arm Cortex M0+ เลข 4 ตัวต่อมาคือจำนวนของ RAM เลขสุดท้ายคือจำนวนของ Flash Memory 

คุณสมบัติที่สำคัญของ RP2040 ที่แตกต่างจากไมโครคอนโทรลเลอร์ตัวอื่น คือ PIO หรือ Programmable Input Output Block

![Raspberry Pi](https://www.arm.com/blogs/blueprint/wp-content/uploads/2021/01/rp2040-2.jpg)
### ```Price```: 4 USD
### ```Speed```: 133 MHz
### ```Memory```: 16 MB 
### ```Port```: USB port, Analog port
> reference [source](https://www.sparkfun.com/rp2040) [price](https://www.arm.com/blogs/blueprint/raspberry-pi-rp2040)

## 🌻 3. ATmega1608  
by AVR
ATmega1608 คือไมโคคอนโทนเลอร์ประกอบไปด้วย 8-bit AVR โปรเซสเซอร์พร้อมกับ hardware multiplier
ซีรีส์นี้ใช้ Core Independent Peripherals รุ่นล่าสุดพร้อมคุณสมบัติที่ใช้พลังงานต่ำ รวมถึง Event System, intelligent analog และอุปกรณ์ต่อพ่วงขั้นสูง

![AVR](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2F1owpf%2FbtqAqf2ykvT%2FGTK6Wk4jcA5KRtNk3a0IO0%2Fimg.jpg)
### ```Price```: 50.98 Bath
### ```Speed```: 20 MHz
### ```Memory```: 16 KB
### ```Port```: COM port
> reference [source](https://www.microchip.com/en-us/product/ATMEGA1608#:~:text=ATmega1608%20is%20a%20microcontroller%20featuring,%2D%20and%2032%2Dpin%20packages.) [price](https://www.digikey.co.th/th/products/detail/microchip-technology/ATMEGA1608-AFR/9973116)


## 🌻 4. MCS-51 
by PIC
บริษัท Microchip Technology เป็นผู้ผลิต PIC(Peripheral Interface Controller ) โดยมากแล้วไมโครคอนโทรลเลอร์ตระกูลนี้มักจะมีรูปร่างของ IC เป็นแบบขนาด 40 ขา ซึ่งแต่ละขาสัญญาณจะมีหน้าที่ที่ระบุชัดเจนตามสัญลักษณ์ชื่อย่อ ที่กำกับในแต่ละขา อย่างไรก็ตามจะมีบางขาสัญญาณที่อาจจะมีหน้าที่ได้มากกว่าหนึ่งอย่าง (ซึ่งเขียนกำกับไว้ว่า ALTERNATE FUNCTION) สามารถใช้งานในเวลาเดียวกันได้ ตัวอย่างเช่น Port3 (P3.0-P3.7) เป็นพอร์ต 2 ทิศทางขนาด 8 บิตและ มีการต่อความตา้นทาน (Pull-up Resistant)
ไว้ภายในทำหน้าที่คือเป็นพอร์ตอินพุตเอาต์พุตทั่วไป ยังใช้งานเป็นสัญญาณควบคุมการติดต่อกับหน่วยความจำ การอินเตอร์รัปต์และอื่นๆ

![PIC](https://micro-research.co.th/pub/media/catalog/product/cache/image/beff4985b56e3afdbeabfc89641a4582/m/t/mt-mcs51-a_5_1.jpg)
### ```Price```: MT-MCS51/S52 (MCU=AT89S52) = 545 Bath
### ```Speed```: 33 MHz
### ```Memory```: 8 KB
### ```Port```: Timer/counter port
> reference [source](https://th.rs-online.com/web/p/microcontrollers/4671690) [price](https://micro-research.co.th/mt-mcs51.html)

 ## 🌻 5. ESP8266 NodeMCU WIFI 
บอร์ด NodeMCU/ESP8266 เป็นบอร์ดไมโครคอนโทลเลอร์ที่มีจำนวนขาพอร์ตอินพุตและเอาต์พุตมากพอสำหรับการนำไปใช้งานจริง สามารถต่อกับเซ็นเซอร์ได้ทั้งแบบดิจิตอลและแอนะล็อก และยังต่อเพื่อขับอุปกรณ์เอาต์พุตให้ทำงาน โดยที่เราจะต้องเขียนโปรแกรมเพื่อสั่งงานให้บอร์ด NodeMCU/ESP8266 สามารถควบคุมอุปกรณ์ต่างๆ เช่น ควบคุมการเปิดปิดหลอดไฟ, ปลั๊กไฟฟ้า หรือเครื่องรดน้ำต้นไม้ เป็นต้น และเนื่องจากมีโมดูล WiFi ในตัว จึงสามารถเชื่อมต่อเพื่อส่งข้อมูลหรือสั่งงานผ่านทางอินเทอร์เน็ตได้โดยไม่ต้องหาซื้ออุปกรณ์มาต่อเพิ่ม นอกจากนั้นยังมีราคาถูก ซึ่งจะช่วยลดต้นทุนลงเป็นอย่างมากหากต้องการนำบอร์ดไปใช้ในการพัฒนาอุปกรณ์ Internet of Things (IoT)
 
 ![ESP8266](http://www.eak-electronic.com/image/cache/data/Product/Arduino/ESP8266%20Node%20MCU%20CH340-500x500.jpg)
### ```Price```: 130 Bath
### ```Speed```: 2.4 - 2.5 GHz
### ```Memory```: 4 MB
### ```Port```: Listening port
> reference [source](https://www.espressif.com/en/products/socs/esp8266) [price](http://www.eak-electronic.com/index.php?route=product/product&product_id=1395)
