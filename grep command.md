# grep command

> Grep command คือคำสั่งที่ใช้ในการค้นหาคำ โดยปกติแล้วจะใช้เพื่อค้นหาว่าไฟล์ไหนมีคำที่เราต้องการหรือไม่ และถ้ามีจะอยู่ที่บรรทัดไหน ซึ่ง grep command นั้นเป็นหนึ่งในคำสั่งที่ถูกใช้และมีประโยชน์ที่สุดใน Linux และ Unix

> [!NOTE]
> คำสั่ง grep นั้นจะมี syntax เป็น
> ```
> grep <option> <word> <file>
> ```
> - `<option>` คือ option ของ grep
> - `<word>` คือคำที่เราต้องการค้นหา
> - `<file>` คือไฟล์ที่เราต้องการทดสอบที่จะค้นหา โดย `<file>` นั้นไม่จำเป็นต้องเป็นไฟล์เดียว อาจจะเป็นการค้นหาในหลายๆไฟล์พร้อมกันได้ก็ได้เช่นกัน

## การค้นหาเบื้องต้น

> หากเราต้องการค้นหาคำว่า security จากไฟล์ที่ชื่อว่า /etc/secplayground จะใช้คำสั่งเป็น

```
grep security /etc/secplayground
```

> หรือหากต้องการค้นหาคำว่า root ภายใน /etc/passwd จะใช้คำสั่งเป็น

```
grep root /etc/passwd
```

## การค้นหาแบบ recursively

> หากเราต้องการค้นหาแบบที่ไล่เข้าไปเรื่อยๆจนกระทั่งถึง directory ภายในสุด จะใช้ -r option ยกตัวอย่างคำสั่งในการค้นหาไฟล์ใดๆที่มีคำว่า noob ที่อยู่ภายใต้ /var จะใช้คำสั่งเป็น

```
grep -r "noob" /var
```

> หรือ

```
grep -R "noob" /var
```

> โดยจะแตกต่างกันคือ -R นั้นจะไล่ตาม symlink ไปด้วย

### ตัวอย่างผลลัพธ์

![Screenshot 2024-05-28 103831](https://github.com/Atiwitch15101/Linux-Knowledge/assets/159407312/3b4718f2-b0b8-482c-a2ea-2e67427ac733)