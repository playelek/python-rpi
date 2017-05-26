## First Step Python

Environment

ใน Directory /home/pi เราสร้างโฟลเดอร์ชื่อ py\_projects ขึ้นมา

### String

'ข้อความ' หรือ "ข้อความ" ซึ่งทั้งสองแบบแสดงผลเหมือนกันไม่แตกต่าง และ """ข้อความ""" หรือ '''ข้อความ''' จะใช้กับข้อความหลายบรรทัด

#### ตัวอย่าง

แบบบรรทัดเดียว

`print ('Beautiful is better than ugly.')`

`print ("Explicit is better than implicit.")`

`print ('"Simple" is better than "complex".')`

`print ("'Complex' is better than 'complicated'.")`

แบบข้อความหลายบรรทัด

`print ("""Flat is better than nested.`

`Sparse is better than dense.`

`Readability counts.`

`Special cases aren't special enough to break the rules."""            
)`

### INDENTATION

ในหลายภาษามีการใช้ { } ปีกกาเพื่อจบคำสั่ง แต่ใน python ไม่เป็นอย่างนั้น การใช้งาน indent จึงเป็นสิ่งที่ต้องพึงระวังใน python เสมอ ในระบบปฏิบัติการต่างกันจะใช้ระยะ  tab ที่ต่างกัน ดังนั้นควรใช้ 1 indent = 4 space bar จะดีกว่าใช้ปุ่ม tab หากใช้ปนกันจะเกิด error ได้

### Comments

บ่อยครั้งที่เราต้องการทิ้งคำอธิบายไว้ในโค้ด โดยข้อความนั้นจะไม่ถูก execue ให้ใช้เครื่องหมาย \# \( number sign/hash/pound \) นำหน้าบรรทัด ซึ่งจะทำการ comment ไปจนสุดบรรทัด ใน Python ไม่มีระบบ comment แบบหลายบรรทัด ถ้าต้องการ comment หลายบรรทัดก็ต้องทำการใส่ \# นำหน้าทุกบรรทัดที่ต้องการ

#### **ตัวอย่าง**

##### อยู่ในบรรทัดเดียวกับโค้ด

`print ('Beautiful is better than ugly.') # ความงามล้ำค่ากว่าไร้ระเบียบ`

##### อยู่คนละบรรทัดกับโค้ด

`# ความชัดแจ้งมีความหมายกว่าทุกนัยยะ`

`print ('Explicit is better than implicit.')`

##### แบบหลายบรรทัด

`# ความเรียบง่ายสมบูรณ์กว่าซับซ้อน`

`# แต่ความซับซ้อนก็ยังดีกว่าความสับสน`

`print ('Simple is better than complex.')`

`print ('Complex is better than complicated.')`

### Numbers

ตัวเลขใน python มี 2 ประเภทคือ integers \( จำนวนเต็ม \) และ floats \( ทศนิยม \)

### Operators and Expressions

ใน python

* บวก, - ลบ, / หาร, \* คูณ, % modulo, &lt; น้อยกว่า, &gt; มากกว่า, &lt;=less-than-equal, &gt;=greater-than-equal

Order Of Operation

PEMDAS as PE\(M&D\)\(A&S\)

### 



