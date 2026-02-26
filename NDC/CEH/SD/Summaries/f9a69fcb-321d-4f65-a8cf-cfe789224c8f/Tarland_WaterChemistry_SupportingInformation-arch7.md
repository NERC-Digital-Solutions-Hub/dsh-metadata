# Tarland catchment study: mean daily flow and water chemistry data (Tarland Burn, 2000-2010)

## Overview
- Part of a Scottish Government funded program spanning ~15 years, focusing on the Tarland Catchment as an upper tributary of the River Dee (NE Scotland).
- Investigates diffuse pollution, river morphology, wastewater from private septic tanks, habitat and biodiversity, and flood mitigation.
- Data intended to support spatial analyses and map-based visualisations of water quality and hydrology.

## Data Description
- Variables: mean daily flow (m3/s) and water chemistry determinands.
- Time coverage: 2000–2010.
- Chemistry determinands (units mg/L where indicated):
  - Total dissolved phosphorus (TDP)
  - Soluble reactive phosphorus (SRP)
  - Total phosphorus (TP)
  - Particulate phosphorus (PP)
  - Nitrate (NO3-N)
  - Ammonium (NH4-N)
  - Suspended solids (SS)
- Location: Tarland Burn sampling site at Coull (near catchment outlet); coordinates provided in both WGS84 and OSGB grids (57.111, -2.810; OSGB 351050, 802540).

## Sampling and Data Collection
- Sampling design:
  - Weekly grab samples (2000–2003).
  - Daily sampling during rainfall events; autosampler used Feb–Mar 2004 (ISCO 3700).
  - Apr 2004–May 2005: daily samples with increased frequency (every 4 hours during storm events).
  - Post June 2005: more infrequent, irregular sampling.
- Autosampler conditions: not refrigerated; housed in a wooden shed; samples returned in cool boxes; sampling intervals typically 5–14 days, with more frequent sampling during storms.

## Laboratory Analysis and Calculations
- Filtration: part of sample filtered through Whatman 0.45 µm filters.
- Suspended solids (SS): determined gravimetrically from filtered residue.
- Filtrate analyses (within 24 hours): NO3-N, NH4-N, and molybdate reactive phosphorus (MRP).
- Further analyses (within ~4 days): total dissolved N (TDN), total dissolved P (TDP), dissolved organic carbon (DOC) via persulfate/UV digestion.
- Unfiltered samples: digested for NO-N and MRP; used to derive:
  - Dissolved organic N (DON) = TDN − (NO3-N + NH4-N)
  - Dissolved organic P (DOP) = TDP − MRP
  - Particulate N (PN) and particulate P (PP) taken as the digest values from the unfiltered sample:
    - PN = TN − TDN
    - PP = TP − MRP

## Discharge Data and Time Referencing
- Stage height calibrated to discharge using velocity-area profiling across the channel at 60% depth.
- Velocities measured with a propeller device (Valeport).
- Stage heights logged at 1-minute intervals; summaries every 15 minutes.
- Mean daily flow calculated from stage/discharge data; day defined as 9:00–08:45 for compatibility with Met Office rainfall data.

## Spatial Reference and Accessibility
- Sampling site location specified with precise geographic coordinates (WGS84) and OSGB grid reference, enabling GIS integration and map-based visualization of locations and flow/chemistry data.

## GIS and Data Integration Considerations
- Suitable for creating spatio-temporal maps of flow and water chemistry across the Tarland Burn catchment.
- Requires handling of multiple data resolutions and irregular sampling, especially after 2005.
- Data processing steps (DON, DOP, PN, PP) provide derived layers for more advanced spatial analyses of dissolved and particulate nutrient dynamics.

## Data Quality and Limitations
- Temporal gaps and irregular sampling after mid-2005; varying sampling frequency over the project.
- Autosampler conditions (not refrigerated) may have implications for sample integrity during warmer periods.
- Metadata on QA/QC procedures beyond standard lab procedures is not detailed, which may affect cross-comparison across years.

## GIS-Relevant Takeaways
- Rich multi-parameter water quality dataset aligned with hydrological measurements and precise site coordinates.
- Enables creation of choropleth/point maps for each determinand, time-series animations, and correlation with rainfall and discharge data.
- Suitable for informing policy and stakeholder discussions on diffuse pollution and flood mitigation within the River Dee catchment.