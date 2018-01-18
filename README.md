![alt githublogo](https://3.bp.blogspot.com/-yc8DO17D1do/WmC6HX7KAhI/AAAAAAAABSw/D2iPGjKom9grVPOcsuVwFTAjsyRivs6oACLcBGAs/s1600/githublogo.png "Start for Github")
# Start for Github [เริ่มต้นใช้งาน github]
## Overview
+ [Github คืออะไร ?](#github-คืออะไร-)
+ [การอัพโหลดขึ้น github](#การอัพโหลดขึ้น-github)
+ [การดาวน์โหลดจาก github](#การดาวน์โหลดจาก-github)
---
## Github คืออะไร ?
Github เป็นเว็บไซต์ที่สามารถใช้งาน git ได้ เป็นระบบในการจัดเก็บไฟล์ หรือโปรเจคต่าง ๆ ของเราได้ หรือให้เข้าใจง่ายๆ ก็คือการจัดเก็บงานบนเซิร์ฟเวอร์นั่นเอง 
ซึ่งเราสามารถย้อนดูเวอร์ชั่นเก่า ๆ ของโปรเจคที่เราเคยอัพโหลดได้ และสามารถดูได้ว่า เวลาใด ใครเป็นคนอัพโหลด เพราะ github จะเน้นในการทำงานแบบเป็นทีม 
หรือทำคนเดียวก็ได้ แต่โปรเจคของเราจะเป็นแบบเปิดเผย(public) ซึ่งเราสามารถตั้งให้เป็นส่วนตัว(private) ได้ แต่จะมีค่าใช้จ่าย 7 ดอลลาร์ หรือประมาณ 200 บาท ต่อเดือน

[[...ย้อนกลับ]](#overview)
## การอัพโหลดขึ้น github
1. เปิด command prompt หรือ teminal บน folder ที่เราต้องการอัพขึ้น github
2. พิมพ์คำสั่ง ดังต่อไปนี้

	```
	echo "# gitstart" >> README.md
	```
	> สร้างไฟล์ชื่อว่า README นามสกุล .md และมีข้อความว่า gitstart

	```
	git init
	```
	> เป็นการสร้างไฟล์ repository ชื่อ .git ขึ้นมา เพื่อเก็บค่าการทำงานต่าง ๆ 


	```
	git add README.md
	```
	> เป็นการ track ไฟล์ README.md เพื่อที่จะทำการ commit ขึ้น github
	```
	git status
	```
	> เป็นการเช็คว่ามีไฟล์ใดบ้าง ที่พร้อมสำหรับการ commit ขึ้น github
	
## การดาวน์โหลดจาก github
---

