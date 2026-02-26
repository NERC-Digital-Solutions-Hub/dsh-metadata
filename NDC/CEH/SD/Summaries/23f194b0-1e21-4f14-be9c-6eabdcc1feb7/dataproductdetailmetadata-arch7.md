# Macroinvertebrate taxonomic abundance, water quality, river flow, air temperature and environmental site descriptors from English rivers, 1965 - 2018

## Overview
- Open data product combining long-term ecological, chemical, hydrological and environmental information for English rivers (1965–2018).
- Core data: macroinvertebrate taxonomic abundance at 1,519 monitoring sites, linked with 41 water quality determinands, river flow, and air temperature, plus static site descriptors.
- Aims to enable environmental data and modelling analyses with map-based data products suitable for GIS users and policy/research audiences.

## Data scope and purpose
- Macroinvertebrate time series at 1,519 sites across England (1965–2018).
- Linked data include: 41 chemical determinands (water quality), daily river flow, CHESS-met-derived air temperature, and static descriptors (work wastewater dilution factor, habitat quality, upstream land cover, altitude, slope, distance from source, channel width/depth, substrate).
- Generated under the ChemPop project (NERC-funded) to study chemical exposure effects on wildlife; delivered as an open data product for broad scientific use.
- Data assembled from Environment Agency (EA), UKCEH, NRFA, and CHESS-met; post-processing addressed non-standard formats and inconsistencies across sources.

## Data sources and integration
- Macroinvertebrate data: EA Freshwater river macroinvertebrate surveys (Biosys), FRMS dataset.
- Water quality: EA Water Quality Data Archive (and pre-2000 EA licensed data).
- River flow: NRFA Gauged Daily Flow (GDF) via NRFA API.
- Air temperature: CHESS-met (Great Britain, 1961–2017).
- Wastewater exposure: EDF (effluent dilution factor) derived from LF2000-WQX model (2000s era).
- Habitat quality: River Habitat Survey (RHS) metrics (HMS, HMS_Class, RSB_SubScore, HQA, HQA_ADJ).
- Land cover: Land Cover Map 2015 (LCM2015) upstream catchment.
- Supporting hydrological context: Integrated Hydrological Digital Terrain Model (IHDTM) flow direction/accumulation grids; UKCEH digital river network (GB 1:50,000).
- Outputs are provided as region-split CSV files for seven EA regions, with linkages across data types via site IDs and sampling dates.

## Spatial and temporal matching (GIS workflow)
- Spatial matching: environmental sampling sites (WQ, RF, RHS) paired to nearest macroinvertebrate site along the river network (distance along network). Also matched RHS and WQ/RF data within 5 km along the river for site descriptors.
- Temporal matching: 6-month window preceding each macroinvertebrate sampling date; environmental time series aggregated (mean, median, min, max, SD). RHS and land cover are static/descriptive (no time dimension).
- EDF modelling: EDF values assigned per macroinvertebrate site by linking to the truncated river network (LF2000-WQX), with gaps due to headwater network differences flagged as NA.
- Land cover extraction: upstream catchment land cover percentage and area derived from LCM2015, snapped to IHDTM flow accumulation grid; catchment area defined by IHDTM cells with accumulation values >200.

## Variables and processing details
- Macroinvertebrate data: taxon abundance time series (BIO_SITE_ID, BIO_SAMPLE_DATE, BIO_ORD_NAME, BIO_FAM_NAME, BIO_SPGRP_NAME, BIO_ABUNDANCE, etc.), region-specific files CP_<REGION>_MInv_taxonAbundance_<startDate-endDate>.csv.
- Water quality: 41 determinands with 6-month statistics per macroinvertebrate site; outputs CP_<REGION>_MInv_<determinandLabel>Stats_<startDate-endDate>.csv. Handling of LoQ below-detection values via three configurations (LoQ1/LoQ2/LoQ3) and upper-range values as reported.
- River flow: POI statistics (20/05/1974–29/03/2019) and 6-month preceding macroinvertebrate date; outputs CP_<REGION>_MInv_riverFlowStats_<startDate-endDate>.csv.
- Air temperature: daily mean values from CHESS-met; six-month preceding statistics per site; outputs CP_<REGION>_MInv_airTempStats_<startDate-endDate>.csv.
- Habitat quality: RHS-derived metrics (HMS, HMS_Class, HMS_RSB_SubScore, HQA, HQA_ADJ) aligned to macroinvertebrate sites; stored as site descriptors CP_<REGION>_MInv_siteVariables.csv.
- Land cover: upstream woodland/arable/seminatural/urban land cover percentages and areas (LC_WOODLAND_PER/AREA, LC_ARABLE_PER/AREA, LC_SEMINATURAL_PER/AREA, LC_URBAN_PER/AREA); linked to macroinvertebrate sites via CP_<REGION>_MInv_siteVariables.csv.
- Site descriptors: combined 1519 macroinvertebrate sites with associated geometry coordinates, catchment details, WQ/RF/RHS links; CP_<REGION>_MInv_siteMatchedLocation.csv.
- Spatial accuracy checks: distance to IHDTM cell < 1 km; land-cover sums within 99.96–100.04% to ensure accuracy.

## File structure and data accessibility
- 7 region-based site descriptor files: CP_<REGION>_MInv_siteVariables.csv (region-wide site descriptors).
- Macroinvertebrate taxon abundance: CP_<REGION>_MInv_taxonAbundance_<startDate-endDate>.csv.
- Water quality statistics: CP_<REGION>_MInv_<determinandLabel>Stats_<startDate-endDate>.csv (41 determinands across 7 regions; some rows contain NA values due to data gaps).
- River flow statistics: CP_<REGION>_MInv_riverFlowStats_<startDate-endDate>.csv.
- Air temperature statistics: CP_<REGION>_MInv_airTempStats_<startDate-endDate>.csv.
- RHS site descriptors: CP_<REGION>_MInv_siteVariables.csv (habitat quality metrics and related RHS-derived descriptors).
- RHS site locations and paired data: CP_<REGION>_MInv_siteMatchedLocation.csv; SiteswithmultipleRHSsurveys.csv.
- Data product note on NA handling and data types; instructions for reading CSVs with missing values (NA) in Python/R.

## GIS considerations and usage
- Coordinate systems: macroinvertebrate and site data use British National Grid (BNG); site matching performed along river network with distance-based and network-based logic.
- Spatial integration relies on vector and raster GIS workflows (ArcGIS IRN extension, IHDTM rasters, 50 m resolution grid for land cover class assignment, GRASS GIS r.accumulate equivalents).
- Data products enable map-based exploration of relationships between macroinvertebrate communities and water quality, flow regimes, temperature, habitat quality, and upstream land cover at multiple spatial scales (site- and catchment-level descriptors).
- Data gaps and licensing restrictions may limit some region/site coverage for water quality data; 34 sites lack water quality matches due to licensing, and 5 have matched sites but no data due to extraction issues.

## Data quality, limitations, and caveats
- Data originate from multiple agencies with varying collection purposes, leading to standardisation and coverage gaps; final output includes gaps (NoData) for many variables.
- Land cover data treated as static due to resource constraints and methodological differences across time.
- Pre-2000 water quality data required special handling; LoQ handling options applied; some measurements above upper quantification limits used as reported.
- CHESS-met ends in 2017; temperature data beyond that date are unavailable for site matching.
- EDF matching may yield NA in headwater areas due to truncated network representation and absence of certain wastewater sources in the truncated model network.
- RHS provides non-temporal indices (static per site) with limited repeat surveys; a small subset of sites had multiple RHS surveys.

## Author contribution and sources
- Data engineering, ecological interpretation, spatial analysis, and GIS-centric data assembly performed by a multi-institution team.
- Primary data sources include EA Biosys FRMS, EA Water Quality Archive, NRFA, CHESS-met, LF2000-WQX, RHS, LCM2015, IHDTM, and the UK river network.

## Usage notes
- Suitable for GIS-based analyses of long-term ecological responses to chemical exposure, hydrology, and habitat factors in English rivers.
- Users should account for missing values, temporal alignment constraints, licensing-related data gaps, and the static nature of some descriptors when designing analyses or visualisations.
- Proper loading of NA values and data types is essential when using Python (Pandas) or R for downstream analyses.