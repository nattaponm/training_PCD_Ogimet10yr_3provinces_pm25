# PCD Air Pollution and OGIMET Meteorological Data Analysis

## Python and Google Colab Training for Environmental Studies

This repository contains **Python codes and Google Colab notebooks developed for teaching and training in environmental data analysis**. The materials are designed primarily for students in **environmental science, geography, geoinformatics, atmospheric science, and related disciplines** who would like to learn how to acquire, manage, visualize, and analyze real environmental datasets using Python.

The training focuses on the integration of **air-quality monitoring data from the Pollution Control Department (PCD), Thailand**, through the **Air4Thai** platform, with meteorological observations obtained from **OGIMET**.

The main study areas used in the exercises are three provinces in Central Thailand:

* **Saraburi**
* **Lopburi**
* **Nakhon Nayok**

The notebooks are intended as practical examples that students can subsequently modify and extend for their own coursework, theses, and environmental research projects.

---

## Objectives

The main objectives of this repository are to provide students with practical experience in:

1. accessing and downloading air-quality monitoring data from PCD/Air4Thai;
2. organizing multi-year air-pollution datasets by monitoring station;
3. working with approximately 5–10 years of daily air-quality observations;
4. comparing air-pollution characteristics among monitoring stations and provinces;
5. downloading meteorological observations from OGIMET;
6. identifying and mapping meteorological stations relevant to the study area;
7. preparing meteorological variables for environmental analysis;
8. visualizing meteorological conditions using time-series graphs and other plots;
9. analyzing wind speed and wind direction;
10. producing **wind rose diagrams**; and
11. integrating air-quality and meteorological information for further environmental analysis.

---

## Study Areas

The examples emphasize monitoring stations located in or around:

### Saraburi Province

Saraburi represents an important mixed industrial, transportation, agricultural, and urban environment. It provides a useful case study for investigating temporal variability in particulate matter and its possible relationships with meteorological conditions.

### Lopburi Province

Lopburi is included to allow comparison of air-quality conditions across neighboring areas and to provide examples of obtaining meteorological observations from stations surrounding the province.

### Nakhon Nayok Province

Nakhon Nayok provides an additional environmental setting for comparison with Saraburi and Lopburi and can be used to explore spatial differences in air-pollution behavior.

---

## Data Sources

### 1. Air-Quality Data

Air-quality observations are obtained from the **Pollution Control Department (PCD), Thailand**, through Air4Thai.

The teaching workflow focuses primarily on station-based observations of:

* PM₂.₅
* PM₁₀
* and other available air-pollution variables, depending on station data availability.

The notebooks demonstrate how multi-year observations can be prepared as **daily datasets** for subsequent temporal and statistical analyses.

---

### 2. Meteorological Data

Meteorological observations are obtained from **OGIMET**, which provides access to meteorological station observations from international weather-reporting networks.

Depending on station and period availability, variables may include:

* air temperature;
* relative humidity;
* atmospheric pressure;
* wind speed;
* wind direction;
* precipitation; and
* other available meteorological observations.

The notebooks demonstrate how to identify appropriate meteorological stations, retrieve observations for selected periods, prepare the data, and visualize meteorological conditions.

---

## Repository Contents

The current teaching notebooks include the following examples.

### `01__PCDpm2_5_pcd_วิเคราะห์5ปี_สระบุรี_ลพบุรี_นครนายก.ipynb`

Introduction to PCD PM₂.₅ data analysis using observations from **Saraburi, Lopburi, and Nakhon Nayok**.

The notebook provides an example of multi-year station-based air-quality analysis and introduces students to the basic workflow for preparing and exploring PM₂.₅ data.

---

### `02__PCDpm2_5_pcd_วิเคราะห์10ปี_สระบุรี_.ipynb`

Example of a longer-term PM₂.₅ analysis focusing on **approximately 10 years of observations in Saraburi Province**.

The notebook can be used as a template for extending the same workflow to additional stations and provinces.

---

### `03_PCDข้อมูลอุต_แผนที่ตำแหน่งสถานีogimet_ประเทศไทย_สระบุรี.ipynb`

Introduction to meteorological station information and the geographic distribution of **OGIMET-compatible meteorological stations** relevant to Thailand and the Saraburi study area.

The notebook helps students understand the spatial relationship between air-quality monitoring stations and meteorological observation stations.

---

### `04_PCDดาวน์โหลดข้อมูลอากาศ_Ogimet_สถานีรอบสระบุรี_เวิร์คข้อมูลทดสอบ.ipynb`

Example workflow for downloading and testing **OGIMET meteorological data from stations surrounding Saraburi**.

This notebook is intended to help students understand the structure of downloaded meteorological observations before proceeding to more detailed analysis.

---

### `05_PCDดาวน์โหลดข้อมูลอุตุนิยมวิทยาจาก_OGIMET_เน้นสถานีลพบุรี_เลือกเวลาได้.ipynb`

Example for retrieving **OGIMET meteorological observations with a user-defined time period**, with emphasis on stations relevant to **Lopburi Province**.

The notebook demonstrates how the same data-acquisition workflow can be adapted to different locations and periods.

---

### `06_PCDวิเคราะห์พลอตข้อมูลอุต_Ogimet_ipynb.ipynb`

Meteorological exploratory data analysis and visualization.

Examples include visualization of meteorological variables and wind characteristics, providing the foundation for analyses such as:

* wind-speed distributions;
* wind-direction distributions;
* temporal meteorological variation;
* wind rose diagrams; and
* comparison between meteorological conditions and air-pollution observations.

---

## General Learning Workflow

The repository follows a progressive environmental-data workflow:

**Air4Thai / PCD data acquisition**

↓

**Station selection**

↓

**Multi-year data preparation**

↓

**Daily air-quality dataset**

↓

**Exploratory data analysis**

↓

**Temporal visualization and descriptive statistics**

↓

**OGIMET station identification**

↓

**Meteorological data acquisition**

↓

**Meteorological visualization**

↓

**Wind-speed and wind-direction analysis**

↓

**Wind rose analysis**

↓

**Integration of air pollution and meteorology**

↓

**Further environmental research applications**

---

## Example Analyses

Students can use the notebooks as a starting point to investigate questions such as:

* How has PM₂.₅ changed during the last 5–10 years?
* Which monitoring stations experience relatively high PM₂.₅ concentrations?
* How does PM₂.₅ vary among Saraburi, Lopburi, and Nakhon Nayok?
* What are the seasonal patterns of air pollution?
* How do dry- and wet-season concentrations differ?
* Are weekday and weekend pollution levels different?
* Which wind directions occur during high-PM₂.₅ conditions?
* How does wind speed influence pollutant accumulation or dispersion?
* Are particular meteorological conditions associated with pollution episodes?
* Can neighboring meteorological stations be used to support interpretation of PCD air-quality observations?

---

## Application to Student Research

These notebooks are designed as **teaching examples rather than fixed analytical pipelines**.

Students are encouraged to modify:

* monitoring stations;
* provinces;
* study periods;
* pollutants;
* meteorological stations;
* temporal aggregation;
* statistical methods; and
* visualization approaches

according to their own research questions.

After completing these exercises, students should be able to use Python and Google Colab as a foundation for more advanced environmental analyses, including:

* long-term air-pollution trend analysis;
* seasonal and interannual variability;
* pollution episode analysis;
* air pollution–meteorology relationships;
* source-direction analysis;
* Conditional Probability Function (CPF);
* trajectory analysis;
* satellite–ground data integration;
* spatial analysis and GIS;
* statistical modeling; and
* air-pollution exposure and health studies.

---

## Software Environment

The notebooks are primarily designed for:

* **Google Colab**
* **Python**
* Pandas
* NumPy
* Matplotlib
* SciPy
* GeoPandas
* windrose and related visualization libraries

Additional libraries may be installed within individual notebooks where required.

Using Google Colab allows students to execute the notebooks through a web browser without requiring a complete local Python installation.

---

## Educational Philosophy

The emphasis of these materials is not only on learning Python syntax, but also on developing a reproducible environmental-data workflow:

> **Data acquisition → Data inspection → Data preparation → Quality control → Exploratory analysis → Visualization → Statistical analysis → Environmental interpretation**

Students are encouraged to understand the environmental meaning of the data before applying advanced statistical or machine-learning methods.

---

## Intended Users

These materials are particularly suitable for:

* undergraduate students in advanced environmental-data courses;
* Master's students beginning Python-based research;
* students in environmental science;
* geography and physical geography students;
* geoinformatics students;
* atmospheric and meteorological science students; and
* researchers beginning air-quality data analysis in Python.

---

## Important Notes

The notebooks are provided primarily for **educational and research-training purposes**.

Data availability, station identifiers, variable names, and access methods from external data providers may change over time. Users should therefore verify the current data structure and metadata from the original data providers before applying the notebooks to formal scientific research.

For research applications, additional quality-control procedures, completeness criteria, statistical assumptions, and validation procedures should be considered according to the specific research objectives.

---

## Data Providers

Air-quality data used in the teaching examples are obtained from the **Pollution Control Department (PCD), Thailand / Air4Thai**.

Meteorological observations are accessed through **OGIMET**.

Users should acknowledge and cite the original data providers appropriately when using the data for theses, reports, conference presentations, or scientific publications.

---

## Purpose of This Repository

The overall purpose of this repository is to provide students with a practical starting point for using **Python and Google Colab to analyze real environmental monitoring data** and to encourage them to adapt these workflows to their own environmental research questions.

The repository will continue to be developed as additional teaching examples and analytical methods are introduced.
