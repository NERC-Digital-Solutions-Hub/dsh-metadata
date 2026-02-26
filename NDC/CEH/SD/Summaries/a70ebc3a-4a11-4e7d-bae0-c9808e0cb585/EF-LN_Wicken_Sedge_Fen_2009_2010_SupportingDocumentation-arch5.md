# Eddy covariance measurements of carbon dioxide, energy and water fluxes at a conservation managed fen, Wicken Sedge Fen, Cambridgeshire, UK, 2009 to 2010

## Overview of dataset
- Time series of land-surface–atmosphere exchanges: net ecosystem CO2 exchange (NEE), sensible heat (H), latent heat (LE), and momentum flux (τ) measured at EF-LN Wicken Sedge Fen.
- Turbulent flux densities collected using eddy covariance (EC) between 2009-03-20 to 2009-12-31 and 2010-04-09 to 2011-01-16.
- Includes ancillary meteorological and soil-physics observations and variables characterising atmospheric turbulence.
- Data provided as a single gap-filled and partitioned CSV with thirty-minute flux intervals; missing data indicated by -9999 where applicable.

## Study site
- Wicken Sedge Fen (EF-LN), 52° 18' 34.86" N, 0° 16' 47.01" E, 2 m amsl; conservation-managed rich fen in Cambridgeshire, UK.
- Temperate maritime climate; mean annual temperature ~10.7°C and precipitation ~563 mm yr^-1 (1981–2010 normals).
- Peat depth ~2–4 m; hydrologically isolated from surrounding arable land; calcareous water from Monks Lode.
- Peat properties: bulk density ~0.37 g cm^-3, pH ~7.5, C content ~32%, C:N ~15.
- Site description informed by multiple references.

## Sampling regime
- Automated flux, meteorological, and soil measurements conducted during two periods: 2009-03-20 14:30 to 2009-12-31 08:30 and 2010-04-09 12:30 to 2011-01-17 00:00.

## Flux data acquisition
- EC measurements above grass canopy at 3.95 m height.
- Instruments: Solent R3 ultrasonic anemometer with LI-7500 CO2 analyzer; raw 20 Hz data captured by CR3000 data logger.
- Variables: NEE (μmol CO2 m^-2 s^-1), τ (kg m^-1 s^-2), H (W m^-2), LE (W m^-2); additional turbulence metrics computed.

## Ancillary data acquisition
- Co-located meteorological and soil observations: air temperature (Ta, °C) at 2 m, relative humidity (RH, %), net radiation (Rnet, W m^-2), shortwave and longwave components, soil heat flux (G), soil temperature (0–0.1 m).
- Equipment: HMP45 probe, CNR1 net radiometer, HFP01 soil heat flux plates, TCAV soil thermocouples.

## Data processing
- Turbulent fluxes computed with EddyPRO software (Version 7.0.6) using 30-minute averaging.
- Processing steps include QC of 20 Hz data, angle-of-attack corrections, 2D rotation to align with local terrain, corrections for spectral attenuation, density corrections for H and LE, and storage corrections for CO2.
- Uncertainty for each 30-min flux calculated following standard approaches.

## Quality control
- Outliers removed using median absolute deviation; flux bounds applied:
  - H: -200 to 550 W m^-2
  - LE: -60 to 600 W m^-2
  - NEE: -50 to 30 μmol CO2 m^-2 s^-1
- NEE filtered by nighttime sign, friction velocity (u*) threshold ≥ 0.18 m s^-1, and flux-footprint criterion (≥ 80% from target ecosystem).
- Weekly visual QA with manual removal of obvious errors.

## Data gap-filling and flux partitioning
- Data gaps in EC fluxes filled using Marginal Distribution Sampling (MDS) approach.
- NEE partitioned into GEP and TER using Reichstein et al. (2005) method driven by Ta data; used REddyProc (R) for gap-filling and partitioning.
- Missing meteorological data filled where possible from on-site automated weather station.
- Gap-filled products: NEE_filled, LE_filled, H_filled, with corresponding uncertainties; GEP and TER estimates provided.

## Details of data structure
- Time series delivered as a single CSV: EF-LN_Wicken_Sedge_Fen_2009_2010.csv.
- Time resolution: 30-minute records; flux data collected in defined windows; some periods absent due to instrument downtime.
- Missing records denoted by -9999.
- Columns include: DateTime, NEE, NEE_sd, LE, LE_sd, H, H_sd, Tau, Tau_sd, CO2_strg, CO2_strg_sd, Ta, RH, VPD, SWin, SWout, LWin, LWout, Rnet, G1, G2, WS, WD, Ustar, TKE, L, zL, Xpeak, x70, x90, fp2D, NEE_filled, NEE_filled_sd, LE_filled, LE_filled_sd, H_filled, H_filled_sd, TER, GEP, etc. (values and units aligned with LI-COR conventions and Reichstein et al. 2016).
- Table 1 in the dataset describes variable names, descriptions, and units.

## Nature and units of recorded values
- NEE, LE, H, and τ are reported with their respective uncertainties and gap-filled variants.
- Meteorological and soil parameters include Ta (°C), RH (%), VPD (hPa), radiation components (W m^-2), soil heat flux (W m^-2), wind metrics (WS m s^-1, WD degrees, Ustar m s^-1), turbulence metrics (TKE, L, zL), footprint metrics (fp2D), and gap-filled products (NEE_filled, LE_filled, H_filled) with standard deviations.

## Access, provenance, and documentation
- Data produced under Natural Environment Research Council award NE/R016429/1; part of UK-SCAPE National Capability.
- Acknowledgments note cooperation with Wicken Fen National Nature Reserve and supporting institutions.
- References provided for data processing methods, QC procedures, and previous site studies.

## Practical considerations for data stewards
- Metadata richness: site details, instrumentation, processing steps, QC criteria, and gap-filling methods are well-documented to support reuse.
- Data standards: use of standardized processing (EddyPRO, REddyProc) and common flux definitions (NEE, GEP, TER) supports interoperability.
- Data availability and limitations: gap-filled products and footprint filtering are clearly described; -9999 marks missing data; flux windows are limited to specific periods.
- Documentation readiness: clear variable descriptions, units, and data structure facilitate discovery, understanding, and integration into larger data ecosystems.