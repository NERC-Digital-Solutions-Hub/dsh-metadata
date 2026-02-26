# Dataset Originator ECN Data Centre (http://data.ecn.ac.uk - ecn@ceh.ac.uk), Centre for Ecology and Hydrology

## Overview
- ECN (Environmental Change Network) program aims to understand environmental change through standardized monitoring and network coordination.
- This document describes ECN data collected at Wytham deer exclosure plots, including coarse-grain vegetation (1993–2012) and woodland vegetation (1993–2014).
- Data are organized to support comparability across sites and years, with quality indicators and detailed metadata.

## Data Holdings and Structure
- Datasets
  - ECNWythamExclosures_species_present: presence/absence of plant species per 40 cm x 40 cm cell.
  - ECNWythamExclosures_tree_data: woodland measurements (e.g., diameter at breast height, height), seedling data, and related measures.
- Key fields
  - Species-present: SITECODE, SYEAR, PLOTPID, CELLID, FIELDNAME (VEG_SPEC or quality codes Q1–Q8), VALUE.
  - Woodland data: SITECODE, SYEAR, PLOTPID, CELLID, TREEID, STEMID, TREE_SPEC, FIELDNAME, VALUE.
- Data content
  - Spatial: plots subdivided into 25 cells per plot; species presence per cell; tree/seedling measurements at tree level.
  - Temporal: multi-year coverage (1993–2014 for woodland; up to 2012 for coarse-grain vegetation).

## Supporting Documentation and Metadata
- Data downloads
  - ECNWythamExclosures_species_present
  - ECNWythamExclosures_tree_data
- Supporting documentation files
  - ECNWythamExclosures_plot_info.csv
  - ECN_VF2.csv (plot-level information)
  - ECNWythamExclosures_cell_info.csv
  - ECNWythamExclosures_quality_info.csv
  - ECN_VF_qtext.csv (quality text for non-standard notes)
- Explanatory context
  - Site codes (e.g., T08 = Wytham) and plot descriptions
  - Species codes crosswalks (VESPAN to BRC concepts; Latin names and synonyms)

## Variables and Codes
- Species codes
  - ECN uses VESPAN species codes with crosswalks to Biological Records Centre (BRC) concepts; extensive mappings provided to link Latin names to codes.
- Quality codes
  - Site managers assign quality codes (Q1, Q2, etc.) describing data quality factors.
  - A supplementary qtext file provides textual descriptions for non-standard notes (e.g., code 999 for unusual events).

## Site Information
- Example site: Wytham (Site Code T08)
  - Location coordinates: 51°46'52.86"N, 1°20'9.81"W
- Additional ECN site information available via ECN catalog

## Usage Guidance for Analysts
- Data quality and reproducibility
  - Protocols ensure comparability across plots/years; refer to accompanying documentation for collection details.
  - Interpret quality codes with the quality_info file and qtext descriptions; acknowledge quality codes in analyses.
- Data access, attribution, and provenance
  - Acknowledge ECN data usage; cite Rennie et al. for coarse-grain vegetation data (1993–2012) and woodland data where applicable.
- Data integration and analysis
  - Datasets are designed for identifying species presence per cell and for detailed tree/seedling measurements.
  - Join across plots, cells, and trees using SITECODE, SYEAR, PLOTPID, and CELLID; use TREEID/STEMID for tree-level records.
  - Metadata and quality flags enable robust correlation analyses and modeling at plot and cell scales.

## Practical Notes for Correlation and Modeling
- Spatial granularity and scope
  - Coarse-grain vegetation data organized into 25 cells per plot within deer exclosures or control plots.
- Temporal coverage
  - Woodland data span 1993–2014; coarse-grain data span 1993–2012.
- Data interoperability
  - Datasets can be merged across plots, cells, and trees via SITECODE, SYEAR, PLOTPID, CELLID; tree-level data use TREEID/STEMID for linkage.
- Accessibility and metadata handling
  - Datasets include metadata and quality flags; consult ECN_VF_qtext.csv for non-standard notes and ensure correct interpretation of quality codes.

## Species Codes Crosswalk (Explanatory Information)
- The document includes extensive mapping of species codes to Latin names and synonyms (e.g., Schistidium strictum and related cross-references to Scirpus, Sedum, Senecio, etc.).
- This crosswalk supports accurate species identification and data integration with external taxonomic references.

## Quality Codes (Explanatory Information)
- A comprehensive list of field- and lab-related quality codes with descriptions and example scenarios (e.g., No information, partial loss, contamination, equipment failure, etc.).
- A dedicated 999 code flags unusual events, with accompanying textual notes in qtext.

## Citations and Acknowledgments
- Usage guidance encourages citing Rennie et al. for UK ECN coarse-grain vegetation data (1993–2012) and Rennie et al. (2017) for woodland data where applicable.