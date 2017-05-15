## การตั้งค่าต่างๆที่แนะนำ

### เปลี่ยนรหัสผ่าน

ไปที่เมนู **Preferences** &gt; **Raspberry Pi Configuration**

![](/assets/raspberrypiconfig.png)

ที่แท็บ System กดปุ่ม Change Password... จะมีหน้าต่างขึ้นมาให้เปลี่ยนรหัสผ่าน โดยเราต้องใส่รหัสผ่านปัจจุบันใน Current Password ใส่รหัสผ่านใหม่ใน Enter New Password และยืนยันรหัสผ่านใหม่ใน Confirm new password จากนั้นกด OK

โดยชื่อผู้ใช้และรหัสผ่านที่เป็นค่าตั้งต้นของ Raspbian คือ Username : pi และ Password : raspberry

![](/assets/changepasswd.png)

### ทำให้ desktop มีขนาดเต็มจอ

บางคนลง Raspbian เสร็จแล้วพบว่า Desktop ไม่เต็มหน้าจอ ให้แก้ไขดังนี้ เปิด Terminal ขึ้นมา

พิมพ์ว่า`cd /boot`เพื่อเข้าไดเรคทอรี่ boot เลื่อน cusor มาที่ overscan เอาเครื่องหมาย \# ออก

Ctl+x ตอบ y และ enter เพื่อ save แล้วรีสตาร์ท

### ตั้งค่าวัน-เวลา

เนื่องจากเวลาตั้งต้นไม่ใช่เวลาตามประเทศไทยดังนั้นเรามาเปลี่ยนเวลาให้เป็นตามประเทศไทยกันก่อน

ไปที่เมนู **Preferences** &gt; **Raspberry Pi Configuration**

กดปุ่ม **Set Timezone... **แล้วเปลี่ยน Area เป็น **Asia** และเปลี่ยน Location เป็น **Bangkok**![](/assets/changetimezone.png)

### การเพิ่มคีย์บอร์ดภาษาไทย

ค่าตั้งต้นของ Raspbian จะเป็นคีย์บอร์ดภาษาอังกฤษ ถ้าเราต้องการใช้งานคีย์บอร์ดภาษาไทยเราก็ต้องทำการเพิ่ม Keyboard Layout เข้าไป

คลิกขวาที่ Task Bar จะมีเมนูขี้มาเลือก Panel Settings

![](/assets/keyboardlayout1.png)

จะขึ้นหน้าต่างชื่อ Panel Preferences เลือกแท็บ Panel Applets จะเห็นว่าในรายการไม่มี Keyboards Layout เราต้องเพิ่มเข้ามาก่อน กด Add

![](/assets/keyboardlayout2.png)

จะขึ้นหน้าต่าง Add plugin to panel เลือก Keyboard Layout Handler แล้วกดปุ่ม Add

![](/assets/keyboardlayout3.png)

จะเห็นว่า Keyboard Layout Handler ได้ถูกเพิ่มเข้ามาใน Panel Applets แล้ว และปรากฏรูปธงชาติที่มุมขวาบนของ Task Bar ด้วย

![](/assets/keyboardlayout4.png)

เพื่อเพิ่มภาษาไทย ในแท็บ Panel Applets เลือก Keyboard Layout Handler แล้วกดปุ่ม Preferences

จะขึ้นหน้าต่าง Keyboard Layout Handler ขึ้นมา เอาติ๊กที่ Keep system layouts ออก

![](/assets/keyboardlayout5.png)

ตั้งค่า Keyboard Model เป็น pc105 หรือ pc104 \( ส่วนใหญ่คีย์บอร์ดไทยใช้โมเดลนี้ \) ที่ Keyboard Layouts กด Add

หน้าต่าง Add Keyboard Layout เลือก th - Thai \(TIS-820.2538\) \( คีย์บอร์ด TIS-820 ได้รับการพัฒนามาจากแป้นแบบเกษมณี \) แล้วกด OK

![](/assets/keyboardlayout6.png)คีย์บอร์ดภาษาไทยจะถูกเพิ่มเข้ามาใน Keyboard Layouts คราวนี้เราต้องตั้งค่าปุ่มเปลี่ยนภาษา โดยกดเปลี่ยนใน Change Layout Option โดยปุ่มแบบไหนที่เราต้องการก็ติ๊ก อันที่ไม่ต้องการก็ติ๊กออก ในที่นี้เราเลือกตามความเคยชินของเราเองคือ Alt+Shift แล้ว OK

![](/assets/keyboardlayout7.png)

เรียบร้อยแล้วกดกากบาทปิด Keyboard Layout Handler

![](/assets/keyboardlayout8.png)

เท่านี้เราก็สามารถใช้ปุ่มสัลบภาษาที่ตั้งไว้สลับคีย์บอร์ดไทย-อังกฤษได้แล้ว

### การปิดเครื่อง

ใน Desktop 

ไปที่เมนู &gt; shutdown &gt; shutdown

หรือใช้คำสั่งใน Terminal

`sudo shutdown -h now`

