# Supporting information for Grid-to-Grid model estimates of daily mean river flow for gauged catchments in Great Britain (1891 to 2015): observed driving data [MaRIUS-G2G-Oudin-daily]

## Overview
- MaRIUS project (2014–2017) developed a risk-based approach to drought and water scarcity.
- Provides Grid-to-Grid (G2G) model estimates of daily mean river flow for 260 NRFA gauged stations across Great Britain, covering 1891–2015.
- Grid and timing: flows are produced on a 1 km × 1 km GB grid with a 15-minute time-step; daily mean is recorded for 09:00 to 09:00 the next day.

## What the dataset contains
- Variable: River flow (m³ s⁻¹) at 260 NRFA gauge locations, as the daily mean from 09:00 to 09:00.
- File: G2G_Oudin_flow_1891_2015.csv (historical; 1891–2015) with a single header line; first column is date, followed by one column per catchment.
- Related file: MaRIUS_NRFAStationInfo.csv providing details for the 260 NRFA stations (station ID, river, location, G2G coordinates, catchment area, data issues).

## Grid-to-Grid (G2G) model details
- A national-scale hydrological model for Britain, run on a 1 km × 1 km grid with 15-minute time steps; incorporates soil type, land-cover, and urban effects on runoff.
- Calibrated with spatial datasets rather than catchment-specific parameter fitting; uses nationally applicable values for parameters where needed.
- Optional snow module not used here; precipitation input is assumed to be rain (no explicit snow routing).
- Simulates natural flows (1891–2015) at 260 sites; spin-up period not included in these outputs.
- Performance: generally good for catchments with natural flow regimes and accurate gauge records; less accurate where artificial abstractions/discharges dominate or where sub-surface hydrology is complex.

## Meteorological inputs and data preparation
- Driving data are observation-based:
  - Rainfall: CEH-GEAR 1 km × 1 km daily rainfall grids (Keller et al. 2015; Tanguy et al. 2016).
  - Potential evapotranspiration (PE): monthly estimates on a 5 km × 5 km grid, derived from temperature (Oudin et al. 2005); corrected to long-term means to align with MORECS (Rudd et al. 2007).
- Early 20th-century rainfall data: sparse in CEH-GEAR; missing values are spatially infilled (Rudd et al. 2017).
- PE for pre-1960 period uses temperature-based estimates; distributed to the 1 km grid and downscaled to 15-minute model steps alongside rainfall.
- PE values are copied to all 1 km cells within the corresponding G2G model grid for each time step.

## Use of the dataset
- Purpose: Compare G2G natural-flow estimates to observed river flows from NRFA for evaluation and drought analyses.
- Best for catchments with natural flow regimes and accurate observed records; less reliable where human abstractions or discharges significantly influence flows.
- The 1 km G2G cell chosen for each NRFA station is the closest in location and catchment area; checks ensure the correct tributary is represented. There may be small mismatches in catchment area size (G2G areas are within 8% of NRFA catchments).

## Format and accessibility
- Data format: CSV with a single header line.
- G2G_Oudin_flow_1891_2015.csv: columns are Date, then one column per catchment (1891–2015).
- Dates follow the Gregorian calendar (365 or 366 days); times recorded as calendar dates with 09:00–09:00 daily means.

## Limitations and caveats
- Model spin-up not included; long-term transient effects may be affected at the start of the series.
- Snow effects not modelled (no snow module used); precipitation input treated as rain.
- Calibration is field-wide rather than catchment-specific, which may affect performance in complex or highly managed basins.
- G2G catchment areas are approximations of NRFA catchments; differences up to 8% may occur, especially for small catchments.

## Acknowledgements and references
- Funded by the UK Natural Environment Research Council (NE/L010208/1) as part of the MaRIUS project.
- Acknowledgements to contributors (Nuria Bachiller-Jareno, Matt Fry, Maliko Tanguy) for support in data availability.
- Key references include Bell et al. (2007, 2009, 2016), Rudd et al. (2017), Kay et al. (2018), Keller et al. (2015), Oudin et al. (2005), Perry & Hollis (2005), Monteith (1965), Hough & Jones (1997).