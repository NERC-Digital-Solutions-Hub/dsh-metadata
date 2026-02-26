# Terrestrial habitat, vegetation and soil data from Cumbria, 1975 Ecological Survey of Cumbria 1975. Dataset Summary

## Overview
- Historic dataset (1975) documenting terrestrial habitats, vegetation, and soils across Cumbria, England.
- Based on stratified sampling of nearly 650 x 200 m2 plots (642 actually surveyed; up to 768 selected overall).
- Standardized methods used to collect plant species, soils, habitat types, and biota.
- Data intended to support county-level land-use planning and nature conservation assessments; currently provided with rich metadata and structured formats.

## Data coverage, scope, and design
- Geographic scope: Cumbria, England (Lake District area prominent).
- Time period: 1975.
- Survey design: stratified sampling across 16 land-class strata; within each stratum, 3 x 1 km2 units randomly selected; within squares, 200 m2 plots located (final: 642–768 plots depending on accessibility).
- Plot-level data collected in nested quadrats for vegetation (4 m2 to 200 m2), soil horizons, pH, habitat types, slope, and aspect.
- Privacy consideration: specific site locations are not provided to protect landowner privacy.

## Data categories and content
- Vegetation data (CUMBRIA_1975_VEG.csv): vascular plants, bryophytes, macro-lichens; species codes, cover percentages, growth forms, and field sheet references.
- Soil data (CUMBRIA_1975_SOIL.csv): horizon descriptions and classifications; depth/description codes; field sheet references.
- Plot data (CUMBRIA_1975_PLOTS.csv): plot-level attributes including stratification, square and plot identifiers, date, slope, aspect, pH, litter/organic/mixed depths, and related measurements.
- Habitat data (CUMBRIA_1975_HABS.csv): within-plot and edge-of-plot habitat classifications, subgroups, and related descriptors.
- Physiography (CUMBRIA_1975_PHYS.csv): main physiographic features within 50 m of plot edge.
- Full species list: extensive catalog of recorded species (with scientific and common names, growth forms, and coding).
- Related publications and field methods referenced (Bunce & Shaw 1973; Bunce et al. 1975; Bunce et al. 1978).

## Methods and data quality
- Field methods: nested quadrat system for vegetation; sequential recording across quadrats (4 m2 → 25 m2 → 50 m2 → 100 m2 → 200 m2); percentage cover estimates; soil pits and augers for horizon descriptions and pH analysis.
- Habitat and physiographic measurements: slope and aspect measured; habitat types mapped within plots and up to 50 m edge.
- Data integrity: surveyors were fully trained; supervisor checks performed; field handbook used for standardized descriptions and classifications.
- Limitations: not all intended plots were accessible (some in crop fields or private land); precise site locations withheld; data reflect methods and standards of 1970s ecological surveying.

## Data schema and access
- CSV datasets with standardized fields:
  - STRATUM, SQUARE, PLOT: hierarchical identifiers for the sampling framework.
  - PLOTS: slope, aspect, pH, depth measurements (litter, organic, mixed horizons, etc.).
  - HABS: habitat classifications and subcategories.
  - VEG: species presence/cover, taxon, growth form, field sheet identifiers.
  - SOIL: horizon-specific codes and descriptions.
  - PHYS: physiographic features near plot edges.
- Full species list provided with scientific names, codes, and growth forms to enable cross-walks and analyses.
- Metadata tied to field sheets; references to original field handbook for method reproducibility.

## Original purpose and contextual notes
- Created to fill an information gap for Cumbria’s structure plan, focusing on extent and nature of wildlife habitats beyond designated sites (SSSIs and reserves).
- Intent to support nature conservation planning, land-use policy, and ecological baseline assessment for the county.
- Related to broader datasets such as Land Classification of Cumbria 1975 (for integrated analysis).

## Relational and reuse considerations for Data Leaders
- System-wide perspective: demonstrates integrating vegetation, soil, habitat, and physiography into a coherent data product; supports cross-domain analytics and historical baselines.
- Data availability and gaps: comprehensive 1975 snapshot with rich attribute detail; gaps include lack of precise site geolocation data and potential changes in habitat/land use since 1975.
- Data standards and metadata: extensive field codes, classifications, and field handbook references enable reproducibility and cross-study linkage; multiple CSVs and a full species list facilitate interoperability.
- Discoverability and discoverable metadata: datasets are described by survey design, strata, plot geometry, and measurement protocols; privacy controls limit precise geolocation but preserve analytical value.
- User needs and governance: suitable for researchers, policy analysts, and conservation planners seeking historical baselines, stratified survey design, and standardized methods; potential for linking with contemporary datasets for change detection.
- Collaboration and community context: anchored in established Bunce/Shaw methodologies; offers a model for transparent data provenance and method documentation in multi-dataset ecological data systems.