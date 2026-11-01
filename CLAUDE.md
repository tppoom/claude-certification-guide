# Claude Certification Guide — Project Instructions

## Auto-Publish & Git Sync Rule (กฎเหล็กประจำโปรเจกต์)
- **GitHub Repository:** `https://github.com/tppoom/claude-certification-guide` (remote: `origin`, branch: `main`)
- **GitHub Pages Live URLs:**
  - Portal รวม (CCDV-F + CCAR-P): `https://tppoom.github.io/claude-certification-guide/` (`guide-th.html`)
  - เฉพาะ CCDV-F: `https://tppoom.github.io/claude-certification-guide/ccdv-f/guide-th.html`
  - เฉพาะ CCAR-P: `https://tppoom.github.io/claude-certification-guide/ccar-p/guide-th.html`
- **ทุกครั้งที่มีการแก้ไขเนื้อหาหรือไฟล์ HTML ในโปรเจกต์นี้:**
  1. ต้องอัปเดตทั้งไฟล์แยก (`ccdv-f/guide-th.html` หรือ `ccar-p/guide-th.html`) และไฟล์พอร์ทัลรวม (`guide-th.html`) ให้ตรงกันเสมอ
  2. **ต้องสั่ง `git add`, `git commit`, และ `git push origin main` ทันทีทุกครั้งหลังแก้ไขเสร็จ** เพื่อให้หน้าเว็บ GitHub Pages อัปเดตตามเสมอโดยไม่ต้องรอให้ผู้ใช้ทวงถาม
