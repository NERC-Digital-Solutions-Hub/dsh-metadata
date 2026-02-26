# Macroinvertebrate taxonomic abundance, water quality, river flow, air temperature and environmental site descriptors from English rivers, 1965 - 2018

- Comprehensive, open data product integrating long-term macroinvertebrate surveys with environmental covariates across England (1965–2018) to enable analyses of chemical exposure and other drivers of freshwater biodiversity.
- Built to support environmental monitoring frameworks by providing dataset provenance, harmonised variables, and analytics-ready formats for policy scrutiny and decision-making.

## Purpose and scope

- Aim: Identify environmental health measures to scrutinise and evaluate policy and inform future decisions.
- Target users: Managers in government or quangos responsible for designing and implementing monitoring strategies.
- Coverage: 1,519 macroinvertebrate monitoring sites; 41 water-quality determinands; river flow; daily air temperature-derived values; static site descriptors (e.g., land cover upstream, habitat quality, wastewater dilution factor).

## Data foundations and sources

- Macroinvertebrate abundance: 1965–2018 at 1,519 England river sites; sourced from Environment Agency Biosys freshwater macroinvertebrate surveys (FRMS).
- Water quality: 41 chemicals measured at matching sites; drawn from the Environment Agency Water Quality Archive (with pre-2000 licensed EA data) and, for 2000 onward, Water Quality Archive records.
- River flow: Daily mean river flow from NRFA (UK National River Flow Archive), paired to macroinvertebrate sites with limited missing data.
- Air temperature: Daily mean temperature from CHESS-met (Great Britain, 1961–2017); extracts temperature time series for each macroinvertebrate site.
- Habitat and land cover: 
  - River Habitat Survey (RHS) indices for habitat quality and modification (HMS, HMS_Class, RSB_SubScore, HQA, HQA_ADJ).
  - Land Cover Map 2015 (LCM2015) upstream catchment percentages and areas for woodland, arable, seminatural, and urban classes.
- Additional site descriptors: static variables such as altitude, slope, distance from source, channel width/depth, substrate, catchment name, water body, and coordinates.
- Wastewater exposure proxy: EDF (effluent dilution factor) derived from LF2000-WQX model, representing wastewater proportion in river flow at each site.

## Data processing and integration

- Harmonisation approach:
  - Spatial matching: pair macroinvertebrate sampling sites with nearby water-quality, river-flow, and RHS sites along the river network; distance along the river network used for matching.
  - Spatial integration: extract modelled/derived variables (EDF, land cover, air temperature) at macroinvertebrate site locations.
  - Temporal matching: align time-series data (water quality, river flow, air temperature) to the 6-month window preceding each macroinvertebrate sampling date; compute descriptive statistics (mean, median, min, max, SD).
- Data cleaning:
  - FRMS data cleaned in MS Access; standardised taxon names against a reference taxonomy; resolved duplications, missing data, and invalid abundances; linked analyses to site and sampling date.
  - Water quality: selection of best nearby sites with reliable proximity, absence of upstream wastewater influence, and adequate data density; LoQ handling strategies (LoQ as LoQ, 0, or LoQ/2) applied for values below detection limits.
  - River flow: nearest gauging station along the network; ensured data completeness (less than 50% missing) for the period of interest.
  - CHESS-met: extracted daily mean temperatures from grid cells covering macroinvertebrate sites; temperature stats computed for 6-month windows; CHESS-met ends in 2017, limiting post-2017 temperature matching.
- Methodological workflow: described step-by-step with a focus on reproducibility; Figure 1 and related workflow illustrate variable pairing and six-month aggregation windows.

## Data products and file structure

- Macroinvertebrate site descriptors (1519 sites):
  - CP_<REGION>_MInv_siteVariables.csv
  - Variables include: BIO_SITE_ID, BIO_ALTITUDE, BIO_SLOPE, BIO_DIST_FROM_SOURCE, BIO_DISCHARGE, BIO_WIDTH, BIO_DEPTH, substrate coverings, EDF means, and land-cover metrics (LC_WOODLAND_PER, LC_ARABLE_PER, LC_SEMINATURAL_PER, LC_URBAN_PER, and areas).
- Macroinvertebrate taxon abundance (per region; time range 1965–2018):
  - CP_<REGION>_MInv_taxonAbundance_<startDate-endDate>.csv
  - Columns cover BIO_SITE_ID, BIO_SAMPLE_ID, BIO_SAMPLE_DATE, BIO_FAM_NAME, BIO_SPGRP_NAME, BIO_ABUNDANCE, etc.
- Water quality statistics (41 determinands; per region):
  - CP_<REGION>_MInv_<determinandLabel>Stats_<startDate-endDate>.csv
  - Statistics for 6-month windows preceding macroinvertebrate sampling; LoQ treatment options codified (LoQ1/LoQ2/LoQ3).
- River flow statistics (per region):
  - CP_<REGION>_MInv_riverFlowStats_<startDate-endDate>.csv
  - Includes means, quartiles, and other hydrological metrics for the period of interest and preceding 6 months.
- Air temperature statistics (per region):
  - CP_<REGION>_MInv_airTempStats_<startDate-endDate>.csv
  - Includes TAS_MIN, TAS_MAX, TAS_MEAN, TAS_STD, etc., for 6-month windows.
- Habitat quality site descriptors (RHS-derived):
  - Included as site descriptors; RHS data linked to macroinvertebrate sites; additional file SiteswithmultipleRHSsurveys.csv captures multiple RHS measurements for a subset of sites.
- Water quality and river flow site matches:
  - CP_<REGION>_MInv_siteMatchedLocation.csv
  - Provides coordinates and matching identifiers for paired WQ, RF, RHS, and macroinvertebrate sites.
- Data completeness and caveats:
  - Some macroinvertebrate sites lack water-quality matches due to licensing restrictions (A.3.1) or failed extraction (A.3.2).
  - Data are provided with NA values to denote missing data; handling guidance provided in the accompanying note (Appendix 5).

## Methodological notes and quality assurance

- Taxonomic aspects:
  - Historic EA data used mixed taxonomic resolution (family level pre-2002; semi-quantitative counts earlier; full quantification after 2002); adjustments made to align data with standardized taxonomy (Davies & Edwards 2011 reference).
- Data quality controls:
  - Rigorous linking of FRMS with WQ, RF, RHS, and CHESS-met data; cross-checking of site IDs, date stamps, and taxon names.
  - Outlier handling and QA measures described; 0s and <LoQ values addressed via explicit rules.
- EDF model considerations:
  - LF2000-WQX uses a conservative approach (no in-stream losses) with 100 mg/L fixed representative concentration; only significant wastewater treatment works (WWTWs) included to represent catchment contributions; headwater exclusions acknowledged.
  - EDF values can be NA where truncated network vs. full river network alignment yields discrepancies.
- Land cover processing:
  - LCM2015 processed with IHDTM flow accumulation; 50 m grid resolution; catchment-level aggregation to water quality descriptors; validation shows cumulative land-cover percentages effectively sum to 100%.

## Practical considerations for monitoring frameworks

- Data coverage and gaps:
  - Long-running, consistent macroinvertebrate time series enable trend analyses; however, post-2017 temperature data gaps and some missing WQ data constrain certain analyses.
  - Licensing restrictions may limit use of some water-quality sites; not all sites have complete covariate coverage.
- Temporal alignment:
  - Six-month aggregation window prior to macroinvertebrate sampling date aligns biological responses with exposure metrics.
- Data governance and openness:
  - Outputs are designed as openly usable data products; metadata, provenance, and data-use notes are embedded to support governance and reproducibility.
- Intended use:
  - Suitable for modelling environmental health indicators, evaluating regulatory scenarios (e.g., chemical exposure, hydrological changes), and informing future monitoring strategies and policy decisions.

## Accessibility and attribution

- Data sources include Environment Agency Biosys, EA Water Quality Archive, NRFA, CHESS-met, RHS, LCM2015, and IHDTM; modelled EDF data provided by LF2000-WQX.
- Acknowledgments emphasize institutional data providers (EA, UKCEH, NRFA) and project funding (ChemPop ERCITE, NE/NERC) with citations and dataset metadata included for transparency and reuse.

## Authorial and project context

- Development and validation: multi-disciplinary team including ecology, hydrology, GIS, and data science experts; aims aligned with monitoring framework development and data governance needs.
- Publication and deposit: data product presented as an open, analysis-ready resource with supporting methodological documentation and appendices detailing data sources, processing steps, and quality checks.