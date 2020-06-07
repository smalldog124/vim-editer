# Vim-editor

## ทำไมต้องใช้ Vim
เมื่อเราต้องการแก้ไข Configuration ของ Application หรือ Server config โดยทั่วไปแล้วจะไม่มีเครื่องมือ Notepad, Notepad++, VS-Code หรือ Text editer ต่างๆ ซึ่งตัว UNIX มี Vim-editor มาให้ใช้อยู่แล้วไม่ต้องโหลดเพิ่ม

## อะไรคือ Vim-editor
Vi IMproved หรือ Vim เป็นเครื่องมือแก้ไขเอกสารที่ติดมากับระบบปฏิบัตการ UNIX และ Apple OS แต่จะไม่ค่อยเป็นมิตรกับผู้เริ่มต้นเท่าไร เมื่อใช้ไประยะหนึ่งจะรู้สึกว่าเป็นอีกเครื่องมือที่มีประสิทธิภาพมากอีกหนึ่งตัว

<img src="https://i.stack.imgur.com/BN6vl.png" />

## เริ่มต้นใช้งาน Vim
หัวข้อได้รับจะเป็นวิธีการใช้งานที่เป็นพื้นฐาน ประกอบไปด้วย
- Command mode
- Insert mode
- Starting the vi editor
- Vi Editing commands
- Moving within a file
- Saving and Closing the file

### Commad mode
เป็น mode เริ่มต้นเมื่อเข้าใช้งาน Vim-editor จำเป็นต้องรู้ว่ามีคำสั่งอะไรบ้างที่ใช้ได้

สามารถ เลื่อน cursor และ cut, copy, paste ข้อความได้

สามารถสั่งให้บันทึกการเปลี่ยนแปละ และออกจาก editer ได้

คำสั่งเป็น case sensitive ดั้งนั้นระวังตัวพิมพ์เล็ก พิมพ์ใหญ่

### Insert mode
เป็น mode ที่เราสามารถแก้ไข, เพิ่ม, ลด ข้อความในไฟล์ได้

เข้า Insert mode โดยกดปุ่ม `i` ที่คีย์บอร์ดื 

เมื่ออยู่ใน Insert mode การกดปุ่มใดๆ เป็นการเป็นข้อความเข้าไปในไฟล์

ถ้าต้องการออกจาก Insert mode ให้กดปุ่ม esc จะกลับไปสู่ Command mode

### Starting the Vim editor
เปิด terminal ขึ้นมาแล้วย้ายไป workspace ของตัวเอง แล้วสร้างไฟล์ profile.txt
```
$ touch profile.txt
```
แก้ไขไฟล์ด้วย Vim
```
$ vi profile.txt
```

### Vi Editing commands
i : เข้าโหมด Insert ตำแหน่ง cursor 

a : เข้าโหมด Insert หลังตำแหน่ง cursor

A : เข้าโหมด Insert หลังบรรทัดของ cursor

ESC : ออกจาก Insert mode

u : Undo ย้อนกลับการเปลี่ยนแปลงครั้งล่าสุด

U : Undo ย้อนกลับ

o : เข้าโหมด Insert เริ่มบรรทัดใหม่

dd : ลบข้อความทั้งบรรทัด

3dd : ลบข้อความ 3 บรรทัด

D : ลบข้อความหลัง cursor

C : ลบข้อความหลัง cursor และเข้าสู่ Insert mode

dw : ลบคำ

x : ลบตัวหนังสือที่ cursor อยู่

R : แก้ไขข้อความโดยทับไปเลย

s : ลบตัวหนังสือตัวที่ cursor อยู่ พร้อมเข้า Insert mode
:/key-word : ค้นหาคำตาม key-word ในไฟล์

### Moving within a file
ย้าย cursor อยู่ในไฟล์สามารถใช้

k,ลูกศรขึ้น : ย้าย cursor ขึ้น

j,ลูกศรลง : ย้าย cursor ลง

h,ลูกศรซ้าย : ย้าย cusor ไปทางด้านซ้าย

l,ลูกศรขวา : ย้าย cusor ไปทางด้านขวา

### Saving and Closing the file
Shift+zz : บันทึกและออกจาก editor

:w : บันทึกและยังไม่ปิด editor

:q : ออกจาก editor โดยไม่มีการบันทึก

:wq : บันทึกและออกจาก editor

---
reference [https://vim.rtorr.com/lang/th](https://vim.rtorr.com/lang/th)
