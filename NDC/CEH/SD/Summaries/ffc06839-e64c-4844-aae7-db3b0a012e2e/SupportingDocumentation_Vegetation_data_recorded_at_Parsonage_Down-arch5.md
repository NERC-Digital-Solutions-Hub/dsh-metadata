# Long-term change in calcareous grassland vegetation and drivers over three time periods between 1970 and 2016

## Overview
- Dataset from Parsonage Down National Nature Reserve (NNR), Wiltshire, covering vegetation and soil measurements across 1970, 1990, and 2016.
- Aims to support understanding of long-term vegetation change in calcareous grassland, with methods consistent with the associated study (In prep).
- Focused on a CG2 Festuca ovina - Avenula pratensis grassland; vegetation recorded with Domin scale and sward height, plus detailed soil properties.

## Study area
- Parsonage Down NNR, 188 ha of chalk grassland; designated as NNR in 1973.
- Long tenure of grazing (cattle and sheep) with no fertiliser usage; management timings and stocking levels varied over time.

## Survey method
- Four transects established in 1970; transects differ in length to include Celtic field boundaries.
- Vegetation sampling: 20 cm x 20 cm quadrats placed every 3 ft along each transect; total of 115 quadrats per year.
- Recording: vascular plants and bryophytes identified to species (Taraxacum microspecies excluded); vegetation height measured in cm; Domin scale used for cover-abundance.
- Data collected in 1970, 1990, and 2016 by experienced botanists, typically in pairs.
- Soil sampling: 22 samples per transect (four transects) at depths 0–5 cm and 5–10 cm; samples processed and analyzed for pH, LOI, exchangeable K, Mg, Ca, Olsen PO4-P, and total N using specified methods.

## Data collection and processing
- In 2016, transects re-located by geo-referencing Wells’ 1970 survey maps against CEH historic maps to Celtic field boundaries; this ensured accurate temporal comparisons and reduced pseudo-turnover due to misplacement.
- Data collected at the same locations and similar time of year as the original survey.
- Soil and vegetation data captured in three CSV files: PD_SurveyData1970.csv, PD_SurveyData1990.csv, PD_SurveyData2016.csv; soil data in PD_SoilData.csv.

## Data structure
- Vegetation data structure:
  - Transect number (1–4)
  - Quadrat number with N/S designation (115 per year)
  - Vegetation height (cm)
  - Recorder initials (LR, PH, RW, TW, JW, RC)
  - Species list (vascular plants and bryophytes; Taraxacum microspecies excluded)
- Soil data structure:
  - Transect
  - Position (feet along transect; N/S)
  - Sample Depth (0–5 cm or 5–10 cm)
  - LOI, pH, K, Ca, Mg, PO4-P, N
  - Note: For transect 3 in 1970 and 1990, only one soil sample per position; 0–5 cm value reflects 0–10 cm depth.

## Quality control and provenance
- Measurements conducted with consistent methods across years; one surveyor contributed to both 1970 and 2016 surveys to maintain continuity.
- Relocation accuracy in 2016 achieved to ±2 m using ArcGIS v10.4 and archaeological GIS layers; careful re-location to ensure valid temporal comparisons and to avoid erroneous turnover observations.

## Accessibility, usage, and limitations
- Data are organized in clearly defined CSV files with documented fields and recording conventions; suitable for comparative analyses of long-term vegetation change and soil chemistry.
- Notable limitation: 0–5 cm soil data for transect 3 in 1970 and 1990 reflect sampling at 0–10 cm depth due to sampling design, which should be considered in analyses.

## References
- Dahl, E., & Hadac, E. (1941). Strandgesellschaften der Insel Ostøy im Oslofjord.
- Fischer, M., & Stöcklin, J. (1997). Local extinctions of plants in remnants of extensively used calcareous grasslands 1950–1985.
- Rodwell, J. S. (1992). British Plant Communities Volume 3.
- Wells, T. C. E. (1993). Effects of excess nitrogen on calcareous grasslands.