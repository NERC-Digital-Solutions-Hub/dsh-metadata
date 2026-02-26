# Dataset Originator ECN Data Centre (http://data.ecn.ac.uk - ecn@ceh.ac.uk), Centre for Ecology and Hydrology

## Overview
- ECN Vegetation data product from the UK Environmental Change Network (ECN) uses standardised protocols to enable cross-site comparability.
- Focuses on vegetation surveys and associated measurements (e.g., trees, shrubs, height, diameter, seedlings) within plots.
- Data collected across ECN sites with repeated measurements over time (coarse-grain surveys and tree-level details).

## Data structure and key mappings
- Main data file: ECN_VW2.csv
  - Key fields: SITECODE, SYEAR, PLOTPID, CELLID, TREEID (within cell), STEMID, TREE_SPEC, FIELDNAME, VALUE.
- Supporting documentation: ECN_VW2.csv
  - Describes plot information (plot identifiers, dominance, dates, etc.).
- Quality and text documentation: ECN_VW_qtext.csv
  - Site manager quality codes (Q1–Q8) with optional narrative text for additional issues; quality text may be coded as 999 in data downloads.
- Explanatory information: Site Codes and Species Codes
  - Site codes (e.g., T08, T09) with geographic context.
  - Extensive species code crosswalk (ECN/VESPAN with cross-references to BRC) to map numeric codes to Latin names; supports cross-dataset joins and accurate species mapping.
- Data download and interpretation
  - Each data row includes SITECODE, SYEAR, PLOTPID, CELLID, TREEID, STEMID, TREE_SPEC, FIELDNAME, VALUE.
  - Quality indicators accompany measurements; ECN_VW_qtext.csv provides context for quality flags.

## Explanatory Information: Species codes
- Provides a comprehensive mapping between numeric species codes and Latin names, with aliases and cross-references (e.g., Bry_902, Vas_902) to support data integration.
- Includes numerous examples showing synonyms and crosswalks to related taxonomic codes; enables robust species-level mapping across datasets.
- Facilitates accurate thematic mapping and cross-dataset joins by standardising species identifiers.

## Explanatory Information: Quality Codes
- Detailed quality code taxonomy describing data reliability and situational context. Examples of categories:
  - 100: No information available - data lost.
  - 101–109, 110–119: Various data collection issues (no sample, partial loss, debris, weather, etc.).
  - 120–135: In-situ contextual issues (change in vicinity, plot relocation, disturbance, etc.).
  - 136–139, 140–149: Operational/field issues (obstruction, flooding, grazing, chemicals, etc.).
  - 150–169: Additional field/plot observations and disturbances.
  - 170–189: Hydrological or environmental conditions affecting sampling (ponding, snow, etc.).
  - 200–203: Adverse conditions affecting sampling/recording (insects, light, etc.).
  - 501–507: Laboratory-related issues (no sample, loss, contamination, etc.).
  - 513: Calculated values or data-type specific caveats.
  - 999: Unusual event (context provided in quality text).
- The accompanying ECN_VW_qtext.csv provides narrative context for quality flags beyond coded values.
- This quality information is essential for mapping, analysis, and interpretation, allowing users to filter or annotate data by reliability.

## GIS and mapping considerations
- Data can be linked to spatial layers via SITECODE, PLOTPID, and CELLID, with site coordinates available in explanatory materials.
- Supports time-series mapping by year (SYEAR) and spatially explicit plots and trees (plot-level and tree-level attributes).
- Species and quality codes enable thematic mapping with reliability context (e.g., high-confidence vs. flagged observations).

## Practical considerations for GIS specialists
- Data integration: join ECN_VW2.csv with spatial boundaries for ECN sites and plots using SITECODE, PLOTPID, and CELLID.
- Multiscale mapping: visualize at tree-level (species, height, DBH) and at plot/site level (canopy characteristics, sampling year).
- Incorporate quality flags: use ECN_VW_qtext.csv to interpret quality flags and display reliability in map symbology.
- Data provenance: acknowledge ECN in publications; reference accompanying crosswalks and explanatory materials.

## Access, attribution, and supporting materials
- ECN provides crosswalks and explanatory information to support interpretation and accurate mapping.
- Supporting materials include site/species code crosswalks and a methods reference (v.pdf) detailing data collection and comparability across sites.
- Acknowledgement and publication reprint requirements are noted for data usage.

## Summary of the data’s GIS relevance
- The ECN_VW2 dataset enables cross-site, time-series GIS analyses of vegetation structure and composition.
- Rich attribute content (species, height, diameter, stem counts, dominance) supports diverse map products.
- Detailed quality codes and narrative notes allow transparent data quality assessment in spatial analyses.