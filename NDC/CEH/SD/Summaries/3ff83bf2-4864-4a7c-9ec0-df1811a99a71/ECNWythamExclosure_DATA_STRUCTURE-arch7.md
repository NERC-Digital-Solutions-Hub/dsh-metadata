# ECN Wytham Exclosures vegetation data

## Overview
- Source and purpose: map-ready vegetation data from ECN Wytham deer exclosure plots, enabling GIS-based analysis of spatial vegetation patterns and temporal change. Data are produced under ECN protocols to ensure comparability across sites and years.
- Timeframe and scope: coarse-grain vegetation data (1993–2012) and woodland vegetation data (1993–2014); plots 501–509 are exclosures (paired with control plots elsewhere).
- Spatial context: dataset organized by ECN site, plot, and grid cell (40 cm x 40 cm); supports per-cell presence/absence visualization and multi-year change detection.
- Access and citation: data should be acknowledged as ECN datasets; cite Rennie et al. 2016 (coarse-grain) and Rennie et al. 2017 (woodland).

## Data products
- ECNWythamExclosures_species_present
  - Core fields: SITECODE, SYEAR, PLOTPID, CELLID, FIELDNAME (e.g., VEG_SPEC or quality code), VALUE (species code or quality code)
- ECNWythamExclosures_tree_data
  - Core fields: SITECODE, SYEAR, PLOTPID, CELLID, TREEID, STEMID, TREE_SPEC, FIELDNAME, VALUE
- Supporting documentation and metadata
  - ECN_VF2.csv (plot information)
  - ECN_VF3.csv (cell information)
  - ECN_VF_qtext.csv (quality text and context)
- Site and coding context
  - Site codes (e.g., T08 = Wytham) with coordinates
  - Extensive species-code mappings (VESPAN and BRC crosswalks) and ECN quality codes

## Data structure and fields
- Vegetation data
  - Presence/absence data: coarse-grain species presence across 25 cells per plot (25 cells per plot, 40 cm x 40 cm each)
  - Woodland data: tree measurements within cells (e.g., DBH, height, dominance, etc.) by tree
- Core field relationships
  - species_present: SITECODE, SYEAR, PLOTPID, CELLID, FIELDNAME, VALUE
  - tree_data: SITECODE, SYEAR, PLOTPID, CELLID, TREEID, STEMID, TREE_SPEC, FIELDNAME, VALUE
- Quality and context
  - Quality codes Q1–Q8 (and variants) describe data quality and collection factors
  - Free-text quality notes linked via ECN_VF_qtext.csv

## Metadata, codes, and crosswalks
- Species codes and mappings
  - Extensive mappings linking numeric species codes to Latin names and cross-references to BRC concepts
  - Includes crosswalks to taxonomic concepts and synonyms; supports translation of FIELDNAME VALUE codes to scientific names
- Quality codes
  - Codes 100–999 with descriptions (e.g., 100 No information available; 201 Failing light affected sampling; 143 Grazing by deer; 237 Tree dead; 999 Unusual event)
  - Used to assess data reliability and to filter or annotate GIS layers
- Data standards
  - ECN protocol alignment ensures comparability across sites and years
  - Crosswalks and supporting docs aid interpretation and integration with other ECN datasets

## GIS workflow and usage
- Data preparation
  - Retrieve ECNWythamExclosures_species_present and ECNWythamExclosures_tree_data with supporting files ECN_VF2.csv, ECN_VF3.csv, ECN_VF_qtext.csv
  - Join datasets by SITECODE, SYEAR, PLOTPID, and CELLID to create spatial layers
- Attribute mapping
  - Map VALUE from FIELDNAME to species codes or quality codes
  - Use species crosswalks to translate codes to Latin names and taxonomic concepts
  - Apply quality codes to filter or annotate data (e.g., exclude low-quality observations or flag uncertainties)
- Spatial integration
  - Combine with plot and cell metadata from ECN_VF2.csv and ECN_VF3.csv
  - Create per-site, per-plot, per-cell layers for species presence and woodland structure
- Temporal analysis
  - Leverage multi-year data to analyze trends, exclosure vs. control comparisons, and temporal vegetation changes
- Outputs and visualization
  - Map-based visualization of species presence/absence, canopy composition, and tree metrics
  - Time-series maps and change-detection analyses across years

## Practical considerations
- Data scale and performance
  - Large, multi-year, cell-level datasets; plan for efficient joins and indexing
- Data quality and uncertainty
  - Use quality codes and quality text to assess reliability; document data gaps
- Standards and attribution
  - Acknowledge ECN datasets in reuse; cite Rennie et al. 2016 and 2017 as relevant data products
- Reuse guidance
  - Combine with ECN_VF2/3 metadata for spatial context; consult ECN quality information for each dataset

## Access, attribution, and next steps
- Access: obtain ECNWythamExclosures_species_present, ECNWythamExclosures_tree_data, plus ECN_VF2.csv, ECN_VF3.csv, and ECN_VF_qtext.csv
- Next steps for GIS workflows
  - Use SITECODE (e.g., T08) and plot/grid identifiers to create spatial layers
  - Link FIELDNAME and VALUE to species codes or quality codes via crosswalks
  - Integrate with site and cell metadata to produce informative map products
- References for methodological context
  - Rennie et al. 2016 (coarse-grain vegetation data)
  - Rennie et al. 2017 (woodland vegetation data)