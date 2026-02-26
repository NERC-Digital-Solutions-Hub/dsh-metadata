# Long-term change in calcareous grassland vegetation and drivers over three time periods between 1970 and 2016

- Purpose: Data from a long-term study of vegetation change at Parsonage Down National Nature Reserve (NNR) from 1970, 1990, and 2016, intended for GIS-based analysis of spatial and temporal vegetation and soil drivers.

- Study area
  - Parsonage Down NNR, Wiltshire (188 ha of chalk grassland).
  - Designated NNR in 1973; grazing with sheep and cattle; no fertiliser usage (timings and numbers varied by period).

- Survey methods
  - Four transects established in 1970; varying lengths (111 ft, 102 ft, 60 ft, 60 ft) to span Celtic field boundaries.
  - Vegetation: vascular plants recorded to species level (except Taraxacum microspecies) in 20 cm x 20 cm quadrats every 3 ft along each transect.
  - Measurements: sward height (cm); Domin scale for cover-abundance (10 categories) used for species in each quadrat.
  - Sampling schedule: surveys conducted in 1970, 1990, and 2016.
  - Data delivered in three vegetation CSVs: PD_SurveyData1970.csv, PD_SurveyData1990.csv, PD_SurveyData2016.csv.

- Soil sampling and analysis
  - 22 soil samples collected along each transect at two depths: 0–5 cm and 5–10 cm (corer 3.5 cm diameter).
  - Analyzed for: pH, loss on ignition (LOI), exchangeable K, Mg, Ca, phosphate (PO4-P), total nitrogen (N).
  - Method details provided for each parameter; notes on 0–5 cm vs 0–10 cm depth for transect 3.
  - Soil data delivered in PD_SoilData.csv.

- Locating transects and plots (2016 re-survey)
  - Transects re-located by geo-referencing Wells’ 1970 map with a 1:125 scale map and archaeological GIS layers; coordinates aligned to Celtic field boundaries.
  - Avoided pseudo-turnover by ensuring precise relocation (±2 m) using ESRI ArcGIS v10.4.
  - Grid references and quadrat positions recorded for 1970, 1990, and 2016 (Table 4 style coordinates).

- Quality control
  - Surveys conducted by experienced botanists in pairs (or threes); consistency in methods and equipment.
  - One surveyor involved across both 1970 and 2016 surveys to aid comparability.
  - Transects relocated as accurately as possible in 2016 to maintain spatial comparability.

- Data structure and files
  - Vegetation data: three CSV files (PD_SurveyData1970.csv, PD_SurveyData1990.csv, PD_SurveyData2016.csv).
  - Soil data: PD_SoilData.csv.
  - Vegetation data structure: fields include Transect number (1–4), Quadrat number (N/S), vegetation height (cm), Recorder (LR, PH, RW, TW, JW, RC), and species list for each quadrat.
  - Soil data structure: fields include Transect (1–4), Position (feet and N/S), Sample Depth (0–5 cm or 5–10 cm), LOI (%), pH, K (mg/kg), Ca (mg/kg), Mg (mg/kg), PO4-P (mg/kg), N (%).

- Data provenance and references
  - Original methods reference Dahl & Hadac (1941), Fischer & Stöcklin (1997), Rodwell (1992), Wells (1993).
  - 2016 re-survey alignment emphasized accurate relocation to maintain validity of temporal comparisons.

- GIS considerations for use
  - Temporal alignment across 1970, 1990, and 2016 requires careful handling of transect positions and quadrat geometries.
  - Ensure consistent coordinate reference system and scale when integrating vegetation and soil layers.
  - Be mindful of depth-specific soil measurements (0–5 cm vs 0–10 cm) for transect 3 during analyses.
  - Use geo-referenced transect data and exact grid references to minimize spatial misalignment and misinterpretation of species turnover.