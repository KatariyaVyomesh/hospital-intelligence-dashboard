# 🏥 Hospital Intelligence Dashboard

A professional, end-to-end analytics solution that turns raw hospital data into crystal-clear insights.  
Built with **Power BI** (front-end), **SQL** (data mart), and **DAX** (business logic), the dashboard lets clinicians and administrators track quality of care, operational efficiency, and financial health in real-time.

---

## 📖 Table of Contents
1. [Project Overview](#project-overview)  
2. [Technology Stack](#technology-stack)  
3. [Screenshots](#screenshots)  
4. [Page-by-Page Feature Guide](#page-by-page-feature-guide)  
   - [Home](#home)  
   - [Overview](#overview-page)  
   - [Patient](#patient-page)  
   - [Doctor](#doctor-page)  
   - [Surgery](#surgery-page)  
   - [Finance](#finance-page)  
5. [DAX Measures](#dax-measures)  
6. [Key Metrics Tracked](#key-metrics-tracked)  
7. [Setup & Deployment](#setup--deployment)  
8. [Author](#author)  
9. [License](#license)  

---

## Project Overview

> **Objective:** Build a single, unified dashboard that consolidates patient, clinical, inventory, and financial data—enabling faster, data-driven decisions and improved patient outcomes.

**Highlights**  
- ⚡ Real-time SQL refresh for up-to-the-minute KPIs  
- 🎛️ Intuitive slicers & bookmarks for rapid filtering  
- 📈 Gauge, line, clustered/stacked bar & 100% stacked column visuals  
- 🔍 Drill-through into individual patients, doctors, surgeries, and SKUs  

---

## Technology Stack

| Layer           | Tools / Frameworks       | Purpose                        |
|----------------|--------------------------|--------------------------------|
| **Data**       | SQL Server / Azure SQL   | ETL, views, stored procs       |
| **Modeling**   | Power BI Data Model, DAX | Business logic & calculations  |
| **Visualization** | Power BI Desktop / Service | Interactive dashboards     |
| **Version Control** | Git + GitHub         | Source management & CI tracking|

---

## Screenshots

| Page     | Image                                   |
|----------|-----------------------------------------|
| Home     | ![Home](Images/Home.png)                |
| Overview | ![Overview](Images/Overview.png)        |
| Patient  | ![Patient](Images/Patient.png)          |
| Doctor   | ![Doctor](Images/Doctor.png)            |
| Surgery  | ![Surgery](Images/Surgery.png)          |
| Finance  | ![Finance](Images/Finance.png)          |

---

## Page-by-Page Feature Guide

### Home
| Section            | Description                                             |
|--------------------|---------------------------------------------------------|
| **Hero Banner**     | “Transforming Healthcare Data into Actionable Insights” |
| **Quick KPIs**      | Doctors · Patients · Beds · Medicine · Finance · Appt. |
| **Navigation Tiles**| Icons for all detail pages                             |
| **Credits**         | By Vyomesh Katariya – [GitHub](https://github.com/vyomeshkatariya) |

---

### Overview Page
| Feature               | Detail                                         |
|-----------------------|------------------------------------------------|
| **Global KPIs**       | Patient, Doctor, Staff, Bill counts · Bed %    |
| **Medicine Activity** | Monthly sales & stock flows                    |
| **Trends**            | Admissions, Discharges, Revenue Line Charts   |
| **Resource Snapshot** | Staff & Doctor availability heatmaps          |

---

### Patient Page
| Area                | Visual / Control  | Description                             |
|---------------------|-------------------|-----------------------------------------|
| **Medicine Tracking**| Line Chart        | Per-patient monthly medicine quantity   |
| **Profile**          | Cards             | Name, Age, Gender, Contact              |
| **Admission History**| Table             | Admit · Discharge · Stay Duration       |
| **Billing**          | KPIs              | Total Bill · Paid · Pending             |
| **Appointments**     | Timeline          | Date · Time · Doctor                    |
| **Bookmark**         | "Edit" Button     | Choose patient name → filters auto-applied|

---

### Doctor Page
| Area                  | Visual / Control | Description                                  |
|-----------------------|------------------|----------------------------------------------|
| **Schedule**          | Table            | Upcoming Appointments (Name · Time)          |
| **Doctor Info**       | Cards            | Specialty · Experience · Contact             |
| **Financials**        | Gauges           | Commission % · Fees · Total Billing          |
| **Live Metrics**      | Real-time KPIs   | SQL-driven bill & commission stats           |
| **History Table**     | Table            | Past & future appointments with status       |
| **Bookmark (“View Doctor Details”)** | Button | *Reveals doctor list → filters full report* |

---

### Surgery Page
| Area                 | Visual / Control    | Description                                |
|----------------------|---------------------|--------------------------------------------|
| **Doctor Slicer**     | Dropdown / Buttons  | Filter surgeries by surgeon                |
| **Age Distribution**  | Clustered Bar Chart | Age-wise surgery counts                    |
| **Bed Utilization**   | 100% Stacked Column | Occupied Beds per Room Type                |
| **Details Table**     | Table               | Full surgery-level info                    |
| **Staff Filter**      | Dropdown            | Filter surgeries by assisting staff        |
| **Doctor Appointment**| Table               | Full surgery schedule by doctor            |

---

### Finance Page
| Area                 | Visual / Control     | Description                                 |
|----------------------|----------------------|---------------------------------------------|
| **Month Slicer**      | Dropdown / Slider    | Global month filter                         |
| **Medicine Sales**    | Line Chart           | Monthly sales quantities                    |
| **KPI Cards**         | Cards                | Bills · Staff · Doctors · Medicine Count    |
| **Financial Overview**| KPI + Card visuals   | Bill Amount · Staff Salaries                |
| **Inventory Charts**  | Bar/Column Charts    | Stock by Category · Cost vs Selling Price   |
| **Bookmark (Medicine)**| Button              | Click → pick medicine → visuals update      |

---

## DAX Measures

| #  | Name                           | Description                                             |
|----|--------------------------------|---------------------------------------------------------|
| 1  | Medicine Quantity              | Total quantity sold / dispensed                        |
| 2  | Sum of Rating (⭐)             | Average star rating by doctor                          |
| 3  | Total Bill Amount              | Overall billing (per patient/month)                    |
| 4  | Doctor Commission %            | Commission % per doctor                                |
| 5  | Doctor Status                  | Active/Inactive status                                 |
| 6  | Dynamic Doctor Appointment     | Sliced appointment table                               |
| 7  | Dynamic Doctor-Patient Appt.   | Patient list filtered by selected doctor               |
| 8  | Estimate Doctor Commission     | Forecasted commission based on bill amount             |
| 9  | Max Amount                     | Highest bill recorded                                  |
|10  | Max Rate                       | Highest rating achieved                                |
|11  | Total Fees by Patient          | Aggregated consultation/treatment fees per patient     |
|12  | Bed Occupied Target KPI        | Target = Previous Month + 5%                           |
|13  | Bed Occupied Selected Month    | Current month's occupancy                              |
|14  | Bed Occupied Trend             | Occupancy trend over time                              |
|15  | Bill Count                     | Number of invoices generated                           |
|16  | Patient Count                  | Unique patients                                         |
|17  | Doctor Count                   | Total active doctors                                   |
|18  | Medicine Count                 | Unique medicine types                                  |
|19  | Staff Count                    | Total staff available                                  |
|20  | Total Admission                | Patient admissions                                     |
|21  | Dynamic Surgery Appointment    | Filtered surgical appointment list                     |

---

## Key Metrics Tracked

- **Clinical:** Admissions · Discharges · Surgeries · Bed Occupancy · Patient Age Mix  
- **Operational:** Doctor Appointments · Staff Allocation · Room/Bed Utilization  
- **Financial:** Total Bills · Doctor Fees · Commissions · Staff Salaries · Surgery Fees  
- **Inventory:** Medicine Sales · Stock Levels · Reorder Counts · Cost vs Selling Price  

---

## Setup & Deployment

```bash
# 1. Clone the repository
git clone https://github.com/vyomeshkatariya/hospital-intelligence-dashboard.git
cd hospital-intelligence-dashboard

# 2. Open Power BI
#    - Load the .pbix file
#    - Set up your SQL connection (if required)
#    - Replace relative paths for images with Power BI Web URLs or base64-encoded images

# 3. Optional
#    - Publish to Power BI Service for auto-refresh setup
#    - Adjust bookmarks/slicers for user-specific roles
