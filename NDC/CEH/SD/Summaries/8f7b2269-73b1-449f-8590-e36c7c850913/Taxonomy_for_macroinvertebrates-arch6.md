# Taxonomy for macroinvertebrates in Welsh upland rivers

## Overview
- Dataset characterises macroinvertebrate taxonomy and abundance across upland Welsh rivers.
- Covers 66 WAWS sites and 44 Wye catchment sites to explore biological responses to acidity gradients and land-use intensification.

## Study design and scope
- WAWS (Welsh Acid Water Survey): gradient in acidity across contrasting geology and acidic exposure.
- Wye catchment: gradient in land-use intensification across the catchment.
- Sampling conducted in spring of 2012 (WAWS) and 2013 (Wye).

## Data collection methods
- Invertebrates collected using 2-minute semiquantitative kick samples in riffles.
- Standard kick-net with 1 mm mesh; major habitats targeted to detect between-site differences.
- On-site preservation with 100% industrial methylated spirit (IMS); laboratory processing used 70% IMS.
- Taxa identified and counted to species or genus where possible; some taxa identified only to family or higher due to development or difficulty.

## Taxonomy and measurements
- Units: abundance of invertebrates.
- Taxonomic levels recorded: class, order, family, genus, species where possible.
- If only family level identified, genus column may also hold the family name to support trait-level analyses.
- Some taxa identified at coarse levels (e.g., Oligochaeta, Tricladida); these have NA in family/genus columns.

## Data structure
- One flatfile with nine columns:
  - dataset
  - site_code
  - year
  - class
  - order
  - family
  - genus
  - taxon_name (finest taxonomic level)
  - abundance

## Supporting documents and metadata
- DURESS_CU_site_description.csv: site metadata with 10 columns including Site_code, Name, Eastings, Northings, Grid, Latitude, Longitude, Elevation, Survey, Catchment.
- Site descriptions provide spatial context for mapping and analysis.

## Quality control and caveats
- No formal quality control procedures documented.
- Some taxa identified only to coarse taxonomic levels; this can affect lineage- or trait-based analyses.
- Calibration steps are not reported.

## References and data accessibility
- Primary methodological references:
  - Bradley DC, Ormerod SJ (2002) on kick-sampling precision.
  - Weatherley NS, Ormerod SJ (1987) on acidification impacts on macroinvertebrates.
- Links to references are available from the CEH Data Catalogue Record; link persistence is not guaranteed.
- Data are provided as a flatfile with associated site metadata for integration and re-use.