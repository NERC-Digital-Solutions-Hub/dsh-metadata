# Supporting information for Grid-to-Grid model estimates of daily mean river flow for gauged catchments in Great Britain (1891 to 2015): observed driving data [MaRIUS-G2G-Oudin-daily]

## Overview
- Provides Grid-to-Grid (G2G) model estimates of daily mean river flow (m3 s-1) for gauged catchments across Great Britain from 1891 to 2015.
- Target variable: daily mean river flow (09:00 to 09:00) at locations corresponding to 260 NRFA gauging stations.
- Purpose: enable comparison between G2G estimates and observed gauged river flows; support drought and water scarcity analyses.

## Dataset contents and scope
- 260 NRFA gauging stations with corresponding G2G grid boxes.
- Daily river flow estimates from G2G for 260 sites, 1891–2015; a companion file provides NRFA station details.
- Output format: CSV with a single header line; first column is date, subsequent columns are flows for each catchment.
- Related file: MaRIUS_NRFAStationInfo.csv containing station ID, river, location, G2G coordinates, catchment area, and data issues.

## Model, inputs, and driving data
- Hydrological model: Grid-to-Grid (G2G) running on a 1 km x 1 km grid with 15-minute time steps; parameterised from spatial data (soil, land cover, topography).
- Model characteristics:
  - Uses rainfall and potential evapotranspiration (PE) as inputs; no calibration to individual catchments.
  - Includes urban land-cover effects on runoff; designed for natural-flow regimes (limited anthropogenic influence).
  - Snow module not used; precipitation treated as rain.
  - Spin-up period not included in these files.
- Meteorological drives:
  - Daily rainfall on a 1 km x 1 km CEH-GEAR grid (Keller et al. 2015; Tanguy et al. 2016).
  - Monthly PE estimates derived from temperature data on a 5 km x 5 km grid (Oudin et al. 2005), with long-term corrections to align with MORECS values (Rudd et al. 2007).
  - Rainfall infilling for early 20th century periods with sparse measurements (Keller et al. 2015; Rudd et al. 2017).

## Data quality, limitations, and caveats
- Model performance: reasonably good for catchments with natural flow regimes and accurate observed flows; less accurate where artificial abstractions/discharges and complex sub-surface hydrology prevail.
- Catchment-area alignment:
  - Flows correspond to the 1 km x 1 km G2G cell that best represents each NRFA station, with additional checks to ensure correct river tributary attribution.
  - Some small catchments may have larger errors due to discretisation; all G2G catchment areas are within 8% of NRFA catchment areas.
- Input data caveats:
  - Early 20th-century rainfall data sparser and infilled spatially.
  - PE estimated via a temperature-based method (Oudin et al., 2005) with factors to fit long-term means to MORECS; not the original Monteith-based method for pre-1960 data.
  - Snow module not used; potential evapotranspiration derived from temperature data, with associated uncertainties.
- Temporal scope: strictly historical; no contemporary updates beyond 1891–2015 in this dataset.

## Format and access
- Main data file: G2G_Oudin_flow_1891_2015.csv
  - Structure: header line; first column = date; subsequent columns = daily mean flows for each catchment.
  - File naming indicates historical span: 1891–2015.
- Supporting file: MaRIUS_NRFAStationInfo.csv
  - Contains NRFA station details and mapping to G2G grid cells, including data issues.
- Source and hosting: NERC Environmental Information Data Centre; MaRIUS project outputs.

## Usage guidance for data stewardship
- Suitable uses:
  - Validation and benchmarking of G2G natural-flow simulations against observed NRFA data.
  - Drought and water-scarcity analyses using long historical records.
  - Spatially distributed hydrological assessments where calibrated site-specific information is limited.
- Cautions:
  - Be mindful of potential mismatches between NRFA catchment areas and the corresponding G2G grid cells, especially for small catchments.
  - Interpret results in light of absence of anthropogenic effects (abstractions/discharges) in G2G for these simulations.
  - Acknowledge uncertainties in early-period rainfall and PE estimates when using for trend or attribution analyses.
- Provenance and governance:
  - Data are part of the MaRIUS project; see acknowledgements and references for foundational methodologies.
  - Data are citable via the provided dataset and linked publications; include appropriate references when reuse.

## Acknowledgements and references
- Acknowledges MaRIUS project support from the UK Natural Environment Research Council (NE/L010208/1).
- Key references include foundational methodological papers on G2G (Bell et al. 2009, 2016; others) and CEH-GEAR rainfall products (Keller et al. 2015; Tanguy et al. 2016), among others.