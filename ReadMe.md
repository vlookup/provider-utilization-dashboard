# Healthcare Provider Utilization & Cost Dashboard  
### CMS Inpatient Claims Analysis (2023)

## 📌 Overview
This project analyzes Medicare inpatient utilization and cost patterns using the publicly available **CMS “Medicare Inpatient Hospitals – By Provider and Service (2023)”** dataset.  
The dashboard highlights:

- Provider-level performance  
- DRG-level cost and utilization  
- Length of stay patterns  
- Cost per encounter  
- High-cost service lines  

This project demonstrates healthcare domain knowledge, claims analytics, KPI design, and dashboard development using Power BI.

---

## 📂 Dataset
**Source:** Centers for Medicare & Medicaid Services (CMS)  
**Dataset:** Medicare Inpatient Hospitals – By Provider and Service (2023)  
**Format:** CSV + PDF documentation

This dataset includes:

- Provider ID & Name  
- DRG (Diagnosis Related Group)  
- Number of discharges  
- Average covered charges  
- Average total payments  
- Average Medicare payments  
- Average length of stay (ALOS)  
- Provider location (city, state, ZIP)

---

## 🧠 Key Metrics (KPIs)

### Utilization
- Total discharges  
- Discharges by DRG  
- Discharges by provider  

### Cost
- Total cost  
- Cost per discharge  
- Average total payments  
- Average Medicare payments  
- Cost by DRG  
- Cost by provider  

### Quality / Efficiency
- Average length of stay (ALOS)  
- Cost vs ALOS comparison  
- DRG efficiency patterns  

---

## 📊 Dashboard Pages

### 1️⃣ Executive Summary
High-level overview of provider utilization and cost.

**Visuals include:**
- KPI strip (Total Discharges, Total Cost, Cost per Discharge, ALOS)  
- Cost by provider  
- Discharges by provider  
- Encounter mix  

---

### 2️⃣ DRG Analysis
Deep dive into service line performance.

**Visuals include:**
- Top DRGs by cost  
- Top DRGs by volume  
- Cost vs ALOS scatter plot  
- DRG detail table  

---

### 3️⃣ Provider Performance
Comparison of hospitals and health systems.

**Visuals include:**
- Provider cost ranking  
- Provider ALOS comparison  
- Provider × DRG heatmap  
- Best/worst performing providers  

---

### 📚 Field Dictionary

This section documents the original CMS field names, their cleaned/renamed versions used in the data model, and a clear description of each field. This improves readability, supports semantic modeling, and ensures the dashboard is business‑friendly.

| Original Field | Renamed Field | Description | Usage in Dashboard |
|----------------|---------------|-------------|--------------------|
| `Rndrng_Prvdr_CCN` | Provider CCN | CMS Certification Number; unique identifier for each hospital/provider | Provider-level grouping, slicers |
| `Rndrng_Prvdr_Org_Name` | Provider Name | Name of the hospital or healthcare organization | Visual labels, tables, slicers |
| `Rndrng_Prvdr_City` | Provider City | City where the provider is located | Optional geography visuals |
| `Rndrng_Prvdr_St` | Provider State | State where the provider is located | State-level comparisons |
| `Rndrng_Prvdr_State_FIPS` | State FIPS | Numeric state code used for federal reporting | Optional mapping or grouping |
| `Rndrng_Prvdr_Zip5` | Provider ZIP | Provider’s 5-digit ZIP code | Optional geography visuals |
| `Rndrng_Prvdr_State_Abrvtn` | State Abbreviation | Standard two-letter state abbreviation | Clean slicer for geography |
| `Rndrng_Prvdr_RUCA` | RUCA Code | Rural–Urban Commuting Area classification code | Provider segmentation (urban vs rural) |
| `Rndrng_Prvdr_RUCA_Desc` | RUCA Description | Text description of RUCA category | Optional demographic segmentation |
| `DRG_Cd` | DRG Code | Diagnosis Related Group code representing a service line | DRG-level analysis, grouping |
| `DRG_Desc` | DRG Description | Description of the DRG (e.g., “Heart Failure & Shock”) | Visual labels, tables |
| `Tot_Dschrgs` | Total Discharges | Number of inpatient discharges for the provider + DRG | Core utilization metric |
| `Avg_Submtd_Cvrd_Chrg` | Avg Submitted Charges | Average submitted covered charges for the DRG | Charge-level cost comparison |
| `Avg_Tot_Pymt_Amt` | Avg Total Payments | Average total payments made for the DRG | Cost per encounter, provider ranking |
| `Avg_Mdcr_Pymt_Amt` | Avg Medicare Payments | Average Medicare payments for the DRG | Payer liability analysis |
