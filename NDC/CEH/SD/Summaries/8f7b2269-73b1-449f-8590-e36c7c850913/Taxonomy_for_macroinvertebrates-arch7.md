# Taxonomy for macroinvertebrates in Welsh upland rivers

## Overview
- Dataset of macroinvertebrate taxonomy and abundance from Welsh upland rivers, covering WAWS (66 sites) and the Wye catchment (44 sites).
- Designed to relate biological assemblages to acidity gradients (WAWS) and land-use intensity (Wye).

## Spatial and Temporal Coverage
- WAWS: 66 sites, collected spring 2012.
- Wye catchment: 44 sites, collected spring 2013.
- Site identifiers: site_code; precise locations provided via coordinates and grid references.

## Data Collection and Methods
- Field sampling: 2-minute semiquantitative kick-samples in riffles using a standard kick-net (1 mm mesh).
- Preservation: on-site with 100% IMS; laboratory sorting and preservation in 70% IMS.
- Taxonomic processing: identification to species/genus where possible; to family or higher when difficult or poorly developed; some taxa identified at coarse levels (e.g., Oligochaeta, Tricladida).
- Analytical methods: visual identification of invertebrates.

## Taxonomy and Data Structure
- Data units: invertebrate abundance per taxon.
- Taxonomic fields (as available): class, order, family, genus, taxon_name (finest taxonomic level).
- Data structure: flatbed CSV with 9 columns
  - dataset, site_code, year, class, order, family, genus, taxon_name, abundance
- Notes on taxonomy handling:
  - When only family-level identification is available, genus may be set to the same value as family to align with trait-level data.
  - Some taxa receive NA for family and genus.

## Supporting Data
- Site description file (DURESS_CU_site_description.csv) with 10 columns:
  - site_code, Name, Eastings, Northings, Grid, Latitude, Longitude, Elevation, Survey (WAWS or Wye), Catchment.
- Coordinate references:
  - British National Grid (Eastings/Northings/Grid)
  - WGS84 latitude/longitude
  - Elevation in metres above sea level

## Data Quality and Provenance
- Quality control: Not documented.
- References and method links:
  - Weatherley & Ormerod (1987)
  - Bradley & Ormerod (2002)
  - CEH Data Catalogue references; external links may not be permanent

## GIS Considerations and Usage
- Coordinate systems: plan for conversion between British National Grid and WGS84 for mapping.
- Multi-resolution taxonomy: account for varying taxonomic resolution when joining with trait data or other layers.
- Data integration: join site-level data (site_code) with abundance data for map-based visualizations of community composition.
- Data cleaning needs: handle NA taxonomic levels and potential inconsistencies in identifications; consider separate handling of WAWS vs. Wye data.
- Potential map-based products: spatial distribution of taxa abundance, diversity metrics, and relationships to acidity or land-use gradients.

## References
- Related literature and data context available through CEH Data Catalogue and cited studies:
  - Weatherley NS, Ormerod SJ (1987)
  - Bradley DC, Ormerod SJ (2002)
  - Additional references linked within the CEH Data Catalogue Record