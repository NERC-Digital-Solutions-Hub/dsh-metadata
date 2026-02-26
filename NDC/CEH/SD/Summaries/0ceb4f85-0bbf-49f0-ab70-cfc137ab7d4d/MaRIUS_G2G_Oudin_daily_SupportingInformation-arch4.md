# Supporting information for Grid-to-Grid model estimates of daily mean river flow for gauged catchments in Great Britain (1891 to 2015): observed driving data [MaRIUS-G2G-Oudin-daily]

## Overview
- MaRIUS project (Managing the Risks, Impacts and Uncertainties of drought and water Scarcity), UK NERC-funded (2014–2017).
- Provides Grid-to-Grid (G2G) model estimates of daily mean river flow for gauged catchments in Great Britain from 1891 to 2015.
- Primary variable: river flow (m3 s-1), daily mean from 09:00 to 09:00 the following day, at locations corresponding to 260 NRFA gauging stations.

## Data lineage and model
- Hydrological model: Grid-to-Grid (G2G), national-scale, 1 km x 1 km grid, 15-minute time-step; parameterised by digital datasets (soil, land cover, topography).
- Accounts for urban/suburban land-cover effects on run-off; does not include abstractions or discharges.
- G2G uses input time-series of precipitation and potential evaporation (PE); snow module not used here.
- Model performance: good for natural-flow regimes; less accurate where artificial withdrawals/discharges or complex subsurface hydrology are important.
- Calibration: generally uses spatial datasets rather than catchment-specific parameter calibration.

## Data content and scope
- Outputs: natural (unregulated) daily river flows for 1891–2015 at 260 sites.
- Station mapping: NRFA gauging station is paired with the nearest 1 km G2G grid cell representing the corresponding catchment; checks ensure correct river/tributary alignment. Some small catchments may have catchment-area differences; all G2G catchment areas are within 8% of NRFA catchment areas.
- Related file: MaRIUS_NRFAStationInfo.csv with NRFA station details (ID, river, location, G2G coordinates, catchment area, data issues).

## Data inputs in detail
- Precipitation: 1 km x 1 km CEH-GEAR daily rainfall (Keller et al. 2015; Tanguy et al. 2016); sparse early-20th-century rainfall data were spatially infilled (Rudd et al. 2017).
- Potential Evaporation (PE): monthly PE derived from gridded temperature data (5 km x 5 km) using a temperature-based method (Oudin et al. 2005); long-term means adjusted with spatial correction factors to fit MORECS values (Rudd et al. 2007); used to generate PE back to 1891.
- Spatial inputs: topography and soil data as in Bell et al. (2009).
- Rainfall and PE are distributed to the 15-minute G2G time-step; the snow module is not employed.

## Data format and access
- File: G2G_Oudin_flow_1891_2015.csv
  - CSV with a single header row.
  - First column: date; subsequent columns: one per catchment.
  - Time convention: daily mean from 09:00 to 09:00 the following day.
  - Coverage: 1891–2015.
- Related: MaRIUS_NRFAStationInfo.csv with station metadata and data issues.
- Documentation notes how to identify the most appropriate G2G cell for each NRFA station.

## Use cases and interpretation
- Intended use: compare G2G natural flows with observed NRFA flows for validation, drought analysis, and historical hydrology studies.
- Suitability: best for catchments with little anthropogenic influence and reliable observed data; less suitable for heavily regulated systems or complex sub-surface hydrology.
- Cautions: small catchments may suffer from discretisation errors; G2G outputs are not calibrated per catchment.

## Data quality, limitations, and caveats
- Not calibrated to individual catchments; uses national parameter values.
- Possible misattribution in small catchments due to grid resolution; catchment areas are within 8% of NRFA areas.
- No account of human withdrawals or discharges; focused on natural flow estimations.
- PE estimation relies on temperature-based method with uncertainties, especially for pre-1960 data.

## Governance, provenance, and acknowledgments
- Funded by the UK Natural Environment Research Council (NE/L010208/1) as part of the UK Drought and Water Scarcity programme.
- Acknowledgements to contributors for data provision and assistance.
- Data accessibility via NERC Environmental Information Data Centre.

## References (selected)
- Bell et al. (2007, 2009, 2016) on high-resolution grid-based river flow models and hydrological data use.
- Keller et al. (2015), Tanguy et al. (2016) on CEH-GEAR rainfall estimates.
- Oudin et al. (2005) and Perry & Hollis (2005) on PE estimation and gridded climate data.
- Rudd et al. (2017), Kay et al. (2018) on drought analyses and validation.