# การหาข้อมูล Kernel และ OS version ภายในเครื่อง

## 1. ใช้คำสั่ง netstat เพื่อแสดงการเชื่อมต่อทั้งหมดของผู้ใช้ 

> เราสามารถตรวจสอบ Kernel และ OS version ภายใน Linux OS ได้ โดยใช้คำสั่งดังต่อไปนี้

```
lsb_release -a
lsb_release -r
uname -a
hostnamectl
```

> เราสามารถตรวจสอบผ่านไฟล์ต่างๆเพื่อตรวจสอบ Kernel และ OS version ได้ โดยไฟล์มีดังต่อไปนี้

```
/etc/os-release
/etc/lsb-release
```

### ยกตัวอย่างการใช้งาน

```
lsb_release -a
```

### ตัวอย่างผลลัพธ์

![Screenshot 2024-05-29 100503](https://github.com/Atiwitch15101/Linux-Knowledge/assets/159407312/59838638-d91f-4ac8-ba3d-d9d06d7bae76)

```
uname -a
```

### ตัวอย่างผลลัพธ์

![Screenshot 2024-05-29 100654](https://github.com/Atiwitch15101/Linux-Knowledge/assets/159407312/6d61e6d7-a334-4b20-a3c2-d0e8dc3e1b0d)

## ตรวจสอบ flag จาก file ที่บ่งบอกถึง Kernel และ Linux version หาที่ไฟล์ที่อยู่ภายใต้ /etc/lsb-release

> เพื่อหาข้อมูลเกี่ยวกับ Kernel และ Linux version และตรวจสอบ flag จากไฟล์ `lsb-release` ซึ่งมักอยู่ที่ `/etc/lsb-release` คุณสามารถใช้คำสั่ง `cat` เพื่อดูเนื้อหาของไฟล์นั้นได้

### การใช้งาน

> ดูข้อมูลจากไฟล์ /etc/lsb-release

```
cat /etc/lsb-release
```

### ผลลัพธ์

![Screenshot 2024-05-29 101329](https://github.com/Atiwitch15101/Linux-Knowledge/assets/159407312/1389169c-3639-4d64-a033-64fa4f5e74d0)
