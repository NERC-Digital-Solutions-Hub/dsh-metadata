# Growing-season eddy covariance measurements of carbon dioxide, energy and water fluxes from a bioenergy maize crop, Yorkshire, UK, 2021

## Overview
- Description of a 2021 dataset of 30-minute observations of land-atmosphere exchange: net ecosystem CO2 exchange (NEE) and sensible (H) and latent heat (LE) fluxes over a bioenergy maize crop.
- Measurements span the growing season from 02/06/2021 to 10/10/2021.
- Includes weather and soil physics measurements to support interpretation of flux data.

## Study site
- Location: University of Leeds Research Farm, 53°51'56.26"N, 1°19'28.22"W.
- Agricultural context: field under continuous arable rotation since 1970; rainfed system.
- Climate: temperate oceanic with long-term mean temperature ~9.5 ± 1 °C and annual rainfall ~885 ± 231 mm.
- Soil: well-drained loamy calcareous brown earth, pH 6.9, bulk density ~1.3 g cm^-3; 0–30 cm soil carbon ~39.5 g kg^-1 and nitrogen ~2.3 g kg^-1.
- Crop management: maize planted 02/06/2021 at 110,000 seeds ha^-1; harvested 10/10/2021; one inorganic N fertilizer application at planting (22.5 kg N ha^-1).

## Data collected (fluxes and ancillary measurements)
- Primary fluxes: NEE, H, LE (30-minute means; 10 Hz data input).
- Ancillary meteorological and soil measurements: air temperature, relative humidity, soil temperature at 5 cm, soil moisture, net radiation (Rnet), short-wave and long-wave radiation components, wind measurements, barometric pressure.
- Turbulent measurements: micrometeorological eddy covariance setup with a closed-path CO2/H2O analyzer and a 3D sonic anemometer mounted on a tall mast.

## Flux instrumentation and fieldwork
- Eddy covariance system: LI-7200RS CO2/H2O analyzer and Gill Windmaster sonic anemometer; data logged with a CR1000X; sensor height adjusted to keep ≥2 m canopy separation.
- Data sampling: 10 Hz; results averaged to 30-minute intervals.
- Field period: 02/06/2021–10/10/2021.

## Data processing
- Primary processing: EddyPro 7 to compute 30-minute fluxes for NEE, H, LE with standard processing steps.
- Corrections applied: angle-of-attack for anemometer, time-lag adjustments, high-/low-frequency co-spectral attenuation corrections.
- Uncertainty: random uncertainty estimates following established methods.

## Quality control
- Software: R (v4.1.3) used for quality control.
- Criteria for data exclusion: statistical outliers, LI-COR signal deviation > baseline by >10%, nonrepresentative footprint (>20% data outside site boundaries), unrealistic flux values (e.g., H outside 200–450 W m^-2, LE outside -50 to 400 W m^-2, NEE outside -60 to 30 μmol m^-2 s^-1), friction velocity u* < 0.14 m s^-1.

## Gap-filling and flux partitioning
- Method: REddyProc package in R for gap-filling and partitioning NEE into assimilation and respiration components.
- Gap-filling approach: marginal distribution sampling.
- Uncertainty for filled periods: standard deviation of the observations used to fill gaps.

## Data structure and file details
- Core dataset: Yorkshire_Bioenergy_Maize_GS_2021.csv.
- Key variables (examples): Date, Time, NEE (and NEE_unc), LE (and LE_unc), H (and H_unc), Tau (and Tau_unc), CO2_strg, LE_strg, H_strg, Pa, Tair, RH, VPD, SWin, SWout, LWin, LWout, Rnet, PAR, G, Tsoil, VWC, windspeed, winddir, Ustar, TKE, Tstar, L, (z-d)/L, NEE_f, NEE_f_sd, Reco, GPP.
- Data columns include preprocessing-ready fields (gap-filled NEE, uncertainty, respiration, and gross primary productivity).

## Acknowledgements and references
- Funding: Leeds-York-Hull NERC Doctoral Training Partnership (DTP Panorama) grant NE/S007458/1.
- Acknowledgement of field facility and collaborators.
- References cover standard eddy covariance processing methods, gap-filling, foot-print modeling, and instrumentation.

## Potential analytical uses
- Analyze correlations between NEE, H, LE and meteorological/soil variables across the maize growing season.
- Develop or validate predictive models of CO2 exchange and energy fluxes for bioenergy crops.
- Compare gap-filled flux estimates (GPP, Reco) with independent ecosystem carbon balance indicators.
- Investigate seasonal dynamics of carbon and energy exchange in rainfed maize systems under temperate climates.