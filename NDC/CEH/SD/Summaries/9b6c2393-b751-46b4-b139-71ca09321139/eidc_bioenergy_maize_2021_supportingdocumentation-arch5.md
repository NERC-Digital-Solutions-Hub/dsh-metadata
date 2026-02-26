# Growing-season eddy covariance measurements of carbon dioxide, energy and water fluxes from a bioenergy maize crop, Yorkshire, UK, 2021

## Overview
- 30-minute observations of land-atmosphere exchange: net ecosystem CO2 exchange (NEE), sensible heat (H), and latent heat (LE) during the maize crop growing season.
- Measurements taken using eddy covariance (EC) micrometeorology from 02/06/2021 to 10/10/2021.
- Additional weather and soil physics measurements included.

## Study site
- Location: University of Leeds Research Farm (53°51'56.26"N, 1°19'28.22"W).
- Context: field in continuous arable rotation since 1970; temperate oceanic climate.
- Soils: loamy, calcareous brown earth, pH 6.9; bulk density 1.3 g cm-3; 0–30 cm soil carbon 39.5 g kg-1; nitrogen 2.3 g kg-1.
- Management: rainfed; maize planted 02/06/2021 at 110,000 seeds ha-1; harvested 10/10/2021; one inorganic N fertiliser application (22.5 kg N ha-1).

## Collection methods and fieldwork instrumentation

### Flux instrumentation
- Eddy covariance and micrometeorological measurements above the maize canopy using a closed-path EC system.
- Sensors on an extendable mast; height adjusted to maintain at least 2 m clearance from canopy.
- CO2/H2O: LI-7200RS gas analyser; wind: Gill Windmaster 3D sonic anemometer.
- Data sampling: 10 Hz; processed to 30-minute means; data logged with a CR1000X datalogger.

### Ancillary measurements
- Energy fluxes: net radiation, short-wave and long-wave radiation components measured with SN-500 net radiometer.
- Air/soil conditions: air temperature and relative humidity (HMP155); soil temperature and moisture (TEROS 11) at 5 cm depth.
- All ancillary data stored as 30-minute means.

## Data processing
- Flux calculation: 30-minute fluxes of NEE, LE, and H computed with EddyPro 7 (v7.0.6).
- Processing steps: data conditioning; angle-of-attack correction for Gill anemometers; lag correction for high-frequency data; correction for co-spectral attenuation (low/high-frequency); random uncertainty estimated per Finkelstein & Sims.
- Software/tools: EddyPro for processing; REddyProc (R) for gap filling and flux partitioning.

## Quality control
- Environment: R (v4.1.3) used for QC.
- QC criteria for data exclusion: statistical outliers; LI-COR signal strength > baseline by >10%; non-representative data by footprint model (>20% outside site boundaries); physically unrealistic flux values (H: 200–450 W m-2; LE: -50 to 400 W m-2; NEE: -60 to 30 μmol m-2 s-1); friction velocity (u*) < 0.14 m s-1.

## Gap-filling
- Method: REddyProc in R.
- Approach: marginal distribution sampling to fill missing periods.
- Uncertainty: reported as the standard deviation of observations used to fill gaps.

## Details of data structure
- File: Yorkshire_Bioenergy_Maize_GS_2021.csv
- Variables (examples): Date (dd/mm/yyyy, GMT), Time (HH:MM:SS, GMT), NEE and NEE_unc, LE and LE_unc, H and H_unc, Tau and Tau_unc, CO2_strg, LE_strg, H_strg, Pa, Tair, RH, VPD, SWin, SWout, LWin, LWout, Rnet, PAR, G, GPP, Tsoil, Tsoil variants, VWC, windspeed, winddir, Ustar, TKE, Tstar, L, (z-d)/L, NEE_f and NEE_f_sd, Reco, etc.
- Purpose: Provides a comprehensive, time-aligned set of flux, meteorological, and soil variables at 30-minute resolution, including gap-filled fluxes and partitioning outcomes.

## Acknowledgements
- Funding: Leeds-York-Hull Natural Environmental Research Council (NERC) Doctoral Training Partnership (DTP) Panorama, grant NE/S007458/1.
- Acknowledgements: University of Leeds Research Farm; Rob Yardley for farm management information.

## References (selected tools and methodologies)
- Eddy covariance processing and quality assessment methods and software (EddyPro; Mauder et al.; Moncrieff et al.).
- Gap-filling and flux partitioning tools (REddyProc).
- Standard data processing and QC references (R, Papale et al.; Reichstein et al.; Ruppert et al.; Vickers & Mahrt; etc.).
- Instrumentation and sensor references (LI-COR LI-7200RS, Gill Windmaster, SN-500 net radiometer, HMP155, TEROS 11).