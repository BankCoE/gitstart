![alt githublogo](https://3.bp.blogspot.com/-yc8DO17D1do/WmC6HX7KAhI/AAAAAAAABSw/D2iPGjKom9grVPOcsuVwFTAjsyRivs6oACLcBGAs/s1600/githublogo.png "Start for Github")
# Start for Github [เริ่มต้นใช้งาน github]
## Overview
+ [Github คืออะไร ?](#github-คืออะไร-)
+ [การอัพโหลดขึ้น github](#การอัพโหลดขึ้น-github)
+ [การดาวน์โหลดจาก github](#การดาวน์โหลดจาก-github)
+ [การใช้งาน git branch](#การใช้งาน-git-branch)
---
## Github คืออะไร ?
Github เป็นเว็บไซต์ที่สามารถใช้งาน git ได้ เป็นระบบในการจัดเก็บไฟล์ หรือโปรเจคต่าง ๆ ของเราได้ หรือให้เข้าใจง่ายๆ ก็คือการจัดเก็บงานบนเซิร์ฟเวอร์นั่นเอง 
ซึ่งเราสามารถย้อนดูเวอร์ชั่นเก่า ๆ ของโปรเจคที่เราเคยอัพโหลดได้ และสามารถดูได้ว่า เวลาใด ใครเป็นคนอัพโหลด เพราะ github จะเน้นในการทำงานแบบเป็นทีม 
หรือทำคนเดียวก็ได้ แต่โปรเจคของเราจะเป็นแบบเปิดเผย(public) ซึ่งเราสามารถตั้งให้เป็นส่วนตัว(private) ได้ แต่จะมีค่าใช้จ่าย 7 ดอลลาร์ หรือประมาณ 200 บาท ต่อเดือน

[[...ย้อนกลับ Overview]](#overview)
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
	> เป็นการ track ไฟล์ README.md เพื่อที่จะทำการ commit ในขั้นตอนต่อไป
	```
	git status
	```
	> เป็นการเช็คว่ามีไฟล์ใดบ้าง ที่พร้อมสำหรับการ commit
	```
	git config --global user.email "thanachat.j@hotmail.com"
	git config --global user.name "BankCoE"
	```
	> เป็นการตั้งค่าอีเมล์และชื่อ สำหรับการใช้งาน github
	```
	git commit -m "gitstart commit"
	```
	> เป็นการ commit ไปยัง git directory (repository) โดยมีคอมเมนต์ว่า gitstart commit
	```
	git remote add origin https://github.com/BankCoE/gitstart.git
	```
	> เป็นการตั้งค่า URL เพื่อ remote repository ไปยัง URL ที่เราตั้งไว้
	```
	git remote -v
	```
	> เป็นการเช็คว่า URL ที่ต้องการ remote repository คืออะไร
	```
	git push -u origin master
	```
	> เป็นการอัพโหลดไฟล์ที่เราได้ commit ไว้ ขึ้นไปยัง github 

เพียงเท่านี้ ไฟล์หรือโปรเจคของเราก็อยู่บน git เรียบร้อย ซึ่งสามารถดาวน์โหลดมาพัฒนาหรือแก้ไขต่อได้

[[...ย้อนกลับ Overview]](#overview)
## การดาวน์โหลดจาก github
1. เปิด command prompt หรือ teminal บน folder ที่เราต้องการดาวน์โหลดจาก github
2. พิมพ์คำสั่ง ดังต่อไปนี้

	```
	git init
	```
	> เป็นการสร้างไฟล์ repository ชื่อ .git ขึ้นมา เพื่อเก็บค่าการทำงานต่าง ๆ 
	```
	git remote add origin https://github.com/BankCoE/gitstart.git
	```
	> เป็นการตั้งค่า URL เพื่อ remote repository ไปยัง URL ที่เราต้องการดาวน์โหลดไฟล์ หรือโปรเจค
	```
	git pull origin master
	```
	> เป็นการดาวน์โหลดไฟล์ หรือโปรเจคของเราจาก URL ที่ตั้งไว้

เพียงเท่านี้ ไฟล์ที่เราต้องการดาวน์โหลด ก็จะอยู่ในโฟลเดอร์ที่เราต้องการเรียบร้อยแล้ว

[[...ย้อนกลับ Overview]](#overview)
## การใช้งาน git  branch
Git branch เป็น feature หนึ่ง ที่ช่วยให้นักพัฒนาสามารถทำงานได้อย่างสะดวกมากขึ้น เพราะ branch เปรียบเสมือนโฟล์เดอร์ ที่สามารถทำงานในส่วน
ที่เราไม่ต้องการนำมาปนกันได้ และเมื่อเราพัฒนางานในส่วนของ branch เสร็จเรียบร้อย ก็สามารถนำมารวมกับ master ในภายหลังได้
### การสร้าง branch
ในการสร้าง branch ใหม่ เราจะใช้คำสั่งว่า

	```
	git init
	```
	> เป็นการสร้างไฟล์ repository ชื่อ .git ขึ้นมา เพื่อเก็บค่าการทำงานต่าง ๆ 

	```
	git branch bankdev
	```
	> เป็นสร้าง branch ใหม่ ที่มีชื่อว่า bankdev (แต่ยังอยู่ใน branch master)
	```
	git branch
	```
	> เป็นการเช็คว่าใน repository ของเรานั้น มี branch อะไรบ้าง
	```
	* master
	bankdev
	```
	> แสดงสถานะ branch ที่เรามีอยู่ใน repository
	


