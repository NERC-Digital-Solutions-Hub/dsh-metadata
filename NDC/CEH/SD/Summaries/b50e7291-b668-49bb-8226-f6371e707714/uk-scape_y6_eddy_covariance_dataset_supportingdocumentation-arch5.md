# Meteorology, soil physics, and eddy covariance measurements of carbon dioxide, energy, and water exchange from a distributed network of sites across England and Wales, 2023 to 2024

## Overview
- Time series dataset of land surface–atmosphere exchanges of sensible heat (H) and latent heat (LE) plus supporting meteorological and soil physics data.
- Collected at six eddy covariance (EC) flux tower sites across England and Wales.
- Accompanied by site metadata and data dictionary files to enable discovery, interpretation, and reuse.
- Data are prepared for sharing with quality-controlled processing, gap-filling, and flux partitioning.

## Study sites
- Six flux monitoring sites with diverse land uses: three croplands (two on peat, one on mineral soils), one peatland grassland, one lowland fen under conservation management, and a relatively intact upland raised bog.
- Elevational range from 2 m below sea level to 565 m above sea level.
- Site metadata include land use, soil type, climate metrics (MAT, MAP), geographic coordinates, measurement heights, instrumentation, and crop year information (Table 1 in UK-SCAPE_Y6_Site_Metadata.csv).

## Sampling regime
- Automated flux, meteorological, and soil physics measurements provided for periods defined by START_DATE and END_DATE in the site metadata file.
- Data captured as time series with high-frequency measurements and summarized to thirty-minute means for flux calculations.

## Flux data acquisition
- Turbulent fluxes of sensible heat (H) and latent heat (LE) measured above canopy using open-path EC systems.
- Instruments: sonic anemometer, LI-7500 IRGA for CO2 and H2O density.
- Sampling rate: 20 Hz; data logged to a CR3000 Micrologger and telemetered to a secure server.
- Measurement heights (Zm) varied by site; standard heights at most sites, with cropping-adjusted height for maize.
- Sensor separations between sonic anemometer and IRGA specified for accurate flux calculations.
- Wind speed and direction derived at EC measurement height.

## Ancillary data acquisition
- Meteorological and soil observations include: air temperature (TA), relative humidity (RH), barometric pressure (PA), net radiation (NETRAD) with components (SW_IN, SW_OUT, LW_IN, LW_OUT), soil heat flux (G), soil moisture and temperature (SWC, TS), precipitation (P), and water table depth at peat sites.
- Vegetation measurements include canopy height, leaf area index (LAI), and biomass; biomass samples analyzed for carbon allocation.
- Data scanned at 0.1 Hz and aggregated to 30-minute means; vegetation data provided as non-continuous time series when available.

## Data processing
- Flux calculations performed with EddyPro software (v7.0.6), producing 30-minute flux averages.
- Processing includes QC of 20 Hz data, coordinate rotation, tilt correction, spectral corrections, density corrections, and footprint-aware verification.
- EddyPro also provides computed wind speed and direction at the EC height.

## Quality control
- Hardware calibration and repairs as needed; calibrations via in-house facilities or manufacturers.
- QC involves outlier removal (median absolute deviation), stationarity and turbulence tests, and friction velocity thresholds.
- Flux representativeness assessed with the footprint model; fluxes considered representative if >80% originate within the target ecosystem.
- All data visually inspected; clearly erroneous values removed manually.
- Missing records indicated by -9999; TIMESTAMP_START/END may appear in scientific notation in some software.

## Data gap-filling and flux partitioning
- Gaps in EC and many ancillary variables filled using the Marginal Distribution Sampling approach.
- Net ecosystem exchange (NEE) partitioned into gross primary production (GPP) and Reco using established night- and day-time methods.
- Gap-filling and partitioning conducted with REddyProc in R; ancillary data gap-filled where possible using COSMOS-UK sites for cross-site support.

## Details of data structure
- Time series data stored as separate CSV files for each of the six sites.
- Each file follows the structure described in UK-SCAPE_Data_Dictionary.csv; missing records denoted by -9999.
- TIMESTAMP_START and TIMESTAMP_END may appear in scientific notation in some software.
- Vegetation data available as non-continuous CSV files with variables described in the data dictionary.

## Nature and units of recorded values
- Variable definitions and units provided in UK-SCAPE_Data_Dictionary.csv; the dictionary should be consulted for precise units and descriptions.

## Acknowledgments
- Gratitude to landowners and partner organizations (Natural Resources Wales, RSPB, Natural England, Great Fen Project, G's Cambs. Growers Ltd., T. C Darby & Sons Ltd.).
- Data collection funded by the NERC UK-SCAPE programme (NE/R016429/1); donor funded the Grange Farm flux tower capital cost.

## References
- Detailed methodological and dataset-specific references supporting QC, footprint analysis, gap-filling, and flux partitioning methods (e.g., Reichstein et al., Mauder et al., Moncrieff et al., Kljun et al., Papale et al., etc.).