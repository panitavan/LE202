# อธิบายการทำงานของการแสดงตัวอักษร PR บน OUTPUT (C0000000) ของ RISC-V software simulator

1. เมื่อเรากด run คำสั่งที่ 1 เข้ามาและคำสั่งจะถุกป้อนเข้ามาทั้งหมด 1 word (4 byte) และนำมาเรียงใหม่ โดยคำสั่งจะถูกนำมาวางไว้ตรง Bus 
และจะถูกเลื่อนมาทางขวาเพื่อนำไปแปลเป็นคำสั่งที่ Instruction ในที่นี้คือ addi (addimmediate) หลังจากนั้นนำข้อมูลของ X0 เข้ามา นำมาบวกกับค่าที่อ่านได้จาก Instruction 
ในที่นี้คือ 00000020 เพราะฉะนั้นผลลัพธ์ที่ได้คือ 00000020 ให้นำมาเก็บไว้ที่ X1 ตรงที่ General-purpose regs ก็จะถือว่าเป็นการจบคำสั่งที่ 1
---
2. คำสั่งที่ 2 ถูกเรียกมา 1 word และคำสั่งจะถูกนำมาวางไว้ตรง Bus และถูกเลื่อนไปทางขวาเพื่อนำไปแปลคำสั่ง เช่นเดิม ในที่นี้จะอ่านได้คำสั่ง lui(load upper immediate) 
หลังจากนั้นนำค่าที่อ่านได้ไปแทนด้านบน จะได้ผลลัพธ์คือ C0000000 นำไปเก็บไว้ X2 ถือว่าเป็นการจบคำสั่งที่ 2
---
3. คำสั่งที่ 3 ถูกเรียกมา 1 word และคำสั่งจะถูกนำมาวางไว้ตรง Bus และถูกเลื่อนไปทางขวาเพื่อนำไปแปลคำสั่ง เช่นเดิม ในที่นี้จะอ่านได้คำสั่ง lbu(load byte unsigned) 
ซึ่งจะนำ Address 00000000 มาบวกกับ 00000020 ผลลัพธ์จะได้  00000020 นำ address นี้ไปชี้ที่ไว้ที่หน่วยความจำและไปเอามา 1 byte(00000050) นำมาเก็บไว้ที่ X3 ถือว่าเป็นการจบคำสั่งที่ 3
---
4. คำสั่งที่ 4 ถูกเรียกมา 1 word และคำสั่งจะถูกนำมาวางไว้ตรง Bus และถูกเลื่อนไปทางขวาเพื่อนำไปแปลคำสั่ง เช่นเดิม ในที่นี้จะอ่านได้คำสั่ง beq(branch if equal)
ซึ่งคำสั่งนี้จะเช็คว่าผลลัพธ์มีค่าเท่ากับศูนย์หรือไม่ โดยเอา 0000000c มาบวกกับ 00000010 จะได้ 0000001c
---
5. คำสั่งที่ 5 ถูกเรียกมา 1 word และคำสั่งจะถูกนำมาวางไว้ตรง Bus และถูกเลื่อนไปทางขวาเพื่อนำไปแปลคำสั่ง เช่นเดิม ในที่นี้จะอ่านได้คำสั่ง sb(store byte)
นำข้อมูลจาก X2 (C0000000) มาบวกกับ 00000000 จะได้ผลลัพธ์เท่ากับ C0000000 นำไปชี้ไว้ที่หน่วยความจำ และนำ X3 ไปชี้ไว้ที่หน่วยความจำด้วยเช่นกัน จะได้ 50 ออกมาจะได้เป็นตัวอักษร P
---
ลูปที่ 2 จะได้ดังนี้
---
6. คำสั่งที่ 6 จะเริ่มทำการลูปใหม่ซึ่งจะถูกเรียกมา 1 word จากนั้นคำสั่งจะถูกนำมาวางไว้ตรง Bus และถูกเลื่อนไปทางขวาเพื่อนำไปแปลคำสั่ง เช่นเดิม ในที่นี้จะอ่านได้คำสั่ง addi (addimmediate)
และนำค่า X1 (00000020) ซึ่งเป็นค่าเดิม มาบวกกับ 00000001 จะได้ผลลัพธ์ใหม่เท่ากับ 00000021 ให้นำไปเก็บไว้ที่ X1 แทนค่าเดิม
---
7. คำสั่งที่ 7 ถูกเรียกมา 1 word และคำสั่งจะถูกนำมาวางไว้ตรง Bus และถูกเลื่อนไปทางขวาเพื่อนำไปแปลคำสั่ง เช่นเดิม ในที่นี้จะอ่านได้คำสั่ง jal(jump and link)
นำค่าที่ได้ (fffffff0) ไปบวกกับ 00000018 จาก program counter ซึ่งจะได้ผลลัพธ์ดังนี้ 00000008 นำผลลัพธ์ที่ได้ไปเก็บไว้ที่ program count และหน่วยความจำ
---
8. คำสั่งที่ 8 ถูกเรียกมา 1 word ซึ่งข้อมูลนำมาจากแถว 00000008 และคำสั่งจะถูกนำมาวางไว้ตรง Bus และถูกเลื่อนไปทางขวาเพื่อนำไปแปลคำสั่ง เช่นเดิม ในที่นี้จะอ่านได้คำสั่ง lbu(load byte unsigned)
หลังจากนั้นนำค่าของ X1 (00000021) มาบวกกับ ค่าที่อ่านได้คือ 00000000 จะได้ผลลัพธ์เท่ากับ 00000021 นำไปชี้ไว้ที่หน่วยความจำ หลังจากนั้นไปเอามา 1 byte(00000052) นำมาเก็บไว้ที่ X3 
---
9. คำสั่งที่ 9 ถูกเรียกมา 1 word และคำสั่งจะถูกนำมาวางไว้ตรง Bus และถูกเลื่อนไปทางขวาเพื่อนำไปแปลคำสั่ง เช่นเดิม ในที่นี้จะอ่านได้คำสั่ง beq(branch if equal) 
หลังจากนั้นนำค่าที่ได้จาก program counter (0000000c) มาบวกกกับ ค่าได้ที่จากการแปลคือ 00000010 ผลลัพธ์ที่ได้จะเท่ากับ 0000001c หลังจากนั้นนำค่า X0 มาเทียบกับค่า X3 ไม่เท่ากับศูนย์
---
10. คำสั่งที่ 10 ถูกเรียกมา 1 word และคำสั่งจะถูกนำมาวางไว้ตรง Bus และถูกเลื่อนไปทางขวาเพื่อนำไปแปลคำสั่ง เช่นเดิม sb(store byte) หลังจากนั้นนำค่าที่อ่านได้ (00000000) 
นำมาบวกกับค่า X2 (c0000000) จะได้ผลลัพธ์เท่ากับ c0000000 นำไปชี้ไว้ที่หน่วยความจำและนำ X3 ไปชี้ไว้ที่หน่วยความจำด้วยเช่นกัน จะได้ 52 ออกมาจะได้เป็นตัวอักษร R