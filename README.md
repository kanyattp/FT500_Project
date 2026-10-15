# คำอธิบายข้อมูล (Data Description)

โฟลเดอร์นี้อธิบายข้อมูลที่ใช้ในโครงงาน **Analysis of Revenue and Profit of Fortune 500 Companies**

## 1. แหล่งที่มาและสิทธิ์การใช้ข้อมูล

| หัวข้อ | รายละเอียด |
| --- | --- |
| ชื่อชุดข้อมูล | Revenue and Profit of Fortune 500 Companies|
| แหล่งที่มาเดิม | https://www.kaggle.com/datasets/yashsrivastava51213/revenue-and-profit-of-fortune-500-companies |
| ประเภทข้อมูล | ข้อมูลทุติยภูมิบริษัท Fortune 500 ที่ประกอบด้วยปี อันดับบริษัท รายได้ และกำไร |

## 2. ไฟล์ในโฟลเดอร์นี้

| ตำแหน่งไฟล์ | คำอธิบาย |
| --- | --- |
| `d:\python\fortune500.xlsx` | ไฟล์ข้อมูล Fortune 500 ที่ใช้ในการวิเคราะห์ มี 29,501 แถว และ 5 คอลัมน์ |
| `d:\python\five_company.xlsx` | ข้อมูลที่คัดเลือกมาแล้วจำนวน 5 บริษัท มี 276 แถว และ 5 คอลัมน์  |



## 3. พจนานุกรมข้อมูล (Data Dictionary) ของ `5_company.xlsx`

ข้อมูลใน five_company มีทั้งหมด 276 แถว 5 คอลัมน์ ตารางต่อไปนี้แสดงชื่อคอลัมน์ ชนิดข้อมูล คำอธิบายของแต่ละคอลัมน์ และจำนวนค่าว่าง

| คอลัมน์ | ชนิดข้อมูล | คำอธิบาย / ค่าที่เป็นไปได้ | ค่าว่าง |
| --- | --- | --- | ---: |
| `Year` | ตัวเลข | ปีของข้อมูลบริษัท Fortune 500 | 0 |
| `Rank` | ตัวเลข | อันดับของบริษัทใน Fortune 500 ในปีนั้น | 0 |
| `Company` | ข้อความ | ชื่อของบริษัท ได้แก่ General Motors, Exxon Mobil, General Electric, PPG Industries, Pfizer | 0 |
| `Revenue (in millions)` | ตัวเลข | รายได้ของบริษัท หน่วยล้านดอลลาร์ | 0 |
| `Profit (in millions)` | ตัวเลข | กำไรของบริษัท หน่วยเป็นล้านดอลลาร์ | 0 |
