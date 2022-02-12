# __A survey of five microcontroller models__ 
## 🌻 1. RISC-V 
Reduced Instruction Set Computer(RISC-V) based instruction set architecture(ISA)

RISC-V ไม่ใช่ CPU, สิ่งนี้คือสถาปัตยกรรมคำสั่ง ISA(Instruction Set Architecture) ISA เฉพาะเจาะจงกับชุดคำสั่งและรีจิสเตอร์บางตัว. ISA ไม่ได้เฉพาะเจาะจงว่า RAM ควรอยู่ส่วนไหน เป้าหมายของ ISA คือการเปิดใช้งานความเข้ากันได้แบบไบนารีระหว่างโปรเซสเซอร์ 2 ตัวที่ใช้ ISA เดียวกัน แม้ว่าสถาปัตยกรรมการใช้งานฮาร์ดแวร์ที่แตกต่างกันก็ตาม ใน RISC-V ISA มีส่วนขยายต่างๆ เช่น 32 บิต 64 บิต การจัดการบิต เป็นต้น

![RISC-V](https://www.extremetech.com/wp-content/uploads/2019/10/SiFive-CPU-Feature-768x425.jpg)
### ```Price```: ไม่มีค่าใช้จ่าย เนื่องจากRISC-V ISA อยู่ภายใต้ใบอนุญาตโอเพนซอร์สที่ไม่ต้องเสียค่าธรรมเนียมในการใช้งาน บริษัทจำนวนมากเสนอให้ฮาร์ดแวร์ RISC-V เป็นระบบปฏิบัติการโอเพ่นซอร์สที่รองรับ RISC-V และชุดคำสั่งได้รับการสนับสนุนในชุดเครื่องมือซอฟต์แวร์ยอดนิยมหลายตัว
> reference [source](https://electronics.stackexchange.com/questions/576154/where-is-the-ram-stored-on-a-risc-v-cpu) [price](https://www.eenewseurope.com/en/worlds-fastest-64bit-risc-v-core-claims-5ghz-speed/)

## 🌻 2. RP2040 
by Raspberry Pi Pico

Raspberry Pi เลข 2 ถัดมาคือจำนวน Core ของ MCU และเลข 0 ในหลักถัดมาคือชนิดของ Arm Core ที่เลือกใช้ 0 คือ M0+ นั้นเอง เลข 4 ตัวต่อมาคือจำนวนของ RAM  ค่านี้ได้จาก log2(RAM/16K) แล้วเอามาปัดเศษกลมๆ เลขสุดท้ายคือจำนวนของ Flash Memory ซึ่งใน RP2040 ไม่ได้ใส่มาเลขได้เลขเป็น 0

คุณสมบัติที่สำคัญของ RP2040 ที่แตกต่างจากไมโครคอนโทรลเลอร์ตัวอื่น คือ PIO หรือ Programmable Input/Output block

![Raspberry Pi](https://www.arm.com/blogs/blueprint/wp-content/uploads/2021/01/rp2040-2.jpg)
### ```Price```: 4 USD
### ```Speed```: 133 MHz
### ```Memory```: 16MB 
> reference [source](https://www.sparkfun.com/rp2040) [price](https://www.arm.com/blogs/blueprint/raspberry-pi-rp2040)

## 🌻 3. ATmega1608  
by AVR
ATmega1608 คือไมโคคอนโทนเลอร์ประกอบไปด้วย 8-bit AVR โปรเซสเซอร์พร้อมกับ hardware multiplier
ซีรีส์นี้ใช้ Core Independent Peripherals รุ่นล่าสุดพร้อมคุณสมบัติที่ใช้พลังงานต่ำ รวมถึง Event System, intelligent analog และอุปกรณ์ต่อพ่วงขั้นสูง

![AVR](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2F1owpf%2FbtqAqf2ykvT%2FGTK6Wk4jcA5KRtNk3a0IO0%2Fimg.jpg)
### ```Price```: 50.98 Bath
### ```Speed```: 20 MHz
### ```Memory```: 16 KB
> reference [source](https://www.microchip.com/en-us/product/ATMEGA1608#:~:text=ATmega1608%20is%20a%20microcontroller%20featuring,%2D%20and%2032%2Dpin%20packages.) [price](https://www.digikey.co.th/th/products/detail/microchip-technology/ATMEGA1608-AFR/9973116)


## 🌻 4. MCS-51 
by PIC
บริษัท Microchip Technology เป็นผู้ผลิต PIC(Peripheral Inerface Controller ) โดยมากแล้วไมโครคอนโทรลเลอร์ตระกูลนี้มักจะมีรูปร่างของ IC เป็นแบบขนาด 40 ขา ซึ่งแต่ละขาสัญญาณจะมีหน้าที่ที่ระบุชัดเจนตามสัญลักษณ์ชื่อย่อ ที่กำกับในแต่ละขา อย่างไรก็ตามจะมีบางขาสัญญาณที่อาจจะมีหน้าที่ได้มากกว่าหนึ่งอย่าง (ซึ่งเขียนกำกับไว้ว่า ALTERNATE FUNCTION) ซึ่งจะไม่สามารถใช้งานในเวลาเดียวกันได้ ตัวอย่างเช่นขาสัญญาณบิต 0 ของพอร์ต 3 (ใช้ตัวย่อเป็น P3.0) อาจจะใช้เป็นขาสัญญาณเอาต์พุตหรืออินพุตตามปกติ 

![PIC](https://micro-research.co.th/pub/media/catalog/product/cache/image/beff4985b56e3afdbeabfc89641a4582/m/t/mt-mcs51-a_5_1.jpg)
### ```Price```: MT-MCS51/S52 (MCU=AT89S52) = 545 Bath
### ```Speed```: 33 MHz
### ```Memory```: 8 kB
> reference [source](https://th.rs-online.com/web/p/microcontrollers/4671690) [price](https://micro-research.co.th/mt-mcs51.html)

 ## 🌻 5. ESP8266 NodeMCU WIFI V3 CH340
 ESP8266EX ถูกรวมเข้ากับโปรเซสเซอร์ Tensilica 32-bit อินเทอร์เฟซอุปกรณ์ต่อพ่วงดิจิตอลมาตรฐาน, สวิตช์เสาอากาศ, RF balun, เพาเวอร์แอมป์, แอมพลิฟายเออร์รับสัญญาณรบกวนต่ำ, ฟิลเตอร์และโมดูลการจัดการพลังงาน ทั้งหมดรวมอยู่ในแพ็คเกจเล็กๆ อันเดียว
 
 ![ESP8266](http://www.eak-electronic.com/image/cache/data/Product/Arduino/ESP8266%20Node%20MCU%20CH340-500x500.jpg)
### ```Price```: 130 Bath
### ```Speed```: 2.4 - 2.5 GHz
### ```Memory```: 4 M
> reference [source](https://www.espressif.com/en/products/socs/esp8266) [price](http://www.eak-electronic.com/index.php?route=product/product&product_id=1395)
