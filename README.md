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
## 📊 การคำนวณ Subnet
Network Address: `192.168.40.0`  
จำนวน Subnet ที่ต้องการ: `2` (Accounts และ Delivery)  
Subnet Mask: `255.255.255.128` หรือ `/25`
<table border="1" cellpadding="6" cellspacing="0">
  <thead>
    <tr>
      <th>Subnet</th>
      <th>แผนก</th>
      <th>Subnet Mask</th>
      <th>Network ID</th>
      <th>ช่วง IP ที่ใช้ได้ (Valid Hosts)</th>
      <th>Broadcast Address</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>1</td>
      <td>🧾 ACCOUNT</td>
      <td>255.255.255.128 (/25)</td>
      <td>192.168.40.0</td>
      <td>192.168.40.1 – 192.168.40.126</td>
      <td>192.168.40.127</td>
    </tr>
    <tr>
      <td>2</td>
      <td>🚚 DELIVERY</td>
      <td>255.255.255.128 (/25)</td>
      <td>192.168.40.128</td>
      <td>192.168.40.129 – 192.168.40.254</td>
      <td>192.168.40.255</td>
    </tr>
  </tbody>
</table>

 ## 📊 Router Command
Router> enable                     // เข้าสู่โหมด privileged EXEC เพื่อให้ตั้งค่าได้
Router# configure terminal        // เข้าสู่โหมด global configuration เพื่อแก้ไข config
Router(config)# interface range gigabitEthernet0/0 - 1   // เลือก interface 0/0 และ 0/1 พร้อมกันเพื่อ config
Router(config-if-range)# no shutdown                     // เปิดใช้งาน interface ทั้งสอง (default มักปิดอยู่)
Router(config-if-range)# do write                         // บันทึกการตั้งค่าปัจจุบันลง startup-config
Router(config-if-range)# exit                             // ออกจาก interface range config กลับ global config
Router(config)# interface gigabitEthernet0/0              // เลือก interface 0/0 เพื่อ config ทีละตัว
Router(config-if)# ip address 192.168.40.1 255.255.255.128 // กำหนด IP และ subnet mask ให้ interface นี้
Router(config-if)# exit                                     // ออกจาก interface config กลับ global config
Router(config)# interface gigabitEthernet0/1               // เลือก interface 0/1 เพื่อ config
Router(config-if)# ip address 192.168.40.129 255.255.255.128 // กำหนด IP สำหรับ interface นี้ (subnet ที่สอง)
Router(config-if)# do write                                 // บันทึก config ลง startup-config อีกครั้ง
Router(config-if)# exit                                     // ออกจาก interface config
Router(config)# do show startup-config                      // แสดง config ที่บันทึกไว้ทั้งหมด
<p align="center">
  <img src="https://github.com/user-attachments/assets/f84bac8b-e3af-4867-9ca5-f0e9fab979a5" width="600"/>
  <br/>
  <img src="https://github.com/user-attachments/assets/78b07abb-095a-469f-a7f4-f54b51bd457f" width="600"/>
</p>


### ขอบคุณที่เนื้อหานี้ประโยชน์ต่อผู้ที่มีความสนใจ 🎉
