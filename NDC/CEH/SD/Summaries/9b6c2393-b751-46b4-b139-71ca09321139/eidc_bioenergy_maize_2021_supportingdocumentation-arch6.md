# Growing-season eddy covariance measurements of carbon dioxide, energy and water fluxes from a bioenergy maize crop, Yorkshire, UK, 2021

## Overview of the dataset
- 30-minute observations of land-atmosphere exchanges: net ecosystem CO2 exchange (NEE) and sensible (H) and latent heat (LE) fluxes during the maize bioenergy crop growing season.
- Turbulent fluxes measured with eddy covariance (EC) between 02/06/2021 and 10/10/2021.
- Dataset also includes weather and soil physics measurements to contextualise fluxes.

## Study site
- Location: field at University of Leeds Research Farm (53°51'56.26"N 1°19'28.22"W).
- Climate: temperate oceanic; mean annual temperature ~9.5°C and precipitation ~885 mm (1992–2022).
- Soil: loamy, calcareous brown earth, pH ~6.9; bulk density ~1.3 g/cm3; soil carbon ~39.5 g/kg and nitrogen ~2.3 g/kg (0–30 cm).
- Agricultural context: rainfed cropping; maize planted 02/06/2021 at 110,000 seeds/ha, harvested 10/10/2021; one inorganic fertiliser application at planting (22.5 kg N/ha).
- Data collection period corresponds to the maize growing season.

## Collection methods and fieldwork instrumentation
- Eddy covariance measurements of CO2 fluxes and weather/soil measurements using a closed-path EC system mounted on an extendable mast; height adjusted to keep sensor >2 m above canopy.
- Instruments: LI-7200RS CO2/H2O gas analyser; Gill Windmaster 3D sonic anemometer; data logged as 30-minute means with 10 Hz sampling.
- Ancillary measurements include energy fluxes (Rnet, SWin, SWout, LWin, LWout), air temperature, relative humidity, soil temperature, and soil moisture (5 cm depth).

## Data processing
- Fluxes (H, LE, NEE) computed with EddyPro 7 software; processing includes data conditioning, angle of attack correction for the sonic anemometer, time-lag cross-correlation, and corrections for high/low-frequency co-spectral attenuation.
- Random uncertainty estimated following established methods.

## Quality control
- Performed in R to ensure high-quality data.
- Data removed for: statistical outliers, LI-COR signal anomalies (>10% above baseline), non-representative footprint (>20% data outside site boundaries), unrealistic flux thresholds (H: 200–450 W/m2; LE: −50 to 400 W/m2; NEE: −60 to 30 μmol CO2 m−2 s−1), and low friction velocity (u* < 0.14 m/s).

## Gap-filling
- Gaps in NEE and flux partitioning addressed with REddyProc (R package) using marginal distribution sampling.
- Uncertainty for gap-filled values represented by the standard deviation of the observations used to fill gaps.

## Details of data structure
- File: Yorkshire_Bioenergy_Maize_GS_2021.csv
- Structure includes:
  - Temporal fields: Date (dd/mm/yyyy, GMT), Time (HH:MM:SS, GMT)
  - Fluxes and uncertainties: NEE (μmol m−2 s−1), NEE_unc; LE (W m−2), LE_unc; H (W m−2), H_unc; Tau (kg m−1 s−2), Tau_unc
  - Storage terms: CO2_strg (μmol m−2 s−1), LE_strg (W m−2), H_strg (W m−2)
  - Environmental state: Pa (kPa), Tair (°C), RH (%), VPD (hPa), SWin/SWout (W m−2), LWin/LWout (W m−2), Rnet (W m−2), PAR (W m−2), G (W m−2), Tsoil (°C), VWC (%), windspeed (m s−1), winddir (degrees), Ustar (m s−1), TKE (m−2 s−2), Tstar (K), L (m), (z−d)/L (dimensionless)
  - Flux components: NEE_f (observed/final), NEE_f_sd (uncertainty of gap-filled NEE), Reco (ecosystem respiration), GPP (gross primary productivity)
- The dataset provides both pre-gap-filled values and gap-filled products to support analysis of ecosystem carbon exchange and energy fluxes.

## File description and usage
- The dataset enables analysis of growing-season carbon, energy, and water exchanges for a bioenergy maize crop, including post-gap-filled flux partitions (GPP and Reco).
- Suitable for studies on ecosystem carbon balance, energy partitioning, and the effects of weather and soil conditions on fluxes in temperate agroecosystems.

## Acknowledgements
- Funded by the Leeds-York-Hull Natural Environmental Research Council (NERC) Doctoral Training Partnership (DTP) Panorama (grant NE/S007458/1).
- Acknowledges the University of Leeds Research Farm and Rob Yardley for farm management information.

## References
- Includes methodological and instrument references (EddyPro, LI-7200RS, footprint and QC methods, gap-filling approaches, and meteorological data sources).