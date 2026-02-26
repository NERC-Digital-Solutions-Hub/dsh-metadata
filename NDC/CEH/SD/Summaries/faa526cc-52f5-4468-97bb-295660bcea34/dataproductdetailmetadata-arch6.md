# Macroinvertebrate taxonomic abundance, water quality, river flow, air temperature and environmental site descriptors from English rivers, 1965 - 2018

## Summary
- Open data product linking macroinvertebrate abundance across 1,519 English river monitoring sites (1965–2018) with 41 water quality determinands, river flow, air temperature, and static environmental descriptors.
- Integrates multiple national-scale datasets to enable environmental analyses and modelling of chemical exposures on freshwater biota.
- Outputs are provided as regionally split CSV files, with accompanying site descriptors, water quality statistics, river flow statistics, air temperature statistics, and habitat and land-cover context.

## What the data include and its purpose
- Macroinvertebrate taxonomic abundance time series (at family to species level where possible) across 1519 sites.
- Temporal covariates aligned to macroinvertebrate sampling dates:
  - Water quality determinands (41 chemicals or metrics) and their 6-month preceding statistics (min, max, mean, median, std) with LoQ handling options.
  - River flow statistics around the sampling date and LIS period (mean, median, std, coefficient of variation, quantiles, exceedance metrics).
  - Air temperature statistics for the 6 months preceding sampling.
- Static site descriptors:
  - Habitat quality indices from River Habitat Survey (RHS): HMS, HMS_Class, RSB_SubScore, HQA, HQA_ADJ.
  - Upstream catchment land cover from Land Cover Map 2015 (LC_WOODLAND_PERCENT, LC_ARABLE_PERCENT, LC_SEMINATURAL_PERCENT, LC_URBAN_PERCENT, and corresponding areas).
  - Site physical parameters (altitude, slope, distance from source, discharge, width, depth, substrate).
  - Wastewater effluent exposure proxy (EDF) derived from LF2000-WQX model.

## Data sources and provenance
- Macroinvertebrate time series: Freshwater river macroinvertebrate surveys (Biosys) via Environment Agency (EA).
- Water quality data: EA Water Quality Archive; pre-2000 data from EA licensed datasets.
- River flow data: National River Flow Archive (NRFA) gauged daily flow data.
- Air temperature: CHESS-met meteorology dataset (Great Britain, 1961–2017).
- Wastewater exposure: LF2000-WQX model (EDF).
- Habitat quality and landscape context: River Habitat Survey (RHS) and Land Cover Map 2015 (LCM2015).
- Geographic framework: UKCEH digital river network, IHDTM land/flow grids, ArcGIS/GRASS workflows; regionally partitioned into seven EA regions.

## Data integration and processing workflow
- Three main integration steps:
  - Spatial matching: link macroinvertebrate sampling sites to nearby water quality, river flow, and RHS survey sites along the river network (nearest in-network distance).
  - Spatial integration: extract modelled/derived variables (EDF, land cover, air temperature) at macroinvertebrate site locations.
  - Temporal matching: align time-series data (water quality, river flow, air temperature) to the macroinvertebrate sampling date with a 6-month look-back window.
- Data processing highlights:
  - FRMS data cleaning to reconcile site IDs, taxonomic names, and abundances; taxonomic harmonisation against Davies & Edwards (2011) with updates for EA nomenclature.
  - Standardization of abundances: transition from semi-quantitative to quantitative counts around 2002.
  - Water quality site matching prioritized proximity, data completeness, and absence of upstream wastewater influences between sites.
  - EDF modelling and extraction to associate macroinvertebrate sites with the closest reach on both truncated and full river networks; discrepancies flagged.
  - Land cover processing via rasterisation and IHDTM flow-accumulation grid to compute upstream catchment land cover percentages and areas.
  - RHS site matching within 5 km, extraction of HMS/HMS_Class/HQA/HQA_ADJ and related RHS components.
- Output structure is designed to support self-service analyses and dashboards.

## Outputs and file structure
- Macroinvertebrate site descriptors (CP_REGION_MInv_siteVariables.csv) per EA region.
- Macroinvertebrate taxon abundance time series (CP_REGION_MInv_taxonAbundance_<startDate-endDate>.csv) per region.
- Water quality determinand statistics (CP_REGION_MInv_<Determinant>Stats_<startDate-endDate>.csv) per region.
- River flow statistics (CP_REGION_MInv_riverFlowStats_<startDate-endDate>.csv) per region.
- Air temperature statistics (CP_REGION_MInv_airTempStats_<startDate-endDate>.csv) per region.
- Site locations and matched pairings (CP_REGION_MInv_siteMatchedLocation.csv) per region.
- RHS-related data and additional file for multiple RHS surveys (SiteswithmultipleRHSsurveys.csv) and related RHS descriptors (within siteVariables files).
- All data are regionally partitioned across seven EA regions; most outputs are CSV with NA representing missing values.
- Documentation and data dictionaries accompany the data (Appendices and Table 7–12 in the accompanying note).

## Key variables and how they are produced
- Macroinvertebrate abundance: taxa counts per sample; taxon name, taxonomy, abundance, sample/date, site.
- Water quality statistics: for each determinand and macroinvertebrate date, compute 6-month statistics (min, max, mean, median, std) under three LoQ handling schemes (LoQ1, LoQ2, LoQ3).
- River flow statistics: POI (1974–2019) and preceding 6-month periods; includes mean, median, std, coefficient of variation, multiple quantiles, and exceedance metrics.
- EDF: mean, 90th, 95th percentile and std of wastewater dilution factor per site, derived from LF2000-WQX; NA when network truncation introduces gaps.
- Air temperature: daily mean temperature statistics for 6-month windows; limited to data up to CHESS-met end (2017).
- Habitat quality indices: HMS, HMS_Class, RSB_SubScore, HQA, HQA_ADJ derived from RHS site observations.
- Land cover: upstream woodland, arable, seminatural, urban percentages and areas (km2) aggregated from LCM2015 using IHDTM flow accumulation for catchments upstream of each site.
- Site descriptors: altitude, slope, distance from source, discharge category, width, depth, substrate composition (boulders/cobble, pebbles/gravel, sand, silt/clay, etc.).

## Data quality, limitations, and caveats
- Gaps and data availability:
  - Final output contains gaps (noData) in many variables due to non-matching records or temporal coverage limitations.
  - Some water quality matches are omitted due to EA licensing restrictions; a few sites have matched water quality sites but lack chemistry data due to retrieval issues.
  - CHESS-met ends in 2017, so post-2017 air temperature matching is unavailable.
  - Land cover data treated as static due to resource constraints and time-varying data integration challenges.
- Temporal alignment and aggregation:
  - 6-month pre-sampling window used for time-series statistics; six-month period choice may influence detected associations.
- Data handling and units:
  - Values below LoQ are treated with three configurations (LoQ1, LoQ2, LoQ3) during statistics computation.
  - Some determinands reported with upper-bound values; in statistics, upper-bound values are used as given.
  - Water quality data prior to 2000 pulled from EA licensed datasets with potentially different QA levels than post-2000 data.
- Spatial matching caveats:
  - Proximity-based matching along river networks; headwater and network truncation can yield NA for EDF in some upstream locations.
  - Distances and river network geometry influence matching, especially for small headwater streams with limited WWTW coverage.

## Data access and usage notes
- Outputs are provided as region-specific CSV files for each data stream, with careful documentation on column definitions and data provenance.
- Users should consult the accompanying documentation (tables, appendices) for detailed field definitions, data provenance, and method descriptions.
- For data ingestion, treat 'NA' as missing values and specify appropriate data types when loading (e.g., pandas in Python, data frames in R).

## Practical applications for data support
- Supports cross-disciplinary analyses of chemical exposure and freshwater biota across long temporal and broad spatial scales.
- Enables dashboards and self-serve exploration of macroinvertebrate responses to water quality, flow regimes, habitat quality, and landscape context.
- Facilitates regional comparisons, trend analyses, and integration with ecological and environmental policy studies.