---
layout: project
type: project
image: img/seq-square.png
title: "Sequential Generator"
date: 2025
published: true
labels:
  - Node.js
  - JavaScript
  - npm
  - Open Source
summary: "โมดูล Node.js สำหรับสร้างรหัสลำดับที่ไม่ซ้ำกัน พร้อมคำนำหน้าวันที่ที่ปรับแต่งได้และรองรับเขตเวลา"
---

# Sequential Generator

<div style="text-align: center;">
  <img src="../img/seq-generator-header.png" alt="Sequential Generator Banner">
</div>

## 🛠 Sequential Generator คืออะไร?

ในแอปพลิเคชันขนาดเล็ก เรามักต้องการระบบสร้างรหัสเอกสาร เช่น ใบแจ้งหนี้ (`INV`) หรือคำสั่งซื้อที่มีวันที่และลำดับที่ชัดเจน **Sequential Generator** ถูกออกแบบมาเพื่อให้:

- **รหัสไม่ซ้ำกัน** เป็นการนับต่อจากเลขเดิม
- **เรียงลำดับได้** ตามลำดับเอกสารรายวัน
- **ระบุวันที่ได้**
- **รองรับ TimeZone** เช่น `Asia/Bangkok`, `UTC` โดยที่ module ใช้งาน [`day.js`](https://day.js.org/)

## 🚀 วิธีใช้งาน

[sequential-generator](https://www.npmjs.com/package/sequential-generator) เป็นโมดูล Node.js โอเพนซอร์สสำหรับสร้างรหัสเอกสารอัตโนมัติ พร้อมคำนำหน้าวันที่ที่ปรับแต่งได้

ตัวอย่าง:  
```plaintext
SEX2505140001 → รหัสที่สร้างเมื่อ 14 พฤษภาคม 2025 พร้อมคำนำหน้า "SEX" และลำดับ "0001"
```

## 🔑 คุณสมบัติ
- ✔ รูปแบบ – กำหนด {prefix}{date}{sequence} 
- 🌍 รองรับ TimeZone – กำหนดเขตเวลาใดก็ได้ (Asia/Bangkok, America/New_York)
- 📅 รูปแบบวันที่ยืดหยุ่น – เลือกรูปแบบ เช่น YYMMDD, YYYYMM เป็นต้น
- 🔢 ความยาวลำดับที่กำหนดได้ – เช่น 0001 สำหรับ 4 หลัก
- 🛠 เครื่องมือตรวจสอบ – ตรวจสอบรหัสและแยกวันที่จากรหัสที่มีอยู่
- ⏭ สร้างรหัสถัดไปอัตโนมัติ – คำนวณรหัสลำดับต่อไปได้

``` js
const SequentialGenerator = require('sequential-generator');

// ตั้งค่าตามต้องการ
const generator = new SequentialGenerator({
  prefix: 'INV',
  dateFormat: 'YYMMDD',
  sequenceLength: 4,
  timezone: 'Asia/Bangkok'
});

// สร้างรหัสใหม่
const invoiceNumber = generator.generate();
// => INV2505140001

// รับรหัสลำดับถัดไป
const nextInvoice = generator.next(invoiceNumber);
// => INV2505140002

// ตรวจสอบความถูกต้องของรหัส
const isValid = generator.validate(invoiceNumber);
// => true
```


