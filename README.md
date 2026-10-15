# คำอธิบายข้อมูล (Data Description)

โฟลเดอร์นี้อธิบายข้อมูลที่ใช้ในโครงงาน **IT Salary Analysis**

## 1. แหล่งที่มาและสิทธิ์การใช้ข้อมูล

| หัวข้อ | รายละเอียด |
| --- | --- |
| ชื่อชุดข้อมูล | Revenue and Profit of Fortune 500 Companies|
| แหล่งที่มาเดิม | https://www.kaggle.com/datasets/yashsrivastava51213/revenue-and-profit-of-fortune-500-companies |
| ประเภทข้อมูล | ข้อมูลทุติยภูมิบริษัท Fortune 500 ที่ประกอบด้วยปี อันดับบริษัท รายได้ และกำไร |

## 2. ไฟล์ในโฟลเดอร์นี้

| ตำแหน่งไฟล์ | คำอธิบาย |
| --- | --- |
| `fortune500(1).xlsx` | ไฟล์ข้อมูล Fortune 500 ที่ใช้ในการวิเคราะห์ มี 29,500 แถว และ 5 คอลัมน์ |
| `5_company(1).xlsx` | ข้อมูลที่คัดเลือกมาแล้วจำนวน 5 บริษัท มี 276 แถว และ 5 คอลัมน์  |

วิธีสร้างไฟล์ที่ประมวลผลแล้วขึ้นใหม่: วางไฟล์ดิบที่ `data/raw/it_salary.csv` แล้วรัน python `code/01_clean_data.py`


## 3. พจนานุกรมข้อมูล (Data Dictionary) ของ `salary_clean.csv`

ข้อมูลหลังจากทำความสะอาดแล้วมีทั้งหมด 1,186 แถว ตารางต่อไปนี้แสดงชื่อคอลัมน์ ชนิดข้อมูล คำอธิบาย และจำนวนค่าว่างของแต่ละคอลัมน์

| คอลัมน์ | ชื่อคอลัมน์เดิม | ชนิดข้อมูล | คำอธิบาย / ค่าที่เป็นไปได้ | ค่าว่าง |
| --- | --- | --- | --- | ---: |
| `age` | Age | ตัวเลข | อายุของผู้ตอบแบบสอบถาม หน่วยเป็นปี | 0 |
| `gender` | Gender | ข้อความ | เพศของผู้ตอบแบบสอบถาม ได้แก่ Male, Female และ Diverse (กลุ่ม Diverse มี 2 รายการ) | 3 |
| `city` | City | ข้อความ | เมืองที่ทำงาน ได้แก่ Berlin, Munich, Frankfurt และ Other | 0 |
| `position` | Position | ข้อความ | ชื่อตำแหน่งงานที่ผู้ตอบแบบสอบถามกรอกด้วยตนเอง มีทั้งหมด 135 รูปแบบ | 2 |
| `exp_total_years` | Total years of experience | ตัวเลข | จำนวนปีของประสบการณ์ทำงานทั้งหมด | 0 |
| `exp_germany_years` | Years of experience in Germany | ตัวเลข | จำนวนปีของประสบการณ์ทำงานในประเทศเยอรมนี | 44 |
| `seniority` | Seniority level | ข้อความ | ระดับตำแหน่งงาน ได้แก่ Junior, Middle, Senior, Lead, Head และ Other | 0 |
| `main_tech` | Your main technology / programming language | ข้อความ | เทคโนโลยีหรือภาษาโปรแกรมหลักที่ใช้งาน กรอกด้วยตนเองและอาจมีรูปแบบการสะกดต่างกัน เช่น Python และ python | 109 |
| `other_tech` | Other technologies/programming languages you use often | ข้อความ | เทคโนโลยีหรือภาษาโปรแกรมอื่น ๆ ที่ใช้งานเป็นประจำ โดยอาจมีหลายรายการในหนึ่งช่อง | 141 |
| `salary_eur` | Yearly brutto salary (without bonus and stocks) in EUR | ตัวเลข | เงินเดือนรวมก่อนหักภาษีต่อปี ไม่รวมโบนัสและหุ้น หน่วยเป็นยูโร เป็นตัวแปรตามหลักสำหรับการวิเคราะห์ | 0 |
| `bonus_eur` | Yearly bonus + stocks in EUR | ตัวเลข | มูลค่าโบนัสและหุ้นที่ได้รับต่อปี หน่วยเป็นยูโร | 396 |
| `salary_prev_year_eur` | Annual brutto salary ... one year ago (only if staying in the same country) | ตัวเลข | เงินเดือนรวมก่อนหักภาษีต่อปีของปีก่อนหน้า สำหรับผู้ที่ยังทำงานอยู่ในประเทศเดิม หน่วยเป็นยูโร | 333 |
| `bonus_prev_year_eur` | Annual bonus+stocks one year ago (only if staying in the same country) | ตัวเลข | มูลค่าโบนัสและหุ้นที่ได้รับในปีก่อนหน้า สำหรับผู้ที่ยังทำงานอยู่ในประเทศเดิม หน่วยเป็นยูโร | 590 |
| `vacation_days` | Number of vacation days | ตัวเลข | จำนวนวันลาพักร้อนต่อปี | 66 |
| `employment_status` | Employment status | ข้อความ | สถานะการทำงาน ได้แก่ Full-time employee, Self-employed (freelancer), Part-time employee, Founder, Working student และ Other | 11 |
| `contract_duration` | Contract duration | ข้อความ | ประเภทสัญญาจ้าง ได้แก่ Unlimited contract (สัญญาไม่มีกำหนดระยะเวลา) และ Temporary contract (สัญญาชั่วคราว) | 22 |
| `work_language` | Main language at work | ข้อความ | ภาษาหลักที่ใช้ในการทำงาน ได้แก่ English, German, Russian และ Other | 10 |
| `company_size` | Company size | ข้อความ | ขนาดบริษัทตามจำนวนพนักงาน ได้แก่ up to 10, 11-50, 51-100, 101-1000 และ 1000+ | 8 |
| `company_type` | Company type | ข้อความ | ประเภทบริษัท ได้แก่ Product, Startup, Consulting / Agency และ Other | 15 |

**หมายเหตุ**
- จำนวนค่าว่าง (Missing Values) นับจากข้อมูลหลังทำความสะอาดแล้ว จำนวน 1,186 แถว



หน่วยของจำนวนเงินทั้งหมดคือยูโร (EUR) และเป็นเงินรวมก่อนหักภาษี (brutto)
