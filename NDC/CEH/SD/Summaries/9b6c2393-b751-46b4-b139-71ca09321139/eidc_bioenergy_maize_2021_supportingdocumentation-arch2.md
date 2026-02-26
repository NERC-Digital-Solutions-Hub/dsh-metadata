# Growing-season eddy covariance measurements of carbon dioxide, energy and water fluxes from a bioenergy maize crop, Yorkshire, UK, 2021

## Overview
- 30-minute observations of land-atmosphere exchange: Net Ecosystem CO2 Exchange (NEE), sensible heat (H), and latent heat (LE) during the maize growing season.
- Data collection period: 02/06/2021 to 10/10/2021.
- Measurements include eddy covariance fluxes and supporting weather and soil physics data.

## Study site
- Location: University of Leeds Research Farm, 53°51'56.26"N 1°19'28.22"W.
- Environment: Continuous arable rotation since 1970; temperate oceanic climate; rainfed system.
- Soil: Well-drained loamy calcareous brown earth; pH 6.9; bulk density 1.3 g cm^-3; 0–30 cm soil carbon 39.5 g kg^-1; nitrogen 2.3 g kg^-1.
- Crop management: Bioenergy maize planted 02/06/2021 at 110,000 seeds ha^-1; harvested 10/10/2021; single inorganic fertilizer application at planting (22.5 kg N ha^-1).

## Data collection and field instrumentation
- Flux measurements: Closed-path eddy covariance system with sensors on a raiseable mast; LI-7200RS CO2/H2O analyser; Gill Windmaster 3D sonic anemometer; data at 10 Hz, averaged to 30-minute intervals.
- Ancillary measurements: Net radiation, shortwave/longwave radiation (incoming and outgoing), air temperature, relative humidity, soil temperature and moisture at 5 cm depth (TEROS 11 probes).
- Data logging: All ancillary and flux data stored as 30-minute means.

## Data processing
- Software: EddyPro 7 for processing raw flux data.
- Processing steps: Data conditioning, angle-of-attack correction for sonic anemometers, lag compensation, high/low-frequency co-spectral attenuation corrections; random uncertainty estimation per standard references.

## Quality control
- Tool: R (v4.1.3) for quality control to ensure high-quality flux data.
- QC criteria for data removal: statistical outliers; LI-COR signal anomalies (>10% higher than baseline); nonrepresentative footprints (>20% outside site boundaries); unrealistic flux thresholds (H, LE, NEE); friction velocity (u*) < 0.14 m s^-1.

## Gap-filling and flux partitioning
- Gap-filling: REddyProc (R, v4.1.3) using marginal distribution sampling; uncertainty from the standard deviation of data used to fill gaps.
- Flux partitioning: Separation of NEE into Gross Primary Productivity (GPP) and ecosystem respiration (Reco); includes reported NEE_f and NEE_f_sd, along with Reco and GPP.

## Data structure
- Dataset file: Yorkshire_Bioenergy_Maize_GS_2021.csv
- Variables (example): 
  - NEE, NEE_unc; LE, LE_unc; H, H_unc; Tau, Tau_unc; CO2_strg; LE_strg; H_strg; Pa; Tair; RH; VPD; SWin; SWout; LWin; LWout; Rnet; PAR; G; G, Tsoil; VWC; windspeed; winddir; Ustar; TKE; Tstar; L; (z-d)/L; NEE_f; NEE_f_sd; Reco; GPP.
- Each variable has both measured (suffixes or pre-gap-filled values) and gap-filled representations where applicable.

## Acknowledgements
- Funded by the Leeds-York-Hull Natural Environmental Research Council (NERC) Doctoral Training Partnership (DTP) Panorama (grant NE/S007458/1).
- Acknowledges the University of Leeds Research Farm and Rob Yardley for farm management information.

## References (selected tools and sources)
- Instrumentation and processing references (e.g., LI-COR LI-7200RS, EddyPro, REddyProc, footprint methods, quality metrics, and standard atmospheric and soil measurement technologies).