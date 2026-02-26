# Carbon dioxide and methane fluxes and associated environmental observations during use as plantation forest on peat bog, Forsinard Flows RSPB Reserve, Scotland, 2016-2017

## Overview
- Measurements of greenhouse gas exchange (CO2 and CH4) over a plantation forest on peat at Forsinard Flow Country, Scotland (site Dyke).
- Afforestation occurred in the 1980s; drains blocked and harvesting completed in late 2017; dataset covers the afforestation period.
- Associated meteorological and pedological observations included for 2016-01-01 to 2017-12-31 at half-hour intervals.
- Project origin: University of Highlands and Islands (UHI) with JHI and RSPB; currently managed by the James Hutton Institute; funded via NERC SCO2FLUX and RESAS; UHI owns infrastructure; RSPB provided land access.

## Parameters
- Land-atmosphere exchange of CO2 (net ecosystem exchange, NEE) and CH4
- Turbulence metrics; latent and sensible heat fluxes (LE, H)
- Net radiation; basic meteorology (air temperature, relative humidity, barometric pressure, solar radiation, precipitation)
- Pedology (soil water content, soil temperature)

## File format and naming
- CSV format
- File naming: UK_$$$_DataProduct_%d_%m_%z.csv
  - $$$ = site reference code (Fluxnet conventions; UK_DKE)
  - %d_%m_%z = submission date (day, month, year)

## File contents
- Primary time series: TIMESTAMP (YYYY-MM-DD HH:mm) at half-hour intervals
- Gas/flux variables: CH4 (nmol CH4/mol), CO2 (µmol CO2/mol), NEE (µmol CO2 m^-2 s^-1), NEE_VUT_REF and NEE_VUT_USTAR variants, GPP components, RECO components, H (sensible heat, W m^-2), LE (latent heat, W m^-2), NETRAD (net radiation, W m^-2), PPFD (PAR), RH, TA, VPD, wind (WD, WS), soil temps (TS_*, TS_AVG), soil moisture, soil heat flux (G_*, e.g., G_1_1_1)
- Derived/diagnostic variables: multiple GPP_NT_VUT_USTAR partitions, NEE with various USTAR/MEF schemes, quality flags (H_F_MDS_QC, LE_F_MDS_QC, NEE_VUT_REF_QC, etc.)
- Precipitation, air pressure, PAR (PPFD_IN, PPFD_OUT, PPFD_IN_F_NS)
- Data quality and processing flags: Biomet Flag, EddyPro Flag, REddyProc Flag
- Missing value indicator: -9999

## Missing values
- Missing values represented by -9999

## Spatial coverage
- Location: latitude 58.427254, longitude -3.96934
- OS grid reference NC85090 50453

## Temporal coverage
- Main observational period: 2016-01-01 00:30 to 2018-01-01 00:00
- Dataset notes indicate measurements for 2016-2017 with processing extending into early 2018

## Experimental design and data collection
- Instrumentation mounted on a tall (≈20 m) mast; measurement height ≈18 m above canopy
- Eddy-covariance setup: Gill Windmaster Pro (turbulence), Licor LI-7200 enclosure (CO2/H2O)
- Meteorological/pedological sensors: air temp, RH, solar radiation, net radiation, soil heat flux, soil temperature, PAR, soil moisture
- Power: off-grid system (solar, methanol fuel cell, wind turbine)
- Data transmission: remote 4G; RAW data stored in binary; half-hour EC fluxes produced and archived
- Initial processing: Licor EddyPro for standard QC; REddyProc used for gap-filling and NEE partitioning

## Data processing and quality control
- EddyPro (v7.0.6) used for flux calculation; standard QC and corrections applied
- 2D footprint model (Kljun et al., 2015) for footprint assessment
- Data screening:
  - Outliers (median absolute deviation)
  - Stationarity tests; flux range checks (H, LE, NEE)
  - u* screening (exclude periods with low friction velocity)
- Gap-filling and partitioning:
  - REddyProc for gap-filling of H, LE, NEE and partitioning NEE into GEP and RE
  - Gap-filling of short gaps (0.5–1 h) by interpolation of biomet data
  - Longer gaps filled via co-located instruments, nearby EC towers, or Kinbrace Met Office data
  - Marginal Distribution Sampling (MDS) for gap-filling
- Calibration:
  - LI-7200 calibrated on 18/05/2017; other sensors not recalibrated during monitoring but reviewed for drift/faults
- Quality flags:
  - Biomet Flag (codes such as 00 raw, 01 primary, 02 calibrated, 13 interpolated, 32 modelled, 03 no data, 04 removed)
  - EddyPro Flag (0 best quality to -9999 missing)
  - REddyProc Flag (00 original, 01 most reliable, 02 medium, 03 least reliable, -9999 missing)

## Access and provenance
- Part of UKCEH network; data processed at UKCEH; supported by NERC SCO2FLUX and RESAS CentrePeat
- Collaboration: UHI, JHI, RSPB; land access facilitated by RSPB
- References and methodological context provided in accompanying references

## Usage considerations for data support
- Expect multiple derived variables and QC flags; plan for data wrangling to align time stamps and flag interpretations
- Use gap-filled NEE and partitioned GEP/RECO data with attention to flag values indicating reliability
- Leverage the dataset’s half-hour resolution and accompanying meteorological/pedological variables to build self-service dashboards or data products across policy or planning topics
- Be mindful of patchy data periods and reliance on gap-filled estimates in long gaps; reference REddyProc and EddyPro QC notes for filtering decisions

## References and funding (highlights)
- Key methodological references for eddy covariance processing, QC, footprint modeling, and gap-filling
- Networks and funders: UKCEH, NERC, RESAS, SCO2FLUX, JHI, UHI, RSPB