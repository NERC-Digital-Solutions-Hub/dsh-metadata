# Environmental_CBPeru.csv

## Overview
- Dataset of measured physicochemical variables in 10 rivers from the glacial valleys of Parón, Huaytapallana, and Llanganuco in the Cordillera Blanca, Ancash, Peru.
- Linked to a study on how declining glacier cover drives changes in aquatic macroinvertebrate biodiversity.
- Aimed to analyze physicochemical changes under glacial retreat along a glacier-coverage gradient and relate them to biodiversity.

## Data content and purpose
- Contains 37 environmental variables collected across two sampling periods (wet and dry seasons) in 2019 and 2020.
- Observations from 10 sites (P01–P10) along three valleys, with site-specific geographic and topographic context.
- Data intended to support understanding of how water chemistry and related factors respond to glacier retreat and how these factors relate to macroinvertebrate biodiversity.

## Methods and data collection
- Field measurements (two periods: Oct 14–30, 2019 and Oct 7–16, 2020) include:
  - In situ: water temperature, electrical conductivity, pH, dissolved oxygen (recorded every 5 seconds and averaged over 5 minutes).
  - Laboratory: turbidity (filtered samples), concentrations of nutrients (total nitrogen, total phosphorus), dissolved organic carbon, dissolved inorganic carbon, and metal ions.
- Analytical methods:
  - Metals: Inductively Coupled Plasma Optical Emission Spectroscopy (ICP-OES).
  - Nutrients: Skalar Sans++ automatic analyzer.
  - Anions: HPLC-IC (Dionex ICS3000).
  - DOC/DIC: Analytik Jena Multi NC2100.
  - Turbidity: Oakton T-100 sensor.
- Physical channel characterization: Pfankuch Index (6 components: substrate angularity, rock brightness, sediment particle size/compaction, scouring/deposition, stability, vegetation).
- Topography and distance to glacier: derived from 12.5 m resolution DEM (slope) and 10 m Sentinel-2 imagery (distance to glacier); glacier delimitation referenced to Sentinel-2 data.

## Data structure and variables
- Structure: single Excel sheet containing data for both sampling periods.
- Columns: sites (first column) and environmental variables (first row); season indicated by d (dry) or w (wet).
- Variables (37 total) include:
  - Turbidity (NTU); Water Temperature (°C); Electrical Conductivity (µS/cm); pH; Dissolved Oxygen (mg/L); Pfankuch Index; Total Nitrogen (mg/L); Total Phosphorus (mg/L); Dissolved Organic Carbon (mg/L); Dissolved Inorganic Carbon (mg/L); Dissolved Carbon (mg/L).
  - Anions: Fluoride (F, mg/L); Chloride (Cl, mg/L); Sulfate (SO4, mg/L); Nitrate (NO3, mg/L).
  - Cations/trace elements: Aluminum (Al), Boron (B), Calcium (Ca), Potassium (K), Magnesium (Mg), Sodium (Na), Silicon (Si), Zinc (Zn), Strontium (Sr), Beryllium (Be), Cadmium (Cd), Cobalt (Co), Chromium (Cr), Copper (Cu), Iron (Fe), Lithium (Li), Manganese (Mn), Nickel (Ni), Lead (Pb), Selenium (Se), Tellurium (Te), Titanium (Ti) with corresponding units (mostly mg/L, some others as listed).
- Site-level context: each row corresponds to a site (P01–P10); site-specific geographic and geomorphometric data included.

## Site and geography
- 10 sites across three valleys:
  - Parón (P01, P02)
  - Huaytapallana (P03, P04)
  - Llanganuco (P05–P10)
- Site attributes include:
  - Basin area, glacier area, glacier coverage (GCC %), distance from glacier, slope (%), altitude (m a.s.l.).
- Notable variation in GCC across sites (ranging from very low to high) and some missing values for distance from glacier at certain sites.

## Quality control and provenance
- Instruments calibrated before field work; use of calibration standards including Environment and Climate Change Canada references and interlaboratory standards for metals.
- Data compiled and prepared by a team of contributors for sample collection, laboratory analysis, supporting information, and planning/management.

## Usage notes and caveats
- Data are provided to enable analysis of glacier retreat effects on water chemistry and downstream biodiversity; users should consider seasonal differences (wet vs. dry) and potential gaps (e.g., missing distance-from-glacier value at P08).
- The dataset supports cross-site comparisons along a glacier-coverage gradient and can feed into analyses of correlations with macroinvertebrate biodiversity reported in the associated article.
- Data origin tied to a University of Leeds laboratory workflow and the Pfankuch channel stability framework.

## References
- Pfankuch, J. D. (1975). Stream reach inventory and channel stability evaluation. USDA Forest Service Northern Region, Montana.