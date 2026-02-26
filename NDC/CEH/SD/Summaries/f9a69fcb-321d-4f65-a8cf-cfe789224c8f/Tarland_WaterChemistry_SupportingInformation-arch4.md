# Tarland catchment water quality and discharge data (Tarland Burn, 2000-2010)

## Overview
- Part of a long-running Scottish Government-funded research program (~15 years) and one of the UK's longest-running comprehensive catchment case studies.
- Aimed at understanding water quality, habitat, biodiversity, diffuse pollution impacts, and flood mitigation within the Tarland catchment, the uppermost tributary of the River Dee in NE Scotland.
- Tarland Burn is sampled near its outlet at Coull; dataset covers mean daily flow and water chemistry from 2000–2010.

## Data content
- Mean daily flow (m3/s) for Tarland Burn.
- Water chemistry determinands (units: mg/l): total dissolved phosphorus (TDP), soluble reactive phosphorus (SRP), total phosphorus (TP), particulate phosphorus (PP), nitrate-nitrogen (NO3-N), ammonium-nitrogen (NH4-N), suspended solids (SS).
- Derived calculations:
  - Dissolved organic N (DON) = TDN − (NO3-N + NH4-N)
  - Dissolved organic P (DOP) = TDP − MRP
  - Particulate N (PN) and Particulate P (PP) derived from digest values of unfiltered samples.
- Location: Coull site (WGS84 57.111, −2.810; OSGB 351050, 802540).

## Sampling and collection methods
- Sampling regime:
  - Weekly grab samples (2000–2003).
  - February–March 2004: daily samples via autosampler (ISCO 3700).
  - April 2004–May 2005: daily sampling, with increased frequency (4-hourly) during storm events.
  - Post-June 2005: more infrequent, irregular sampling.
- Autosampler housed in a wooden shed under shade; not refrigerated.
- Sampling cadence and site location designed to capture variability, including rainfall events.

## Laboratory analysis and data processing
- Filtration: aliquots filtered through 0.45 µm cellulose acetate filters; SS determined gravimetrically.
- Colorimetric analyses: NO3-N, NH4-N, and molybdate reactive P (MRP) using a San++ analyser within 24 hours.
- Additional analyses (within ~4 days): total dissolved N (TDN), TDP, dissolved organic carbon (DOC) after persulphate/UV digestion.
- Unfiltered samples digested (within ~4 weeks) by persulphate autoclave to quantify NO-N and MRP (for PN and PP calculations).
- Data handling ensured derivation of DON, DOP, PN, PP from digestion results as described.

## Discharge data and data handling
- Stage height calibrated against discharge using velocity-area profiling across the channel at 60% depth; velocities measured with a propeller (Valeport).
- Stage heights logged at 1-minute intervals; daily flow computed with a 9:00–8:45 window to align with Met Office rainfall data.
- Data structured for compatibility with other meteorological datasets (e.g., rainfall records).

## Data provenance, quality, and use
- Detailed methodological descriptions support data quality, reproducibility, and reuse in broader catchment analyses.
- Site coordinates and sampling strategy enable integration with spatial datasets and cross-site comparisons.
- Time-varying sampling frequency and autosampler conditions noted as caveats for long-term analyses and trend interpretation.