# Background: This data was created for a study which examined long-term vegetation change at Parsonage Down National Nature Reserve (NNR) between 1970 and 2016.

- Purpose and scope
  - Dataset documents long-term vegetation change at Parsonage Down NNR from 1970 to 2016.
  - Primary data files: PD_SurveyData1970.csv, PD_SurveyData1990.csv, PD_SurveyData2016.csv (vegetation data); PD_SoilData.csv (soil data).

- Study area
  - Parsonage Down NNR, Wiltshire (188 ha of chalk grassland).
  - Designated as an NNR in 1973; grazing by sheep and cattle without fertilisers in later periods; management changes over time.

- Survey design and data collection (vegetation)
  - Four transects established in 1970 (Wells, 1993); transect lengths and coordinates chosen to cover Celtic field boundaries.
  - Domin scale (10 categories) used to record vascular plant and bryophyte cover in 20 cm x 20 cm quadrats every 3 ft along each transect (total 115 quadrats/year).
  - Measurements per quadrat: vegetation height (cm); species recorded to species level (except Taraxacum microspecies); recorders noted (LR, PH, RW, TW, JW, RC).
  - Years of vegetation data: 1970, 1990, 2016; same methodologies and timing as closely as possible across years.

- Soil sampling and analysis
  - 22 soil samples per transect across depths 0–5 cm and 5–10 cm.
  - Analyzed for: pH, loss on ignition (LOI), exchangeable K, Mg, Ca, phosphate (PO4-P), and total nitrogen (N).
  - Detailed analytical methods provided for each soil property, including instrumentation and quality controls.

- 2016 relocation and georeferencing
  - Transects re-located in 2016 by geo-referencing Wells’ original maps (1:125 scale) with CEH data to align Celtic field boundaries.
  - Purpose: minimize pseudo-turnover due to mislocated transects; relocation accuracy ± ~2 m.
  - Data collected in 2016 at similar times of year and in the same locations as earlier surveys; used ESRI ArcGIS v10.4 for geospatial processing.

- Location, grid references, and data capture
  - Precise start/end coordinates and quadrat references provided for all transects (Table 4 references with grid IDs like SU0419…).
  - Quadrats numbered with a North/South convention (e.g., 51N, 48N, … 0, then 0S, 3S, …).

- Data structure and formats
  - Vegetation data: three CSV files (PD_SurveyData1970.csv, PD_SurveyData1990.csv, PD_SurveyData2016.csv).
    - Fields include: transect, quadrat/row description, quadrat number, vegetation height, recorder, species list.
  - Soil data: PD_SoilData.csv
    - Fields include: transect, position, depth (0–5 cm or 5–10 cm), LOI, pH, K, Ca, Mg, PO4-P, N.
  - Numbering and depth notes: for transect 3, 0–5 cm values reflect 0–10 cm due to sampling specifics in 1970 and 1990.

- Quality control and consistency
  - Surveys conducted by experienced botanists in pairs or threes with consistent methods across years.
  - One surveyor participated in multiple years to maintain methodological continuity.
  - Transects relocated carefully to maintain comparability; consistent timing within years.

- References and context
  - Foundational methodological context from Dahl & Hadac (1941), Fischer & Stöcklin (1997), Rodwell (1992), and Wells (1993).