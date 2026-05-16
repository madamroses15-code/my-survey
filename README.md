# Document Management System : waneephan 🌹

เว็บแอปพลิเคชันแบบ Single Page Application สำหรับจัดการเอกสารเข้า-ออก พร้อมฟอร์มบันทึกข้อมูล, Dashboard, ค้นหา/กรองแบบ Real-time, แก้ไขข้อมูล, Print Preview, Export Excel และการเชื่อมต่อ Google Sheets ผ่าน Google Apps Script API

## วิธีใช้งาน

เปิด `index.html` ด้วยเบราว์เซอร์ หรือรันเซิร์ฟเวอร์แบบ static เช่น:

```bash
python3 -m http.server 4173
```

จากนั้นเข้า `http://127.0.0.1:4173`

## การเชื่อมต่อ Google Apps Script

ไปที่แท็บ **ตั้งค่า API** แล้วใส่ Google Apps Script Web App URL ระบบจะส่ง payload แบบ JSON ผ่าน `POST` โดยรองรับ action หลัก:

- `ping` สำหรับทดสอบการเชื่อมต่อ
- `list` สำหรับดึงข้อมูลจาก Google Sheets
- `create` สำหรับเพิ่มเอกสารและไฟล์แนบแบบ base64
- `update` สำหรับแก้ไขข้อมูล
- `delete` สำหรับลบข้อมูล

หากยังไม่ได้ตั้งค่า API ระบบจะบันทึกข้อมูลใน `localStorage` เพื่อให้ทดลองใช้งานได้ทันที
