# Fish abundance, habitat, water quality, flow and climate in English rivers 1975-2017

- A comprehensive, open data product linking fish population data with habitat, water quality, flow, and climate covariates across 1180 English river sites, covering 1975–2017.
- Built from multiple sources with varying formats and purposes, requiring substantial integration and standardisation.
- Aims to support analyses of whether chemical releases affect wildlife populations and how such effects interact with other drivers.

## Data governance and stewardship considerations

- Data governance: harmonises disparate datasets (fish counts, habitat scores, water quality, land cover, temperature, flow, and climate indices) to create a usable, analysis-ready resource.
- Metadata and provenance: detailed documentation of data sources, processing steps, and variable definitions; clear attribution to data owners (Environment Agency, UKCEH, CHESS-MET, PML, NCAR, etc.).
- Data updates and maintenance: dataset curated by a multi-author team with explicit contributions; acknowledges open data aims and licensing constraints.
- Sharing limitations: some water quality data are restricted due to licensing, resulting in exclusions (33 fish sites) from the Water Quality Archive portion of the dataset.
- Usability safeguards: extensive quality checks, explicit handling rules for LoQ values, and standardized coding (ChemPop Species Codes, region-specific data tables).

## Data sources and provenance

- Primary fish data: Environment Agency National Fish Population Database (NFPD) for adult abundances; supplementary juvenile data excluded.
- Habitat data: River Habitat Survey (RHS) and HABSCORE for habitat modification and quality.
- Water quality: 41 determinands from UKEA Water Quality Archive; some data assembled from 1960–1999 internally and 2000–2017 via the EA archive.
- Hydrology and climate: LF2000-WQX model for effluent dilution factors (EDF); Base Flow Index (BFI); river flow stats from NRFA; water temperature via gauged stations and CHESS-Met air temperature; Gulf Stream Index (GSI) and North Atlantic Oscillation Index (NAOI).
- Land cover and terrain: Land Cover Map 2015; Integrated Hydrological Digital Terrain Model (IHDTM).
- Geospatial tools: ArcGIS, GRASS GIS, and DataLabs for data integration and extraction.

## Data integration and processing workflow

- Spatial and temporal matching:
  - Sites aligned along river networks; covariates matched to nearest sites within defined spatial relationships (e.g., 5 km RHS pairing, river network distances for WQ and EDF).
  - Temporal alignment to ecologically meaningful windows (e.g., covariates matched to the year prior to fish surveys; 3-, 6-, 12-month windows for flow).
- Data harmonisation:
  - Standardised fish densities (per 100 m2) from raw counts, accounting for sampling method differences (semi-quantitative vs first catch of quantitative surveys).
  - Conversion of habitat and land cover metrics into consistent site-based covariates (HQA, HMS, woodland/arable/urban percentages and areas).
- Modeling and proxies:
  - Water temperature time series generated with GAMMs across different BFIs; degree-days above 12°C computed for recruitment-relevant periods.
  - EDF (wastewater) estimated via LF2000-WQX to reflect 90% of catchment wastewater influence; results expressed as EDF_Mn, EDF_SD, EDF_Q90, EDF_Q95.
- Water quality determinants:
  - Nearest-neighbour matching to select up to three water quality determinand sites per fish site, with criteria to ensure reasonable hydrological relationships (e.g., proximity, upstream/downstream relative to wastewater sources).
  - Extraction of 41 determinands and computation of statistics (min, max, median, mean, SD) across antecedent periods, with LOQ handling rules and data-count metadata.
- Quality checks and data completeness:
  - Distances between sampling points and reference grid points validated; completeness heatmaps produced to show data availability by region/year.
  - Noted that altitude, land use, BFI, GSI, and NAOI are 100% complete for covariates; other covariates have gaps due to coverage and overlap limitations.

## Key datasets and structure

- Species and sites
  - CP_Fish_SpeciesTable.csv: unique fish species codes, Latin names, EA codes, common names.
  - CP_Fish_SiteVariables_region.csv: region-specific site metadata (identifiers, coordinates, habitat scores, altitude, land cover percentages/areas, BFI, EDF metrics).
  - CP_Fish_DataTable_region.csv: per-survey data, including survey date, location, species densities (per 100 m2), and habitat quality scores.
- Hydrology and climatology
  - CP_Fish_HydrologyStats_Region.csv: river flow statistics (mean, median, SD, CV, quantile-based metrics) and 3/6/12-month percentile thresholds and derived metrics for each NRFA station relative to survey dates.
  - Region_FISHWIMSStats_DET.csv: determinand-level water quality statistics and matching metadata.
- Water quality determinants and chemistry
  - 329 data tables covering 329 region-determinand combinations; each table includes WQ sampling metadata (WIMS point refs) and LOQ-handling configurations for 41 determinands (e.g., Lead, Mercury, Nitrate, Organo-halogen compounds, metals, organics, etc.).
  - Table A1 (appendix) provides determinand descriptions, units, and maximum thresholds where applicable.
  - Table A2 lists fish sites not extractable for water quality data due to licensing restrictions.
- Supplemental data and maps
  - Heatmaps and figures illustrating data completeness by year/region and spatial distribution of sites, RHS matches, HABSCORE data, water temperature stations, NRFA flow stations, and WQ determinand locations.

## Data quality, limitations, and exclusions

- Completeness: 100% complete for altitude, land use, BFI, GSI, and NAOI covariates; other covariates have varying coverage due to temporal overlap and site proximity constraints.
- Gaps and exclusions:
  - 33 fish sites excluded from water quality data due to licensing restrictions; no water quality data published for these sites.
  - Some RHS/HABSCORE match limitations; not all RHS sites could be paired with fish survey locations.
- Data resolution and interoperability:
  - Combining data from diverse sources required bespoke spatial linking along river networks and careful treatment of sampling methodologies; some residual heterogeneity remains due to original data purposes.
- Data usage caveats:
  - EDF reflects a modeled distribution of wastewater influence and may not capture all local nuances; smaller wastewater treatment works may be omitted if they contribute negligibly to 95% of catchment DWF.
  - Temperature modeling uses GAMMs and BFIs to account for groundwater influence; results are model-derived and subject to assumptions.

## Access, licensing, and usage guidance

- Access model: open data product with extensive documentation; however, some water quality components are restricted, limiting full public exposure to certain site-level data.
- Data provenance and attribution: dataset credits for all data sources; usage should acknowledge EA, UKCEH, CHESS-Met, PML, NCAR, and contributing authors.
- Practical use for data stewards:
  - Leverage the harmonised fish-habitat-water quality-flow-climate framework for governance, auditing of dataset lineage, and reproducible analyses.
  - Use the region-based file organization to manage region-specific updates or governance reviews.
  - Monitor licensing-restricted sites and track the impact on downstream analyses or replication attempts.
- Documentation and metadata:
  - Rich metadata accompanying each file, including data sources, processing steps, LoQ handling, and missing data codes (-9999 or NA equivalents) to ensure reproducibility and governance oversight.

## Authorship, governance, and acknowledgments

- Collaborative authorship spanning data curation, modeling, and project administration; explicit contribution notes for each author.
- Acknowledgments to funders (NERC) and data owners; explicit statements about licensing constraints and data rights.
- References and methodological background provided to support reproducibility and governance audits.

- This dataset is designed to enable robust, governance-friendly research into how chemical exposures and other drivers influence fish populations and river ecosystem function across England, with explicit metadata, provenance, and data quality controls to support data stewards in stewardship activities.