
## Enterprise Network Project #1 🌐🖧📡⚙️📈
---
### เครดิต
[**Gurutech Networking Training**](https://www.youtube.com/watch?v=T8F5F9Jt8Yk&list=PLvUOx2WG6R7PMM8UhMWevH75QzGyXOv4g)  
---
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
#📝Assignment 
<p align="center">
  <img src="https://github.com/user-attachments/assets/8d763c37-7843-446a-9ad3-fdd2a289ac24" width="600"/> <br/>
  <small>แหล่งที่มา:  
  <a href="https://www.youtube.com/watch?v=T8F5F9Jt8Yk&list=PLvUOx2WG6R7PMM8UhMWevH75QzGyXOv4g" target="_blank" rel="noopener noreferrer">Gurutech Networking Training - YouTube Playlist</a>
  </small>
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
      <td>ACCOUNT</td>
      <td>255.255.255.128 (/25)</td>
      <td>192.168.40.0</td>
      <td>192.168.40.1 – 192.168.40.126</td>
      <td>192.168.40.127</td>
    </tr>
    <tr>
      <td>2</td>
      <td>DELIVERY</td>
      <td>255.255.255.128 (/25)</td>
      <td>192.168.40.128</td>
      <td>192.168.40.129 – 192.168.40.254</td>
      <td>192.168.40.255</td>
    </tr>
  </tbody>
</table>

 ##💻⚙️Router Command
 ** ย่อคำสั่งเพื่อให้ เข้าใจง่ายๆ ส่วนการ command จริงจะอยู่ในภาพด้านล่าง
 <table>
  <thead>
    <tr>
      <th>คำสั่ง Router</th>
      <th>คำอธิบาย</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Router&gt; enable</td>
      <td>เข้าสู่โหมด privileged EXEC เพื่อให้ตั้งค่าได้</td>
    </tr>
    <tr>
      <td>Router# configure terminal</td>
      <td>เข้าสู่โหมด global configuration เพื่อแก้ไข config</td>
    </tr>
    <tr>
      <td>Router(config)# interface range gigabitEthernet0/0 - 1</td>
      <td>เลือก interface 0/0 และ 0/1 พร้อมกันเพื่อ config</td>
    </tr>
    <tr>
      <td>Router(config-if-range)# no shutdown</td>
      <td>เปิดใช้งาน interface ทั้งสอง (default มักปิดอยู่)</td>
    </tr>
    <tr>
      <td>Router(config-if-range)# do write</td>
      <td>บันทึกการตั้งค่าปัจจุบันลง startup-config</td>
    </tr>
    <tr>
      <td>Router(config-if-range)# exit</td>
      <td>ออกจาก interface range config กลับ global config</td>
    </tr>
    <tr>
      <td>Router(config)# interface gigabitEthernet0/0</td>
      <td>เลือก interface 0/0 เพื่อ config ทีละตัว</td>
    </tr>
    <tr>
      <td>Router(config-if)# ip address 192.168.40.1 255.255.255.128</td>
      <td>กำหนด IP และ subnet mask ให้ interface นี้</td>
    </tr>
    <tr>
      <td>Router(config-if)# exit</td>
      <td>ออกจาก interface config กลับ global config</td>
    </tr>
    <tr>
      <td>Router(config)# interface gigabitEthernet0/1</td>
      <td>เลือก interface 0/1 เพื่อ config</td>
    </tr>
    <tr>
      <td>Router(config-if)# ip address 192.168.40.129 255.255.255.128</td>
      <td>กำหนด IP สำหรับ interface นี้ (subnet ที่สอง)</td>
    </tr>
    <tr>
      <td>Router(config-if)# do write</td>
      <td>บันทึก config ลง startup-config อีกครั้ง</td>
    </tr>
    <tr>
      <td>Router(config-if)# exit</td>
      <td>ออกจาก interface config</td>
    </tr>
      <tr>
      <td>do sh start = do show startup-config</td>
      <td>ใช้ดู config ที่ถูกบันทึกไว้ใน startup-config ขณะอยู่ในโหมด config โดยไม่ต้องออกไปที่ privileged EXEC mode</td>
    </tr>
  </tbody>
</table>
<p align="center">
  <img src="https://github.com/user-attachments/assets/f84bac8b-e3af-4867-9ca5-f0e9fab979a5" width="600"/>
  <br/>
  <img src="https://github.com/user-attachments/assets/78b07abb-095a-469f-a7f4-f54b51bd457f" width="600"/>
</p>


### ขอบคุณที่เนื้อหานี้ประโยชน์ต่อผู้ที่มีความสนใจ 🎉
