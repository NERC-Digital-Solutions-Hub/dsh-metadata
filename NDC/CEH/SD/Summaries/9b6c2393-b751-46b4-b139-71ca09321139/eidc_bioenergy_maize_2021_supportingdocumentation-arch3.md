# Growing-season eddy covariance measurements of carbon dioxide, energy and water fluxes from a bioenergy maize crop, Yorkshire, UK, 2021

## Overview
- 30-minute observations of net ecosystem CO2 exchange (NEE) and sensible (H) and latent heat (LE) fluxes measured over the growing season of bioenergy maize in Yorkshire, UK.
- Eddy covariance (EC) micrometeorological method used to capture land-atmosphere exchanges between 02/06/2021 and 10/10/2021.
- Dataset also includes accompanying weather and soil physics measurements.

## Study site
- Field located at the University of Leeds Research Farm (coordinates provided).
- Continuous arable rotation since 1970; temperate oceanic climate.
- Soil: well-drained loamy calcareous brown earth, pH 6.9, bulk density 1.3 g cm-3; soil carbon ~39.5 g kg-1 and nitrogen ~2.3 g kg-1 at 0–30 cm.
- Rainfed system with a single inorganic N fertilizer application at planting (22.5 kg N ha-1).
- Maize planted on 02/06/2021 at 110,000 seeds ha-1; harvested on 10/10/2021.

## Collection methods and fieldwork instrumentation
- Flux measurements: closed-path EC system with sensors mounted on an extendable mast; minimum 2 m separation from canopy maintained by height adjustment.
- Instruments: LI-7200RS CO2/H2O analyzer; Gill Windmaster 3D sonic anemometer; data logged at 10 Hz and aggregated to 30-minute means.
- Ancillary measurements: net radiation (Rnet), short-wave and long-wave radiation components, air temperature (Tair), relative humidity (RH), soil temperature (Tsoil) and soil moisture (5 cm depth) using TEROS 11 probes; all as 30-minute means.

## Data processing
- Fluxes (H, LE, NEE) computed from raw EC data using EddyPro v7.0.6.
- Processing steps include data conditioning, angle-of-attack correction for the anemometer, time-lag cross-correlation, and corrections for high- and low-frequency co-spectral attenuation.
- Random uncertainty estimated following established methods (Finkelstein & Sims, 2001).

## Quality control
- Performed in R to ensure high-quality flux data.
- Data exclusion criteria include: statistical outliers; LI-COR signal >10% above baseline; nonrepresentative footprint (>20% data outside site boundaries); unrealistic flux thresholds (H: 200–450 W m-2; LE: -50 to 400 W m-2; NEE: -60 to 30 μmol m-2 s-1); friction velocity (u*) < 0.14 m s-1.

## Gap-filling
- Gap filling and NEE partitioning performed with REddyProc (R package) in R 4.1.3.
- Gaps filled via marginal distribution sampling; uncertainty of filled periods represented by the standard deviation of the data used for filling.

## Details of data structure
- Dataset file: Yorkshire_Bioenergy_Maize_GS_2021.csv.
- Variables include: Date, Time, NEE and uncertainty, LE and uncertainty, H and uncertainty, Tau and uncertainty, CO2 storage term, LE/H storage terms, atmospheric pressure, Tair, RH, VPD, radiation components (SWin, SWout, LWin, LWout, Rnet, PAR), G (soil heat flux), Tsoil, VWC, windspeed and winddir, Ustar, TKE, Tstar, L, (z-d)/L, NEE_f (gap-filled NEE), NEE_f_sd, Reco, GPP.
- Table 1 documents units and descriptions for all variables.

## Acknowledgements
- Funded by Leeds-York-Hull NERC DTP Panorama (grant NE/S007458/1).
- Acknowledges University of Leeds Research Farm and Rob Yardley for farm management information.

## Relevance for monitoring frameworks
- Provides a transparent, well-documented data lineage from instrument setup through processing to gap-filled flux estimates.
- Demonstrates rigorous QA/QC criteria, uncertainty estimation, and standardized data processing (EddyPro, REddyProc) suitable for integration into monitoring dashboards and policy evaluation datasets.
- Includes comprehensive metadata on site characteristics, instrumentation, processing steps, and data structure to support data governance, reproducibility, and future decision-making.