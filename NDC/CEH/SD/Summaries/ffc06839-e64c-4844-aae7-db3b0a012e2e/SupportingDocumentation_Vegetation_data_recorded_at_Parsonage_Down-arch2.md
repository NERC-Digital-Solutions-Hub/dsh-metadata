# Long-term change in calcareous grassland vegetation and drivers over three time periods between 1970 and 2016

## Overview
- A dataset from Parsonage Down National Nature Reserve (NNR), Wiltshire, examining long-term vegetation change across three time periods: 1970, 1990, and 2016.
- Focuses on calcareous chalk grassland and associated soil properties to understand drivers of vegetation change.
- Data designed for monitoring environmental health and policy performance over time, with standardized methods and robust quality control.

## Study Area
- Parsonage Down NNR, Wiltshire (188 ha of chalk grassland).
- Designated as an NNR in 1973; management has involved grazing (cattle and sheep) with no fertilizer usage in the Natural England era; stocking levels have varied over time.

## Methods

### Vegetation Survey
- Four transects established in 1970; transect lengths: 111 ft (transects 1), 102 ft (transect 2), 60 ft (transects 3 and 4).
- Vegetation recorded in 20 cm x 20 cm quadrats every 3 ft along each transect.
- Vascular plants identified to species level (Taraxacum microspecies excluded); bryophytes included.
- Domin scale used to record cover/abundance (scale 1–10; with explicit cover ranges).
- Average sward height measured per quadrat.
- Survey years: 1970, 1990, 2016.
- Data structure: PD_SurveyData1970.csv, PD_SurveyData1990.csv, PD_SurveyData2016.csv.
- Recorder initials recorded (e.g., LR, PH, RW, TW, JW, RC).

### Soil Sampling and Analysis
- 22 soil samples per transect, at depths 0–5 cm and 5–10 cm.
- Analyzed properties per sample: pH, loss on ignition (LOI), exchangeable K, Mg, Ca, phosphate (PO4-P), total nitrogen (N).
- Analytical methods detailed per property (pH measurement protocol; LOI via ignition; N via combustion; cation analysis via ICP-OES; PO4-P via Olsen extraction and colorimetric analysis).
- Data structure: PD_SoilData.csv.
- Note: For transect 3 in 1970 and 1990, only one soil sample per position; the 0–5 cm value reflects depth 0–10 cm.

### Transect Relocation and Georeferencing
- In 2016, transects re-located by geo-referencing Wells’ 1970 maps to 1:125 scale CEH GIS layers, ensuring alignment with Celtic field boundaries.
- This step reduces pseudo-turnover by preventing misattribution of species turnover due to misplacement.
- Layout and coordinates for start/end of transects and quadrats recorded with high precision (± 2 m) and documented grid references.

### Quality Control
- Surveys conducted by experienced botanists in pairs (or threes); one observer involved across years to ensure consistency.
- Consistent recording methods and equipment used across years.

## Data Collected and Structure

### Vegetation Data
- Files: PD_SurveyData1970.csv, PD_SurveyData1990.csv, PD_SurveyData2016.csv.
- Fields (example structure): 
  - Transect number (1–4)
  - Quadrat number with N/S designation
  - Vegetation height (cm)
  - Recorder initials (e.g., LR, PH, RW, TW, JW, RC)
  - Species (all recorded vascular plants and bryophytes)

### Soil Data
- File: PD_SoilData.csv
- Fields (example structure):
  - Transect number (1–4)
  - Position (feet along transect; N/S)
  - Sample Depth (0–5 cm or 5–10 cm)
  - LOI (%)
  - pH
  - K (mg/kg)
  - Ca (mg/kg)
  - Mg (mg/kg)
  - PO4-P (mg/kg)
  - N (%)

### Special Notes on Data
- For transect 3, 1970 and 1990 have only one soil sample per position; the 0–5 cm value for these entries reflects 0–10 cm depth.
- Vegetation data capture 115 quadrats per year across all transects.

## Temporal Coverage and Location Details
- Survey years: 1970, 1990, 2016.
- Transects relocated and re-surveyed in 2016 using GIS-based alignment to original Celtic field boundaries to ensure accurate comparison across time.

## Relevance for Environmental Monitoring Analysts
- Standardized long-term dataset enabling the assessment of environmental health and policy outcomes in calcareous grasslands.
- Combines vegetation composition and structure with soil chemistry, aiding examination of abiotic drivers of vegetation change.
- Geo-referenced relocation supports robust trend analysis and reduces turnover artefacts, aligning with best practices in Environmental Monitoring.
- Data are organized in clear, standardized CSV formats suitable for integration with other datasets and for temporal trend analyses.

## References
- Dahl, E., & Hadac, E. (1941). Strandgesellschaften der Insel Ostøya im Oslofjord.
- Fischer, M., & Stöcklin, J. (1997). Local extinctions of plants in remnants of extensively used calcareous grasslands 1950–1985. Conservation Biology, 11(3), 727-737.
- Rodwell, J. S. (1992). British Plant Communities Volume 3. Cambridge University Press.
- Wells, T. C. E. (1993). Effects of excess nitrogen on calcareous grasslands. In Annual Report 1992-1993, Institute of Terrestrial Ecology, NERC.