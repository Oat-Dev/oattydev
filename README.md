## เริ่มใช้งาน

docker-compose up (ที่ root นอกสุด) สำหรับ API

yarn install และ yarn dev (ที่ root www) WWW

## services

WWW : http://localhost:8000

## build

- Merge code เข้า branch develop -> master
- เมื่อเสร็จแล้ว ให้ ssh เข้า server cd เข้า oattydev
- run git pull origin master
- run docker-compose up --build -d
