# Change Preventers
* กลิ่นเหล่านี้หมายความว่าเมื่อคุณต้องการเปลี่ยนแปลงโค้ดแค่ที่เดียว แต่คุณต้องทำการเปลี่ยนแปลงหลายอย่างในที่อื่นด้วย ส่งผลการพัฒนาโปรแกรมมีความซับซ้อนและมีราคาแพงกว่ามาก
## Divergent Change
* Divergent Change คล้ายกับ Shotgun Surgery แต่เป็นกลิ่นที่ตรงกันข้าม Divergent Change คือเมื่อมีการเปลี่ยนแปลงหลายอย่างในคลาสเดียว Shotgun Surgery หมายถึงเมื่อมีการเปลี่ยนแปลงครั้งเดียวในหลายคลาสพร้อมกัน
* Signs and Symptoms (สัญญาณและอาการ)
    * เมื่อต้องเปลี่ยน method มากมายที่ไม่เกี่ยวข้องตอนทำการเปลี่ยนแปลงในคลาส ตัวอย่างเช่นเมื่อเพิ่ม product type ใหม่คุณต้องเปลี่ยน method เพื่อค้นหา และแสดง product นั้นๆ
* Reasons for the Problem (สาเหตุของปัญหา)
    * บ่อยครั้งที่การปรับเปลี่ยนที่แตกต่างกันเหล่านี้เกิดจากโครงสร้างโปรแกรมที่ไม่ดีหรือเรียกว่า "copypasta programming"
* Treatment (การรักษา)
    * แยกพฤติกรรมของคลาสผ่าน [Extract Class](https://sourcemaking.com/refactoring/extract-class)
    * หากคลาสต่างๆมีพฤติกรรมเหมือนกันคุณอาจต้องการรวมคลาส ( [Extract Superclass](https://sourcemaking.com/refactoring/extract-superclass) และ [Extract Subclass](https://sourcemaking.com/refactoring/extract-subclass) )
* Payoff (ผลตอบแทน)
    * ช่วยให้จัดการกับโค้ดได้ดีขึ้น
    * ลดความซ้ำซ้อนของโค้ด
    * ลดความยุ่งยากในการสนับสนุน
## Shotgun Surgery
* Signs and Symptoms (สัญญาณและอาการ)
    * การปรับเปลี่ยนที่ต้องทำการเปลี่ยนแปลงเล็กๆ น้อยๆ กับคลาสต่างๆ 
* Reasons for the Problem (สาเหตุของปัญหา)
    * ความรับผิดชอบเดียวได้ถูกแบ่งออกเป็นคลาสจำนวนมาก สิ่งนี้สามารถเกิดขึ้นได้หลังจากการใช้ **Divergent Change** มากเกินไป
* Treatment (การรักษา)
    * ใช้ [Move Method](https://sourcemaking.com/refactoring/move-method) และ [Move Field](https://sourcemaking.com/refactoring/move-field) เพื่อย้ายพฤติกรรมคลาสที่มีอยู่ไปยังคลาสเดียว หากไม่มีคลาสที่เหมาะสมสำหรับสิ่งนี้ให้สร้างใหม่
* Payoff (ผลตอบแทน)
    * ทำให้การจัดการและบำรุงรักษาง่ายขึ้น
    * ลดความซับซ้อนของโค้ด
