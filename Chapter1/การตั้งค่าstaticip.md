## ตั้งค่า IP address ให้เป็น Static IP Address 

บทความนี้เป็นการตั้งค่าใน OS Raspbian ที่อออกตั้งแต่พ.ค. 2015 เป็นต้นไปคือ Raspbian Jessie กับ Raspbian Wheezy 2015-05-05 ถ้าเก่ากว่านี้ต้องใช้วิธีตั้งค่าในไฟล์ /etc/network/interfaces

ใช้ Terminal พิมพ์คำสั่ง

`$ sudo ifconfig`

แสดงข้อมูลเน็ตเวิร์คปัจจุบันที่ถูกตั้งไว้ ข้อมูล inet, bcast, mask

![](/assets/rpistaticip1.jpg)

พิมพ์คำสั่ง

`$ sudo route -n`

เพื่อดูข้อมูลของเราเตอร์ของเรา จำค่า Gateway ไว้ เราต้องใช้มันกำหนด static router กับ static domain\_name\_servers

![](/assets/rpistaticip2.png)

เปิดไฟล์ /etc/dhcpcd.conf ขึ้นมา

`$ sudo nano /etc/dhcpcd.conf`

เลื่อนลงมาล่างสุดของโค้ดเพื่อเพิ่มบรรทัดใหม่เข้าไปดังตัวอย่าง

`interface eth0`

`static ip_address=192.168.1.222/24`

`static routers=192.168.1.20`

`static domain_name_servers=192.168.1.20`

interface = การกำหนดว่าจะกำหนด ip address ให้กับ network interface ไหน ถ้าเป็น Ethernet อย่างในตัวอย่างก็กำหนดเป็น eth0  แต่ถ้าเป็น wireless ก็กำหนดเป็น wlan0

static ip\_address = กำหนด IP address ที่เราต้องการ อย่าลืมเติม /24 ต่อท้ายด้วย

static routers = IP address ของ gateway อย่างเราใช้ที่บ้านก็ IP address เราเตอร์ที่บ้าน

static domain\_name\_servers = IP address ของ DNS เราใช้ที่บ้านก็ใช้ IP ของเราเตอร์ที่บ้าน

เสร็จแล้วก็กด ctrl+x แล้ว save โดยพิมพ์ y แล้ว Enter



ทำการีสตาร์ท

`$ sudo reboot`

เมื่อ RPI บูทขึ้นมา เปิด Terminal แล้วพิมพ์คำสั่ง

`$ ifconfig`

ก็จะเห็น IP address เป็นไปตามที่เรากำหนดแล้ว

![](/assets/rpistaticip3.jpg)

