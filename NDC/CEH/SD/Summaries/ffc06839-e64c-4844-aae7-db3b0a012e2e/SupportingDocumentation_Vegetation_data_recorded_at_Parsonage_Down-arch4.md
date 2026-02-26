# Background: This data was created for a study which examined long-term vegetation change at Parsonage Down National Nature Reserve (NNR) between 1970 and 2016.

## Scope and purpose
- Data collected to analyze long-term vegetation change at Parsonage Down NNR across three time periods (1970, 1990, 2016).
- Includes vegetation survey data and soil chemistry data to support analysis of drivers of change.
- Aims to enable assessment of trends over time and reproducibility of the survey methodology.

## Study area
- Parsonage Down NNR, Wiltshire (51°10'17"N, 1°55'25"W), 188 ha chalk grassland.
- Designated NNR in 1973; land managed by Natural England with grazing (sheep and cattle) and no fertilisers; management timing and stocking varied across periods.

## Methods

### Vegetation survey
- Four transects laid in 1970 (Wells 1993): two longer transects (111 ft, 102 ft) and two shorter (60 ft each) to encompass Celtic field boundaries.
- Domin scale (Dahl & Hadac 1941) used to record vascular plants and bryophytes in 20 cm x 20 cm quadrats every 3 ft along each transect (total of 115 quadrats per year).
- Species identified to species level (except Taraxacum microspecies); average sward height measured in each quadrat.

### Soil survey
- 22 soil samples along each transect at depths 0–5 cm and 5–10 cm (3.5 cm diameter core).
- Analyzed for pH, loss on ignition (LOI), exchangeable K, Mg, Ca, phosphate (PO4-P) and total N.
- Detailed analytical procedures provided for each metric, including preparation, instrumentation, and QA practices.

### Transect relocation and georeferencing (2016)
- In 2016, transects re-located using geo-referenced maps to align with Wells' original Celtic field boundaries.
- Used 1:125 scale maps from CEH and archaeological GIS layers; essential to minimize pseudo-turnover due to misplacement.
- Location data collected with precision of ±2 m, with coordinates recorded for start/end of transects.

## Data collection and structure

### Vegetation data
- Files: PD_SurveyData1970.csv, PD_SurveyData1990.csv, PD_SurveyData2016.csv.
- Fields include: Transect number, Quadrat number (with N/S designation), vegetation height (cm), recorder initials, and species recorded.

### Soil data
- File: PD_SoilData.csv.
- Fields include: Transect, Position (feet along transect and N/S designation), Sample Depth (0–5 cm or 5–10 cm), LOI (%), pH, K (mg/kg), Ca (mg/kg), Mg (mg/kg), PO4-P (mg/kg), N (%).
- Note: For transect 3 in 1970 and 1990, only one soil sample per position was taken; the 0–5 cm value reflects 0–10 cm depth.

## Quality control
- Surveys conducted by experienced botanical surveyors in pairs or threes, with consistent methods and equipment.
- One surveyor contributed to both the 1970 and 2016 surveys to aid comparability.

## Data provenance, references, and access
- Transect locations and quadrat numbering aligned with Wells’ 1970 map; grid references provided for start/end of transects (±2 m accuracy) and corresponding quadrat references.
- Use of ESRI ArcGIS v10.4 for georeferencing; re-survey aligned with Celtic field boundaries to prevent misinterpretation of change.
- Data tables and methodology parallels across years to support robust temporal comparisons.
- References cited for background methods: Dahl & Hadac (1941); Fischer & Stöcklin (1997); Rodwell (1992); Wells (1993).