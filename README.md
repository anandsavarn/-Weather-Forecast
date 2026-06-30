<div align="center">

<!-- HEADER BANNER -->
<img src="https://capsule-render.vercel.app/api?type=waving&color=0:1a1a2e,50:16213e,100:0f3460&height=200&section=header&text=Weather%20Analytics%20Dashboard&fontSize=38&fontColor=4fc3f7&fontAlignY=38&desc=Real-Time%20Weather%20Intelligence%20%7C%20Power%20BI&descAlignY=58&descColor=90caf9&animation=fadeIn" width="100%"/>

<br/> 
 
![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)
![REST API](https://img.shields.io/badge/REST%20API-4fc3f7?style=for-the-badge&logo=postman&logoColor=white)
![DAX](https://img.shields.io/badge/DAX-0078D4?style=for-the-badge&logo=microsoft&logoColor=white)
![JSON](https://img.shields.io/badge/JSON-000000?style=for-the-badge&logo=json&logoColor=white)
![WeatherAPI](https://img.shields.io/badge/WeatherAPI.com-FF6B35?style=for-the-badge&logo=cloudflare&logoColor=white)

<br/>

> **Transforming raw weather API data into actionable intelligence using Power BI, DAX, and real-time API integration.**

<br/>

[![View Project](https://img.shields.io/badge/📂%20View%20Project%20Files-Google%20Drive-4285F4?style=for-the-badge&logo=googledrive&logoColor=white)](https://drive.google.com/file/d/1loejnlgIycp4daC6-NcuSU83-aNSM2Sq/view?usp=drive_link)
[![LinkedIn Post](https://img.shields.io/badge/💼%20LinkedIn%20Post-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/feed/update/urn:li:activity:7406832792334110720/)
[![Portfolio](https://img.shields.io/badge/🌐%20Portfolio-anandsavarn.vercel.app-00C896?style=for-the-badge)](https://anandsavarn.vercel.app)

</div>

---

## 📸 Dashboard Preview

<div align="center">
<img src="https://raw.githubusercontent.com/Anandsavarn/Weather-Analytics-Dashboard/main/assets/dashboard-preview" alt="Weather Analytics Dashboard" width="95%" style="border-radius:10px; box-shadow: 0 4px 20px rgba(0,0,0,0.3);"/>

> *Real-time weather dashboard showing temperature trends, AQI, forecast, wind speed, and precipitation data for multiple cities.*
</div>

---

## 🌟 Project Overview

The **Real-Time Weather Analytics Dashboard** is a data analytics project built in **Microsoft Power BI** that connects live to the WeatherAPI.com REST API, fetches JSON weather data, transforms it using **Power Query**, and visualizes it through an interactive multi-panel dashboard.

This project goes beyond basic charts — it implements **DAX time intelligence**, **wind classification logic**, **AQI indicators**, and **conditional formatting** to provide a complete picture of atmospheric conditions across multiple Indian cities.

---

## ✅ What This Project Demonstrates

| Skill Area | Details |
|---|---|
| 🔌 **API Integration** | Live REST API connection via Power BI Web connector |
| 🧹 **Data Cleaning** | JSON flattening, null handling, type conversion in Power Query |
| 🧮 **DAX Calculations** | Time intelligence, KPIs, risk indicators, classification logic |
| 📊 **Dashboard Design** | Multi-panel layout, conditional formatting, AQI gauge |
| 📡 **Real-Time Data** | Dynamic refresh with live weather feed |

---

## 🛠️ Tech Stack

```
📊 Microsoft Power BI     →  Dashboard & Visualization
🌐 WeatherAPI.com REST    →  Real-time JSON Data Source
🔄 Power Query (M)        →  ETL & Data Transformation
🧮 DAX                    →  Measures, KPIs, Time Intelligence
📁 JSON → Tabular         →  Schema flattening & normalization
```

--- 

## 📡 Data Source

| Property | Detail |
|---|---|
| **Provider** | [WeatherAPI.com](https://www.weatherapi.com/) |
| **Format** | JSON (REST API endpoint) |
| **Type** | Real-time + Historical Weather Data |
| **Cities Tracked** | Amritsar, Hyderabad, Jaipur (expandable) |

**Parameters fetched:**

`Date/Time` • `Location` • `Temperature °C` • `Feels Like °C` • `Humidity %` • `Wind Speed km/h` • `Precipitation mm` • `Pressure mb` • `UV Index` • `Visibility` • `Weather Condition` • `AQI Components (CO, PM2.5, PM10, O3, NO2, SO2)`

---

## 🔄 Data Pipeline

```
WeatherAPI.com (JSON)
        │
        ▼
Power BI Web Connector
        │
        ▼
Power Query (ETL)
  ├── JSON → Tabular Expansion
  ├── Duplicate Removal
  ├── Null/Missing Value Handling
  ├── Date-Time Format Standardization
  ├── Unit Normalization (°C, km/h, mm)
  └── Column Renaming & Type Assignment
        │
        ▼
Data Model + DAX Measures
        │
        ▼
Interactive Power BI Dashboard
```

---

## 📊 Dashboard Modules

### 🌡️ 1. Temperature Analysis
- Average temperature measure with variance tracking
- **Actual vs Feels Like** temperature comparison
- Heat index / wind chill delta
- 24-hour and 7-day trend line

### ⏳ 2. Time Intelligence (DAX)
- Previous Day Temperature comparison
- Week-over-Week change calculation
- Dynamic date slicer with rolling window

### 🌬️ 3. Wind Speed Classification

| Category | Speed Range |
|---|---|
| 🟢 Calm | 0–5 km/h |
| 🔵 Breeze | 6–20 km/h |
| 🟡 Moderate | 21–40 km/h |
| 🟠 High Wind | 41–70 km/h |
| 🔴 Extreme | > 70 km/h |

### 🎨 4. Dynamic Conditional Formatting

```
Temperature > 30°C  →  🔴 Red   (Hot)
Temperature 15–30°C →  🟡 Yellow (Mild)
Temperature < 15°C  →  🔵 Blue  (Cold)
```

### 🌧️ 5. Rainfall Risk KPI
- High Risk Alert triggered at `precipitation > 2.5mm`
- Flood Risk Indicator with color-coded severity

### 🫁 6. Air Quality Index (AQI) Panel
Real-time pollutant tracking across 6 parameters:

| Pollutant | Measured |
|---|---|
| CO | Carbon Monoxide |
| PM10 | Coarse Particulate Matter |
| O3 | Ozone |
| PM2.5 | Fine Particulate Matter |
| NO2 | Nitrogen Dioxide |
| SO2 | Sulfur Dioxide |

---

## 📌 Key Insights Discovered

> 💡 **Humidity & Precipitation Correlation** — Rainfall events observed predominantly when humidity exceeded **85%**
>
> 💡 **Feels Like Gap** — A consistent **2–4°C difference** between actual and perceived temperature under high humidity conditions
>
> 💡 **AQI Alert** — Dashboard flagged *"Unhealthy for Sensitive Groups"* status in Amritsar (AQI: 132.15), matching real-world winter fog patterns
>
> 💡 **Dynamic Refresh** — API-connected model enables up-to-date reporting without manual data entry

---

## 🧠 Skills Demonstrated

```
✔ REST API Integration in Power BI
✔ JSON Data Extraction & Flattening
✔ Power Query (M Language) Transformations
✔ Advanced DAX — Measures, Calculated Columns, Variables
✔ Time Intelligence Functions (DATEADD, PREVIOUSDAY, etc.)
✔ KPI Cards & Conditional Formatting
✔ AQI Gauge & Risk Indicator Design
✔ Multi-city Comparative Dashboard
✔ Analytical Thinking & Business Storytelling
```

---

## 🔮 Future Roadmap

- [ ] 🔵 Azure ML integration for temperature forecasting
- [ ] 🌍 Multi-city comparative dashboard (pan-India)
- [ ] 🔔 Automated alert system for extreme weather events
- [ ] 📡 Real-time streaming dataset via Power BI Streaming API
- [ ] 🗺️ Map visualization by geo-coordinates
- [ ] 📱 Mobile-optimized Power BI report layout

---

## 📁 Repository Structure

```
📦 Weather-Analytics-Dashboard
 ┣ 📊 WeatherDashboard.pbix       ← Main Power BI file
 ┣ 📄 README.md                   ← Project documentation
 ┣ 📁 assets/
 ┃  ┗ 🖼️ dashboard-preview.png   ← Dashboard screenshot
 ┣ 📁 data-samples/
 ┃  ┗ 📋 sample-weather.json      ← Sample API response
 ┗ 📁 dax-measures/
    ┗ 📝 measures.md              ← Key DAX formulas documented
```

---

## 📖 References

- [WeatherAPI.com Documentation](https://www.weatherapi.com/docs/)
- [Microsoft Power BI Official Docs](https://docs.microsoft.com/en-us/power-bi/)
- [DAX Guide — SQLBI](https://dax.guide/)
- [World Meteorological Organization Standards](https://www.wmo.int/)

---

<div align="center">

### 👨‍💻 Author

**Anand Kumar**
B.Tech – Computer Science Engineering (Data Science)
Lovely Professional University, Punjab

<br/>

[![Portfolio](https://img.shields.io/badge/🌐%20Portfolio-anandsavarn.vercel.app-00C896?style=for-the-badge)](https://anandsavarn.vercel.app)
[![GitHub](https://img.shields.io/badge/GitHub-Anandsavarn-181717?style=for-the-badge&logo=github)](https://github.com/Anandsavarn)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=for-the-badge&logo=linkedin)](https://www.linkedin.com/feed/update/urn:li:activity:7406832792334110720/)

<br/>

---

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0f3460,50:16213e,100:1a1a2e&height=100&section=footer" width="100%"/>

*⭐ Star this repo if you found it helpful!*

</div>
