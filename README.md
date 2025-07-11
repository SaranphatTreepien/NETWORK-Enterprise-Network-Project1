##Enterprise Network Project #1 🌐🖧📡⚙️📈

#🖼️ PREVIEW
<p align="center">
  <img src="https://github.com/user-attachments/assets/05fb4ba2-674c-477a-8c9d-67d3c1572e28" width="600"/>
  <br/>
  <img src="https://github.com/user-attachments/assets/7e8cebcb-0c1c-45d7-bab2-aa123470c25b" width="600"/>
  <br/>
  <img src="https://github.com/user-attachments/assets/30670a2c-4c56-44c5-848e-4b1d860e5287" width="600"/>
  <br/>
  <img src="https://github.com/user-attachments/assets/fad07cfe-f38b-481b-a3dc-2ec3c7c91b7c" width="600"/>
</p>


#โจทย์
<p align="center">
  <img src="https://github.com/user-attachments/assets/8d763c37-7843-446a-9ad3-fdd2a289ac24" width="600"/> <br/>
</p>
#การคำนวณ
Network Address = 192.168.40.0           // เครือข่ายหลักที่ได้รับมา ใช้เป็นจุดเริ่มต้นของการแบ่ง Subnet
No. of subnets = 2                       // ต้องการแบ่งเครือข่ายออกเป็น 2 ส่วน (เช่น แผนก Accounts และ Delivery)

2^n = no.of subnet ==== 2^n=2           // ใช้สูตร 2^n เพื่อหาจำนวน Subnet ที่ต้องการ (ในที่นี้ n = 1)
N=1                                      // ยืม 1 bit จาก host portion เพื่อสร้าง Subnet
11111111.11111111.11111111.10000000      // แสดง Subnet Mask ในรูปแบบ Binary (25 บิตแรกเป็น Network)
255.255.255.128 ==> subnet mask          // รูปแบบ Subnet Mask แบบ Decimal (/25)

1'Subnet == ACCOUNT                      // Subnet แรกใช้สำหรับแผนก Accounts
Subnet mask = 255.255.255.128            // ใช้ Subnet Mask /25 หรือ 255.255.255.128
network ID = 192.168.40.0                // เป็น Network ID ของ Subnet แรก (ใช้เพื่อบอกว่าเป็นเครือข่ายย่อยนี้)
Range of Valid Host = 192.168.40.1 - 192.168.40.126   // ช่วง IP ที่ใช้ได้จริงสำหรับอุปกรณ์ เช่น Router, PC
broadcast ID = 192.168.40.127            // ใช้ส่งข้อมูลถึงทุกเครื่องใน Subnet นี้ (ห้ามใช้กับอุปกรณ์)

2'Subnet == DELEVERY                     // Subnet ที่สองสำหรับแผนก Delivery
Subnet mask = 255.255.255.128            // ใช้ Subnet Mask /25 เหมือนกัน
network ID = 192.168.40.128              // เป็น Network ID ของ Subnet ที่สอง
Range of Valid Host = 192.168.40.129 - 192.168.40.254 // ช่วง IP ที่ใช้ได้สำหรับอุปกรณ์ฝั่ง Delivery
broadcast ID = 192.168.40.255            // Broadcast address ของ Subnet ที่สอง (ห้ามใช้กับอุปกรณ์)

คอมมาน เราท์เตอร์ แบบสรุป

Network Add<img width="631" height="627" alt="Router Command" src="https://github.com/user-attachments/assets/f84bac8b-e3af-4867-9ca5-f0e9fab979a5" />
<img width="741" height="1109" alt="Router Command2" src="https://github.com/user-attachments/assets/78b07abb-095a-469f-a7f4-f54b51bd457f" />

ress = 192.168.40.0           // เครือข่ายหลักที่ได้รับมา ใช้เป็นจุดเริ่มต้นของการแบ่ง Subnet
No. of subnets = 2                       // ต้องการแบ่งเครือข่ายออกเป็น 2 ส่วน (เช่น แผนก Accounts และ Delivery)

2^n = no.of subnet ==== 2^n=2           // ใช้สูตร 2^n เพื่อหาจำนวน Subnet ที่ต้องการ (ในที่นี้ n = 1)
N=1                                      // ยืม 1 bit จาก host portion เพื่อสร้าง Subnet
11111111.11111111.11111111.10000000      // แสดง Subnet Mask ในรูปแบบ Binary (25 บิตแรกเป็น Network)
255.255.255.128 ==> subnet mask          // รูปแบบ Subnet Mask แบบ Decimal (/25)

1'Subnet == ACCOUNT                      // Subnet แรกใช้สำหรับแผนก Accounts
Subnet mask = 255.255.255.128            // ใช้ Subnet Mask /25 หรือ 255.255.255.128
network ID = 192.168.40.0                // เป็น Network ID ของ Subnet แรก (ใช้เพื่อบอกว่าเป็นเครือข่ายย่อยนี้)
Range of Valid Host = 192.168.40.1 - 192.168.40.126   // ช่วง IP ที่ใช้ได้จริงสำหรับอุปกรณ์ เช่น Router, PC
broadcast ID = 192.168.40.127            // ใช้ส่งข้อมูลถึงทุกเครื่องใน Subnet นี้ (ห้ามใช้กับอุปกรณ์)

2'Subnet == DELEVERY                     // Subnet ที่สองสำหรับแผนก Delivery
Subnet mask = 255.255.255.128            // ใช้ Subnet Mask /25 เหมือนกัน
network ID = 192.168.40.128              // เป็น Network ID ของ Subnet ที่สอง
Range of Valid Host = 192.168.40.129 - 192.168.40.254 // ช่วง IP ที่ใช้ได้สำหรับอุปกรณ์ฝั่ง Delivery
broadcast ID = 192.168.40.255            // Broadcast address ของ Subnet ที่สอง (ห้ามใช้กับอุปกรณ์)


### ขอบคุณที่เนื้อหานี้ประโยชน์ต่อผู้ที่มีความสนใจ 🎉
