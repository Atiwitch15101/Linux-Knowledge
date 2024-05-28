# Hard link และ symbolic link

> การสร้าง symbolic link (symlink) ให้กับไฟล์ `target.txt` และวางไว้ที่ `/tmp/target.txt` สามารถทำได้โดยใช้คำสั่ง `ln -s` หลังจากนั้นสามารถเข้าถึงและดูเนื้อหาของไฟล์ `/tmp/flag.txt` ได้ด้วยคำสั่ง `cat`

### ขั้นตอนการสร้าง symbolic link และตรวจสอบ flag:

1. สร้าง symbolic link จาก `target.txt` ไปที่ `/tmp/target.txt`

```
ln -s /home/noob/target.txt /tmp/target.txt
```

2. ตรวจสอบว่าการสร้าง symbolic link สำเร็จ

```
ls -l /tmp/target.txt
```

3.เมื่อสร้าง symbolic link ที่ target.txt แล้วไว้ที่ /tmp/target.txt จากนั้นจะพบ flag ที่อยู่ใน /tmp/flag.txt

```
cat /tmp/flag.txt
```

### ตัวอย่างผลลัพธ์

![Screenshot 2024-05-28 102726](https://github.com/Atiwitch15101/Linux-Knowledge/assets/159407312/6d800457-b841-43f8-b4d6-cc205e870f2e)
