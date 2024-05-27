# netstat command

### Metasploit Framework 

> คำสั่ง netstat ใน Kali Linux ใช้สำหรับแสดงข้อมูลเกี่ยวกับการเชื่อมต่อเครือข่าย, routing tables, interface statistics, masquerade connections, และ multicast memberships โดยสามารถดูสถานะการเชื่อมต่อทั้ง TCP, UDP, และ UNIX sockets ได้ เป็นเครื่องมือที่ช่วยในการตรวจสอบและแก้ไขปัญหาเครือข่ายได้อย่างมีประสิทธิภาพ

```
sudo netstat -tulnp
```
-t: แสดงการเชื่อมต่อ TCP
-u: แสดงการเชื่อมต่อ UDP
-l: แสดงพอร์ตที่เปิดใช้งานการรับฟัง (listening)
-n: แสดงหมายเลขพอร์ตแทนชื่อ
-p: แสดงโปรแกรมที่ใช้พอร์ตนั้น

### ตัวอย่างผลลัพธ์

![Screenshot 2024-05-27 152020](https://github.com/Atiwitch15101/Linux-Knowledge/assets/159407312/27881231-6103-4254-85e7-c731a4afd2ed)
