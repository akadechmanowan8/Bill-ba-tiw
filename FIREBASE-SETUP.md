# ต่อ Firebase ให้ข้อมูลถาวร

1. Firebase Console → Realtime Database → แท็บ **Rules** → วางโค้ดนี้ แล้วกด **Publish**

{
  "rules": {
    ".read": false,
    ".write": false,
    "bill_pa_tiw": {
      ".read": true,
      ".write": true
    }
  }
}

2. แท็บ **Data** → คัดลอก URL ที่อยู่ด้านบน (ขึ้นต้น https:// ลงท้าย .firebasedatabase.app)
3. เปิด index.html → หาบรรทัด `const DB_URL = '';` → วาง URL ในเครื่องหมายคำพูด → บันทึก แล้วอัปขึ้น GitHub
