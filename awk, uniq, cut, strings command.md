# awk, uniq, cut, strings command

## awk command

> `awk` เครื่องมือประมวลผลข้อความและข้อมูล ใช้สำหรับค้นหาและจัดรูปแบบข้อมูลในไฟล์ข้อความ

> [!NOTE]
> Awk ถือเป็น script language อันหนึ่ง ซึ่งใช้เพื่อเปลี่ยนแปลงข้อมูลและสร้าง report ได้ โดย awk command เป็นตัวที่ช่วยได้มากในการจัดการข้อมูลในลักษณะต่างๆ ไม่ว่าจะเป็น
> - การ scan file แบบบรรทัดต่อบรรทัด
> - การแยกข้อความในแต่ละ line ให้เป็น field
> - การเปรียบเทียบระหว่าง input และ field กับ pattern
> - กระทำใดๆกับข้อความที่ตรงกับเงื่อนไข

### โดย syntax จะใช้เป็น

```
awk options 'selection _cDriteria {action }' input-file > output-file
```

### ตัวอย่างการใช้งาน awk

> ในการใช้ awk คู่กับ length เพื่อค้นหาบรรทัดที่มีความยาวมากที่สุดในไฟล์

```
awk 'length > max_length { max_length = length; longest_line = $0 } END { print longest_line }' flag.txt
```
> [!NOTE]
> - `length > max_length` ตรวจสอบว่าความยาวของบรรทัดปัจจุบันมากกว่าค่าความยาวสูงสุดที่เก็บไว้หรือไม่
> - `max_length = length` ถ้าใช่ ให้ปรับค่าความยาวสูงสุดเป็นค่าความยาวของบรรทัดปัจจุบัน
> - `longest_line = $0` เก็บบรรทัดที่ยาวที่สุดในตัวแปร longest_line
> - `END { print longest_line }` เมื่อประมวลผลทั้งหมดเสร็จสิ้น ให้พิมพ์บรรทัดที่ยาวที่สุด

### ผลลัพธ์

![Screenshot 2024-05-28 160927](https://github.com/Atiwitch15101/Linux-Knowledge/assets/159407312/71f2e569-3641-4e2a-942b-8e98682a336e)

## uniq command

> คำสั่ง `uniq` ใช้เพื่อกรองรายการซ้ำจากข้อมูลที่เรียงลำดับแล้ว โดยจะแสดงเฉพาะบรรทัดที่ไม่ซ้ำกัน

### ตัวอย่างการใช้งาน

```
sort flag.txt | uniq -u
```

> [!NOTE]
> - `sort flag.txt` คำสั่งนี้จะเรียงลำดับบรรทัดในไฟล์ flag.txt ตามตัวอักษร
> - `uniq -u` คำสั่งนี้จะกรองบรรทัดที่ไม่ซ้ำกันออกมา และ -u หมายถึงแสดงเฉพาะบรรทัดที่ไม่ซ้ำกันเท่านั้น

### ผลลัพธ์

![Screenshot 2024-05-28 163802](https://github.com/Atiwitch15101/Linux-Knowledge/assets/159407312/f4507dfe-55db-4a5c-b70f-fd73fcc1820c)


