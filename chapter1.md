# ติดตั้ง Raspberry Pi

## อุปกรณ์ที่ต้องเตรียม

### Raspberry Pi

### Power Adapter

ช่องต่อPowerของRaspberry Piเป็นMicro USBดังนั้นPower Adapterของเราต้องมีหัวเป็นMicro USB

Output Voltage 5V dc

Output Current 700-1000 mA

### SD Card และ SD Card Adapter

ถ้าคอมพิวเตอร์ต้องมีฮาร์ดไดร์ฟ \( Hard Drive \) SD Card ก็เป็นเหมือนฮาร์ดไดร์ฟของ Raspberry Pi เราต้องติดตั้งระบบปฏิบัติการ \( Operating System - OS \) ลงใน SD Card อันนี้ และไฟล์ต่างๆของเราจะเก็บไว้ในนี้นั่นเอง

ความจุของ sd card

* เราต้องการ อย่างน้อย 8GB Class 4

ขนาดของ SD Card

* ใช้กับ Raspberry Pi รุ่นเก่าอย่าง Model A และ Model B ต้องใช้ SD Card ขนาดมาตรฐาน \( Standard size \) หรือ SD

ใช้กับ Raspberry Pi รุ่นใหม่ขึ้นมาตั้งแต่ Model A+, Model B+, Pi 2 Model B, Pi Zero และ Pi 3 Model B ต้องใช้ SD Card ขนาดไมโคร \( Micro size \) หรือ Micro SD

### จอภาพและอุปกรณ์ต่อกับจอภาพ

Raspberry Pi นั้นมี HDMI Port สำหรับต่อออกจอภาพ ถ้ามีจอที่มี HDMI port เราสามารถหาสาย HDMI-to-HDMI มาต่อจอได้เลย แต่ถ้าจอเราเป็น port แบบอื่น เช่น DVI ก็ให้หาสายที่เป็น HDMI-to-DVI มาใช้หรือ VGA ก็หาสาย HDMI-to-VGA

### Network

การใช้งาน Raspberry Pi จำเป็นต้องอินเตอร์เน็ต ซึ่งเราต้องใช้สาย Ethernet ต่อเข้ากับเครือข่ายของเรา หรือใช้ Wireless Dongle สำหรับเชื่อมต่อกับเครือข่ายที่เป็น wireless \( สำหรับ Raspberry Pi 3 Model B ไม่ต้อง wireless dongle เพราะมีในตัว \)

### คีย์บอร์ดและเมาส์

Raspberry pi มี USB port ดังนั้น ต้องใช้คีย์บอร์ดและเมาส์ที่เป็น USB Port หรือคีย์บอร์ดและเมาส์ที่เป็น USB Wireless ก็ใช้ได้เช่นกัน

## เตรียม SD Card

การติดตั้ง OS ลงใน SD Card มีอยู่ 2 วิธีคือ ติดตั้งด้วย NOOB กับติดตั้งด้วยไฟล์ Image ในเล่มนี้เราจะเล่าทั้งสองวิธี แต่ถ้าคุณเป็นมือใหม่มากๆละก็แนะนำวิธี NOOB ค่ะ

### วิธีติดตั้ง OS ด้วย NOOB

ดาวน์โหลด NOOBS

เราสามารถดาวน์โหลด NOOBS จากเว็บ [https://www.raspberrypi.org/downloads/noobs/](https://www.raspberrypi.org/downloads/noobs/) ในหน้านี้มี NOOBS กับ NOOBS Lite ซึ่ง NOOBS จะมี Raspbian มาให้ไม่ต้องดาวน์โหลดผ่านเน็ตทีหลัง แต่ NOOBS Lite ทุก OS ต้องโหลดผ่านเน็ตหมดตอนติดตั้งใน Pi ในตัวอย่างเราเลือก NOOBS ละกัน จะได้ไฟล์ .zip![](/assets/nbnoobs.jpg)Format SD Card

ดาวน์โหลดโปรแกรม SD Formatter [https://www.sdcard.org/downloads/formatter\_4/index.html](https://www.sdcard.org/downloads/formatter_4/index.html) มาติดตั้งในคอมพิวเตอร์ของเรา แล้วทำการ Format SD Card โดยใช้  SD Formatter

เลือก Drive ที่ต้องการ Format แล้วคลิก Format

![](/assets/Sketch5.png)

จะถามว่าต้องการจะ Quick Format ใช่ไหม ตอบ OK

![](/assets/Sketch6.png)

โปรแกรมจะบอกว่าอย่าถอดไดร์ฟออกขณะกำลัง Format นะ ตอบ OK

![](/assets/Sketch7.png)

โปรแกรมจะทำการ Format จนเสร็จ กด OK และ Exit เพื่อออกจากโปรแกรม

![](/assets/Sketch8.png)

ติดตั้ง NOOB บน SD Card

ไฟล์ NOOBS ที่เราได้จะเป็นไฟล์ .zip แตกไฟล .zip ออกจะได้ไฟล์ต่างๆดังรูปข้างล่าง \( ถ้าไม่มีโปรแกรมแตกไฟล์ zip ให้ดาวน์โหลดโปรแกรมมาติดตั้ง ในที่นี้แนะนำ 7zip [http://www.7-zip.org/ ](http://www.7-zip.org/)\)

Copy file ทั้งหมดจากไฟล์ zip ที่แตกออกมาไปวางไว้ในไดร์ฟของ SD Card อย่าให้ขาดแม้แต่ไฟล์เดียว

![](/assets/copynoobs.jpg)

![](/assets/Sketch10.png)

รอสักครู่ ไฟล์ก็จะถูก copy อยู่ใน SD Card เรียบร้อย

![](/assets/pastefinish.jpg)

การนำ SD Card ไปใช้กับ Raspberry Pi

นำ SD card ที่ลง NOOBS แล้วไปใส่ช่อง SD Card ของ Raspberry Pi ต่อพอร์ตต่างๆ คือ Ethernet , Mouse ,Keyboard, HDMI ต่อกับจอ monitor จากนั้นจึงต่อกับ Power Supply

เมื่อเสียบ Power หน้าจอจะขึ้นหน้าต่างให้เราเลือกว่าจะลง OS อะไร ในที่นี้เลือก Raspbian ที่บาร์ข้างล่างจะมีให้เลือกภาษาโดยตั้งต้นเป็น English \(UK\) ถ้าไม่ชินเปลี่ยนเป็น English \(US\) ก็ได้ ส่วน Keyboard เลือกเป็น US จะดีกว่าเพราะส่วนใหญ่คีย์บอร์ดไทยมันจะเรียงอักขระกับสัญลักษณ์แบบคีย์บอร์ด US \( เราเคยลืมเปลี่ยนแหละ ตั้ง keyboard เป็น UK ปรากฎว่าพิมพ์ @ แล้วดันได้เป็น ” งงอยู่แปบนึงก็..อ่อ...ลืมเปลี่ยนคีย์บอร์ด \) ตั้งค่าเสร็จกด Install ที่ปุ่มบนซ้าย

![](/assets/install1.jpg)

จะมีคำถามให้ยืนยันว่าจะติดตั้งนะ ก็ตอบ Yes

![](/assets/install2.jpg)

จากนั้นก็รอ...

![](/assets/install3.jpg)

เสร็จแล้วจะขึ้นหน้าต่าง OS\(es\) Installed Successfully กด OK ระบบจะทำการรีบูท

![](/assets/install5.jpg)

เมื่อรีบูทขึ้นมาใหม่แล้ว ก็จะเข้าสู่หน้า Desktop ของ Raspbian เป็นอันเสร็จ

![](/assets/install6.jpg)

## สิ่งที่ต้องทำหลังจากติดตั้งแล้ว

ทำให้ desktop มีขนาดเต็มจอ

บางคนลง Raspbian เสร็จแล้วพบว่า Desktop ไม่เต็มหน้าจอ ให้แก้ไขดังนี้ เปิด Terminal ขึ้นมา

พิมพ์ว่า` cd /boot `เพื่อเข้าไดเรคทอรี่ boot เลื่อน cusor มาที่ overscan เอาเครื่องหมาย \# ออก 

 Ctl+x ตอบ y และ enter เพื่อ save แล้วรีสตาร์ท



