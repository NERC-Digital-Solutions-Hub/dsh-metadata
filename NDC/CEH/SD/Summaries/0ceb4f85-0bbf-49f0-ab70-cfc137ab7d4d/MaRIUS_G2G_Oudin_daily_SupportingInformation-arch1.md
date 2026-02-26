# Supporting information for Grid-to-Grid model estimates of daily mean river flow for gauged catchments in Great Britain (1891 to 2015): observed driving data [MaRIUS-G2G-Oudin-daily]

## Purpose and context
- Provides observed driving data and model output to support Grid-to-Grid (G2G) estimates of daily mean river flow for gauged catchments in Great Britain (1891–2015).  
- Part of the MaRIUS project (Managing the Risks, Impacts and Uncertainties of drought and water Scarcity), a UK NERC-funded research program (2014–2017).

## What the dataset contains
- Daily mean river flow (m³ s⁻¹) from the G2G model at 1 km grid cells corresponding to 260 NRFA gauging stations, recorded as 09:00 to 09:00 the following day.  
- Each column after the date corresponds to a catchment’s G2G flow; a related file lists the 260 NRFA gauging stations.

## Model and driving data
- Model: Grid-to-Grid (G2G), national-scale hydrological model on a 1 km grid with a 15-minute time-step; parameterised using soils, land-cover, topography, and other spatial datasets. Urban/suburban land-cover effects are included; the model emphasizes natural flow and does not simulate abstractions or discharges directly. Calibration is not performed for individual catchments; national, spatial data drive parameters like kinematic wave speeds. The optional snow module is not used here.
- Forcing data:
  - Daily rainfall at 1 km resolution (CEH-GEAR).
  - Monthly potential evapotranspiration (PE) estimated from temperature on a 5 km grid (Oudin et al. 2005).
- Handling of missing rainfall: sparsely measured periods in the early 20th century are spatially infilled (Keller et al. 2015; Rudd et al. 2017).
- PE estimation: a temperature-based method (Oudin et al. 2005) with long-term mean correction factors to align with MORECS values.
- Spin-up: model spin-up is not included in these files.

## How the driving data are matched to observations
- The G2G flows are assigned to the NRFA gauging stations by selecting the 1 km grid cell that best represents each station, considering location and catchment area; checks ensure the correct river tributary is used. Some discrepancies between derived G2G catchment areas and NRFA catchment areas can occur, particularly for small catchments, but all G2G catchment areas are within 8% of NRFA catchment areas.

## Format and access
- Data format: CSV file with a single header line. First column is date; subsequent columns are the 260 catchments. File name: G2G_Oudin_flow_1891_2015.csv (1891–2015). Flows are daily means from 09:00 to 09:00 the next day.
- Related station information: MaRIUS_NRFAStationInfo.csv provides station IDs, river names, locations, G2G coordinates, catchment areas, and data issues.

## How to use the dataset
- Use G2G natural-flow estimates (1891–2015) to compare with observed NRFA river flows.
- Model performance: generally reasonable, especially for catchments with natural flow regimes and reliable observed records; performance declines where abstractions/discharges dominate or where sub-surface hydrology is complex.
- Limitations to consider:
  - G2G is most reliable for natural flow regimes; where human interference is strong, discrepancies may be larger.
  - The 1 km grid cell may not perfectly match the NRFA catchment boundary, particularly for small catchments.
  - The dataset represents natural flows and does not include deliberate water management interventions.

## Data quality, limitations, and caveats
- Catchment-area differences between NRFA and G2G can introduce up to ~8% discrepancy in individual catchments.
- Artificial water use (abstraction/discharge) is not embedded in the G2G simulations.
- Early 20th-century rainfall data require infilling in sparse periods; PE estimates rely on a temperature-based method with historical adjustments.
- Spin-up not included; simulation starts from model initialization rather than a long spin-up period.

## Acknowledgements and references
- Funded by the UK Natural Environment Research Council (MaRIUS project; NE/L010208/1) as part of the UK Drought and Water Scarcity programme.
- Acknowledges contributions from researchers including Nuria Bachiller-Jareno, Matt Fry, and Maliko Tanguy.
- Key references include foundational MaRIUS and G2G methodology papers and data sources for CEH-GEAR, MORECS, and Oudin PE formulations (listed in the document).