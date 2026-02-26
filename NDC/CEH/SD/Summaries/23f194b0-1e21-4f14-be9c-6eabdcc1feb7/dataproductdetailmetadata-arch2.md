# Macroinvertebrate taxonomic abundance, water quality, river flow, air temperature and environmental site descriptors from English rivers, 1965 - 2018

- A comprehensive open data product linking macroinvertebrate taxonomic abundance with water quality, river flow, air temperature and static environmental site descriptors across English rivers from 1965 to 2018.
- Coverage: 1,519 macroinvertebrate monitoring sites with time-series data (1965–2018), plus associated water quality measurements (41 determinands), river flow, air temperature and static site descriptors.
- Purpose: Developed under the ChemPop project to investigate whether chemical exposure affects wildlife populations in rivers; intended as a reusable resource for environmental data analyses and modelling.

## What this dataset contains

- Macroinvertebrate abundance time series for 1,519 sites across England (1965–2018).
- Co-located data for each site:
  - 41 water quality determinands (determinands expressed with 6-month preceding period statistics).
  - Daily river flow data and derived flow statistics.
  - Estimated air temperature values (CHESS-met) paired to sampling dates.
  - Land cover in the upstream catchment (Land Cover Map 2015) and wastewater dilution factors (EDF) modeled with LF2000-WQX.
  - Static site descriptors: altitude, slope, distance from source, channel width, depth, substrate, and RHS-derived habitat indices (HMS, HMS_Class, RSB_SubScore, HQA, HQA_ADJ).
- File structure designed for region-based organisation (seven EA regions).

## Data sources and integration

- Data sources:
  - Freshwater macroinvertebrate surveys (EA Biosys FRMS) for abundance time series.
  - EA Water Quality Data Archive for 41 determinands (plus pre-2000 licensed EA data).
  - National River Flow Archive (NRFA) for river flow.
  - CHESS-met for estimated air temperature.
  - LF2000-WQX model for wastewater effluent dilution factor (EDF).
  - River Habitat Survey (RHS) for habitat indices.
  - Land Cover Map 2015 (LCM2015) for upstream land cover.
  - Integrated Hydrological Digital Terrain Model (IHDTM) and UKCEH river networks for spatial processing.
- Integration approach:
  - Spatial matching: pair macroinvertebrate sites with nearest water quality, river flow, and RHS data along the river network.
  - Spatial integration: extract model/analysis-generated variables (EDF, land cover, air temperature) at macroinvertebrate site locations.
  - Temporal matching: align time-series observations (water quality, river flow, air temperature) to the macroinvertebrate sampling date, using a 6-month window preceding the sample date.
- Processing and harmonisation:
  - FRMS data cleaned and taxonomic names standardised against a reference (Davies & Edwards 2011).
  - Macroinvertebrate abundance data recoded from semi-quantitative to fully quantified from 2002 onwards; outliers and improbable values addressed where feasible.
  - Land cover treated as static due to resource constraints; land cover and EDF integrated as site descriptors.

## Temporal and spatial matching details

- Spatial matching: nearest macroinvertebrate site to water quality, river flow and RHS sites along the river network; regional counts provided for BIO, WQ, RF, HS sites and pairings.
- Temporal matching: 6-month period before each macroinvertebrate sampling date used to compute statistics (min, max, median, mean, std) for water quality; air temperature statistics derived from CHESS-met for the same preceding period.
- EDF modeling and extraction:
  - EDF values derived from LF2000-WQX, representing the percentage of wastewater in river flow; includes mean, 90th and 95th percentile, and standard deviation.
  - EDF data are stored as site descriptors linked to macroinvertebrate sites.
- River flow statistics:
  - POI: 20/05/1974 – 29/03/2019; plus 6-month preceding each macroinvertebrate sample date.
  - Statistics include mean, median, std, coefficient of variation, Q5/mean, Q95/mean, and various exceedance metrics per the Indicator of Hydrologic Alteration framework.
- Air temperature:
  - Daily mean air temperature from CHESS-met (1961–2017) interpolated to site locations; statistics computed for the 6-month preceding sample date.
  - CHESS-met ends in 2017, so post-2017 air temperature data are not available for matching.

## Data files and structure

- Site descriptors (7 region-specific files):
  - CP_REGION_MInv_siteVariables.csv
  - Columns include BIO_SITE_ID, altitude, slope, distance from source, discharge, width, depth, substrate covers, EDF metrics, land cover percentages/area, and RHS-derived descriptors.
- Macroinvertebrate taxon abundance (7 region-specific files):
  - CP_REGION_MInv_taxonAbundance_<startDate-endDate>.csv
  - Columns include BIO_SITE_ID, BIO_SAMPLE_ID, BIO_SAMPLE_DATE, taxon names, and abundances.
- Water quality determinand statistics (41 determinands; region-specific files):
  - CP_REGION_MInv_<determinandLabel>Stats_<startDate-endDate>.csv
  - Includes WQ_MIN_LOQ1/2/3, WQ_MAX_LOQ1/2/3, WQ_MEDIAN_LOQ1/2/3, WQ_MEAN_LOQ1/2/3, WQ_STD_LOQ1/2/3, WQ_COUNT, WQ_COUNT_LOQ breakdowns, etc.
- River flow statistics (region-specific files):
  - CP_REGION_MInv_riverFlowStats_<startDate-endDate>.csv
- Air temperature statistics (region-specific files):
  - CP_REGION_MInv_airTempStats_<startDate-endDate>.csv
- Site matched locations (region-specific files):
  - CP_REGION_MInv_siteMatchedLocation.csv
- Additional RHS and land-cover related files are described (e.g., SiteswithmultipleRHSsurveys.csv).

## Data quality, gaps and cautions

- Gaps and exclusions:
  - Some macroinvertebrate sites lack matched water quality data due to licensing restrictions (A.3.1) or have matched water quality sites but data extraction failed (A.3.2).
  - Pre-2000 water quality data sourced from EA licensed database; not as comprehensively quality assured as Water Quality Archive data.
- Temporal limitations:
  - CHESS-met ends 2017; no CHESS-met data beyond that date for air temperature.
  - Land Cover Map 2015 treated as static; successive updates not included due to resource intensity.
- Data handling:
  - Values below LoQ handled using three configurations (LoQ1, LoQ2, LoQ3) for statistics.
  - Some determinands with values above upper measurement range used as reported.
  - NA coding used for missing data; guidance provided for parsing in Python/R.

## Usage context for Analysts Monitoring the Environment

- Enables long-term assessment of environmental health by linking biotic indicators (macroinvertebrates) with chemical, hydrological and climatic drivers.
- Useful for investigating chemical exposure effects on freshwater biota, trend detection, and policy performance assessment over multi-decadal scales.
- Provides harmonised, analysis-ready datasets with clear provenance and methodological documentation to support reproducible analyses.

## Accessibility and acknowledgment

- Data product is presented as an open data output from the ChemPop project (NERC) with acknowledgment of EA, UKCEH, NRFA data and other contributing datasets.
- Documentation and data sources are referenced, with access details provided in the accompanying materials.