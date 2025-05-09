---
layout: project
type: project
image: img/oms-square.png
title: "OMS (Online Management System)"
date: 2024
published: true
labels:
  - Refine
  - TypeScript
  - Sequelize
  - Express.js
  - React.js
summary: "An integrated system for managing and tracking orders across multiple marketplaces by linking invoice, tracking, and order data to ensure accurate and efficient delivery."
---

<img class="img-fluid" src="../img/oms-header.png" alt="OMS Header">

---

## 🔍 Project Overview / รายละเอียดโปรเจกต์

**EN:**  
OMS is an internal web application designed to manage and track product delivery from the warehouse. It connects **Orders**, **Invoices**, and **Tracking data** to allow real-time updates and reduce human error.

**TH:**  
OMS เป็นระบบจัดการภายในที่ใช้สำหรับติดตามและบริหารจัดการ **คำสั่งซื้อ**, **ใบแจ้งหนี้**, และ **ข้อมูลการจัดส่ง** เพื่อให้สามารถอัปเดตสถานะการจัดส่งได้แบบเรียลไทม์ และลดข้อผิดพลาดในการดำเนินงาน

---

## 🎯 Objective / วัตถุประสงค์

- **EN:** Link invoice and tracking data with orders for efficient warehouse management  
- **TH:** เชื่อมโยงข้อมูลใบปะหน้าและใบแจ้งหนี้เข้ากับคำสั่งซื้อ เพื่อการจัดการคลังที่แม่นยำ

---

## 🚀 Key Features / ฟีเจอร์หลัก

### 📦 Order & Delivery Management / การจัดการคำสั่งซื้อและการจัดส่ง

- ✅ **Record Tracking**  
  EN: Track and log every shipping label  
  TH: บันทึกและติดตามเลขใบปะหน้าทุกรายการ

- ✅ **Invoice Verification**  
  EN: Sync invoice data from internal ERP  
  TH: ตรวจสอบความถูกต้องของใบแจ้งหนี้จากระบบภายใน

- ✅ **Tracking Status Update**  
  EN: Real-time status updates of each parcel  
  TH: อัปเดตสถานะ Tracking ในคลังสินค้าแบบเรียลไทม์

- ✅ **Multi-box per Tracking**  
  EN: Group multiple boxes under one tracking number (Lot)  
  TH: รองรับการจัดกล่องหลายใบภายใต้ Tracking เดียว

- ✅ **Tracking Dashboard**  
  EN: Display real-time summary by status per day  
  TH: แดชบอร์ดแสดงสรุปสถานะ Trackings รายวัน

---

### ⚙️ Master Data Management / การตั้งค่าเบื้องต้น

- ➕ **Stations**  
  EN: Add station codes from external systems manually  
  TH: เพิ่มรหัสสถานีโดยอ้างอิงจากระบบภายนอก (ไม่ผ่าน API)

- ➕ **Couriers**  
  EN: Add new delivery couriers freely  
  TH: เพิ่มชื่อบริษัทขนส่งได้อิสระ

- ➕ **Marketplace Platforms**  
  EN: Manage supported platforms (e.g. Shopee, Lazada)  
  TH: รองรับการเพิ่มแพลตฟอร์มเช่น Shopee, Lazada

- 📦 **Box Sizes**  
  EN: Add and manage different parcel box types  
  TH: จัดการประเภทและขนาดของกล่องสินค้า

- 🛠️ **Reasons**  
  EN: Add reasons for updates/cancellations  
  TH: ระบุเหตุผลสำหรับการแก้ไขหรือยกเลิกคำสั่งซื้อ

---

## 👥 User & Role Management / ระบบผู้ใช้และบทบาท

| User Code | Role    |
|-----------|---------|
| 11111     | Admin   |
| 22222     | Store   |
| 33333     | Manager |

**EN:** Each user is assigned a unique `User Code` and a single `Role` (e.g., admin, store, manager) to determine their level of access. No fine-grained permissions are implemented.

**TH:** ผู้ใช้แต่ละคนจะมี `User Code` เฉพาะ และบทบาทเดียว เช่น admin, store, manager เพื่อควบคุมสิทธิ์การเข้าถึงระดับฟีเจอร์ โดยไม่มีระบบกำหนดสิทธิ์รายฟังก์ชัน

---

## 🛠️ Tech Stack / เทคโนโลยีที่ใช้

- **Frontend:** React.js + Refine + TypeScript  
- **Backend:** Express.js + Sequelize (ORM)  
- **Database:** SQL Server  
- **Server:** IIS (Hosting) + PM2 (Process Manager)

---

## 📈 Expected Outcomes / ผลลัพธ์ที่คาดหวัง

- ✅ Improve delivery accuracy  
  → ลดข้อผิดพลาดในการจัดส่งสินค้า

- ✅ Centralize and unify data from multiple platforms  
  → เชื่อมโยงข้อมูลจากหลากหลายแพลตฟอร์มให้เป็นศูนย์กลาง

- ✅ Provide real-time insights via dashboard  
  → ให้ภาพรวมสถานะการจัดส่งแบบเรียลไทม์ผ่านแดชบอร์ด

---

## 🔐 Notes

> **EN:**  
> This project is private. The source code is not publicly available.  
> However, if you're interested in the system architecture or would like to discuss its development approach,  
> **feel free to reach out.**

> **TH:**  
> โครงการนี้เป็นโครงการส่วนตัว ซอร์สโค้ดยังไม่เปิดเผยต่อสาธารณะ  
> หากสนใจแนวคิดการออกแบบระบบ หรืออยากสอบถามแนวทางพัฒนา  
> **สามารถติดต่อเพิ่มเติมได้โดยตรง**

---
