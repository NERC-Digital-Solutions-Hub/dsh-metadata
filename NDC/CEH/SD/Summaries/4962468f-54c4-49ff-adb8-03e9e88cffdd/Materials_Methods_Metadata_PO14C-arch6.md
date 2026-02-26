# Materials and methods, and metadata for Freshwater Particulate Organic Radiocarbon for Four Major UK Catchments, 2013-2014

## Overview
- Document describes field sampling, laboratory methods, and metadata for freshwater particulate organic radiocarbon (14C) across four major UK catchments during 2013–2014.
- Data are derived from the study “Aged riverine particulate organic carbon in four UK catchments” (Adams et al., 2015, Science of the Total Environment).
- Focus is on generating and standardizing 14C (as % modern carbon, pMC) and δ13C data for suspended particulate matter (SPM) and related organic carbon content.

## Study catchments and site context
- Ribble catchment (NW England): high population density (≈989 km^-2); subcatchments Hodder and Calder; Calder includes Burnley/Blackburn; upper catchment shows flashy response.
- River Conwy (North Wales): population density ≈49 km^-2; largely mountainous; rapid river response to rainfall events.
- Hampshire Avon (South England): population density ≈108 km^-2; groundwater-dominated with chalk aquifers; tidal limit shows limited rainfall response.
- River Dee (NE Scotland): population density ≈4 km^-2 above tidal limit; upper catchment is mountainous with rapid response to rainfall/snowmelt.

## Sampling and sample preparation
- Water samples (5 L) collected at tidal limits; additional upstream samples from Ribble and Dee.
- SPM isolation by centrifugation (approximately 9600 rpm for 30 min; ~100 mL final suspension).
- Organic carbon content measured by two methods:
  - Filtration through pre-weighed GF/F filters to determine SPM concentration [SPM].
  - Total carbon analysis with elemental analyzers (Vario EL and Thermo Flash 2000).

## Radiocarbon (14C) analysis and isotopic corrections
- Graphite targets prepared from CO2 recovered from combusted samples; CO2 reduced to iron/graphite (Sn/Slota method).
- δ13C measured (to correct 14C) with dual-inlet mass spectrometry (Thermo Fisher Delta V); δ13C used to normalize 14C data to -25 ‰ VPDB.
- Most 14C analyses conducted at SUERC AMS Laboratory (East Kilbride); three smaller samples analyzed at UCIAMS (Keck Carbon Cycle AMS) due to sample size (<500 μg C).
- Quality controls included size-matched process background materials and known age standards; accuracy checks performed to ensure reliability.
- 14C results reported as absolute pMC (percent modern carbon), adjusted for radioactive decay relative to AD 1950; bomb carbon scenarios acknowledged when applicable.
- Overall analytical precision is stated as 1σ.

## Data products and output
- Outputs include 14C pMC values and associated δ13C corrections for each sample, plus SPM concentration and % organic carbon (%OC).
- Data are organized in a dataset with explicit metadata fields (Riverine_PO14C_Raw_Data).

## Metadata and column definitions (Riverine_PO14C_Raw_Data)
- Catchment: study catchment name.
- Site: river within the catchment.
- Flow: qualitative flow condition at sampling (e.g., High/Low).
- Lat/Long: geographic coordinates.
- Publication code: analysis-stage unique code for data.
- Date: sampling date.
- d13CVPDB‰: stable carbon isotope ratio.
- 14C pMC: radiocarbon content relative to modern standard.
- +/- 1σ PMC: analytical uncertainty.
- [SPM]: suspended particulate matter concentration.
- %OC: organic carbon content.
- Additional fields capture units and notes for each column.

## Data quality, limitations, and usage notes
- Handling of patchy or diverse data formats across sites; emphasis on clear metadata to enable data integration.
- Acknowledges need for clear communication of methods and uncertainty to support re-use and cross-study comparisons.
- Outputs are suitable for dashboards or reports to enable end-user exploration and self-service data analysis.

## References (key methods and standards)
- Boutton et al. (1983): combustion tube comparison for stable carbon isotope analysis.
- Slota (1987): preparation of small samples for 14C AMS targets.
- Xu et al. (2004): SUERC 5MV AMS facility capabilities for 14C dating.
- Stuiver & Polach (1977): reporting of 14C data and decay corrections.