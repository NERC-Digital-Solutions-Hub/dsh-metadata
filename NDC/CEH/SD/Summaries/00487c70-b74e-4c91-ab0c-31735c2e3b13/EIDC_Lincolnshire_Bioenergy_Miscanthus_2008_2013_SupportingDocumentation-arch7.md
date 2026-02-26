# Eddy covariance measurements of carbon dioxide, energy and water fluxes at a commercial Miscanthus x. giganteus plantation, Lincolnshire, UK, 2008 to 2013

## Overview
- Time series dataset Lincolnshire_Bioenergy_Miscanthus_2008_2013.csv records surface-atmosphere exchanges: net ecosystem CO2 exchange (NEE), sensible heat (H), latent heat (LE), and momentum (τ).
- Turbulent flux densities were measured with open-path eddy covariance (EC) from 2008-05-01 00:30 to 2013-02-18 00:00; ancillary meteorology and soil physics data and atmospheric turbulence metrics are included.
- Data include both raw/quality-controlled observations and gap-filled/partitioned outputs (GEP, TER) suitable for GIS-driven temporal analyses and integration with other spatial datasets.

## Study site
- Location: Miscanthus x. giganteus plantation, 53°19'10.07"N, 0°35'18.65"W; 11.5 ha mature commercial bioenergy site ~10 km north of Lincoln, UK.
- Climate: temperate maritime; mean annual air temperature ~9.8°C and precipitation ~614 mm yr^-1 (1981–2010 baseline).
- Soils: Beccles 1 association; seasonally waterlogged fine loams over mudstone; soil properties include bulk density ~1.46–1.53 g cm^-3, texture ~49% sand, 36% silt, 15% clay, soil organic carbon ~68 t C ha^-1, total nitrogen ~11 t N ha^-1.
- Land use history and management: former arable land planted spring 2006; initial replanting in 2007; no fertilizer until 2010 (Fibrefoss 660 kg ha^-1); annual spring harvests from 2008 onward.

## Sampling regime and data collection
- Flux measurements: EC system on a mobile mast at the plantation center, with height adjusted to ~2× canopy height.
- Sensors: sonic anemometer-thermometer and LI-7500 CO2/H2O analyzer; 20 Hz raw data sampled and 30-minute flux averages calculated.
- Ancillary data: meteorology and soil physics from scaffold tower (Ta, RH at 4 m; Rnet and radiation components; under-canopy PPFDbc; soil heat flux G; soil moisture and temperature; wind measurements; footprint indicators).
- Data products include both observed fluxes and ancillary measurements.

## Data processing and quality control
- Processing: EddyPRO v6.1 used for QC and flux calculation; includes coordinate rotation, tilt corrections, high/low-frequency attenuation corrections, density corrections, and uncertainty estimates.
- Quality control: outlier removal via median absolute deviation and EddyPRO flags; fluxes outside specified plausible ranges are excluded; footprint-based representativeness assessed with ART Footprint Tool; weekly visual inspection with manual cleaning.
- Uncertainties: random uncertainties for fluxes computed; additional variables (e.g., u*, TKE, L, z/L) derived for diagnostics.

## Data gap-filling and flux partitioning
- Gap-filling: Marginal Distribution Sampling (Reichstein et al. 2005) used to fill NEE, LE, H gaps.
- Flux partitioning: NEE separated into GEP and TER via Reichstein et al. (2005) framework using air temperature (Ta) driving; implemented with REddyProc (R package) for data processing and plotting.
- Output includes gap-filled fluxes and partitioned components (NEE_filled, NEE_filled_sd, LE_filled, H_filled, TER, GEP, and corresponding uncertainties).

## Data structure and units
- Data are provided as a single CSV with 30-minute time steps; timestamps are end of each flux averaging period (UTC/GMT).
- -9999 denotes missing records due to failures or QC filtering.
- Key variables and units (examples):
  - DateTime (yyyy-mm-dd HH:MM); NEE (μmol CO2 m^-2 s^-1); NEE_unc (μmol CO2 m^-2 s^-1)
  - LE (W m^-2); LE_unc (W m^-2)
  - H (W m^-2); H_unc (W m^-2)
  - Tau (kg m^-1 s^-2); Tau_unc (kg m^-1 s^-2)
  - Ta (°C); RH (%); VPD (hPa); Pa (kPa)
  - SWin, SWout, LWin, LWout, Rnet, SWin_total, SWin_diffuse
  - PPFDbc1-3 (μmol photons m^-2 s^-1); G1-2 (W m^-2); Tsoil1-2 (°C); VWC1-2 (%)
  - Windspeed1-2 (m s^-1); Winddir (degrees)
  - FootprintFraction1-2 (%); Ustar (m s^-1); TKE (m^-2 s^-1); L (m); zL (dimensionless)
  - NEE_filled, NEE_filled_sd; LE_filled, LE_filled_sd; H_filled, H_filled_sd; TER, GEP
  - NEE_filled represents gap-filled NEE; NEE_filled_sd its uncertainty; analogous for LE and H.

## Footprint and spatial relevance
- Footprint analysis (non-neutral conditions considered) ensures fluxes primarily originate from the target Miscanthus ecosystem; fluxes retained if >75% originate within the ecosystem.
- Data are suitable for GIS-based analyses combining fluxes with spatial layers (soil, climate, land cover) and can be integrated with other gridded environmental datasets.

## Access, references and acknowledgments
- Data collection funded by the Natural Environment Research Council (CarboBiocrop project) and CEH Integrating Fund; authors acknowledge landowner cooperation.
- References provided for methods and context (EddyPRO, REddyProc, footprint modeling, and related flux studies).

## Potential GIS applications
- Develop time-series maps of flux magnitudes (NEE, H, LE, τ) across the study period, aligned to 30-minute intervals.
- Combine with spatial rasters of climate, soil properties, and vegetation to analyze drivers of fluxes.
- Use footprint fractions to weight spatial contributions, enabling more accurate spatial representations of net ecosystem exchanges.
- Compare observed vs gap-filled fluxes for uncertainty visualization and gap-fatching impact assessment.
- Integrate with ancillary data (Rnet, PAR, soil moisture) to build multivariate GIS layers for policy and management insights.