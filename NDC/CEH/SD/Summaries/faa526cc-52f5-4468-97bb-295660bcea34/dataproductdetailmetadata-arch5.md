# Macroinvertebrate taxonomic abundance, water quality, river flow, air temperature and environmental site descriptors from English rivers, 1965 - 2018

- Overview of the data product: a comprehensive, regionally disaggregated, open data collection that combines macroinvertebrate taxonomic abundance time series with multiple environmental covariates for 1,519 English river sites (1965–2018). Includes 41 water quality determinands, daily/derived river flow metrics, air temperature, habitat and land-cover descriptors, and static site descriptors. Developed under the ChemPop project to enable analyses of chemical exposures on freshwater wildlife and provided as an open data product while acknowledging some licensing restrictions on certain water quality data.

- Aims for data stewardship: deliver a usable, well-documented, machine-readable resource that supports discovery, reuse, and governance of large environmental datasets; provide provenance, processing steps, and quality checks to enable robust downstream analysis.

## Data scope and structure

- Temporal and spatial coverage
  - Macroinvertebrate observations across 1,519 sites in England, 1965–2018.
  - Associated covariates include water quality (41 determinands), river flow, air temperature, habitat quality indicators, and land-cover data upstream of each site.
  - Static site descriptors include altitude, slope, distance from source, discharge, width, depth, and substrate type.

- Data products and file organization (regionally split)
  - Macroinvertebrate taxon abundance: CP_<REGION>_MInv_taxonAbundance_<startDate-endDate>.csv
  - Macroinvertebrate site descriptors: CP_<REGION>_MInv_siteVariables.csv
  - Water quality statistics for each determinand: CP_<REGION>_MInv_<determinandLabel>Stats_<startDate-endDate>.csv
  - River flow statistics: CP_<REGION>_MInv_riverFlowStats_<startDate-endDate>.csv
  - Air temperature statistics: CP_<REGION>_MInv_airTempStats_<startDate-endDate>.csv
  - Habitat quality indices linked to macroinvertebrate sites: included in site descriptor files
  - Matched site locations (for macrosite–WQ/RF/RHS pairing): CP_<REGION>_MInv_siteMatchedLocation.csv

- Data provenance and sources (summary)
  - Macroinvertebrates: Environment Agency Biosys freshwa ter macroinvertebrate surveys (FRMS).
  - Water quality: Environment Agency Water Quality Data Archive (and pre-2000 licensed EA data with QA caveats).
  - River flow: National River Flow Archive (NRFA) via Gauged Daily Flow data.
  - Air temperature: CHESS-met daily meteorology dataset (1961–2017).
  - Wastewater influence: LF2000-WQX modelled effluent dilution factor (EDF).
  - Habitat: River Habitat Survey (RHS) indices (HMS, HMS_Class, RSB_SubScore, HQA, HQA_ADJ).
  - Land cover: Land Cover Map 2015 (LCM2015), upstream catchment summaries.
  - Catchment and river network context: Integrated Hydrological Digital Terrain Model (IHDTM) and UKCEH digital river network.

## Data processing, integration, and quality assurance

- Data integration approach
  - Spatial matching: pair macroinvertebrate sampling locations with the nearest water quality, river flow, and RHS survey sites along the river network (distance along network).
  - Spatial integration: extract model/analysis-based variables (EDF, land cover, air temperature) at macroinvertebrate site locations.
  - Temporal matching: align time-series data (water quality, river flow, air temperature) to the 6 months preceding each macroinvertebrate sampling date; habitat and land-cover variables treated as static site descriptors.

- Key processing steps by data type
  - FRMS macroinvertebrate data cleaning
    - Remove duplicates, fix site IDs, standardize taxon names to Davies & Edwards (2011) reference; resolve taxonomic synonyms; convert abundance to consistent numeric values; remove zero-abundance taxa; export cleaned CSVs.
  - EDF modelling and extraction
    - Use LF2000-WQX to estimate percent wastewater with a conservative 100 mg/L placeholder for a network of wastewater treatment works; store EDF (mean, SD, 90th/95th percentiles) per site.
    - Associate EDF values with macroinvertebrate sites via nearest reach on the truncated river network; flag discrepancies with NA where applicable.
  - Water quality
    - Pre-2000 data sourced from EA licensed database; post-2000 data from Water Quality Archive.
    - Matching water quality sites to macroinvertebrate sites via River IRN extension; manual checks to ensure same river, no intervening wastewater works, and no major tributaries between sites.
    - Statistics (6-month window before macroinvertebrate date) calculated for 41 determinands; three LoQ treatments applied for values below LoQ (LoQ, 0, LoQ/2); upper-limit values used as reported. Outputs include min, max, median, mean, std and sample counts.
  - River flow
    - Nearest gauging station to each macroinvertebrate site; require less than 50% missing data across the period 20/05/1974–29/03/2019.
    - Statistics for period of interest and 6-month pre-sample window: mean, median, std, coefficient of variation, Q5/mean, Q95/mean; 6-month indicators (thresholds, exceedances, patch length) following Indicators of Hydrologic Alteration (Richter et al., 1996).
  - Air temperature
    - CHESS-met daily mean air temperature extracted for macroinvertebrate sites; 6-month statistics (mean, median, min, max, std) computed; CHESS-met ends 2017, so post-2017 data not available.
  - Habitat quality
    - RHS indices (HMS, HMS_Class, RSB_SubScore, HQA, HQA_ADJ) extracted for RHS sites within 5 km of macroinvertebrate sites; RHS provides a single measurement per site (72 sites have multiple RHS surveys; included in a separate file).
  - Land cover
    - LCM2015 processed to determine upstream catchment composition (woodland, arable, seminatural, urban); 50 m grid, flow-direction alignment, and IHDTM-based catchment delineation; validated to ensure totals sum to 100% up to small rounding differences.
  - Data quality checks
    - Distance-based matching threshold checks (<1 km for site–IHDTM cell proximity); checks that land-cover categories upstream sum to ~100%; documentation of NA values and data gaps.

## Variables, descriptors, and file contents

- Site descriptors (CP_<REGION>_MInv_siteVariables.csv)
  - Core fields include BIO_SITE_ID, altitude, slope, distance from source, discharge category, width, depth, substrate covers, EDF mean, and related land-cover indicators upstream.
  - Inline metadata describing units and data sources for each column.

- Macroinvertebrate abundance (CP_<REGION>_MInv_taxonAbundance_<startDate-endDate>.csv)
  - BIO_SITE_ID, BIO_SAMPLE_ID, BIO_SAMPLE_DATE, BIO_SPGRP_NAME (taxon name), BIO_FAM_NAME, BIO_ORD_NAME, BIO_ABUNDANCE, analysis metadata, and related fields.

- Water quality statistics (CP_<REGION>_MInv_<determinandLabel>Stats_<startDate-endDate>.csv)
  - Includes BIO_SITE_ID, BIO_SAMPLE_DATE, determinand-specific aggregates (WQ_MIN_LOQ1/2/3, WQ_MAX_LOQ1/2/3, WQ_MEDIAN_LOQ1/2/3, WQ_MEAN_LOQ1/2/3, WQ_STD_LOQ1/2/3, WQ_COUNT, WQ_COUNT_L_LOQ, WQ_COUNT_G_LOQ), plus LoQ handling configuration.
  - Determinand labels correspond to table A.1 (41 determinands with units and codes).

- River flow statistics (CP_<REGION>_MInv_riverFlowStats_<startDate-endDate>.csv)
  - BIO_SITE_ID, BIO_SAMPLE_DATE, RF_MEAN_POI, RF_Q50_POI, RF_STD_POI, RF_COV_POI, RF_Q5/95_MEAN_POI, and related quantile-based metrics for both period of interest and 6-month preceding the sample date.

- Air temperature statistics (CP_<REGION>_MInv_airTempStats_<startDate-endDate>.csv)
  - BIO_SITE_ID, BIO_SAMPLE_DATE, TAS_MIN, TAS_MAX, TAS_MEAN, TAS_MEDIAN, TAS_STD, etc.

- Site location matches (CP_<REGION>_MInv_siteMatchedLocation.csv)
  - BIO_SITE_ID, catchment name, water body, coordinates (Easting/Northing), and matched water quality and river flow site identifiers where applicable.

- Data accessibility notes
  - Data sources include EA, NRFA, CHESS-met, LCM2015, IHDTM; licensing restrictions apply to certain water quality data, which are documented in discrepancy appendices. The dataset is deposited and accessible via the UKCEH/EIDC framework and associated data portals.

## Limitations, caveats, and data quality considerations

- Data gaps and completeness
  - Final product contains gaps (noData) in many variables due to non-availability of matching records at required spatio-temporal resolutions.
  - Some water quality data pre-2000 are licensed and not publicly available; some macroinvertebrate–water quality matches lack data due to extraction/licensing issues.
  - Land cover is treated as static because of historical variations between map products and resource demands for full temporal harmonization.

- Methodological considerations
  - EDF values rely on an upstream headwater representation; 0 EDF may reflect catchments with minor or unmodeled WWTWs and is not always a true zero.
  - Water quality matching used stringent criteria (same water body, no intervening STWs, no major tributaries) to identify the best match; some regions/sites may have non-ideal matches.
  - CHESS-met data ends in 2017; post-2017 air temperature values are not available for macroinvertebrate dates after that.
  - RHS habitat indices are cross-sectional; a small subset of sites have multiple RHS surveys (documented in an additional file).

- Data handling decisions
  - LoQ treatment options for below-LoQ values (LoQ, 0, LoQ/2) are documented and applied per determindant in the water quality statistics files.
  - Upper-bound (above measurement range) values are used as reported.
  - Spatial matching along the river network uses distance along the network with manual QA checks to avoid cross-catchment misjoins.

## Practical guidance for Data Stewards and users

- Documentation and reproducibility
  - Follow the methodological sections and appendices to understand data lineage, matching criteria, and processing steps.
  - Use the regional files and start-end date stamps to align data across variables for analysis pipelines.

- Data quality and governance
  - Be aware of licensing restrictions affecting some water quality data; reference Table A.1 and Appendix 3 for site-level exclusions.
  - Handle NA values explicitly when loading CSVs (the data use 'NA' to denote missing values; ensure proper dtype handling in your tooling).
  - Where LoQ handling choices exist, consistently apply the chosen configuration across analyses or explicit documentation of the chosen approach per determinand.

- Use cases and applications
  - Long-term ecological and environmental trend analyses linking macroinvertebrate communities to water chemistry, hydrology, temperature, habitat quality, and land-use context.
  - Modelling chemical exposure effects on freshwater biota, with covariates to account for flow regime, wastewater influences, and habitat alterations.
  - Cross-regional comparisons and prioritization of sites for monitoring or conservation actions, leveraging the standardized metadata and region-specific outputs.

- Access and attribution
  - Acknowledge data sources (EA, NRFA, CHESS-met, LCM2015, RHS, IHDTM) and the ChemPop project funding and data deposit arrangements; follow specified citations and acknowledgments as described in the data product documentation.