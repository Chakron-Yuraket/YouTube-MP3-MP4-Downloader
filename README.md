
YouTube MP3 & MP4 Downloader

เว็บแอปพลิเคชันสำหรับดาวน์โหลดวิดีโอจาก YouTube ในรูปแบบไฟล์ MP4 และแปลงเป็นไฟล์เสียง MP3 สร้างขึ้นด้วย Node.js, Express, และใช้ FFmpeg สำหรับการประมวลผลไฟล์เสียง โปรเจกต์นี้ถูกออกแบบมาให้มีโครงสร้างที่เรียบง่ายและสามารถนำไป Deploy ใช้งานได้อย่างรวดเร็วผ่าน Docker


✨ คุณสมบัติหลัก (Features)

ดาวน์โหลดวิดีโอ (MP4): เลือกความละเอียดต่างๆ ของวิดีโอที่ต้องการดาวน์โหลด

แปลงเป็นเสียง (MP3): แปลงและดาวน์โหลดไฟล์เสียงจากวิดีโอในรูปแบบ MP3 คุณภาพ 128kbps

ส่วนติดต่อผู้ใช้ที่เรียบง่าย: ออกแบบให้ใช้งานง่าย ไม่ซับซ้อน

แสดงผลทันที: แสดงข้อมูลวิดีโอ, ภาพขนาดย่อ, และตัวเลือกการดาวน์โหลดหลังจากวางลิงก์

พร้อมสำหรับ Docker: มี Dockerfile สำหรับการสร้าง Image และนำไป Deploy บนแพลตฟอร์มที่รองรับ Container ได้ทันที

🛠️ เทคโนโลยีที่ใช้ (Tech Stack)

Backend: Node.js, Express.js

Template Engine: EJS (Embedded JavaScript templates)

YouTube Core: @distube/ytdl-core

Video/Audio Processing: fluent-ffmpeg

Deployment: Docker

🚀 วิธีการติดตั้งและใช้งานในเครื่อง (Local Setup)
สิ่งที่ต้องมี (Prerequisites)

Node.js: (แนะนำเวอร์ชัน 18.x ขึ้นไป) - ดาวน์โหลดที่นี่

FFmpeg: (จำเป็นสำหรับการแปลงไฟล์เป็น MP3) - ดาวน์โหลดที่นี่

หมายเหตุ: สำหรับการใช้งานในเครื่อง, โปรเจกต์นี้ใช้ @ffmpeg-installer/ffmpeg ซึ่งจะติดตั้ง FFmpeg ภายใน node_modules โดยอัตโนมัติ ทำให้ไม่จำเป็นต้องติดตั้ง FFmpeg แยกต่างหากในระบบ

ขั้นตอนการติดตั้ง

Clone a repository:

Generated bash
git clone https://github.com/your-username/your-repository.git


ไปยังโฟลเดอร์โปรเจกต์:

Generated bash
cd your-repository
IGNORE_WHEN_COPYING_START
content_copy
download
Use code with caution.
Bash
IGNORE_WHEN_COPYING_END

ติดตั้ง Dependencies:

Generated bash
npm install
IGNORE_WHEN_COPYING_START
content_copy
download
Use code with caution.
Bash
IGNORE_WHEN_COPYING_END

รันเซิร์ฟเวอร์:

Generated bash
node server.js
IGNORE_WHEN_COPYING_START
content_copy
download
Use code with caution.
Bash
IGNORE_WHEN_COPYING_END

เปิดเว็บเบราว์เซอร์แล้วไปที่ http://localhost:3000

🐳 การใช้งานผ่าน Docker

โปรเจกต์นี้มาพร้อมกับ Dockerfile ที่ช่วยให้คุณสามารถ build และ run แอปพลิเคชันใน container ได้

Build Docker image:

Generated bash
docker build -t youtube-downloader .
IGNORE_WHEN_COPYING_START
content_copy
download
Use code with caution.
Bash
IGNORE_WHEN_COPYING_END

Run Docker container:

Generated bash
docker run -p 3000:3000 youtube-downloader
IGNORE_WHEN_COPYING_START
content_copy
download
Use code with caution.
Bash
IGNORE_WHEN_COPYING_END

แอปพลิเคชันจะทำงานบน http://localhost:3000

☁️ การ Deploy

โปรเจกต์นี้ถูกออกแบบมาเพื่อการ Deploy บนแพลตฟอร์มที่รองรับ Docker ได้เป็นอย่างดี เช่น Render, Fly.io, หรือ Railway

ตัวอย่างการ Deploy บน Render:

เชื่อมต่อ Repository ของคุณกับ Render

สร้าง "New Web Service" ใหม่

ในหน้าตั้งค่า, เลือก Environment เป็น Docker

Render จะตรวจจับ Dockerfile และทำการ Build และ Deploy ให้โดยอัตโนมัติ

📜 สัญญาอนุญาต (License)

โปรเจกต์นี้อยู่ภายใต้ลิขสิทธิ์ของ MIT License - ดูรายละเอียดเพิ่มเติมได้ที่ไฟล์ LICENSE.