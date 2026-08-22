# การวิเคราะห์มลพิษทางอากาศจาก PCD/Air4Thai และข้อมูลอุตุนิยมวิทยาจาก OGIMET
## ชุดฝึกปฏิบัติ Python และ Google Colab สำหรับนิสิตด้านสิ่งแวดล้อม ภูมิศาสตร์ และภูมิสารสนเทศ

Repository นี้รวบรวม **Python codes และ Google Colab notebooks สำหรับการเรียนการสอนและการฝึกวิเคราะห์ข้อมูลสิ่งแวดล้อมจากข้อมูลจริง** โดยเน้นการบูรณาการข้อมูลคุณภาพอากาศจาก **กรมควบคุมมลพิษ (Pollution Control Department: PCD) / Air4Thai** กับข้อมูลอุตุนิยมวิทยาจาก **OGIMET**

พื้นที่ศึกษาหลักประกอบด้วย 3 จังหวัด ได้แก่

- **สระบุรี**
- **ลพบุรี**
- **นครนายก**

ชุดการสอนออกแบบสำหรับนิสิตระดับปริญญาตรีชั้นปีที่ 3–4 และสามารถใช้เป็นพื้นฐานสำหรับนิสิตระดับบัณฑิตศึกษาในสาขา **วิทยาศาสตร์สิ่งแวดล้อม ภูมิศาสตร์ ภูมิสารสนเทศ อุตุนิยมวิทยา วิทยาศาสตร์บรรยากาศ และสาขาที่เกี่ยวข้อง**

> **แนวคิดหลักของชุดการสอน**
>
> `ข้อมูลจริง → ตรวจสอบข้อมูล → จัดเตรียมข้อมูล → วิเคราะห์ PM₂.₅ → ข้อมูลอุตุนิยมวิทยา → ลมและ Wind Rose → บูรณาการเพื่อการตีความสิ่งแวดล้อม`

---

# Start Here — เริ่มต้นใช้งาน

Notebook ทุกไฟล์ออกแบบให้เปิดและรันบน **Google Colab** ได้โดยตรง

สำหรับผู้เรียนที่ต้องการเห็นภาพรวมทั้งระบบ แนะนำให้เริ่มจาก Notebook **00** แล้วเรียนตามลำดับ 01 → 06

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/nattaponm/training_PCD_Ogimet10yr_3provinces_pm25/blob/main/00_PCD_Air4Thai_Station_Metadata_Thailand_Map.ipynb)

```text
00  Air4Thai station metadata + Thailand station map
                 ↓
01  PM₂.₅ analysis: 3 provinces / multi-year
                 ↓
02  PM₂.₅ long-term analysis: Saraburi
                 ↓
03  OGIMET station locations and mapping
                 ↓
04  Download OGIMET data around Saraburi
                 ↓
05  Flexible OGIMET download: Lopburi / selected period
                 ↓
06  Meteorological plots + wind analysis + wind rose
                 ↓
     Air pollution–meteorology interpretation
```

---

# เปิด Notebook ใน Google Colab

| Notebook | ชื่อไฟล์ | เนื้อหาหลัก | บทบาท | Colab |
|---|---|---|---|---|
| **00** | `00_PCD_Air4Thai_Station_Metadata_Thailand_Map.ipynb` | ข้อมูลสถานี Air4Thai ทั้งประเทศ แผนที่ และ export metadata | พื้นฐานข้อมูลเชิงพื้นที่ | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/nattaponm/training_PCD_Ogimet10yr_3provinces_pm25/blob/main/00_PCD_Air4Thai_Station_Metadata_Thailand_Map.ipynb) |
| **01** | `01_PCDpm2_5_pcd_วิเคราะห์5ปี_สระบุรี_ลพบุรี_นครนายก.ipynb` | วิเคราะห์ PM₂.₅ หลายปีในสระบุรี ลพบุรี และนครนายก | Air quality | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/nattaponm/training_PCD_Ogimet10yr_3provinces_pm25/blob/main/01_PCDpm2_5_pcd_วิเคราะห์5ปี_สระบุรี_ลพบุรี_นครนายก.ipynb) |
| **02** | `02_PCDpm2_5_pcd_วิเคราะห์10ปี_สระบุรี_.ipynb` | วิเคราะห์ PM₂.₅ ระยะยาวประมาณ 10 ปีของจังหวัดสระบุรี | Long-term air quality | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/nattaponm/training_PCD_Ogimet10yr_3provinces_pm25/blob/main/02_PCDpm2_5_pcd_วิเคราะห์10ปี_สระบุรี_.ipynb) |
| **03** | `03_PCDข้อมูลอุต_แผนที่ตำแหน่งสถานีogimet_ประเทศไทย_สระบุรี.ipynb` | ค้นหาและทำแผนที่สถานีอุตุนิยมวิทยา OGIMET ที่เกี่ยวข้อง | Station mapping | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/nattaponm/training_PCD_Ogimet10yr_3provinces_pm25/blob/main/03_PCDข้อมูลอุต_แผนที่ตำแหน่งสถานีogimet_ประเทศไทย_สระบุรี.ipynb) |
| **04** | `04_PCDดาวน์โหลดข้อมูลอากาศ_Ogimet_สถานีรอบสระบุรี_เวิร์คข้อมูลทดสอบ.ipynb` | ดาวน์โหลดและตรวจโครงสร้างข้อมูล OGIMET รอบสระบุรี | Meteorological data | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/nattaponm/training_PCD_Ogimet10yr_3provinces_pm25/blob/main/04_PCDดาวน์โหลดข้อมูลอากาศ_Ogimet_สถานีรอบสระบุรี_เวิร์คข้อมูลทดสอบ.ipynb) |
| **05** | `05_PCDดาวน์โหลดข้อมูลอุตุนิยมวิทยาจาก_OGIMET_เน้นสถานีลพบุรี_เลือกเวลาได้.ipynb` | ดาวน์โหลด OGIMET แบบเลือกสถานีและช่วงเวลา โดยเน้นลพบุรี | Flexible acquisition | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/nattaponm/training_PCD_Ogimet10yr_3provinces_pm25/blob/main/05_PCDดาวน์โหลดข้อมูลอุตุนิยมวิทยาจาก_OGIMET_เน้นสถานีลพบุรี_เลือกเวลาได้.ipynb) |
| **06** | `06_PCDวิเคราะห์พลอตข้อมูลอุต_Ogimet_ipynb.ipynb` | วิเคราะห์และพลอตข้อมูลอุตุนิยมวิทยา รวมถึงลมและ wind rose | Meteorological analysis | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/nattaponm/training_PCD_Ogimet10yr_3provinces_pm25/blob/main/06_PCDวิเคราะห์พลอตข้อมูลอุต_Ogimet_ipynb.ipynb) |

> หากชื่อไฟล์ใน repository ถูกเปลี่ยนภายหลัง ต้องแก้ URL ของปุ่ม Colab ให้ตรงกับชื่อไฟล์ใหม่ด้วย

---

# วัตถุประสงค์การเรียนรู้

เมื่อเรียนครบชุด Notebook นี้ นิสิตควรสามารถ:

1. เข้าใจโครงสร้างข้อมูลคุณภาพอากาศจาก PCD/Air4Thai
2. ดาวน์โหลดและจัดเตรียมข้อมูล PM₂.₅ แบบรายวันและหลายปี
3. ตรวจสอบ station code, station metadata, latitude และ longitude
4. สร้างแผนที่ตำแหน่งสถานีตรวจวัดคุณภาพอากาศ
5. วิเคราะห์ข้อมูล PM₂.₅ รายสถานีและรายจังหวัด
6. ศึกษาความแปรผันรายปี รายเดือน และตามฤดูกาล
7. เปรียบเทียบความแตกต่างระหว่างจังหวัดและสถานี
8. เปรียบเทียบวันธรรมดาและวันสุดสัปดาห์
9. ค้นหาและคัดเลือกสถานีอุตุนิยมวิทยาที่เหมาะสมกับพื้นที่ศึกษา
10. ดาวน์โหลดข้อมูลอุตุนิยมวิทยาจาก OGIMET ตามสถานีและช่วงเวลาที่กำหนด
11. ตรวจสอบและจัดเตรียมตัวแปรอุตุนิยมวิทยา
12. วิเคราะห์อุณหภูมิ ความชื้น ความกดอากาศ ปริมาณฝน และลม
13. วิเคราะห์ wind speed และ wind direction
14. สร้างและตีความ **wind rose**
15. เชื่อมโยงสภาพอุตุนิยมวิทยากับการสะสมหรือการระบายมลพิษอย่างระมัดระวัง
16. พัฒนา workflow ต่อเป็นหัวข้องานวิจัย วิทยานิพนธ์ หรือโครงงานด้านสิ่งแวดล้อมได้

---

# พื้นที่ศึกษา

## จังหวัดสระบุรี

สระบุรีมีลักษณะการใช้ประโยชน์ที่ดินและแหล่งกำเนิดหลากหลาย ทั้งพื้นที่เมือง อุตสาหกรรม การคมนาคม และเกษตรกรรม จึงเหมาะสำหรับใช้ศึกษาความแปรผันของ PM₂.₅ และความสัมพันธ์กับสภาพอุตุนิยมวิทยา

## จังหวัดลพบุรี

ลพบุรีใช้เป็นพื้นที่เปรียบเทียบกับจังหวัดใกล้เคียง และเป็นตัวอย่างสำหรับการค้นหาและดาวน์โหลดข้อมูลสถานีอุตุนิยมวิทยาจาก OGIMET ตามพื้นที่และช่วงเวลาที่กำหนด

## จังหวัดนครนายก

นครนายกเพิ่มความหลากหลายของบริบทพื้นที่ศึกษา และช่วยให้นิสิตฝึกเปรียบเทียบลักษณะมลพิษทางอากาศระหว่างจังหวัด

> Repository นี้ใช้ 3 จังหวัดเป็น **teaching case** ผู้เรียนสามารถเปลี่ยนจังหวัด สถานี ช่วงเวลา หรือสารมลพิษให้สอดคล้องกับคำถามวิจัยของตนเองได้

---

# แหล่งข้อมูล

## 1. ข้อมูลคุณภาพอากาศ — PCD / Air4Thai

ข้อมูลคุณภาพอากาศมาจาก **กรมควบคุมมลพิษ (PCD)** ผ่านระบบ **Air4Thai**

ตัวแปรที่ใช้เป็นหลัก ได้แก่:

- PM₂.₅
- PM₁₀
- และตัวแปรมลพิษอื่นตาม availability ของแต่ละสถานี/ช่วงเวลา

การวิเคราะห์ใน repository นี้เน้นการจัดข้อมูลให้อยู่ในรูปที่เหมาะสำหรับ:

- daily analysis
- station comparison
- province comparison
- monthly analysis
- seasonal analysis
- weekday/weekend comparison
- long-term variability

---

## 2. ข้อมูลอุตุนิยมวิทยา — OGIMET

OGIMET ให้ข้อมูลสถานีอุตุนิยมวิทยาจากเครือข่ายสังเกตการณ์สากล

ตัวแปรที่อาจพบ ขึ้นกับสถานีและช่วงเวลา เช่น:

- air temperature
- relative humidity
- atmospheric pressure
- wind speed
- wind direction
- precipitation
- visibility
- และตัวแปรอุตุนิยมวิทยาอื่นที่สถานีนั้นรายงาน

Notebook ชุดนี้สอนทั้งการเลือกสถานี ดาวน์โหลด ตรวจสอบ และนำข้อมูลไปวิเคราะห์ร่วมกับมลพิษทางอากาศ

---

# Notebook 00 — Air4Thai Station Metadata, Thailand Map และ CSV Export

**File:** `00_PCD_Air4Thai_Station_Metadata_Thailand_Map.ipynb`

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/nattaponm/training_PCD_Ogimet10yr_3provinces_pm25/blob/main/00_PCD_Air4Thai_Station_Metadata_Thailand_Map.ipynb)

Notebook นี้ใช้เพื่อทำความเข้าใจ **metadata ของสถานี Air4Thai** และตำแหน่งสถานีทั่วประเทศไทย

เนื้อหาหลัก:

- ดึง station metadata จาก Air4Thai
- ตรวจ `stationID`
- ตรวจชื่อสถานีและพื้นที่
- ตรวจ latitude / longitude
- ตรวจสถานีซ้ำและพิกัดผิดปกติ
- สร้าง Pandas DataFrame
- สร้าง GeoDataFrame
- แสดงตำแหน่งสถานีบนแผนที่ประเทศไทย
- สร้าง interactive map
- export station metadata เป็น CSV
- export GeoJSON สำหรับ QGIS / ArcGIS / Python GIS

แนวคิด:

```text
Air4Thai station metadata
        ↓
QC station ID / coordinate
        ↓
GeoDataFrame
        ↓
Thailand station map
        ↓
CSV / GeoJSON
```

Notebook นี้ช่วยให้นิสิตเข้าใจว่า ก่อนวิเคราะห์ time series ควรรู้ก่อนว่า **สถานีอยู่ที่ไหนและเป็นตัวแทนของพื้นที่ใด**

---

# Notebook 01 — วิเคราะห์ PM₂.₅ หลายปี: สระบุรี ลพบุรี และนครนายก

**File:** `01_PCDpm2_5_pcd_วิเคราะห์5ปี_สระบุรี_ลพบุรี_นครนายก.ipynb`

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/nattaponm/training_PCD_Ogimet10yr_3provinces_pm25/blob/main/01_PCDpm2_5_pcd_วิเคราะห์5ปี_สระบุรี_ลพบุรี_นครนายก.ipynb)

Notebook นี้เป็น introduction สู่การวิเคราะห์ PM₂.₅ จาก PCD/Air4Thai สำหรับ 3 จังหวัด

เนื้อหาหลัก:

- อ่านและจัดรูปข้อมูล PM₂.₅
- ตรวจสถานี
- วิเคราะห์ข้อมูลหลายปี
- เปรียบเทียบสถานี
- เปรียบเทียบจังหวัด
- time series
- monthly variation
- seasonal variation
- descriptive statistics
- เตรียมข้อมูลสำหรับการวิเคราะห์ต่อ

เหมาะสำหรับใช้เป็น template เมื่อผู้เรียนต้องการเปลี่ยนพื้นที่ศึกษาหรือช่วงเวลา

---

# Notebook 02 — วิเคราะห์ PM₂.₅ ระยะยาวประมาณ 10 ปี: จังหวัดสระบุรี

**File:** `02_PCDpm2_5_pcd_วิเคราะห์10ปี_สระบุรี_.ipynb`

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/nattaponm/training_PCD_Ogimet10yr_3provinces_pm25/blob/main/02_PCDpm2_5_pcd_วิเคราะห์10ปี_สระบุรี_.ipynb)

Notebook นี้ขยายการวิเคราะห์จาก multi-year ไปสู่การวิเคราะห์ระยะยาว โดยเน้นจังหวัดสระบุรี

หัวข้อ:

- long-term PM₂.₅ data
- station-level time series
- interannual variation
- monthly variation
- seasonal comparison
- dry vs wet season
- weekday vs weekend
- descriptive/statistical comparison
- การตรวจ data completeness ก่อนตีความ trend

หลักการสำคัญ:

> **การมีข้อมูลหลายปีไม่ได้หมายความโดยอัตโนมัติว่าสามารถสรุป trend ได้ทันที**

ควรตรวจ station continuity, missing data, measurement changes และ completeness ของแต่ละช่วงด้วย

---

# Notebook 03 — ข้อมูลสถานีอุตุนิยมวิทยาและแผนที่ตำแหน่งสถานี OGIMET

**File:** `03_PCDข้อมูลอุต_แผนที่ตำแหน่งสถานีogimet_ประเทศไทย_สระบุรี.ipynb`

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/nattaponm/training_PCD_Ogimet10yr_3provinces_pm25/blob/main/03_PCDข้อมูลอุต_แผนที่ตำแหน่งสถานีogimet_ประเทศไทย_สระบุรี.ipynb)

Notebook นี้เชื่อมงานคุณภาพอากาศเข้ากับข้อมูลอุตุนิยมวิทยา

เนื้อหาหลัก:

- ทำความเข้าใจ station metadata ของสถานีอุตุนิยมวิทยา
- ระบุตำแหน่งสถานี
- ทำแผนที่สถานีที่เกี่ยวข้องกับประเทศไทยและพื้นที่สระบุรี
- ประเมินระยะทางและความเหมาะสมเชิงพื้นที่
- เตรียม station ID สำหรับการดาวน์โหลด OGIMET

คำถามสำคัญสำหรับผู้เรียน:

> สถานีอุตุนิยมวิทยาที่ใกล้ที่สุด จำเป็นต้องเป็นสถานีที่เป็นตัวแทนพื้นที่ดีที่สุดเสมอหรือไม่?

ควรพิจารณาทั้งระยะทาง ภูมิประเทศ ความสูง สภาพเมือง/ชนบท และความต่อเนื่องของข้อมูล

---

# Notebook 04 — ดาวน์โหลดและทดสอบข้อมูล OGIMET รอบจังหวัดสระบุรี

**File:** `04_PCDดาวน์โหลดข้อมูลอากาศ_Ogimet_สถานีรอบสระบุรี_เวิร์คข้อมูลทดสอบ.ipynb`

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/nattaponm/training_PCD_Ogimet10yr_3provinces_pm25/blob/main/04_PCDดาวน์โหลดข้อมูลอากาศ_Ogimet_สถานีรอบสระบุรี_เวิร์คข้อมูลทดสอบ.ipynb)

Notebook นี้สอน workflow การดาวน์โหลดข้อมูลอุตุนิยมวิทยาและตรวจโครงสร้างข้อมูลก่อนวิเคราะห์จริง

หัวข้อ:

- กำหนด station ID
- กำหนดช่วงเวลา
- ดาวน์โหลด OGIMET
- ตรวจ column และ units
- ตรวจ missing values
- ตรวจวัน/เวลา
- ตรวจความต่อเนื่องของข้อมูล
- สร้างตัวอย่าง time series
- เตรียมข้อมูลสำหรับการวิเคราะห์ขั้นต่อไป

หลักการ:

> **Download success ≠ analysis-ready data**

ต้องตรวจ metadata, units, missingness และ temporal structure ก่อนเสมอ

---

# Notebook 05 — ดาวน์โหลด OGIMET แบบเลือกช่วงเวลา โดยเน้นสถานีลพบุรี

**File:** `05_PCDดาวน์โหลดข้อมูลอุตุนิยมวิทยาจาก_OGIMET_เน้นสถานีลพบุรี_เลือกเวลาได้.ipynb`

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/nattaponm/training_PCD_Ogimet10yr_3provinces_pm25/blob/main/05_PCDดาวน์โหลดข้อมูลอุตุนิยมวิทยาจาก_OGIMET_เน้นสถานีลพบุรี_เลือกเวลาได้.ipynb)

Notebook นี้เน้นให้ผู้เรียนปรับ parameter ด้วยตนเอง

สามารถกำหนด:

- สถานี
- วันที่เริ่มต้น
- วันที่สิ้นสุด
- ช่วงเวลาที่ต้องการ
- ตัวแปรที่จะใช้

เหมาะสำหรับนำ workflow เดียวกันไปประยุกต์กับจังหวัดอื่นหรือช่วงเหตุการณ์เฉพาะ เช่น:

- PM₂.₅ episode
- smoke/haze episode
- dry-season pollution
- high-wind event
- precipitation event

---

# Notebook 06 — วิเคราะห์และพลอตข้อมูลอุตุนิยมวิทยาจาก OGIMET

**File:** `06_PCDวิเคราะห์พลอตข้อมูลอุต_Ogimet_ipynb.ipynb`

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/nattaponm/training_PCD_Ogimet10yr_3provinces_pm25/blob/main/06_PCDวิเคราะห์พลอตข้อมูลอุต_Ogimet_ipynb.ipynb)

Notebook นี้เป็นขั้นวิเคราะห์ meteorological data

เนื้อหา:

- time-series visualization
- temperature variation
- humidity variation
- pressure variation
- precipitation
- wind speed distribution
- wind direction distribution
- wind rose
- การตีความลมร่วมกับมลพิษทางอากาศ

ตัวอย่างคำถาม:

- ช่วง PM₂.₅ สูงมีลมอ่อนหรือไม่?
- ลมส่วนใหญ่มาจากทิศใด?
- ทิศลมในช่วง PM₂.₅ สูงต่างจากวันปกติหรือไม่?
- ฝนสัมพันธ์กับการลดลงของ PM₂.₅ หรือไม่?
- สภาพอากาศนิ่งอาจเอื้อต่อ pollutant accumulation หรือไม่?

---

# Workflow สำหรับนิสิต

แนะนำให้ทำตามลำดับ:

```text
Air4Thai station metadata
        ↓
เลือกสถานีและพื้นที่ศึกษา
        ↓
PCD PM₂.₅ multi-year data
        ↓
ตรวจข้อมูลและสร้าง daily dataset
        ↓
วิเคราะห์รายปี / รายเดือน / ฤดูกาล
        ↓
เลือก OGIMET station
        ↓
ดาวน์โหลด meteorological data
        ↓
QC และจัดเตรียมข้อมูล
        ↓
วิเคราะห์ temperature / humidity / rain / wind
        ↓
สร้าง wind rose
        ↓
เชื่อมโยง PM₂.₅ กับ meteorology
        ↓
ตั้งคำถามวิจัยใหม่
```

---

# ตัวอย่างคำถามที่ใช้เป็นแบบฝึกหัด

นิสิตสามารถใช้ชุด Notebook นี้ตอบคำถาม เช่น:

1. PM₂.₅ เปลี่ยนแปลงอย่างไรในช่วง 5–10 ปี?
2. จังหวัดใดมีระดับ PM₂.₅ สูงกว่ากัน?
3. สถานีใดมีจำนวนวัน PM₂.₅ สูงบ่อย?
4. PM₂.₅ มี seasonal cycle หรือไม่?
5. dry season แตกต่างจาก wet season อย่างไร?
6. weekday และ weekend แตกต่างกันหรือไม่?
7. ช่วง PM₂.₅ สูงมี wind speed ต่ำหรือไม่?
8. ทิศลมใดเกิดบ่อยในช่วง pollution episode?
9. ฝนมีความสัมพันธ์กับ PM₂.₅ อย่างไร?
10. สถานีอุตุนิยมวิทยาที่อยู่ใกล้สถานี PCD เพียงพอสำหรับใช้แทน meteorology ของพื้นที่หรือไม่?

---

# การวิเคราะห์ฤดูกาล

สำหรับประเทศไทย การกำหนดฤดูกาลต้องระบุให้ชัดเจนในงานวิเคราะห์

ตัวอย่างหนึ่งที่สามารถใช้ในการสอน:

```text
Wet season : May–October
Dry season : November–April
```

แต่ควรระบุว่าเป็น **operational definition สำหรับการวิเคราะห์**

หากใช้ในงานวิจัยจริง อาจพิจารณา:

- monsoon onset / withdrawal
- precipitation climatology
- regional climate
- study-specific definition

---

# Weekday vs Weekend

ตัวอย่าง teaching definition:

```text
Weekday : Monday–Friday
Weekend : Saturday–Sunday
```

การเปรียบเทียบนี้อาจช่วยสำรวจ activity-related differences

แต่ไม่ควรสรุป source contribution จาก weekday/weekend เพียงอย่างเดียว เพราะ PM₂.₅ อาจได้รับอิทธิพลจาก:

- regional transport
- biomass burning
- boundary-layer conditions
- industrial activity
- traffic
- precipitation
- atmospheric chemistry

---

# Wind Rose และการตีความ

Wind rose ใช้แสดง:

- ความถี่ของทิศลม
- distribution ของ wind speed ตามทิศ
- prevailing wind direction

Wind rose มีประโยชน์ในการศึกษาความสัมพันธ์ระหว่างลมกับมลพิษ

แต่:

> **wind direction ≠ source attribution**

หากต้องการวิเคราะห์ source direction อย่างจริงจัง ควรพิจารณาวิธีเพิ่มเติม เช่น:

- pollution rose
- Conditional Probability Function (CPF)
- Conditional Bivariate Probability Function (CBPF)
- trajectory analysis
- emission inventory
- hotspot/fire data

---

# Air Pollution–Meteorology Interpretation

ความเข้มข้น PM₂.₅ ที่สถานีหนึ่งเป็นผลจากหลายกระบวนการ:

```text
Emission
   +
Transport
   +
Dilution / Ventilation
   +
Boundary-layer mixing
   +
Humidity / Aerosol growth
   +
Precipitation / Removal
   +
Atmospheric chemistry
```

ดังนั้นความสัมพันธ์ เช่น:

```text
PM₂.₅ สูง + ลมอ่อน
```

อาจสอดคล้องกับสภาวะที่การระบายมลพิษไม่ดี

แต่ไม่เพียงพอสำหรับกล่าวว่า:

```text
ลมอ่อนเป็นสาเหตุเดียวที่ทำให้ PM₂.₅ สูง
```

---

# หลักการ Quality Control

ก่อนทำสถิติหรือกราฟ ควรตรวจอย่างน้อย:

- station ID
- station location
- duplicated records
- date/time format
- units
- missing values
- impossible values
- data completeness
- station continuity
- temporal gaps

สำหรับข้อมูลหลายปี ควรระวัง:

- การย้ายสถานี
- การเปลี่ยนเครื่องมือ
- การเปลี่ยนหน่วย
- การเปลี่ยนวิธีรายงาน
- station metadata ที่เปลี่ยนตามเวลา

---

# หลักการทางสถิติ

## Descriptive statistics มาก่อน hypothesis test

เริ่มจาก:

- count
- mean
- median
- standard deviation
- IQR
- percentiles
- boxplot
- time series
- ECDF

ก่อนใช้ statistical tests

---

## Statistical significance ≠ Environmental significance

ค่า:

```text
p < 0.05
```

ไม่ได้หมายความว่า:

- effect ใหญ่
- environmental effect สำคัญเสมอ
- causal relationship ถูกพิสูจน์แล้ว

ควรรายงานร่วมกับ:

- effect size
- sample size
- distribution
- environmental mechanisms

---

## Correlation ≠ Causation

```text
correlation ≠ causation
```

PM₂.₅ และ meteorological variable อาจสัมพันธ์กันเพราะมี common seasonal cycle หรือ shared forcing

ควรพิจารณา temporal structure และ confounding factors ด้วย

---

# Software Environment

Notebook ออกแบบสำหรับ:

- **Google Colab**
- Python
- pandas
- NumPy
- Matplotlib
- SciPy
- GeoPandas
- Shapely
- Requests
- OpenPyXL
- windrose
- Folium และ libraries ที่เกี่ยวข้องตามแต่ละ Notebook

แต่ละ Notebook สามารถติดตั้ง package เพิ่มเติมด้วย `pip` ภายใน Colab ตามที่จำเป็น

---

# แนวคิดการเรียนการสอน

เป้าหมายของ repository ไม่ใช่ให้จำ Python syntax ทุกคำสั่ง

แต่ต้องการพัฒนาลำดับการคิด:

```text
รู้ว่าข้อมูลมาจากไหน
        ↓
รู้ว่าสถานีอยู่ที่ไหน
        ↓
ตรวจคุณภาพข้อมูล
        ↓
จัดโครงสร้างข้อมูล
        ↓
สร้างกราฟ
        ↓
เลือกสถิติที่เหมาะสม
        ↓
ตีความด้วยหลักสิ่งแวดล้อมและอุตุนิยมวิทยา
```

---

# Suggested Mini Projects

หลังเรียนครบชุดนี้ สามารถพัฒนาต่อเป็น mini project เช่น:

### Project A — PM₂.₅ Long-Term Variability

เปรียบเทียบความแปรผันรายปีของสระบุรี ลพบุรี และนครนายก

### Project B — Dry vs Wet Season

เปรียบเทียบ PM₂.₅ ระหว่างฤดูแห้งและฤดูฝน

### Project C — Weekday vs Weekend

ศึกษาความแตกต่างระหว่างวันทำงานและวันสุดสัปดาห์

### Project D — PM₂.₅ and Wind

วิเคราะห์ PM₂.₅ ร่วมกับ wind speed, wind direction และ wind rose

### Project E — Pollution Episode

เลือกเหตุการณ์ PM₂.₅ สูง แล้ววิเคราะห์:

- PM₂.₅ time series
- wind
- RH
- precipitation
- meteorological persistence

---

# การต่อยอดเชิงวิจัย

Repository นี้สามารถต่อยอดไปสู่:

- long-term trend analysis
- seasonal/interannual variability
- pollution episode analysis
- air pollution–meteorology relationships
- source-direction analysis
- CPF / CBPF
- trajectory analysis
- satellite–ground integration
- hotspot / biomass-burning analysis
- spatial GIS analysis
- exposure assessment
- health-effect studies
- statistical modeling
- machine learning

แต่ก่อนใช้วิธีขั้นสูง ควรตรวจ data quality และ conceptual model ของระบบมลพิษให้ชัดเจนก่อน

---

# Reproducibility

การวิเคราะห์ที่ทำซ้ำได้ควรเก็บ:

- source URL / data provider
- station ID
- station metadata
- study period
- raw data
- processed data
- QC rules
- parameter settings
- output tables
- figures
- package/version information

แนะนำให้แยก folder เช่น:

```text
project/
├── 00_raw/
├── 01_metadata/
├── 02_processed/
├── 03_output/
└── 04_figures/
```

---

# ข้อควรระวัง

1. Data availability ของ PCD/Air4Thai และ OGIMET อาจเปลี่ยนตามเวลา
2. URL หรือรูปแบบการเข้าถึงข้อมูลภายนอกอาจเปลี่ยน
3. station code และ metadata ต้องตรวจทุกครั้ง
4. ข้อมูลหลายปีอาจมี missing periods
5. ใกล้เชิงระยะทางไม่ได้หมายความว่า meteorological representativeness ดีที่สุดเสมอ
6. wind rose ไม่สามารถระบุแหล่งกำเนิดมลพิษได้ด้วยตัวเอง
7. correlation ไม่เท่ากับ causation
8. seasonal cycle อาจสร้าง apparent correlation
9. ควรตรวจ assumptions ของ statistical tests
10. งานวิจัยจริงควรเพิ่ม QC, completeness criteria และ validation ตามวัตถุประสงค์ของงาน

---

# Data Providers

## ข้อมูลคุณภาพอากาศ

**Pollution Control Department (PCD), Thailand / Air4Thai**

## ข้อมูลอุตุนิยมวิทยา

**OGIMET**

เมื่อใช้ข้อมูลในรายงาน วิทยานิพนธ์ การประชุมวิชาการ หรือบทความ ควรอ้างอิงผู้ให้บริการข้อมูลต้นทางตามความเหมาะสม

---

# Repository

**training_PCD_Ogimet10yr_3provinces_pm25**

https://github.com/nattaponm/training_PCD_Ogimet10yr_3provinces_pm25

---

# Citation / Acknowledgment

หากนำ code หรือ workflow จาก repository นี้ไปใช้ในการเรียน การสอน หรือการวิจัย ควรระบุแหล่งที่มาและ data providers

ตัวอย่าง acknowledgement:

> ข้อมูลคุณภาพอากาศที่ใช้ในการฝึกวิเคราะห์ได้จากกรมควบคุมมลพิษ (PCD) ผ่าน Air4Thai และข้อมูลอุตุนิยมวิทยาได้จาก OGIMET โดยใช้ Python และ Google Colab สำหรับการจัดเตรียม วิเคราะห์ และแสดงผลข้อมูล

---

# สำหรับนิสิต

สิ่งสำคัญไม่ใช่เพียง:

```text
"รันโค้ดได้"
```

แต่คือสามารถตอบได้ว่า:

1. ข้อมูลมาจากไหน?
2. สถานีอยู่ที่ใด?
3. ข้อมูลมีคุณภาพและความครบถ้วนเพียงใด?
4. ตัวแปรแต่ละตัวมีหน่วยอะไร?
5. กราฟที่สร้างตอบคำถามอะไร?
6. วิธีสถิติที่เลือกเหมาะสมหรือไม่?
7. PM₂.₅ กับ meteorology มีความสัมพันธ์เชิงกายภาพอย่างไร?
8. ข้อจำกัดของการตีความคืออะไร?

เป้าหมายคือ:

```text
"เข้าใจข้อมูล → ตรวจคุณภาพ → วิเคราะห์ → เชื่อมโยงเชิงพื้นที่และเวลา → ตีความอย่างมีเหตุผล → พัฒนาสู่คำถามวิจัย"
```
