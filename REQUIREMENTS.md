---
project: MUVFAST — Home page redesign (+ Unit details)
client: MUVFAST (muvfast.com — แพลตฟอร์มเช่าที่พักรายเดือนในไทย)
channel: ยังไม่ระบุ
status: drafting (Home 3 ดราฟต์)
created: 2026-10-06
updated: 2026-10-06
---

# Requirements: MUVFAST Home

## 1. สรุปงาน
- ลูกค้า: MUVFAST แพลตฟอร์มเช่าคอนโด/เซอร์วิสอพาร์ตเมนต์รายเดือนในกรุงเทพฯ กลุ่มหลักคือผู้เช่าต่างชาติ (expat) + เจ้าของห้อง (Landlord) + Agent
- เป้าหมาย: ออกแบบหน้า Home ใหม่ อ้างอิงเว็บเดิม https://www.muvfast.com/en เป็นหลัก ให้ "คลีนๆ"
- งานก่อนหน้าใน repo: `index.html` = หน้า Unit details (ได้คอมเมนต์ลูกค้าใน `comment unit details.pdf`)
- ภาษา: EN เป็นหลัก มีปุ่มสลับ EN / TH

## 2. ขอบเขต
**อยู่ใน (รอบนี้):**
- หน้า Home 3 ดีไซน์ (ดราฟต์ HTML) ให้ลูกค้าเลือก
- Responsive Desktop + Mobile

**ยังไม่ชัด / รอลูกค้า:**
- ส่วนที่จะเพิ่มในหน้า Home → ลูกค้าบอกว่า "เดี๋ยวส่งให้"
- หน้า Unit details แก้ตามคอมเมนต์ (งานแยก)

## 3. ราคา / เงื่อนไข
- แพ็กเกจ: ยังไม่ระบุ
- งบ: ยังไม่ระบุ
- จำนวนรอบแก้: ยังไม่ระบุ
- Deadline: ยังไม่ระบุ

## 4. ดีไซน์ (จากลูกค้า)
- โทน: คลีน เรียบ **สีไม่เยอะ** ("เล่นสีเยอะไป ลูกกวาดไปหน่อย", "ขอเรียบๆ")
- สีแบรนด์: ส้มจากโลโก้ #FC4A1A (ใช้เป็นสีเน้นสีเดียว)
- โลโก้: ใช้โลโก้ที่ลูกค้าทำมา (logo.svg) **วางกลาง header**
- เมนูหลัก: โลโก้ / Landlord / Agent / EN-TH / Sign in — ไม่ต้องก๊อปเมนูเว็บเดิม
- Ref การวาง main menu รูปภาพ และ headline: apartments.com, zillow.com
- ฟอนต์แบรนด์ที่ลูกค้าใช้: CoStar Brown (ไฟล์ยังไม่มีใน repo → ใช้ฟอนต์ฟรีแนวใกล้เคียงในดราฟต์)
- ทุกการ์ดห้องต้องมี "min stay … mth" ให้เด่น (แปะบนรูปได้)
- การ์ดห้องฉบับย่อ (ทุกลิสต์):
  1. min stay + ราคา
  2. BR / BA / sqm / floor
  3. ชื่อโครงการ
  4. เขต, จังหวัด
- FAQ อยู่ท้ายหน้า

## 5. โครงหน้า Home (อิง muvfast.com/en)
1. Header (Landlord · Agent | โลโก้กลาง | EN/TH · Sign in)
2. Hero: "Thailand Monthly Property Rentals" + Easy / Secure / Expert + ช่องค้นหา (Location, Move-in, Duration, Budget/month)
3. 4 จุดเด่น: Book from Anywhere / Secure Booking / Move-in Protection / Local Expert Support
4. Discover Your Lifestyle Home in Bangkok (12 หมวด)
5. Featured rentals in Bangkok (การ์ดห้องฉบับย่อ)
6. FAQ (8 คำถามจากเว็บเดิม)
7. Footer (ที่อยู่ เบอร์ อีเมล LINE โซเชียล Solutions Privacy/Terms)
+ ส่วนที่ลูกค้าจะส่งมาเพิ่ม

## 6. Assets
| รายการ | สถานะ | หมายเหตุ |
|---|---|---|
| โลโก้ | มี | logo.svg (#FC4A1A) |
| ฟอนต์ CoStar Brown | ยังไม่มี | fonts/README.md รอไฟล์ |
| รูปภาพจริง | ยังไม่มี | ดราฟต์ใช้ Unsplash ชุดเดียวกับหน้า Unit details |
| รายการห้อง/ราคาจริง | ยังไม่มี | ใช้ข้อมูล demo ติดป้าย demo |
| คำตอบ FAQ | มีแค่ข้อค่าธรรมเนียม | ข้ออื่นเว้นไว้ "รอเนื้อหาจาก MUVFAST" |
| ข้อมูลติดต่อ | มี | จาก footer muvfast.com |
| ส่วนที่จะเพิ่ม | รอ | ลูกค้าจะส่ง |

## 7. เทคนิค
- ดราฟต์: HTML/CSS ไฟล์เดียวต่อแบบ ไม่ใช้ Tailwind CDN (เปิดดูได้แม้ออฟไลน์ ยกเว้นรูป/ฟอนต์/ไอคอน)
- ไอคอน: Phosphor (CDN)
- ไฟล์ดราฟต์ (แยกไฟล์ ไม่ใช้ index.html): muvfast/home-a-open-search.html, home-b-split-listing.html, home-c-quiet-type.html
- ปลายทางจริง: ยังไม่ระบุ (เว็บเดิมเป็น Next.js)

## 8. ข้อที่ยังไม่ชัด
- [ ] ส่วนที่จะเพิ่มในหน้า Home (ลูกค้าจะส่ง)
- [ ] แพ็กเกจ / งบ / deadline / รอบแก้
- [ ] ปลายทาง: ส่งเป็น HTML ให้ทีม dev ลูกค้า หรือขึ้น WordPress?
- [ ] ไฟล์ฟอนต์ CoStar Brown
- [ ] คำตอบ FAQ ครบ 8 ข้อ
- [ ] รูปและรายการห้องจริงสำหรับ Featured

## 9. ประวัติการตัดสินใจ
- 2026-10-06: Home อิง muvfast.com/en โทนคลีน ทำ 3 ดีไซน์ (A Open Search / B Split Listing / C Quiet Type) ใช้กฎเมนู/โลโก้/การ์ดจากคอมเมนต์หน้า Unit details
- 2026-10-06: Apex ขอให้ดราฟต์ Home เป็นไฟล์ .html แยก ไม่ใช้ index.html → ย้ายเป็น home-a/b/c-*.html ที่ root ของ muvfast (index.html = หน้า Unit details เดิม)

## 10. เช็กลิสต์ส่งมอบ
- [ ] 3 ดราฟต์ผ่านเทสต์ 1440 / 390
- [ ] Apex ตรวจ + อนุญาต deploy
- [ ] ลูกค้าเลือกดีไซน์
- [ ] ใส่ส่วนที่ลูกค้าเพิ่ม
- [ ] ลบป้าย demo ตอนทำจริง
