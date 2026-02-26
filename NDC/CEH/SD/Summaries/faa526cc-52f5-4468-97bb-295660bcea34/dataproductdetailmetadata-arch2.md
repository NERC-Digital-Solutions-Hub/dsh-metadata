# Macroinvertebrate taxonomic abundance, water quality, river flow, air temperature and environmental site descriptors from English rivers, 1965 - 2018

- A consolidated open data product combining long-term macroinvertebrate abundance (1,519 sites, 1965–2018) with 41 water quality determinands, river flow, air temperature and static environmental site descriptors.
- Developed under the ChemPop project (NERC-funded, 2018–2022+) to investigate chemical exposure effects on freshwater wildlife; intended for community use and modelling analyses.
- Data assembled from multiple sources (Environment Agency, UKCEH, NRFA, CHESS-met) and harmonised for spatial and temporal analysis across England.

## Aim and audience

- Purpose: present environmental health and policy performance over time using a consistent, analysis-ready dataset.
- Target users: analysts monitoring environmental health, policy evaluators, modelers seeking integrated environmental covariates alongside macroinvertebrate indicators.
- Outputs emphasize standardized formats (CSV files, region-specific datasets) to facilitate scrutiny and reuse.

## Data scope and contents

- Macroinvertebrate data
  - Observations from 1,519 sites across England (1965–2018).
  - Taxa abundances recorded (ranked from historical semi-quantitative to fully quantitative post-2002; harmonised to standard naming).
  - Site descriptors include altitude, slope, distance from source, discharge, width, depth, substrate type.
- Water quality data
  - 41 determinands from the EA Water Quality Data Archive (2000 onwards; some pre-2000 data from EA licensed database).
  - Statistics computed for the 6-month period preceding each macroinvertebrate sampling date.
  - Data handling for below-LoQ values (three configurations) and for values above upper quantification limits.
- River flow data
  - Daily mean river flow from NRFA gauging stations; linked to macroinvertebrate sites by nearest river-network distance.
  - POI statistics (20/05/1974–29/03/2019) and 6-month preceding each sampling date.
  - Metrics include mean, median, std, coefficient of variation, Q5/mean, Q95/mean, and hydrologic alteration indicators (from Richter et al.).
- Air temperature
  - Daily mean air temperature from CHESS-met (1961–2017) at 1 km resolution; linked to sites via grid cells.
  - 6-month preceding statistics for each macroinvertebrate sampling date.
  - CHESS-met time series end date means temperature data beyond 2017 are not available for matching.
- Habitat quality (RHS)
  - River Habitat Survey metrics: Habitat Modification Score (HMS), HMS Class, RSB SubScore, Habitat Quality Assessment (HQA) and adjusted HQA (HQA_ADJ).
  - RHS site selections: nearest RHS site within 5 km of macroinvertebrate site; RHS is a single-visit dataset (72 sites with multiple RHS surveys included in a separate file).
- Land cover upstream (LC)
  - Land Cover Map 2015 (LCM2015) processed to obtain upstream woodland, arable, seminatural and urban percentages and areas.
  - Catchment-scale upstream results derived using IHDTM flow accumulation; all macroinvertebrate sites have matching land cover data.
- Additional site descriptors
  - Land cover upstream areas, catchment areas, and various physical site descriptors (altitude, slope, distance from source, width, depth, substrate).

## Data sources and integration workflow

- Data sources
  - Macroinvertebrate abundance and site parameters: EA Freshwater river macroinvertebrate surveys (Biosys).
  - Water quality: EA Water Quality Archive; pre-2000 data from EA licensed database.
  - River flow: NRFA Gauged Daily Flow data.
  - Air temperature: CHESS-met (GB).
  - Wastewater exposure: LF2000-WQX model (EDF – effluent dilution factor).
  - Habitat: River Habitat Survey (RHS) details and summaries.
  - Land cover: Land Cover Map 2015 (LCM2015).
  - River network, IHDTM grids, and 1:50k river network data for spatial processing.
- Integration approach
  - Spatial matching: nearest-neighbor pairing along the river network between macroinvertebrate sites and water quality, flow, and RHS sites.
  - Spatial integration: extraction of model/analytical variables (EDF, land cover, air temperature) at macroinvertebrate site locations.
  - Temporal matching: align water quality, flow, and temperature time series to the 6-month window before each macroinvertebrate sampling date; RHS and land cover treated as static site descriptors.
- Data processing and harmonisation
  - FRMS data cleaning included duplicate removal, ID harmonisation, taxonomic name reconciliation against Davies & Edwards (2011), and outlier handling.
  - Taxon abundance conversions from historical categories to numeric counts where possible.
  - EDF mapping used LF2000-WQX to estimate percentage wastewater for each site; potential 0 EDF in headwaters may reflect model limitations rather than true absence.

## Outputs and file structure

- Macroinvertebrate abundance files
  - CP_<REGION>_MInv_taxonAbundance_<startDate-endDate>.csv (7 region files)
- Water quality statistics
  - CP_<REGION>_MInv_<determinandLabel>Stats_<startDate-endDate>.csv (41 determinands, 287 files)
- River flow statistics
  - CP_<REGION>_MInv_riverFlowStats_<startDate-endDate>.csv (7 region files)
- Air temperature statistics
  - CP_<REGION>_MInv_airTempStats_<startDate-endDate>.csv (7 region files)
- Habitat and land cover site descriptors
  - CP_<REGION>_MInv_siteVariables.csv (site descriptors including EDF, land cover, RHS indices)
- Site locations and matched data
  - CP_<REGION>_MInv_siteMatchedLocation.csv
  - WQ_SITE, RF_SITE, HS_SITE identifiers and coordinates for matched sites
- Additional RHS data and multiple RHS surveys (if applicable)
  - SiteswithmultipleRHSsurveys.csv
- Appendix materials (descriptions, maps, and heatmaps) accompanying the data product

## Quality, gaps, and caveats

- Gaps and data completeness
  - final output contains gaps (noData) for many variables due to non-standardisation and temporal/spatial mismatches.
  - Some macroinvertebrate sites lack matched water quality data due to EA licensing restrictions; a few matched water quality sites have no available chemistry data due to extraction failures.
  CHESS-met ends in 2017, so post-2017 temperature values aren’t available for matching.
  Land cover is treated as a static variable (LCM2015) due to the resource intensity of integrating successive land cover products.
- Data quality and harmonisation
  - Ongoing taxonomic name harmonisation against Davies & Edwards (2011); some EA names retained if not previously encountered in UKCEH projects.
  - Water quality data handling includes LoQ treatment options and decision rules for outliers and censored data.
  - River flow statistics rely on nearest gauging station along the river network with limited missing data (less than 50% missing during the POI).
- Utility and scope
  - Intended as an analysis-ready, community-open data product enabling research into chemical exposure effects and environmental drivers of macroinvertebrate communities, while acknowledging limitations in cross-dataset standardisation and temporal coverage.

## Accessibility and usage

- Data accessible as a comprehensive, open data product deposited for long-term use (ChemPop/UKCEH data infrastructure) with clear metadata, data sources, and methodological documentation.
- Documentation provides guidance on data sources, integration methodology, variable definitions, and file structures to support reproducible analysis.
- Users should reference the data product’s accompanying methodological sections and appendices for dataset suitability, interpretation of LoQ handling, EDF limitations, and regional matching nuances.

## Relevance for environmental monitoring and policy evaluation

- Delivers a harmonised, multi-factor dataset enabling assessment of environmental health over more than five decades, combining biological indicators with chemical, hydrological, climatic and habitat context.
- Supports policy performance evaluation by enabling analyses of chemical exposure links to macroinvertebrate communities, and by providing standardized time windows and regionally consistent outputs.
- Encourages data integration and re-use by providing underlying data links and a framework for extending analyses with additional datasets.