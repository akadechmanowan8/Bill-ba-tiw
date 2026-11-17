# ตั้งค่า Firebase

## โหมดปัจจุบัน: ทุกคนที่มีลิงก์ ดูและแก้ไขได้ (ไม่ต้องล็อกอิน)
Realtime Database → แท็บ Rules → วางโค้ดนี้ แล้วกด Publish

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

## ถ้าภายหลังอยากให้เจ้าของแก้ได้คนเดียว
1. ใน index.html เปลี่ยน `const REQUIRE_LOGIN = false;` เป็น `true`
2. Authentication → เปิด Email/Password → Add user (อีเมล+รหัสผ่านของคุณ) → คัดลอก User UID
3. แก้ Rules ตรง ".write" ของ bill_pa_tiw เป็น:
   "auth != null && auth.uid === 'UID-ของคุณ'"
