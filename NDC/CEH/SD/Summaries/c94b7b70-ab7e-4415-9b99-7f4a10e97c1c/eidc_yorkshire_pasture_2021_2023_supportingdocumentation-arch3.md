# Eddy covariance measurements of carbon dioxide, energy and water fluxes at a pasture, Yorkshire, UK, 2021-2023

## Overview of the dataset
- 30-minute observations of land-atmosphere exchange: net ecosystem CO2 exchange (NEE), sensible heat (H), and latent heat (LE) over 1.5 years.
- Measurements conducted with micrometeorological eddy covariance (EC) method from 01/09/2021 to 01/01/2023.
- Dataset includes accompanying weather and soil physics measurements.

## Study site
- Location: field at the University of Leeds Research Farm (53°51'58.64"N, 1°19'11.08"W).
- Management: grazed by sheep since 2012; occasional silage cutting; rainfed with no fertiliser.
- Climate: temperate oceanic; mean annual temperature ~9.5 °C; precipitation ~885 mm (1992–2022).
- Soil: loamy, calcareous brown earth; pH ~6.8; bulk density ~1.1 g cm-3; soil carbon ~27.7 g kg-1 and nitrogen ~2.3 g kg-1 (0–30 cm).
- Grazing and silage events during the measurement period (including July 2022 silage cut).

## Collection methods and fieldwork instrumentation
- Flux measurements: closed-path EC system with sensors 2 m above canopy.
- Instruments: LI-7200RS CO2/H2O, Gill Windmaster 3D anemometer; data logged at 10 Hz as 30-minute means.
- Ancillary measurements: SN-500 net radiometer, HMP155 air temp/humidity probe, TEROS 11 soil temperature/moisture probes (5 cm depth). All logged as 30-minute means.
- Data workflow: integrated with a Smartflux 2 processing computer; ancillary data combined with flux measurements.

## Data processing
- Processing workflow follows Morrison et al. (2019).
- Fluxes computed with EddyPro 7; steps include data conditioning, angle-of-attack correction, cross-correlation for time lags, and corrections for co-spectral attenuation.
- Random uncertainty estimated per Finkelstein & Sims (2001).

## Quality control
- Software: R (v4.1.3).
- Criteria for data removal include: statistical outliers, LI-COR signal anomalies (>10% above baseline), nonrepresentative footprint (>20% outside site boundaries), unrealistic flux thresholds (e.g., H, LE, NEE limits), and friction velocity u* < 0.14 m s-1.

## Gap-filling
- Gap filling and flux partitioning performed with REddyProc (R) v0.6-0/r9 (Reichstein et al. 2016).
- Gaps filled using marginal distribution sampling; uncertainty of filled values derived from the standard deviation of donor observations (Reichstein et al. 2005; 2016).

## Details of data structure
- Primary dataset file: Yorkshire_Pasture_2021_2023.csv.
- Variables include: NEE, NEE_unc, LE, LE_unc, H, H_unc, Tau, Tau_unc, CO2_strg, LE_strg, H_strg, Pa (barometric pressure), Tair, RH, VPD, SWin, SWout, LWin, LWout, Rnet, PAR, G, GPP, Tsoil, VWC, windspeed, winddir, Ustar, TKE, Tstar, L, (z-d)/L, NEE_f, NEE_f_sd, Reco, NEE_f etc.
- Data columns provide both pre-gap-filled and gap-filled values, with associated uncertainties where applicable.

## Accessibility and governance
- Acknowledged funding: Leeds-York-Hull NERC DTP Panorama (grant NE/S007458/1).
- Site contributions from the University of Leeds Research Farm; dataset authors acknowledge management information support.
- References and metadata provided to support reproducibility and methodological transparency.

## Relevance for Monitoring Frameworks
- Demonstrates an end-to-end monitoring data pipeline: from instrument acquisition and field deployment to data processing, quality control, gap-filling, and uncertainty quantification.
- Captures key environmental health indicators relevant to policy monitoring and decision-making:
  - Net ecosystem CO2 exchange (NEE) and its partitioning into GPP and Reco.
  - Energy fluxes (H, LE) and storage terms for CO2, heat, and moisture.
  - Environmental drivers (PAR, air/soil temperature, humidity, soil moisture, wind, pressure) and meteorological context (Rnet, radiation components).
- Emphasizes data governance considerations:
  - Documentation of processing steps and corrections (angle of attack, time lags, co-spectral corrections) to enable reproducibility.
  - Quality control criteria and thresholds to ensure data reliability.
  - Metadata detailing units, data provenance, and gap-filled vs. raw values.
  - Data sharing readiness through explicit data structure and uncertainty reporting.
- Highlights practical barriers and requirements for policymakers:
  - Need for standardized metadata and standardized processing to facilitate cross-site comparisons.
  - Importance of transparent gap-filling methodologies and uncertainty estimates to inform decision-making under data gaps.
  - Potential data accessibility challenges due to dataset size and complexity; gap between raw measurements and policy-ready indicators.

## Limitations and considerations
- Single-field study with a specific pasture and management regime; may limit generalizability to other ecosystems.
- Measurement period spans 1.5 years with notable agricultural events (e.g., silage cut) that influence flux dynamics.
- Some data gaps exist; reliance on gap-filling introduces additional uncertainty that is quantified but still requires careful interpretation for policy use.