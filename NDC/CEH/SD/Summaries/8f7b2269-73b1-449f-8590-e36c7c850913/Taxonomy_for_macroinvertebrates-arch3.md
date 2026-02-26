# Taxonomy for macroinvertebrates in Welsh upland rivers

## Overview and purpose
- Describes a dataset of macroinvertebrate taxonomy and abundance from Welsh upland rivers, intended to support ecological monitoring and assessment across environmental gradients.
- Covers responses to acidity gradients (WAWS) and land-use intensification (Wye catchment), aiding policy scrutiny and decision-making on river health.

## Study design and sampling sites
- WAWS: 66 sites; Wye catchment: 44 sites.
- Sampling aims to capture biological responses to contrasting geologies and acidic episodes (WAWS) and varying land-use intensity (Wye).
- Sampling conducted in spring 2012 (WAWS) and 2013 (Wye).

## Collection methods and laboratory processing
- Invertebrates collected using 2-minute semi-quantitative kick samples in riffles; standard method calibrated to detect between-site differences.
- On-site preservation with 100% IMS; laboratory preservation in 70% IMS.
- Identification: major groups identified and counted to species or genus where possible; some taxa identified only to family or higher (e.g., Diptera); in some cases, coarse taxa (Oligochaeta, Tricladida) recorded with NA for family/genus.
- Field equipment: standard kick-net with 1 mm mesh; laboratory microscopes.
- Calibration steps and values: none reported.

## Taxonomy, data structure, and units
- Analytical method: visual identification of invertebrates.
- Units: abundance of each taxon.
- Taxonomic resolution: data include taxon_class, order, family, genus, and taxon_name; when genus is not resolved, family is carried in the genus column; some taxa identified only at coarse levels.
- Data structure: flatbed file with nine columns:
  - dataset, site_code, year, class, order, family, genus, taxon_name, abundance.

## Metadata, quality control, and data governance
- Quality control: none explicitly documented.
- Supporting site metadata: DURESS_CU_site_description.csv with 10 columns (site_code, name, Eastings, Northings, Grid, Latitude, Longitude, Elevation, Survey, Catchment) providing spatial context and survey details.
- Data references and accessibility: links to CEH Data Catalogue records; note that external links may not be permanent.

## Data availability and governance considerations for monitoring frameworks
- Data is organized to enable cross-site comparisons along environmental gradients, suitable for informing policy evaluations and trend analysis.
- Rich site-level metadata supports data integration and transparency for governance and reporting.
- Some limitations to consider for monitoring use: absence of formal quality control documentation, partial taxonomic resolution for certain taxa, and potential challenges in data integration due to variable taxonomic resolution across taxa.

## Supporting materials
- Site description file: DURESS_CU_site_description.csv with site_code, name, coordinates, grid reference, elevation, survey, and catchment.