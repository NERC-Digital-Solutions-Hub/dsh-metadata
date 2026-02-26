# Carbon dioxide and methane fluxes and associated environmental observations from an unmodified blanket bog, Forsinard Flows RSPB Reserve, Scotland, 2016-2022

## Overview
- Long-term, near-natural blanket bog site measurements in Flow Country, Caithness and Sutherland.
- Records greenhouse gas exchange (CO2 and CH4) plus meteorological and pedological observations from 2016-10-19 to 2022-12-31 at half-hourly intervals (with table of contents hinting up to 2023-01-01).
- Installed in 2008 and now managed by The James Hutton Institute as part of the SCO2FLUX network; supported by NERC, RESAS, and local institutions (UHI, RSPB).
- Site access and ongoing operation supported by UKCEH team and local partners; designed to reflect an ecohydrologically pristine peat bog state.

## What the data contain
- Land-atmosphere exchange measurements of CO2 (net ecosystem exchange, NEE) and CH4, plus turbulence, heat fluxes (latent and sensible), net radiation, basic meteorology, and pedology (temperature, humidity, pressure, solar radiation, precipitation, soil moisture and temperature, soil heat flux).
- Additional derived and auxiliary variables including ET, various GPP/RECO components, footprint parameters, and quality control indicators.
- Data processed and gap-filled using established eddy covariance pipelines (EddyPro for fluxes; REddyProc for gap-filling and partitioning; MDS for gap-filling of H/LE).

## Data structure, format, and naming
- File format: CSV.
- File naming convention: UK_$$$_DataProduct.csv, where $$$ is a Fluxnet-convention site code; site reference UK_CLS.
- Key data columns include: TIMESTAMP, CH4, CO2, ET, FCH4, G, GPP/NEE components (e.g., GPP_DT_VUT_REF, NEE_VUT_REF, RECO, etc.), energy and biomet signals (H, LE, NEE, PPFD_IN, PAR, air temperature, humidity, etc.), footprint metrics (FETCH_10/30/50/70/90, FETCH_MAX), QC flags (FCH4_QC, H_qc, LE_qc, NEE_VUT_REF_QC, REddyProc flags, Biomet Flag), and metadata (units, descriptions).
- Missing values indicated by -9999.

## Spatial and temporal coverage
- Spatial: Lat/long 58.371598, -3.965194 (OS grid NC 85220 44146); point-scale measurement site.
- Temporal: 2016-10-19 00:30:00 to 2023-01-01 00:00 (half-hourly intervals; main focus 2016-2022 with extension noted up to 2023 in the table of contents).

## Experimental design and data collection
- Instruments mounted on ~3 m tripods over a large, flat bog; minimal direct management, slight grazing by red deer.
- Measurements collected continuously; eddy-covariance approach using:
  - Turbulence and CO2/H2O: Campbell Scientific IRGASON (10 Hz).
  - CH4: LI-7700 analyzer.
  - Other sensors: net radiometer, photosynthetically active radiation, soil moisture, soil temperature, soil heat flux, water table depth, etc.
- Data retrieved remotely via 4G; processed and archived with UKCEH software tools; gap-filled with REddyProc.

## Processing, quality control, and data products
- Processing chain:
  - EddyPro for flux calculations with standard corrections and quality controls.
  - 2D footprint modeling; rotation corrections; lag removal; cospectral corrections.
  - REddyProc for gap-filling and partitioning NEE into GEP and RECO; MDS for gap-filling H and LE.
  - Short gaps interpolated; longer gaps filled with co-located instrument data or nearby sources.
- Quality control procedures:
  - Outlier screening and physical plausibility checks; stationarity tests; flux ranges screening.
  - u* (friction velocity) threshold applied to exclude low-turbulence periods.
  - 2D footprint modeling to ensure appropriate source area.
  - QC flags:
    - Biomet Flag: codes for data review, calibration, gap interpolation, alternatives, or removal.
    - EddyPro Flag: 0 best quality, 1 suitable for general analysis, 2 should be discarded, -9999 missing.
    - REddyProc Flag: 0 original, 1 most reliable, 2 medium, 3 least reliable, -9999 missing.
- Data products and outputs include numerous NEE/RECO/GPP variants, energy fluxes (H, LE), and ancillary variables with associated uncertainties and QC fields.

## Calibration, data quality, and limitations
- 2016 refurbishment included a new IRGASON and sensor updates; IRGASON calibration in 2019; some sensors not recalibrated due to Covid.
- Soil heat flux sensors were expanded in 2019; final dataset averages across five sensors post-installation (26/08/2019).
- Calibration and quality notes highlight changes in instrumentation and logging, with ongoing drift checks and cross-instrument comparisons.
- Limitations include potential data gaps and calibration history constraints; QC flags help identify reliability levels across parameters.

## Metadata and references
- Dataset is part of a broader peer-reviewed context with references to standard methods and intercomparison studies for eddy covariance data processing (e.g., EddyPro, REddyProc, footprint models) and related site studies.
- Acknowledgments include NERC UKCEH, RESAS, JHI, UHI, and RSPB partners.

## Practical takeaways for Data Leaders
- The dataset provides a robust, long-term, high-frequency record of CO2 and CH4 fluxes from a natural peat bog, with comprehensive ancillary environmental data.
- It employs standardized, transparent processing and QC workflows (EddyPro, REddyProc) enabling reproducible analysis and reliable gap-filling/partitioning of NEE.
- Rich metadata includes file naming conventions, units, data flags, and detailed description of each variable, enhancing discoverability and governance.
- There are explicit notes on calibration history, sensor changes, and data limitations to inform assessment of data quality and suitability for policy or management-oriented analyses.
- For system-wide data strategy, the dataset exemplifies co-ownership of data products, cross-institution collaboration, and careful attention to data format, discoverability, and continuity across networks.