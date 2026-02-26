# Terrestrial habitat, vegetation and soil data from Cumbria, 1975 Ecological Survey of Cumbria 1975. Dataset Summary

## Overview
- A comprehensive ecological survey of Cumbria (England) conducted in 1975 to document terrestrial habitats, soils and vegetation.
- Aimed at informing land-use planning, nature conservation, and understanding the county’s ecological status.
- Note: specific site locations are not provided to protect landowner privacy; most sites are/private ownership.

## Scope and time frame
- Geographic coverage: Cumbria, England; centered on areas including the Lake District.
- Time period: 1975.
- Data categories: Vegetation data (vascular plants, bryophytes, lichens), Soil data (horizon depths, descriptions, pH), Habitat data (within-plot and near-plot habitats), Physiographical features near plot edges.

## Sampling design and field methods
- Sampling design: Stratified sampling across Cumbria with 16 strata defined by land classification; within each stratum, 3 x 1 km2 areas were randomly selected from ~7,100 km2, then 200 m2 plots located within selected squares.
- Plot selection: 16 random points per stratified area to locate 200 m2 plots; adjustments due to accessibility (lakes, seas, crop fields) led to 768 plots selected; 642 surveyed in practice.
- Within-plot methodology:
  - Vegetation: nested quadrats (4 m2, 25 m2, 50 m2, 100 m2, then 200 m2) with species recorded progressively and percentage cover estimates.
  - Soil: surface horizon description via shallow pit, auger samples for lower horizons, top 10 cm sampled for pH.
  - Habitat: categories recorded inside plot and within 50 m edge; slope and aspect measured.
- Field handbook and standardized procedures (Bunce & Shaw 1973) guided surveys; surveys conducted by trained field staff with supervisor checks.

## Data content and structure
- Vegetation data (CUMBRIA_1975_VEG.csv)
  - Columns include: STRATUM, SQUARE, PLOT, NEST, COVER, CODE, BRC_NUMBER, SCIENTIFIC_NAME, COMMON_NAME, GROWTH_FORM, FIELD_SHEET, etc.
  - Records vascular plants, bryophytes and macro-lichens by species and cover per plot.
- Soil data (CUMBRIA_1975_SOIL.csv)
  - Columns: STRATUM, SQUARE, PLOT, CODE, DESCRIPTION, GROUP, FIELD_SHEET.
  - Depths and descriptive categories for soil horizons; CODE linked to descriptive taxonomy.
- Plot-level data (CUMBRIA_1975_PLOTS.csv)
  - Columns: STRATUM, SQUARE, PLOT, DATE, SLOPE, ASPECT, PH, LITTER_FROM/TO, ORG_FROM/TO, MIXED_FROM/TO, LEACH_FROM/TO, WEATHER_FROM/TO, UNDER_DEPTH.
  - Captures site-level physical measurements (orientation, soil chemistry, horizon depths).
- Habitat data (CUMBRIA_1975_HABS.csv)
  - Columns: STRATUM, SQUARE, PLOT, CODE, DESCRIPTION, GROUP, SUBGROUP, FIELD_SHEET.
  - Habitat classifications for within-plot and related habitats.
- Physiographical features near plot (CUMBRIA_1975_PHYS.csv)
  - Columns: STRATUM, SQUARE, PLOT, CODE, DESCRIPTION, GROUP, FIELD_SHEET.
  - Descriptions of features within 50 m of plot edge.
- Full list of species
  - A long list of recorded taxa (scientific names with cross-references to codes and common names).
- Data sheets and field references
  - Field sheets referenced; alignment with Bunce, Shaw and related field handbooks.
- Data formats
  - CSV files with explicit schema and field definitions; coded taxonomy and growth forms provided for data standardization.

## Data quality, provenance and controls
- Data collected by fully trained surveyors using standardized methods; fieldwork quality controlled by supervisors.
- Standardized field handbook and procedures underpin data consistency across plots and variables.
- Privacy controls: site locations withheld to protect landowners; most plots were privately held.

## Related datasets, publications and references
- Related historical datasets and methodological references:
  - Bunce, R.G.H. & Shaw, M.W. (1973): A Standardized Procedure for Ecological Survey.
  - Bunce, R.G.H., Smith, R.S., Hill, M.O. (2015): Land Classification of Cumbria 1975 (DOI provided).
  - Bunce, R.G.H. & Smith, R.S. (1978): An ecological survey of Cumbria.
  - Field handbook: Ecological Survey of Cumbria – Handbook of Field Methods (unpublished, County Planning Department/ITE Merlewood).
- Data center and access
  - Related entry: Land Classification of Cumbria 1975 (NERC Environmental Information Data Centre DOI).
  - This dataset’s components are organized as distinct CSV files with cross-references to the original field sheets.

## Origin and purpose
- Origin: commissioned by Cumbria County Council to inform a county structure plan and policies for land use, nature conservation, and wildlife habitat protection.
- Rationale: prior to policy formation, needed a baseline of the extent and nature of wildlife habitats beyond existing designated sites (SSSIs and nature reserves).

## Potential usage for data support
- Enables self-service exploration of Cumbria’s 1975 ecological state via species, habitats, and soil characteristics across sampled plots.
- Can support historical comparisons, ecological habitat mapping, soil profile studies, and trend analyses when combined with other time points.
- Useful for validating or recalibrating landscape classification schemes and for metadata-driven data curation and re-use.
- Limitations to note: site location privacy; 1975 time frame; sampling adjustments due to accessibility; some plots incomplete or inaccessible.